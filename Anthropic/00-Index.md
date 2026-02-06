---
title: "Anthropic 系统提示词学习索引 | Anthropic System Prompts Learning Index"
source: "https://docs.anthropic.com/en/release-notes/system-prompts"
source_type: "Anthropic"
original_language: "en"
date: 2026-02-06
status: indexed
importance: "critical"
difficulty: "advanced"
learning_stage: "comprehension"
annotation_version: "1.0"
annotation_language: "bilingual"
cssclasses: prompt-learning
reading_progress: "0%"
next_review: 2026-02-13
review_count: 0
tags:
  - system-prompts
  - anthropic
  - claude
  - prompt-engineering
  - bilingual
related_docs:
  - "[[DocFramework/Microsoft-Style-Guide/02-Annotated/welcome]]"
  - "[[DocFramework/Diataxis/02-Annotated/start-here]]"
---

# Anthropic 系统提示词学习索引 | Anthropic System Prompts Learning Index

> [!success] 核心要点 | Core Concept
> ==System Prompts | 系统提示词==
>
> System prompts are the foundational instructions that define an AI assistant's behavior, capabilities, and limitations. They are the "blueprint" that shapes how AI models respond to user queries.
> 系统提示词是定义 AI 助手行为、能力和限制的基础指令。它们是塑造 AI 模型如何响应用户查询的"蓝图"。
>
> **Why Study System Prompts? | 为什么要研究系统提示词？**
> - Understanding AI behavior | 理解 AI 行为机制
> - Prompt engineering | 提示词工程最佳实践
> - AI safety | AI 安全与对齐研究
> - Transparency | 透明度与可解释性

---

## 📚 学习路径 | Learning Path

### 阶段 0：词汇基础 | Stage 0: Vocabulary Foundations

> [!info] 新增学习阶段
> **推荐学习顺序**: 词汇基础 → 核心机制 → 能力限制 → 版本演进
>
> **为何先学词汇？**
> - 理解系统提示词的"微妙词汇运用"
> - 掌握五类词汇：程度修饰、语气控制、边界词、微妙表达、操作指导
> - 为深入理解核心机制打下基础

| 文档 | Document | 重点 | Focus | 难度 | Difficulty |
|:-----|:---------|:-----|:-------|:----:|:-----------:|
| [[00-Vocabulary/vocabulary-index]] | **词汇总索引** | 词汇体系概览，学习路径导航 | ⭐⭐ | Intermediate |
| [[00-Vocabulary/01-Degree-Modifiers]] | **程度修饰语** | appropriately, strategically, carefully... | ⭐⭐⭐ | Advanced |
| [[00-Vocabulary/02-Tone-Controllers]] | **语气控制词** | MUST, NEVER, strongly, should... | ⭐⭐⭐ | Advanced |
| [[00-Vocabulary/03-Boundary-Words]] | **边界词** | unless, only, maximum, approximately... | ⭐⭐ | Intermediate |
| [[00-Vocabulary/04-Nuanced-Expressions]] | **微妙表达** | naturally, politely, breaks continuity... | ⭐⭐⭐⭐ | Expert |
| [[00-Vocabulary/05-Action-Guides]] | **操作指导词** | Extract, Avoid, Prioritize, Synthesize... | ⭐⭐⭐ | Advanced |
| [[00-Vocabulary/vocabulary-extraction-guide]] | **提取指南** | 手动提取方法，识别规则 | ⭐⭐⭐⭐ | Expert |
| [[00-Vocabulary/Cross-Document-Comparisons]] | **跨文档对比** | 公司/版本风格对比分析 | ⭐⭐⭐⭐ | Expert |
| [[00-Vocabulary/Vocabulary-Exercises]] | **综合练习** | 80+ 练习题目，闪卡+场景应用 | ⭐⭐⭐ | Advanced |

### 阶段 1：核心机制理解 | Stage 1: Core Mechanisms

| 文档 | Document | 重点 | Focus | 难度 | Difficulty |
|------|----------|------|-------|------|------------|
| [[01-Annotated/thinking-mode]] | **思维模式** | Chain of Thought, 推理透明化 | ⭐⭐⭐ | Advanced |
| [[01-Annotated/past-chats-tools]] | **对话检索** | conversation_search, recent_chats | ⭐⭐ | Intermediate |
| [[01-Annotated/search-behavior]] | **搜索行为** | web_search 决策树, 版权边界 | ⭐⭐⭐⭐ | Expert |

### 阶段 2：能力与限制 | Stage 2: Capabilities & Constraints

| 文档 | Document | 重点 | Focus |
|------|----------|------|-------|
| [[02-Annotated/artifacts]] | **Artifacts 系统** | 代码生成, 可视化, 交互式内容 |
| [[02-Annotated/memory-system]] | **记忆系统** | 上下文连续性, 项目记忆 |
| [[02-Annotated/end-conversation]] | **对话终止** | 安全边界, 滥用防护 |

### 阶段 3：版本演进 | Stage 3: Version Evolution

| 版本 | Version | 关键特性 | Key Features | 文档 | Document |
|------|----------|----------|--------------|----------|----------|
| Claude 3.7 Sonnet | 基础工具使用 | Tools, Search | [[03-Evolution/claude-3.7]] |
| Claude 4.1 Opus | **思维模式** | Thinking Mode (interleaved) | [[03-Evolution/claude-4.1-opus]] |
| Claude 4.5 Sonnet | 增强推理 | Extended thinking | [[03-Evolution/claude-4.5]] |
| Claude Code | CLI 集成 | Terminal, Git, Files | [[03-Evolution/claude-code]] |

---

## 🎯 按主题学习 | Topic-Based Learning

### 主题 1：推理与思维 | Reasoning & Thinking

> [!abstract] 核心思想 | Core Idea
> **思维模式 (Thinking Mode)** 是 Claude 4.1+ 的核心特性，通过显式的推理块让 AI "思考关于思考的过程"（元认知）。

**核心文档 | Core Documents:**
- [[01-Annotated/thinking-mode]]
- [[03-Evolution/claude-4.1-opus-thinking]]

**学习目标 | Learning Objectives:**
1. 理解 interleaved 思维模式的工作原理
2. 掌握何时使用 thinking 块
3. 了解 max_thinking_length 的作用

### 主题 2：搜索与信息检索 | Search & Information Retrieval

> [!info] 搜索策略框架 | Search Strategy Framework
> Claude 的搜索行为基于复杂的决策树，根据信息稳定性、变化频率和查询复杂度动态调整搜索次数（0-20次）。

**核心文档 | Core Documents:**
- [[01-Annotated/search-behavior]]
- [[01-Annotated/copyright-boundaries]]

**学习目标 | Learning Objectives:**
1. 理解搜索决策树
2. 掌握版权保护边界（<15词引用）
3. 学习关键词提取策略

### 主题 3：对话上下文管理 | Conversation Context Management

> [!tip] 认知连续性原则 | Cognitive Continuity Principle
> 过去对话检索系统打破会话壁垒，实现跨会话的上下文连贯性。

**核心文档 | Core Documents:**
- [[01-Annotated/past-chats-tools]]
- [[02-Annotated/memory-system]]

**学习目标 | Learning Objectives:**
1. 理解 conversation_search vs recent_chats 的使用场景
2. 掌握高置信度关键词提取
3. 学习时间范围过滤参数

---

## 🔑 关键触发关键词 | Key Trigger Keywords

### 搜索触发词 | Search Triggers

| 类别 | Category | 触发词 | Trigger Words | 动作 | Action |
|------|----------|--------|---------------|-------|--------|
| **单次搜索** | current/latest/recent, weather, price | `web_search` ×1 |
| **研究型** | deep dive, comprehensive, analyze, evaluate | `web_search` ×5+ |
| **无需搜索** | 永恒事实、基础概念 | 直接回答 |

### 对话检索触发词 | Conversation Retrieval Triggers

```
"Continue our conversation about..."
"Where did we leave off with..."
"What did we discuss..."
"What did we talk about [yesterday/last week]"
"As I mentioned before..."
"Remember when..."
```

---

## 📊 版本对比表 | Version Comparison

### 思维能力演进 | Thinking Capability Evolution

| 版本 | 思维模式 | 最大长度 | 应用场景 |
|------|----------|----------|----------|
| Claude 3.7 Sonnet | 无 | N/A | 基础对话 |
| Claude 4.1 Opus | **interleaved** | 16,000 tokens | 复杂推理 |
| Claude 4.5 Sonnet | enhanced | 扩展 | 深度分析 |

### 工具能力演进 | Tool Capability Evolution

| 工具 | 3.7 Sonnet | 4.1 Opus | 4.5 Sonnet | Claude Code |
|------|------------|----------|------------|-------------|
| web_search | ✅ | ✅ | ✅ | ✅ |
| past_chats | ❌ | ✅ | ✅ | ✅ |
| thinking_mode | ❌ | ✅ | ✅ | ✅ |
| terminal | ❌ | ❌ | ❌ | ✅ |
| git operations | ❌ | ❌ | ❌ | ✅ |

---

## ⚠️ 安全与约束 | Safety & Constraints

> [!warning] 核心约束 | Critical Constraints
>
> ### 版权强制要求
> ```xml
> NEVER reproduce >15 word quotes
> NEVER reproduce song lyrics (even in artifacts)
> Maximum ONE short quote (<15 words) per response
> ```
>
> ### 对话终止条件
> - 自伤或暴力倾向 → 永不终止对话
> - 滥用行为 → 多次重定向失败后可终止
> - 用户主动请求 → 需确认永久性

**相关文档 | Related Documents:**
- [[02-Annotated/end-conversation]]
- [[01-Annotated/copyright-boundaries]]

---

## 🧪 学习检验 | Learning Assessment

### 自我检查 | Self-Check

> [!question] 自我检查 | Self-Check
> 在继续深入学习前，问自己：
>
> 1. **概念理解**：你能解释什么是 "interleaved thinking mode" 吗？
> 2. **决策判断**：以下情况是否应该调用 web_search？
>    - "Python 中的 for 循环语法是什么？"
>    - "今天的天气怎么样？"
>    - "分析 2024 年美国总统选举的影响"
> 3. **应用能力**：如何使用 conversation_search 找到上周讨论的 "Claude artifacts"？
>
> ==关键点 | Key Point==：**搜索决策**（Search Decision）和**思维模式**（Thinking Mode）是现代 AI 系统提示词的两大核心创新。

---

## 📖 学习资源 | Learning Resources

### 官方资源 | Official Resources

- [Anthropic System Prompts Documentation](https://docs.anthropic.com/en/release-notes/system-prompts)
- [Claude.ai Documentation](https://docs.anthropic.com/en/docs/claude)
- [Anthropic Research](https://www.anthropic.com/research)

### 相关框架 | Related Frameworks

- [[DocFramework/Diataxis/02-Annotated/start-here]] - 文档分类框架
- [[DocFramework/Google-Style-Guide/02-Annotated/highlights]] - 技术写作风格
- [[DocFramework/Microsoft-Style-Guide/02-Annotated/welcome]] - 写作风格指南

---

## 📝 学习笔记模板 | Learning Note Template

当学习新的系统提示词文档时，使用以下模板：

```markdown
---
title: "[文档标题 | Document Title]"
source: "[来源 URL]"
source_type: "Anthropic"
status: annotated # reading | annotated | practicing | mastered
importance: "[low|medium|high|critical]"
difficulty: "[beginner|intermediate|advanced|expert]"
learning_stage: "[reading|comprehension|application|mastery]"
annotation_version: "1.0"
tags:
  - system-prompts
  - [specific-tags]
---

> [!success] 核心要点 | Core Concept
> ==核心概念 | Core Concept==

> [!question] 启发式思考 | Guiding Question
> **核心问题 | Core Question**：[问题 | Question]
> **提示 | Hint**：[思考方向 | Thinking direction]
>
> <details>
> <summary>查看答案与解析 | View Answer & Analysis</summary>
>
> **答案 | Answer**：[详细答案 | Detailed answer]
>
> **深入分析 | Deep Dive**：[深入分析 | In-depth analysis]
> **实际应用 | Application**：[如何应用 | How to apply]
> </details>

> [!example] 示例 | Example
> **好做法 | Good Practice**：
> ```markdown
> # 好的做法
> ```
>
> **坏做法 | Bad Practice**：
> ```markdown
> # 不好的做法
> ```
```

---

**最后更新 | Last Updated**: 2026-02-06
**下一计划 | Next Review**: 2026-02-13