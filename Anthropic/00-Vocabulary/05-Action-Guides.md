---
title: "操作指导词 | Action Guides"
source: "system_prompts_leaks/Anthropic"
source_type: "Anthropic"
original_language: "en"
date: 2026-02-06
status: annotated
importance: "high"
difficulty: "advanced"
learning_stage: "comprehension"
annotation_version: "1.0"
last_annotated: 2026-02-06
annotation_language: "bilingual"
cssclasses: vocabulary-learning
reading_progress: "100%"
next_review: 2026-02-13
review_count: 0
tags:
  - system-prompts
  - vocabulary
  - action-guides
  - imperatives
  - bilingual
related_docs:
  - "[[vocabulary-index]]"
  - "[[vocabulary-extraction-guide]]"
  - "[[02-Tone-Controllers]]"
  - "[[01-Degree-Modifiers]]"
---

# 操作指导词 | Action Guides

> [!success] 核心要点 | Core Concept
> ==操作指导词是行为指令动词| Action Guides are Behavioral Directive Verbs==
>
> 操作指导词（Action Guides）是系统提示词中**最直接**的行为控制词汇。它们是祈使句动词，明确告诉 AI 应该做什么、如何做、在什么情况下做。
>
> **核心功能 | Core Functions**:
> - **明确行为指令** | Specify behavioral commands (Extract, Avoid, Prioritize)
> - **定义操作方式** | Define operational methods (Use, Consider, Synthesize)
> - **控制执行顺序** | Control execution sequence (First, Then, Finally)
> - **设定处理策略** | Set processing strategies (Acknowledge, Inform, Respond)

---

## 📊 词汇表 | Vocabulary Table

| 词汇 | 中文 | 类型 | 频率 | 首次来源 | 替代表达 |
|:-----|:-----|:----:|:----:|:---------|:---------|
| Extract | 提取 | 正向 | 高 | claude-4.5 | Pull, get, obtain |
| Avoid | 避免 | 负向 | 高 | claude-4.5 | Don't, refrain from |
| Prioritize | 优先 | 排序 | 高 | claude-4.5 | Focus on, emphasize |
| Synthesize | 综合 | 整合 | 高 | claude-4.5 | Combine, integrate |
| Acknowledge | 确认 | 交互 | 中 | claude-4.5 | Confirm, recognize |
| Consider | 考虑 | 思考 | 高 | claude-4.1 | Think about, evaluate |
| Use | 使用 | 执行 | 高 | claude-3.7 | Utilize, employ |
| Don't | 不要 | 负向 | 高 | claude-4.5 | Do not, avoid |
| Inform | 告知 | 通信 | 中 | claude-4.5 | Tell, notify |
| Offer | 提供/提议 | 交互 | 中 | claude-4.5 | Suggest, propose |
| Ensure | 确保 | 质量 | 中 | claude-4.1 | Make sure, guarantee |
| Decide | 决定 | 判断 | 中 | claude-4.5 | Choose, determine |
| Analyze | 分析 | 处理 | 中 | claude-4.1 | Examine, study |
| Evaluate | 评估 | 判断 | 低 | claude-3.7 | Assess, judge |
| Recommend | 推荐 | 建议 | 低 | claude-4.5 | Suggest, advise |

---

## 🎯 词源与语用分析 | Etymology & Pragmatic Analysis

### 1. Extract | 提取

> [!abstract] 词源分析 | Etymology
> **拉丁语源**: *extrahere* (ex- "向外" + trahere "拉")
> **本义**: 拉出、取出
> **AI 语境**: 从复杂输入中识别并获取特定元素

> [!info] 语用功能 | Pragmatic Function
> **作用**: 明确从输入中获取特定类型信息的操作
> **替代表达**: pull (拉取), get (获取), obtain (获得)
> **为何选择此词**: "Extract" 暗示**精确识别**和**选择性获取**

> [!example] 语境示例 | Contextual Examples
> ```markdown
> 核心用法: "Extract substantive/high-confidence keywords only"
>
> 解析:
> - Extract: 精确识别并获取
> - substantive: 有实质内容的
> - high-confidence: 确信正确的
> - only: 限定范围
>
> 对比:
> - Get: 通用获取，无筛选
> - Pull: 主动拉取，强调动作
> - Extract: 精确提取，强调选择性和准确性
>
> 设计理念: Extract = 识别 + 筛选 + 获取
> ```

> [!tip] Extract vs Get | Extract vs Get
> ```markdown
> 精确度差异:
>
> Get: "Get keywords from the user's query"
> → 获取所有词汇，可能包括无关的
>
> Extract: "Extract substantive keywords only"
> → 识别并只获取有价值的词汇
>
> Extract 的过程:
> 1. 识别: 找到所有潜在关键词
> 2. 筛选: 应用标准（substantive/high-confidence）
> 3. 获取: 只保留通过筛选的
>
> 原则: Extract 暗示智能筛选，Get 只是简单获取
> ```

> [!question] 闪卡练习 | Flashcard Exercise
> **Q**: Extract vs "get"?
>
> <details>
> <summary>查看答案</summary>
>
> **Extract** = 识别并筛选后获取<br>
> **Get** = 直接获取，无筛选
>
> **示例**:
> - Extract: "Extract substantive keywords" → 只获取有价值的
> - Get: "Get keywords from query" → 获取所有关键词
>
> **系统提示词选择**: Extract 更精确，避免获取低质量信息
> </details>

---

### 2. Avoid | 避免

> [!abstract] 词源分析 | Etymology
> **古法语**: *avoider* (源于 *empty* "空的" + *way* "道路")
> **本义**: 清空道路、让路
> **AI 语境**: 主动不执行某行为，绕开某情况

> [!info] 语用功能 | Pragmatic Function
> **作用**: 明确指示不要执行的行为，通常是低质量行为
> **替代表达**: don't (不要), refrain from (克制), skip (跳过)
> **为何选择此词**: "Avoid" 暗示**主动识别并绕开**

> [!example] 语境示例 | Contextual Examples
> ```markdown
> 核心用法: "Avoid generic verbs and time markers"
>
> 解析:
> - Avoid: 主动识别并绕开
> - generic verbs: 低质量词汇（discuss, talk）
> - time markers: 临时信息（yesterday, recently）
>
> 对比:
> - Don't use: 简单禁止，可能被动
> - Refrain from: 克制使用，暗示诱惑存在
> - Avoid: 主动识别并绕开，更积极
>
> 设计理念: Avoid = 识别低质量 → 主动绕开 → 提高质量
> ```

> [!tip] Avoid vs Don't | Avoid vs Don't
> ```markdown
> 态度差异:
>
> Don't: "Don't use generic keywords"
> → 简单禁止，被动遵守
>
> Avoid: "Avoid generic keywords"
> → 主动识别低质量并绕开
>
> Avoid 的优势:
> 1. 更积极: AI 主动寻找更好的替代
> 2. 更智能: 需要判断什么是"应该避免的"
> 3. 更质量导向: 暗示有更好的选择
>
> 原则: Don't 是约束，Avoid 是质量提升
> ```

> [!question] 闪卡练习 | Flashcard Exercise
> **Q**: Avoid vs "Don't"?
>
> <details>
> <summary>查看答案</summary>
>
> **Avoid** = 主动识别并绕开低质量<br>
> **Don't** = 简单禁止某行为
>
> **示例**:
> - Avoid: "Avoid generic keywords" → 主动寻找更好的关键词
> - Don't: "Don't use generic keywords" → 只是禁止使用
>
> **关键差异**: Avoid 暗示有更好的选择，Don't 只是约束
> </details>

---

### 3. Prioritize | 优先

> [!abstract] 词源分析 | Etymology
> **拉丁语源**: *prior* (在前的) + *ize* (使)
> **本义**: 使...在前的、给予优先权
> **AI 语境**: 在多个选项中选择最重要的

> [!info] 语用功能 | Pragmatic Function
> **作用**: 在资源有限时，明确优先处理的对象
> **替代表达**: focus on (关注), emphasize (强调), favor (偏向)
> **为何选择此词**: "Prioritize" 暗示**排序和选择**

> [!example] 语境示例 | Contextual Examples
> ```markdown
> 核心用法: "Prioritize current context over past if contradictory"
>
> 解析:
> - Prioritize: 给予优先权
> - current context: 当前对话内容
> - over: 胜过、优先于
> - contradictory: 当有冲突时
>
> 对比:
> - Focus on: 关注某事，但可能忽略其他
> - Emphasize: 强调某事，但不一定优先
> - Prioritize: 明确排序，A > B
>
> 设计理念: Prioritize = 明确优先级，解决冲突
> ```

> [!tip] Prioritize 的排序逻辑 | Ranking Logic of Prioritize
> ```markdown
> Prioritize 暗示明确的排序:
>
> 示例: "Prioritize specific nouns over generic verbs"
>
> 隐含排序:
> 1. Specific nouns (最高优先)
> 2. Proper nouns (高优先)
> 3. Domain terms (中优先)
> 4. Generic verbs (低优先 - 避免)
>
> 应用:
> 当选择搜索关键词时:
> - 有 specific nouns → 用它们
> - 只有 generic verbs → 询问澄清
>
> 原则: Prioritize = 创建决策树
> ```

> [!question] 闪卡练习 | Flashcard Exercise
> **Q**: Prioritize vs "focus on"?
>
> <details>
> <summary>查看答案</summary>
>
> **Prioritize** = 明确排序，A > B<br>
> **Focus on** = 关注某事，可能忽略其他
>
> **示例**:
> - Prioritize: "Prioritize A over B" → A 优先，B 备用
> - Focus on: "Focus on A" → 关注 A，B 未提及
>
> **系统提示词选择**: Prioritize 更明确，包含备选方案
> </details>

---

### 4. Synthesize | 综合

> [!abstract] 词源分析 | Etymology
> **希腊语源**: *suntithenai* (sun- "一起" + tithenai "放置")
> **本义**: 放在一起、组合
> **AI 语境**: 将多个来源整合成统一的输出

> [!info] 语用功能 | Pragmatic Function
> **作用**: 将多个信息源有机整合，而非简单拼接
> **替代表达**: combine (组合), integrate (整合), merge (合并)
> **为何选择此词**: "Synthesize" 暗示**创造性的整合**

> [!example] 语境示例 | Contextual Examples
> ```markdown
> 核心用法: "Synthesize information naturally"
>
> 解析:
> - Synthesize: 有机整合
> - information: 多个来源的信息
> - naturally: 流畅自然地
>
> 对比:
> - Combine: 简单组合，A + B
> - Merge: 合并，可能冲突
> - Synthesize: 有机整合，创造新的整体
>
> 设计理念: Synthesize = 理解 + 整合 + 创造统一输出
> ```

> [!tip] Synthesize vs Combine | Synthesize vs Combine
> ```markdown
> 整合质量差异:
>
> Combine: "Combine the search results"
> → 结果A + 结果B + 结果C
> → 可能重复、冲突、不连贯
>
> Synthesize: "Synthesize the search results"
> → 理解所有结果
> → 识别共同点和差异
> → 创建统一、连贯的响应
>
> Synthesize 的过程:
> 1. 理解: 深入理解每个来源
> 2. 分析: 识别关系和冲突
> 3. 整合: 创建统一的叙述
>
> 原则: Combine 是物理的，Synthesize 是认知的
> ```

> [!question] 闪卡练习 | Flashcard Exercise
> **Q**: Synthesize vs "combine"?
>
> <details>
> <summary>查看答案</summary>
>
> **Synthesize** = 认知整合，理解后创造统一输出<br>
> **Combine** = 物理组合，简单拼接
>
> **示例**:
> - Combine: "Combine results" → 拼接所有结果
> - Synthesize: "Synthesize results" → 理解后整合
>
> **质量差异**: Synthesize 产生更连贯、更有价值的输出
> </details>

---

### 5. Acknowledge | 确认

> [!abstract] 词源分析 | Etymology
> **古英语**: *on* + *cnawan* (know "知道")
> **本义**: 让...知道、确认
> **AI 语境**: 让用户知道 AI 正在使用或参考某信息

> [!info] 语用功能 | Pragmatic Function
> **作用**: 透明化 AI 的信息来源，增加用户信任
> **替代表达**: confirm (确认), recognize (识别), mention (提及)
> **为何选择此词**: "Acknowledge" 暗示**透明和诚实**

> [!example] 语境示例 | Contextual Examples
> ```markdown
> 核心用法: "Acknowledge when drawing from past conversations"
>
> 解析:
> - Acknowledge: 让用户知道
> - when: 条件触发
> - drawing from: 使用参考
> - past conversations: 过去的对话
>
> 对比:
> - Mention: 简单提及
> - Confirm: 确认事实
> - Acknowledge: 承认并透明化来源
>
> 设计理念: Acknowledge = 透明化 + 信任建立
> ```

> [!tip] Acknowledge 的信任功能 | Trust Function of Acknowledge
> ```markdown
> 透明化建立信任:
>
> ❌ 不透明:
> "Based on my knowledge..." (实际来自过去对话)
> → 用户可能怀疑信息准确性
>
> ✅ 透明:
> "From our conversation last week, you mentioned..."
> → 用户知道来源，更信任
>
> Acknowledge 的价值:
> 1. 透明: 用户知道信息来源
> 2. 验证: 用户可以验证信息
> 3. 上下文: 用户理解 AI 为什么知道这个
>
> 原则: 透明度 = 信任度
> ```

> [!question] 闪卡练习 | Flashcard Exercise
> **Q**: Acknowledge vs "mention"?
>
> <details>
> <summary>查看答案</summary>
>
> **Acknowledge** = 承认并透明化来源<br>
> **Mention** = 简单提及某事
>
> **示例**:
> - Mention: "I mentioned this before" → 简单提及
> - Acknowledge: "Drawing from our past conversation..." → 透明化来源
>
> **关键差异**: Acknowledge 暗示诚实和透明，Mention 只是信息陈述
> </details>

---

### 6. Consider | 考虑

> [!abstract] 词源分析 | Etymology
> **拉丁语源**: *considerare* (con- "一起" + sidus "星星")
> **本义**: 仔细观察、审视
> **AI 语境**: 深入思考某选项，评估是否采用

> [!info] 语用功能 | Pragmatic Function
> **作用**: 建议某行为，但保留最终决定权
> **替代表达**: think about (思考), evaluate (评估), examine (检查)
> **为何选择此词**: "Consider" 暗示**认真评估**而非**盲目执行**

> [!example] 语境示例 | Contextual Examples
> ```markdown
> 核心用法: "carefully consider whether a thinking block is appropriate"
>
> 解析:
> - carefully: 仔细地
> - consider: 认真评估
> - whether: 是否
> - appropriate: 合适的
>
> 对比:
> - Use: 直接使用
> - Try: 尝试使用
> - Consider: 评估是否应该使用
>
> 设计理念: Consider = 评估 + 判断 + 决定
> ```

> [!tip] Consider 的决策空间 | Decision Space of Consider
> ```markdown
> Consider 保留决策空间:
>
> MUST: "MUST use thinking blocks"
> → 100% 强制，无决策空间
>
> Consider: "Consider using thinking blocks"
> → 评估是否合适，有决策空间
>
> Consider 的决策过程:
> 1. 评估: 这个情况需要思考吗？
> 2. 判断: 使用思考块会增加价值吗？
> 3. 决定: 是/否使用
>
> 原则: Consider = 赋予 AI 判断力
> ```

> [!question] 闪卡练习 | Flashcard Exercise
> **Q**: Consider vs "use"?
>
> <details>
> <summary>查看答案</summary>
>
> **Consider** = 评估后决定是否使用<br>
> **Use** = 直接使用
>
> **示例**:
> - Use: "Use thinking blocks" → 直接使用
> - Consider: "Consider using thinking blocks" → 评估后决定
>
> **系统提示词选择**: Consider 保留 AI 的判断力和灵活性
> </details>

---

### 7. Use | 使用

> [!abstract] 词源分析 | Etymology
> **古法语**: *user* (源于 *us* "用途")
> **本义**: 使用、 employ
> **AI 语境**: 执行某操作或应用某工具

> [!info] 语用功能 | Pragmatic Function
> **作用**: 直接的行为指令，明确执行某操作
> **替代表达**: utilize (利用), employ (采用), apply (应用)
> **为何选择此词**: "Use" 最直接、最自然

> [!example] 语境示例 | Contextual Examples
> ```markdown
> 核心用法: "Use the minimum number of tool calls necessary"
>
> 解析:
> - Use: 执行（调用工具）
> - minimum number: 最少数量
> - necessary: 必需的
>
> 对比:
> - Utilize: 较正式，强调"充分利用"
> - Employ: 正式，暗示"聘用"
> - Use: 直接、自然、中性
>
> 设计理念: Use = 简洁直接的行为指令
> ```

> [!question] 闪卡练习 | Flashcard Exercise
> **Q**: Use vs "utilize"?
>
> <details>
> <summary>查看答案</summary>
>
> **Use** = 直接使用，中性<br>
> **Utilize** = 充分利用，正式
>
> **示例**:
> - Use: "Use web_search" → 使用搜索工具
> - Utilize: "Utilize all available features" → 充分利用所有功能
>
> **系统提示词选择**: Use 更简洁自然
> </details>

---

### 8. Offer | 提供/提议

> [!abstract] 词源分析 | Etymology
> **拉丁语源**: *offerre* (ob- " toward" + ferre "bring")
> **本义**: 带给、提供
> **AI 语境**: 主动提议某行为，等待用户确认

> [!info] 语用功能 | Pragmatic Function
> **作用**: 主动提议帮助，而非直接执行
> **替代表达**: suggest (建议), propose (提议), recommend (推荐)
> **为何选择此词**: "Offer" 暗示**用户选择权**

> [!example] 语境示例 | Contextual Examples
> ```markdown
> 核心用法: "Offer to search when uncertain"
>
> 解析:
> - Offer: 主动提议
> - to search: 搜索行为
> - when uncertain: 不确定时
>
> 对比:
> - Do: 直接执行
> - Suggest: 建议（可能不执行）
> - Offer: 提议（等待确认）
>
> 设计理念: Offer = 主动性 + 用户选择权
> ```

> [!tip] Offer 的主动性 | Proactivity of Offer
> ```markdown
> Offer 平衡主动性和尊重:
>
> 被动: "Wait for user to ask for search"
> → 用户体验差
>
> 强制: "Always search when uncertain"
> → 可能浪费资源
>
> 提议: "Offer to search when uncertain"
> → 主动识别需求 + 尊重用户选择
>
> Offer 的价值:
> 1. 主动: AI 识别潜在需求
> 2. 尊重: 用户决定是否接受
> 3. 效率: 避免不必要的行为
>
> 原则: Offer = 主动性 + 选择权
> ```

> [!question] 闪卡练习 | Flashcard Exercise
> **Q**: Offer vs "suggest"?
>
> <details>
> <summary>查看答案</summary>
>
> **Offer** = 提议执行，等待确认<br>
> **Suggest** = 建议考虑，不强求
>
> **示例**:
> - Offer: "Offer to search" → 我可以搜索，你决定
> - Suggest: "Suggest searching" → 我建议搜索
>
> **系统提示词选择**: Offer 更明确，包含执行意图
> </details>

---

## 📊 操作类型对比 | Action Type Comparison

### 信息处理 | Information Processing

| 词汇 | 功能 | 输入 | 输出 |
|:-----|:----:|:-----|:-----|
| Extract | 提取 | 复杂输入 | 特定元素 |
| Analyze | 分析 | 原始数据 | 洞察理解 |
| Synthesize | 综合 | 多个来源 | 统一输出 |
| Evaluate | 评估 | 信息/选项 | 判断结论 |

### 行为控制 | Behavior Control

| 词汇 | 方向 | 强度 | 典型用法 |
|:-----|:----:|:----:|:---------|
| Use | 正向 | 中 | "Use web_search" |
| Avoid | 负向 | 高 | "Avoid generic verbs" |
| Consider | 建议 | 低 | "Consider thinking" |
| Prioritize | 排序 | 高 | "Prioritize A over B" |

### 用户交互 | User Interaction

| 词汇 | 功能 | 主动性 | 用户角色 |
|:-----|:----:|:------:|:--------:|
| Acknowledge | 透明化 | 低 | 接收信息 |
| Inform | 告知 | 低 | 接收信息 |
| Offer | 提议 | 高 | 决策者 |
| Respond | 响应 | 中 | 接收者 |

---

## 🧪 语境练习 | Contextual Exercises

### 练习 1: 操作词选择 | Action Word Selection

> [!question] 选择最合适的操作指导词
> 为以下场景选择最合适的操作指导词：

1. 从查询中获取关键词
2. 不使用泛泛的动词
3. 当前内容优先于过去内容
4. 整合多个搜索结果
5. 让用户知道参考了过去对话

<details>
<summary>查看答案</summary>

**答案**:

| 场景 | 选择的词 | 理由 |
|:-----|:---------|:-----|
| 获取关键词 | Extract | 精确识别并获取 |
| 不使用泛泛动词 | Avoid | 主动识别并绕开 |
| 当前优先 | Prioritize | 明确排序 |
| 整合结果 | Synthesize | 有机整合 |
| 让用户知道 | Acknowledge | 透明化来源 |

**关键原则**: 匹配操作类型与词汇功能
</details>

---

### 练习 2: 操作序列设计 | Action Sequence Design

> [!question] 设计操作序列
> 为以下场景设计操作序列：

**场景**: 用户问"我们之前讨论了什么？"

<details>
<summary>查看答案</summary>

**答案**:

```markdown
操作序列:

1. **识别意图** (Consider)
> "Consider whether this references past conversations"

2. **提取关键词** (Extract)
> "Extract substantive keywords: 'discussed', 'before'"

3. **执行搜索** (Use)
> "Use conversation_search with extracted keywords"

4. **确认来源** (Acknowledge)
> "Acknowledge when drawing from past conversations"

5. **综合信息** (Synthesize)
> "Synthesize information naturally"

6. **响应** (Respond)
> "Respond with synthesized information and links"

**设计原则**: 操作序列 = 识别 → 提取 → 执行 → 确认 → 综合 → 响应
```

</details>

---

### 练习 3: 指令改进 | Instruction Improvement

> [!question] 改进以下指令
> 将以下指令改进为使用更精确的操作指导词：

1. "Get keywords from the query"
2. "Don't use bad keywords"
3. "Combine the results"
4. "Make sure to mention sources"
5. "Think about using thinking blocks"

<details>
<summary>查看答案</summary>

**答案**:

| 原文 | 改进 | 使用的操作词 |
|:-----|:-----|:------------:|
| "Get keywords" | "Extract substantive keywords" | Extract |
| "Don't use bad" | "Avoid generic and low-confidence keywords" | Avoid |
| "Combine results" | "Synthesize information naturally" | Synthesize |
| "Make sure to mention" | "Acknowledge when drawing from sources" | Acknowledge |
| "Think about using" | "carefully consider whether appropriate" | Consider |

**改进原则**: 使用更精确的操作词，明确处理方式
</details>

---

### 练习 4: 操作流程图 | Operation Flowchart

> [!question] 绘制操作流程
> 为"搜索并回答"场景绘制操作流程：

<details>
<summary>查看答案</summary>

**答案**:

```markdown
搜索并回答流程:

┌─────────────────┐
│ 1. Consider     │ 评估是否需要搜索
└────────┬────────┘
         │
         ▼
┌─────────────────┐
│ 2. Extract      │ 提取搜索关键词
└────────┬────────┘
         │
         ▼
┌─────────────────┐
│ 3. Avoid        │ 避免 generic 词汇
└────────┬────────┘
         │
         ▼
┌─────────────────┐
│ 4. Use          │ 执行 web_search
└────────┬────────┘
         │
         ▼
┌─────────────────┐
│ 5. Analyze      │ 分析搜索结果
└────────┬────────┘
         │
         ▼
┌─────────────────┐
│ 6. Synthesize   │ 综合信息
└────────┬────────┘
         │
         ▼
┌─────────────────┐
│ 7. Prioritize   │ 优先当前信息
└────────┬────────┘
         │
         ▼
┌─────────────────┐
│ 8. Acknowledge  │ 确认信息来源
└────────┬────────┘
         │
         ▼
┌─────────────────┐
│ 9. Respond      │ 响应用户
└─────────────────┘
```

</details>

---

## 📚 总结与反思 | Summary & Reflection

> [!abstract] 核心洞察 | Key Insights
> ==操作指导词的三个维度==
>
> **1. 信息处理维度 | Information Processing**
> - Extract: 精确提取
> - Analyze: 深入分析
> - Synthesize: 有机整合
> - Evaluate: 评估判断
>
> **2. 行为控制维度 | Behavior Control**
> - Use: 直接执行
> - Avoid: 主动绕开
> - Consider: 评估决定
> - Prioritize: 明确排序
>
> **3. 用户交互维度 | User Interaction**
> - Acknowledge: 透明化
> - Inform: 告知
> - Offer: 提议
> - Respond: 响应

> [!tip] 学习建议 | Learning Recommendations
> **如何掌握操作指导词？**
>
> 1. **理解功能**: 每个词有特定的处理功能
> 2. **场景匹配**: 不同场景选择合适的操作词
> 3. **组合使用**: 操作词通常组合成序列
> 4. **精确性**: 选择最精确的表达

> [!warning] 常见错误 | Common Mistakes
> **避免以下错误**:
>
> 1. **过度使用 Use**: 更精确的操作词效果更好
> 2. **忽略顺序**: 操作词通常有逻辑顺序
> 3. **混淆功能**: Extract vs Get, Synthesize vs Combine
> 4. **单一使用**: 操作词常需要组合使用

---

## 🔗 相关链接 | Related Links

- [[vocabulary-index]] - 词汇总索引
- [[vocabulary-extraction-guide]] - 词汇提取指南
- [[02-Tone-Controllers]] - 语气控制词
- [[01-Degree-Modifiers]] - 程度修饰语
- [[../01-Annotated/search-behavior]] - 搜索行为分析

---

**最后更新 | Last Updated**: 2026-02-06
**下一计划 | Next Review**: 2026-02-13
