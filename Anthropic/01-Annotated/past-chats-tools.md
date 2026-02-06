---
title: "Past Chats Tools | 对话检索工具"
source: "claude-4.1-opus-thinking.md (past_chats_tools section)"
source_type: "Anthropic"
original_language: "en"
date: 2026-02-06
status: annotated
importance: "critical"
difficulty: "intermediate"
learning_stage: "comprehension"
annotation_version: "1.0"
last_annotated: 2026-02-06
annotation_language: "bilingual"
cssclasses: prompt-learning
reading_progress: "100%"
next_review: 2026-02-13
review_count: 0
tags:
  - system-prompts
  - anthropic
  - conversation-retrieval
  - context-memory
  - bilingual
related_docs:
  - "[[../00-Index]]"
  - "[[thinking-mode]]"
  - "[[search-behavior]]"
  - "[[../../claude-4.1-opus-thinking]]"
---

# Past Chats Tools | 对话检索工具

> [!success] 核心要点 | Core Concept
> ==Past Chats Tools | 对话检索工具==
>
> Claude has **two tools** to search past conversations, enabling **cross-session context continuity** and breaking through the traditional barrier of isolated chat sessions.
> Claude 有**两个工具**来搜索过去的对话，实现**跨会话上下文连续性**，突破了传统孤立会话的壁垒。
>
> **双工具架构 | Dual-Tool Architecture**：
> - `conversation_search` - 基于主题/关键词搜索（Topic/keyword-based）
> - `recent_chats` - 基于时间范围检索（Time-based retrieval）

---

## 🧠 为什么需要对话检索？| Why Conversation Retrieval?

> [!abstract] 核心思想 | Core Idea
> **认知连续性原则 | Cognitive Continuity Principle**
>
> 传统 AI 对话的问题是**会话孤岛**（Conversation Islands）：
> - 每次新对话都是"空白状态"
> - 无法回忆之前讨论的内容
> - 用户体验不连贯
>
> **对话检索工具解决这个问题**：
> - 打破会话壁垒
> - 保持长期对话的一致性
> - 快速找到之前讨论的内容
> - 支持项目级别的上下文记忆

> [!question] 启发式思考 | Guiding Question
> **核心问题**：为什么需要两个不同的工具？一个不够吗？
> **提示**：考虑你如何搜索电脑文件...
>
> <details>
> <summary>查看答案与解析 | View Answer & Analysis</summary>
>
> **答案 | Answer**：因为**人类记忆有两种模式**（Two memory modes）：
>
> 1. **语义记忆**（Semantic Memory）：基于内容/主题
>    - "我们讨论过 Python 装饰器吗？"
>    - 需要 `conversation_search`
>
> 2. **情景记忆**（Episodic Memory）：基于时间/情境
>    - "昨天我们聊了什么？"
>    - 需要 `recent_chats`
>
> **深入分析 | Deep Dive**：
> - **搜索效率**：针对性工具比单一工具更高效
> - **参数优化**：每个工具针对特定搜索类型优化参数
> - **用户意图匹配**：符合用户的自然查询模式
>
> **类比 | Analogy**：
> - 就像电脑文件搜索：
>   - 按名称搜索 = `conversation_search`
>   - 按日期排序 = `recent_chats`
> </details>

---

## 🛠️ 工具详解 | Tool Details

### Tool 1: conversation_search | 对话搜索

> [info] 工具规格 | Tool Specifications
>
> **搜索类型 | Search Type**：主题/关键词（Topic/keyword-based）
>
> **使用场景 | Use Cases**：
> - "What did we discuss about [specific topic]?"
> - "Find our conversation about [X]"
> - "你之前提到过那个概念..."
>
> **查询参数 | Query Parameter**：
> - 仅包含**高置信度关键词**（High-confidence keywords only）
> - 名词、专有名词、领域术语
> - 避免通用动词、时间标记

#### 关键词提取策略 | Keyword Extraction Strategy

> [!warning] 关键难点 | Critical Challenge
> **关键词质量决定搜索效果**
>
> | ✅ 高置信度关键词 | ❌ 低置信度关键词 |
> |---------------------|---------------------|
> | 名词：robot, pasta | 通用动词：discuss, talk |
> | 领域术语：machine learning, OAuth | 时间标记：yesterday, last week |
> | 项目名：Project Tempest | 模糊名词：thing, stuff |
> | 专有名词：San Francisco, Microsoft | 元对话词：conversation, chat |
> | 领域术语：SQL queries, derivative | 问题：issue, problem（无具体内容） |

> [!example] 示例：关键词提取 | Example: Keyword Extraction
>
> **用户查询 | User Query**：
> > "What did we discuss about Chinese robots yesterday?"
>
> **提取结果 | Extracted Keywords**：
> - ✅ "Chinese robots"（高置信度名词）
> - ❌ "discuss"（通用动词）
> - ❌ "yesterday"（时间标记 - 应该用 recent_chats）
>
> **搜索调用 | Search Call**：
> ```javascript
> conversation_search(query: "Chinese robots")
> ```

> [!question] 启发式思考 | Guiding Question
> **核心问题**：为什么不应该用 "discuss"、"talk" 作为关键词？
>
> <details>
> <summary>查看答案</summary>
>
> **答案**：因为**几乎每个对话都包含这些词**（Low discriminative power）。
>
> **信息论视角 | Information Theory Perspective**：
> - **高价值关键词**：罕见、特定、有区分度
> - **低价值关键词**：常见、通用、无区分度
>
> **示例**：
> - "machine learning" → 高价值（出现在少数对话中）
> - "discuss" → 低价值（出现在几乎所有对话中）
>
> **搜索原则 | Search Principle**：
> > Be specific to be relevant.
> > 具体才能相关。
> </details>

### Tool 2: recent_chats | 最近对话

> [info] 工具规格 | Tool Specifications
>
> **搜索类型 | Search Type**：时间范围（Time-based retrieval）
>
> **使用场景 | Use Cases**：
> - "What did we talk about yesterday?"
> - "Show me chats from last week"
> - "我们上周讨论了什么？"
>
> **参数 | Parameters**：
>
> | 参数 | 类型 | 范围 | 说明 |
> |------|------|------|------|
> | `n` | number | 1-20 | 返回的对话数量 |
> | `sort_order` | string | 'asc'/'desc' | 排序方向（默认 desc） |
> | `before` | datetime | ISO format | 过滤此时间之前的对话 |
> | `after` | datetime | ISO format | 过滤此时间之后的对话 |

> [!tip] 使用技巧 | Usage Tips
> **分页策略 | Pagination Strategy**：
> - 用户需要 >20 个结果时，多次调用工具
> - 使用 `before` 参数从上一批最早的对话继续
> - 最多约 5 次调用后停止，告知用户结果不全面

> [!example] 示例：时间范围查询 | Example: Time Range Query
>
> **场景**："Summarize our chats from last week"
>
> **假设**：今天是 2026-02-06（周三）
> - 上周开始：2026-01-30（周一）00:00:00
> - 上周结束：2026-02-05（周日）23:59:59
>
> **调用 | Call**：
> ```javascript
> recent_chats(
>   n: 20,
>   after: '2026-01-30T00:00:00Z',
>   before: '2026-02-05T23:59:59Z',
>   sort_order: 'desc'
> )
> ```
>
> **如果结果超过 20 个**：
> ```javascript
> // 第二次调用，使用最早结果的 updated_at
> recent_chats(
>   n: 20,
>   before: '2026-01-30T15:30:00Z',  // 第一批最早的 updated_at
>   after: '2026-01-30T00:00:00Z',
>   sort_order: 'desc'
> )
> ```

---

## 🌳 决策框架 | Decision Framework

> [!success] 核心要点 | Core Concept
> ==工具选择决策树==
>
> 官方提供的决策框架：
> ```markdown
> 1. Time reference mentioned? → recent_chats
> 2. Specific topic/content mentioned? → conversation_search
> 3. Both time AND topic? → 根据具体情况选择
>    - 有特定时间范围 → recent_chats
>    - 有 2+ 个具体关键词 → conversation_search
>    - 否则 → recent_chats（更保守的选择）
> 4. Vague reference? → 询问澄清
> 5. No past reference? → 不使用工具
> ```

> [!example] 示例：决策过程 | Example: Decision Process
>
> **场景 1**："What did we discuss yesterday?"
> - 时间引用：✅ "yesterday"
> - 特定主题：❌ 无
> - **决策**：`recent_chats`
>
> **场景 2**："Where did we leave off with Python debugging?"
> - 时间引用：❌ 无
> - 特定主题：✅ "Python debugging"
> - **决策**：`conversation_search(query: "Python debugging")`
>
> **场景 3**："What about those Chinese robots from yesterday?"
> - 时间引用：✅ "yesterday"
> - 特定主题：✅ "Chinese robots"
> - **决策**：
>   - 有特定时间 → `recent_chats`（after: 昨天开始, before: 昨天结束）
>   - 或 `conversation_search(query: "Chinese robots")`
>   - **优先**：`recent_chats`（时间约束更严格）
>
> **场景 4**："What was that thing we discussed?"
> - 时间引用：❌ 无
> - 特定主题：❌ "thing" 太模糊
> - **决策**：询问澄清 "Which thing specifically?"

---

## 🎯 触发模式 | Trigger Patterns

> [info] 官方触发词列表 | Official Trigger Words
>
> 以下表达模式应该触发对话检索工具：

| 模式 | English | 中文 |
|------|---------|------|
| **Explicit reference** | "Continue our conversation about..." | "继续我们关于...的对话" |
| **Continuation** | "Where did we leave off with/on..." | "我们在...上停在哪了？" |
| **Personal reference** | "What did I tell you about..." | "我告诉过你关于..." |
| **Discussion reference** | "What did we discuss..." | "我们讨论了什么..." |
| **Time reference** | "What did we talk about [yesterday/this week]" | "[昨天/这周]我们聊了什么" |
| **Date reference** | "Show me chats from [date]" | "给我看[日期]的对话" |
| **Memory check** | "Did I mention..." | "我提到过...吗？" |
| **History check** | "Have we talked about..." | "我们谈论过...吗？" |
| **Recall** | "Remember when..." | "记得当...时" |

> [!warning] 常见错误 | Common Mistake
> ❌ **错误**：用户提到"我之前..."就立即触发工具
>
> ✅ **正确**：检查是否有具体的主题或时间引用
>
> **示例**：
> - "我之前说了..." + 具体主题 → 触发
> - "我之前不太确定..." → 不触发（无历史引用意图）

---

## 📊 响应格式 | Response Format

> [info] 返回数据结构 | Response Data Structure
>
> **返回格式 | Return Format**：
> ```xml
> <chat uri='{uri}' url='{url}' updated_at='{updated_at}'>
>   [对话片段内容 | Conversation snippet content]
> </chat>
> ```
>
> **重要规则 | Important Rules**：
> 1. **仅供参考**：`<chat>` 标签内的内容仅供参考，不要直接复制给用户
> 2. **链接格式**：始终将对话链接格式化为可点击：`<https://claude.ai/chat/{uri}>`
> 3. **自然综合**：自然地综合信息，不要直接引用片段
> 4. **承认来源**：自然地承认来自过去的对话
> 5. **XML 禁用**：响应中不要使用 XML 标签（除非用户明确要求）

> [!example] 好的响应示例 | Good Response Example
>
> **用户查询**："上周我们讨论了什么关于 Python 装饰器的内容？"
>
> **好的响应**：
> > 上周我们在讨论 Python 装饰器时，您提到了想了解如何在类方法上使用装饰器。我们讨论了 `@property` 装饰器以及如何创建自定义装饰器来处理方法调用。您还想深入了解更多吗？
>
> **相关对话**：<https://claude.ai/chat/abc123>
>
> ---
>
> **不好的响应**：
> > `<chat uri='abc123'>...content...</chat>` 告诉你，我们在 `<chat uri='def456'>...content...</chat>` 中讨论了装饰器。

---

## 🚫 不使用工具的场景 | When NOT to Use

> [!warning] 关键约束 | Critical Constraints
> **以下情况不应该使用对话检索工具**：
>
> | 场景 | 示例 | 原因 |
> |------|------|------|
> | 需要更多信息才能搜索 | "What did we decide about that thing?" | "thing" 太模糊 |
> | 通用知识问题 | "What is the capital of France?" | Claude 已知道 |
> | 当前事件/新闻 | "Who won the election?" | 应该用 web_search |
> | 技术问题（无历史引用） | "How to parse JSON in Python?" | 直接回答即可 |
> | 全新话题（有完整上下文） | 用户提供了所有必要信息 | 无需检索 |
> | 简单事实查询 | "What is 2+2?" | 直接计算 |

> [!question] 启发式思考 | Guiding Question
> **核心问题**：为什么对于"首都"问题不用对话检索？
>
> <details>
> <summary>查看答案</summary>
>
> **答案**：因为**通用知识不需要检索**（General knowledge ≠ personal history）。
>
> **区分原则 | Distinction Principle**：
> - **通用知识**（General Knowledge）：直接从 Claude 训练数据中获取
> - **个人历史**（Personal History）：需要从用户过去对话中检索
>
> **示例对比**：
> - ❌ "巴黎的首都是哪里？" → 通用知识，不检索
> - ✅ "我们之前讨论过哪个城市？" → 个人历史，检索
> </details>

---

## 🧪 学习练习 | Learning Exercises

> [!help] 学习练习 | Learning Exercise

**练习 1：选择正确的工具 | Choose the Right Tool**

对于以下用户查询，应该使用哪个工具（或不使用）？

1. "What did we talk about yesterday?"
2. "Find our discussion about OAuth authentication."
3. "What's the weather like today?"
4. "What did I tell you about my project?"
5. "How do I center a div in CSS?"

<details>
<summary>查看答案 | View Answer</summary>

**答案 | Answer**：

1. ✅ **recent_chats** - 时间引用 "yesterday"
2. ✅ **conversation_search** - 特定主题 "OAuth authentication"
3. ❌ **不使用工具** - 当前事件，应该用 web_search
4. ✅ **conversation_search** - 主题引用 "my project"（关键词：project）
5. ❌ **不使用工具** - 技术问题，直接回答

**关键原则**：Time → recent_chats; Topic → conversation_search; General → No tool
</details>

**练习 2：关键词提取 | Keyword Extraction**

从以下查询中提取高置信度关键词：

1. "What did we discuss about Chinese robots yesterday?"
2. "Where did we leave off with the customer dashboard API?"
3. "Show me what we talked about regarding machine learning."

<details>
<summary>查看答案 | View Answer</summary>

**答案 | Answer**：

1. **"Chinese robots"**
   - ❌ 去掉：discuss（通用动词）、yesterday（时间标记）

2. **"customer dashboard API"** 或 **"customer dashboard"**
   - ✅ 保留：customer, dashboard, API（都是具体名词）
   - ❌ 去掉：where, leave off

3. **"machine learning"**
   - ✅ 保留：machine learning（领域术语）
   - ❌ 去掉：show me, what, talked about, regarding

**提取原则**：
> Extract substantive/high-confidence keywords only.
> 仅提取实质性/高置信度关键词。
</details>

**练习 3：参数配置 | Parameter Configuration**

用户问："Summarize everything from July 2025"，今天是 2025-08-15。

如何配置 `recent_chats` 调用？

<details>
<summary>查看答案 | View Answer</summary>

**答案 | Answer**：

```javascript
// 第一次调用
recent_chats(
  n: 20,
  after: '2025-07-01T00:00:00Z',
  before: '2025-07-31T23:59:59Z',
  sort_order: 'desc'
)

// 如果需要更多结果（第二次调用）
// 假设第一次最早的 updated_at 是 '2025-07-10T10:00:00Z'
recent_chats(
  n: 20,
  after: '2025-07-01T00:00:00Z',
  before: '2025-07-10T10:00:00Z',
  sort_order: 'desc'
)

// 最多约 5 次调用后停止
```

**关键点**：
- ISO 8601 格式：`YYYY-MM-DDTHH:MM:SSZ`
- 使用整个月的时间范围
- 按 `updated_at` 分页
</details>

---

## 📊 总结与反思 | Summary & Reflection

> [!abstract] 核心思想 | Core Idea
> ==对话检索工具的核心价值==
>
> **打破记忆壁垒 | Breaking Memory Barriers**：AI 不再是"金鱼记忆"，可以跨会话回忆
> **上下文连续性 | Context Continuity**：长期对话变得连贯自然
> **效率提升 | Efficiency**：快速找到之前讨论的内容，无需重复
> **项目感知 | Project Awareness**：项目级别的上下文记忆

> [!tip] 实践建议 | Practical Recommendations
> **如何在自己的 AI 应用中应用类似功能？**
>
> 1. **向量存储**：使用向量数据库（如 Pinecone）存储对话嵌入
> 2. **混合检索**：
>    - 语义搜索（类似 conversation_search）
>    - 元数据过滤（类似 recent_chats）
> 3. **排名机制**：对搜索结果进行相关性排名
> 4. **隐私考虑**：确保用户只能检索自己的对话

> [!warning] 局限性 | Limitations
> **对话检索工具不是完美的**：
> - 需要用户提供明确的引用（不能"猜测"）
> - 搜索质量取决于关键词质量
> - 不能检索跨项目对话（在项目模式中）
> - 结果可能有噪音（需要人工筛选）

---

## 🔗 相关链接 | Related Links

- [[../00-Index]] - Anthropic 系统提示词学习索引
- [[thinking-mode]] - 思维模式
- [[search-behavior]] - 搜索行为与决策树
- [[../../past_chats_tools.md]] - 原始文档

---

**最后更新 | Last Updated**: 2026-02-06
**下一计划 | Next Review**: 2026-02-13
