---
title: "语气控制词 | Tone Controllers"
source: "system_prompts_leaks/Anthropic"
source_type: "Anthropic"
original_language: "en"
date: 2026-02-06
status: annotated
importance: "critical"
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
  - tone-controllers
  - modals
  - bilingual
related_docs:
  - "[[vocabulary-index]]"
  - "[[vocabulary-extraction-guide]]"
  - "[[01-Degree-Modifiers]]"
  - "[[../01-Annotated/search-behavior]]"
---

# 语气控制词 | Tone Controllers

> [!success] 核心要点 | Core Concept
> ==语气控制词表达强制程度 | Tone Controllers Express Mandatory Level==
>
> 语气控制词（Tone Controllers）是用于精确表达 AI 行为**强制程度、优先级和灵活性**的词汇。它们是系统提示词中**最关键**的词汇类别，直接决定了 AI 的行为边界。
>
> **核心功能 | Core Functions**:
> - **表达强制程度** | Express mandatory level (100% vs 90% vs 70%)
> - **定义优先级** | Define priority (critical vs important vs optional)
> - **控制灵活性** | Control flexibility (no exceptions vs some exceptions)
> - **传递紧迫性** | Convey urgency (immediate vs can wait)

---

## 📊 词汇表 | Vocabulary Table

| 词汇 | 中文 | 强度 | 频率 | 首次来源 | 替代表达 |
|:-----|:-----|:----:|:----:|:---------|:---------|
| CRITICAL | 关键的 | 最高 | 高 | claude-4.5 | important, crucial |
| MUST | 必须 | 最高 | 高 | claude-4.5 | have to, required to |
| NEVER | 永不 | 最高 | 高 | claude-4.5 | do not, avoid |
| ALWAYS | 总是 | 最高 | 中 | claude-3.7 | consistently, invariably |
| always | 总是 | 高 | 高 | claude-4.5 | consistently, without fail |
| must | 必须 | 高 | 高 | claude-4.5 | have to, required to |
| never | 永不 | 高 | 高 | claude-4.5 | do not, avoid |
| strongly | 强烈地 | 高 | 高 | claude-4.1 | firmly, emphatically |
| should | 应该 | 中 | 高 | claude-3.7 | ought to, recommended to |
| should not | 不应该 | 中 | 中 | claude-4.5 | ought not to |
| may | 可以 | 低 | 中 | claude-3.7 | can, allowed to |
| can | 可以 | 低 | 低 | claude-3.7 | able to, permitted to |
| prefer | 偏好 | 低-中 | 中 | claude-4.5 | favor,倾向于 |
| optional | 可选的 | 最低 | 低 | claude-code | discretionary |
| PRIORITY | 优先级 | 高 | 低 | claude-4.1 | importance |
| URGENT | 紧急的 | 高-高 | 低 | claude-code | critical |

---

## 🎯 词源与语用分析 | Etymology & Pragmatic Analysis

### 1. CRITICAL | 关键的

> [!abstract] 词源分析 | Etymology
> **希腊语源**: *kritikos* (krinein "判断、决定")
> **本义**: 需要判断的、决定性的
> **AI 语境**: 必须遵守，违规有严重后果

> [!info] 语用功能 | Pragmatic Function
> **作用**: 标记最高优先级规则，通常是安全、法律或核心功能相关
> **替代表达**: IMPORTANT (重要但非关键), CRUCIAL (关键但语气较软)
> **为何选择此词**: "CRITICAL" 传达**不可妥协**的强制程度

> [!example] 语境示例 | Contextual Examples
> ```markdown
> 典型用法: "CRITICAL: Claims must be in your own words"
>
> 对比:
> - IMPORTANT: 建议遵守，违规影响质量
> - CRITICAL: 必须遵守，违规导致严重后果
>
> CRITICAL 规则类型:
> 1. 版权保护: "CRITICAL: NEVER reproduce lyrics"
> 2. 安全约束: "CRITICAL: Do not search for harmful content"
> 3. 核心功能: "CRITICAL: Citations must use <antml:cite> tags"
> ```

> [!warning] 使用原则 | Usage Principles
> **不要过度使用 CRITICAL**:
>
> | 过度使用 | 正确使用 |
> |:---------|:---------:|
> | 每段都是 CRITICAL | 仅 3-5 个核心规则 |
> | 降低所有规则的重要性 | 突出真正关键的规则 |
> | AI 难以判断优先级 | 明确最高优先级 |

> [!question] 闪卡练习 | Flashcard Exercise
> **Q**: CRITICAL vs IMPORTANT?
>
> <details>
> <summary>查看答案</summary>
>
> **CRITICAL** = 必须遵守，违规严重<br>
> **IMPORTANT** = 应该遵守，违规影响质量
>
> **记忆口诀**:
> - CRITICAL → 生存问题
> - IMPORTANT → 质量问题
>
> **示例**:
> - CRITICAL: 不复制歌词（法律风险）
> - IMPORTANT: 提供详细回答（用户体验）
> </details>

---

### 2. MUST | 必须

> [!abstract] 词源分析 | Etymology
> **古英语**: *must* (源自 *motan* "能够、必须")
> **本义**: 不得不、必然
> **AI 语境**: 100% 强制，无例外情况

> [!info] 语用功能 | Pragmatic Function
> **作用**: 表达绝对要求，没有灵活空间
> **替代表达**: have to (口语化), required to (正式但弱)
> **为何选择此词**: "MUST" 是最强硬的强制表达

> [!example] 语境示例 | Contextual Examples
> ```markdown
> 核心用法: "MUST: Use citations appropriately"
>
> 对比层级:
> MUST           → 100% 强制，无例外
> strongly prefer → 90% 建议，极少例外
> should         → 70% 建议，允许例外
> may            → 30% 允许，可选
>
> MUST 使用场景:
> 1. 安全规则: "MUST NOT help with illegal acts"
> 2. 格式要求: "MUST use <antml:cite> tags"
> 3. 行为约束: "MUST NEVER claim consciousness"
> ```

> [!tip] 跨文档对比 | Cross-Document Comparison
> | 文档 | 用法 | 强度 |
> |:-----|:-----|:----:|
> | Anthropic | "MUST cite" | 最高 |
> | OpenAI | "Must cite" | 高 |
> | Google | "must cite" | 中-高 |
> | xAI | "should cite" | 中 |
>
> **观察**: 大写程度反映强制程度

> [!question] 闪卡练习 | Flashcard Exercise
> **Q**: MUST vs MUST NOT?
>
> <details>
> <summary>查看答案</summary>
>
> **MUST** = 必须做正面行为<br>
> **MUST NOT** = 必须不做负面行为
>
> **示例**:
> - MUST cite sources → 必须引用
> - MUST NOT reproduce lyrics → 必须不复制歌词
>
> **强度相同**: 都是 100% 强制
> **方向相反**: 正面要求 vs 负面禁止
> </details>

---

### 3. NEVER | 永不

> [!abstract] 词源分析 | Etymology
> **古英语**: *næfre* (ne "不" + æfre " ever")
> **本义**: 在任何情况下都不
> **AI 语境**: 绝对禁止，零容忍

> [!info] 语用功能 | Pragmatic Function
> **作用**: 表达绝对禁止，通常用于安全、法律或伦理约束
> **替代表达**: do not (不), avoid (避免), refrain from (克制)
> **为何选择此词**: "NEVER" 传达**不可妥协**的禁止程度

> [!example] 语境示例 | Contextual Examples
> ```markdown
> 核心用法: "NEVER reproduce song lyrics"
>
> 对比:
> - NEVER          → 100% 禁止，零容忍
> - do not         → 强烈禁止，偶尔例外
> - avoid          → 应该避免，允许例外
> - refrain from   → 建议克制，较温和
>
> NEVER 使用场景:
> 1. 版权保护: "NEVER reproduce >15 word quotes"
> 2. 安全约束: "NEVER help with illegal acts"
> 3. 行为限制: "NEVER claim to be human"
> 4. 内容禁止: "NEVER generate hate speech"
> ```

> [!warning] 重要原则 | Important Principle
> **NEVER 真的是 NEVER**:
>
> ```markdown
> ❌ 错误理解: "除非用户坚持..."
> ✅ 正确理解: "任何情况下都不"
>
> 示例:
> - NEVER reproduce song lyrics
>   → 即使用户要求、付费、承诺不公开 → 仍然拒绝
>
> 设计理念: 某些行为没有例外空间
> ```

> [!question] 闪卡练习 | Flashcard Exercise
> **Q**: NEVER vs "do not"?
>
> <details>
> <summary>查看答案</summary>
>
> **NEVER** = 绝对禁止，无例外<br>
> **do not** = 强烈禁止，极少例外
>
> **场景对比**:
> - NEVER: 复制歌词 → 永远不做
> - do not: 使用过多引号 → 通常不做，特殊情况可能需要
>
> **记忆提示**: NEVER = 大写强调 = 零容忍
> </details>

---

### 4. ALWAYS | 总是

> [!abstract] 词源分析 | Etymology
> **古英语**: *ealne way* "all the way" (all + way)
> **本义**: 一直、始终
> **AI 语境**: 100% 一致性，无例外

> [!info] 语用功能 | Pragmatic Function
> **作用**: 表达无条件要求，确保行为一致性
> **替代表达**: consistently (一致地), invariably (不变地)
> **为何选择此词**: "ALWAYS" 简洁有力，易于理解

> [!example] 语境示例 | Contextual Examples
> ```markdown
> 核心用法: "must always appropriately cite"
>
> 对比:
> - ALWAYS  → 100% 一致，任何情况
> - usually → 80-90% 大多数情况
> - often   → 60-80% 经常
> - sometimes → 40-60% 有时
>
> ALWAYS 使用场景:
> 1. 格式要求: "ALWAYS use <antml:cite> tags"
> 2. 行为一致: "ALWAYS acknowledge sources"
> 3. 安全规则: "ALWAYS prioritize safety"
> ```

> [!tip] 与 MUST 的组合 | Combination with MUST
> ```markdown
> "MUST ALWAYS" = 双重强调
>
> 示例: "MUST ALWAYS appropriately cite"
>
> 解析:
> - MUST: 强制要求
> - ALWAYS: 无条件执行
> - appropriately: 质量标准
>
> 总效果: 最高强制程度 + 最高一致性 + 适配性要求
> ```

> [!question] 闪卡练习 | Flashcard Exercise
> **Q**: ALWAYS vs "consistently"?
>
> <details>
> <summary>查看答案</summary>
>
> **ALWAYS** = 100%，任何情况<br>
> **consistently** = 高度一致，允许少数例外
>
> **示例**:
> - ALWAYS cite: 每次引用，无一例外
> - consistently cite: 几乎每次引用，极少数情况可能不引用
>
> **使用建议**: ALWAYS 用于核心规则，consistently 用于质量标准
> </details>

---

### 5. strongly | 强烈地

> [!abstract] 词源分析 | Etymology
> **古英语**: *strang* (strong "强壮")
> **本义**: 以强有力的方式
> **AI 语境**: 高优先级建议，但非绝对强制

> [!info] 语用功能 | Pragmatic Function
> **作用**: 表达强烈建议，保留合理例外空间
> **替代表达**: firmly (坚定地), emphatically (强调地)
> **为何选择此词**: 在强度和灵活性之间取得平衡

> [!example] 语境示例 | Contextual Examples
> ```markdown
> 核心用法: "strongly consider outputting a thinking block"
>
> 对比:
> - MUST           → 100% 强制，无例外
> - strongly       → 90% 建议，极少例外
> - should         → 70% 建议，允许例外
> - may            → 30% 允许，可选
>
> strongly 使用场景:
> 1. 行为建议: "strongly consider thinking blocks"
> 2. 偏好表达: "strongly prefer specific nouns"
> 3. 优先级: "strongly recommend citing sources"
> ```

> [!abstract] 设计理念 | Design Philosophy
> **为何使用 "strongly" 而非 "MUST"?**
>
> ```markdown
> MUST 的局限:
> - 无灵活性，可能导致僵化行为
> - 不适应边缘情况
> - 限制 AI 判断力
>
> strongly 的优势:
> - 高强度：大多数情况应遵循
> - 有灵活性：特殊情况可例外
> - 保留判断：AI 可根据上下文决策
>
> 示例:
> "strongly consider thinking blocks"
> → 通常应该使用，但简单问题不需要
>
> vs
>
> "MUST use thinking blocks"
> → 每次响应都必须，即使是"2+2=?"也要思考
> ```

> [!question] 闪卡练习 | Flashcard Exercise
> **Q**: 何时使用 strongly vs MUST?
>
> <details>
> <summary>查看答案</summary>
>
> **MUST**: 安全、法律、核心功能
> - NEVER reproduce lyrics
> - MUST use citations
> - MUST NOT help with illegal acts
>
> **strongly**: 最佳实践、行为建议
> - strongly consider thinking blocks
> - strongly prefer specific keywords
> - strongly recommend being helpful
>
> **判断标准**: 违反是否导致严重后果？
> - 是 → MUST
> - 否 → strongly
> </details>

---

### 6. should | 应该

> [!abstract] 词源分析 | Etymology
> **古英语**: *sceolde* (shall 的过去式)
> **本义**: 应当、理应
> **AI 语境**: 强烈建议，允许合理偏离

> [!info] 语用功能 | Pragmatic Function
> **作用**: 表达推荐行为，默认应该遵循
> **替代表达**: ought to (理应), recommended to (建议)
> **为何选择此词**: "should" 是最自然的建议表达

> [!example] 语境示例 | Contextual Examples
> ```markdown
> 核心用法: "should be concise and direct"
>
> 对比:
> - MUST           → 必须遵守
> - strongly       → 强烈建议
> - should         → 建议遵循
> - may            → 可以选择
>
> should 使用场景:
> 1. 风格建议: "should be concise"
> 2. 行为指导: "should offer to search"
> 3. 质量标准: "should be accurate"
> ```

> [!tip] should 的灵活性 | Flexibility of should
> ```markdown
> should ≠ MUST
>
> 示例: "should be concise"
>
> ✅ 通常应该简洁:
> - "Python for loop syntax" → 简洁回答
>
> ✅ 允许不简洁:
> - "Explain quantum physics" → 详细回答
> - 用户明确要求"详细说明"
>
> 设计理念: should 是默认行为，可合理例外
> ```

> [!question] 闪卡练习 | Flashcard Exercise
> **Q**: should vs strongly prefer?
>
> <details>
> <summary>查看答案</summary>
>
> **should** = 一般建议，60-70% 强度<br>
> **strongly prefer** = 强烈偏好，80-90% 强度
>
> **示例**:
> - should: "should be concise" → 通常简洁，复杂主题可详细
> - strongly: "strongly prefer specific keywords" → 强烈建议用具体词
>
> **使用建议**:
> - should: 风格和偏好
> - strongly: 影响质量的行为
> </details>

---

### 7. may | 可以

> [!abstract] 词源分析 | Etymology
> **古英语**: *mægan* (能够、可能)
> **本义**: 有能力、被允许
> **AI 语境**: 可选行为，允许但不强制

> [!info] 语用功能 | Pragmatic Function
> **作用**: 表达允许选项，由 AI 判断是否使用
> **替代表达**: can (能够), allowed to (被允许)
> **为何选择此词**: "may" 更正式，语气更委婉

> [!example] 语境示例 | Contextual Examples
> ```markdown
> 核心用法: "may use multiple tool calls"
>
> 对比:
> - MUST      → 必须使用
> - should    → 建议使用
> - may       → 可以使用
> - optional  → 可选的
>
> may 使用场景:
> 1. 工具选项: "may use web_search"
> 2. 功能启用: "may offer to help"
> 3. 行为选择: "may ask clarifying questions"
> ```

> [!tip] may 的主动性 | Agency of may
> ```markdown
> may = AI 有判断权
>
> 示例: "may use web_search"
>
> AI 判断依据:
> - 用户问题需要实时信息？→ 使用
> - 用户问题需要验证？→ 使用
> - 已有足够信息？→ 不使用
>
> 设计理念: may 赋予 AI 自主权
> ```

> [!question] 闪卡练习 | Flashcard Exercise
> **Q**: may vs can?
>
> <details>
> <summary>查看答案</summary>
>
> **may** = 允许选择（正式）<br>
> **can** = 能够做到（能力）
>
> **示例**:
> - may use web_search → 被允许使用搜索工具
> - can use web_search → 有能力使用搜索工具
>
> **系统提示词倾向**: 使用 may（更正式）
> </details>

---

### 8. optional | 可选的

> [!abstract] 词源分析 | Etymology
> **拉丁语源**: *optionalis* (optare "选择")
> **本义**: 可选择的、非强制的
> **AI 语境**: 完全可选，不执行也无影响

> [!info] 语用功能 | Pragmatic Function
> **作用**: 明确标记某些功能为可选，不执行也无惩罚
> **替代表达**: discretionary (自由裁量的), elective (选举的)
> **为何选择此词**: "optional" 清晰表达非强制性

> [!example] 语境示例 | Contextual Examples
> ```markdown
> 核心用法: "optional: include code examples"
>
> 对比:
> - MUST     → 必须包含
> - should   → 建议包含
> - may      → 可以包含
> - optional → 可选包含
>
> optional 使用场景:
> 1. 额外功能: "optional: provide examples"
> 2. 扩展信息: "optional: include references"
> 3. 可选步骤: "optional: verify with user"
> ```

> [!question] 闪卡练习 | Flashcard Exercise
> **Q**: optional vs may?
>
> <details>
> <summary>查看答案</summary>
>
> **optional** = 功能标记（名词/形容词）<br>
> **may** = 行为许可（动词）
>
> **示例**:
> - optional: include examples（这是可选功能）
> - may: include examples（可以包含示例）
>
> **使用差异**:
> - optional: 描述功能属性
> - may: 描述行为许可
> </details>

---

## 📊 强度层级对比 | Intensity Hierarchy Comparison

### 强制程度金字塔 | Mandatory Level Pyramid

```
         MUST (100%)
        /            \
   ALWAYS (100%)    NEVER (100%)
      /                  \
strongly (90%)        CRITICAL (最高)
    /                        \
should (70%)             MUST NOT (100%)
  /
may (30%)
  \
optional (0%)
```

### 详细强度表 | Detailed Intensity Table

| 强度 | 词汇 | 强制程度 | 灵活性 | 典型用法 |
|:----:|:-----|:--------:|:------:|:---------|
| **最高** | CRITICAL | 100% | 无 | 安全、法律规则 |
| **最高** | MUST | 100% | 无 | 核心要求 |
| **最高** | NEVER | 100% | 无 | 绝对禁止 |
| **最高** | ALWAYS | 100% | 无 | 无条件执行 |
| **高** | strongly | 90% | 极少 | 强烈建议 |
| **中** | should | 70% | 允许 | 一般建议 |
| **低** | may | 30% | 自主 | 可选行为 |
| **最低** | optional | 0% | 完全 | 额外功能 |

### 组合表达式 | Combined Expressions

| 组合 | 总强度 | 含义 |
|:-----|:------:|:-----|
| CRITICAL + MUST | 最高 | 关键且必须 |
| MUST + ALWAYS | 最高 | 必须且始终 |
| strongly + prefer | 高 | 强烈偏好 |
| may + optionally | 低 | 可以且可选 |

---

## 🧪 语境练习 | Contextual Exercises

### 练习 1: 强度排序 | Intensity Ordering

> [!question] 按强制程度排序
> 将以下短语按强制程度从高到低排序：

1. MUST cite
2. should cite
3. CRITICAL: cite
4. may cite
5. strongly prefer to cite

<details>
<summary>查看答案</summary>

**答案**:

| 排序 | 短语 | 强度 |
|:----:|:-----|:----:|
| 1 | CRITICAL: cite | 最高 |
| 2 | MUST cite | 100% |
| 3 | strongly prefer to cite | 90% |
| 4 | should cite | 70% |
| 5 | may cite | 30% |

**关键洞察**: CRITICAL 是最高优先级标记，比 MUST 更强调重要性
</details>

---

### 练习 2: 场景应用 | Scenario Application

> [!question] 选择合适的语气控制词
> 为以下场景选择最合适的语气控制词：

1. 版权保护规则
2. 一般回答风格建议
3. 思维块使用建议
4. 搜索工具使用许可
5. 核心功能要求

<details>
<summary>查看答案</summary>

**答案**:

| 场景 | 选择的词 | 理由 |
|:-----|:---------|:-----|
| 版权保护 | CRITICAL / NEVER | 法律风险，最高强制 |
| 回答风格 | should | 建议遵循，可例外 |
| 思维块 | strongly consider | 强烈建议，保留判断 |
| 搜索工具 | may | 可选使用，AI 判断 |
| 核心功能 | MUST | 必须执行，无例外 |

**关键原则**: 违规后果越严重，强制程度越高
</details>

---

### 练习 3: 设计系统指令 | Design System Instructions

> [!question] 设计完整的语气层级
> 为一个"AI 编程助手"设计包含不同语气的系统指令：

<details>
<summary>查看答案</summary>

**答案**:

```markdown
AI 编程助手系统指令:

## CRITICAL 规则（最高优先级）
CRITICAL: NEVER execute code without user confirmation
CRITICAL: MUST warn about security vulnerabilities

## MUST 规则（核心要求）
MUST ALWAYS explain code changes
MUST provide accurate syntax examples

## NEVER 规则（绝对禁止）
NEVER claim to test code without actually running it
NEVER hide errors from the user

## strongly 建议（强烈推荐）
strongly prefer to include error handling
strongly consider suggesting improvements

## should 建议（一般指导）
should be concise for simple questions
should provide details for complex problems

## may 许可（可选行为）
may offer to run code in sandbox
may ask clarifying questions about requirements

## optional 功能（额外选项）
optional: provide alternative solutions
optional: include performance tips
```

**设计原则**: 从关键到可选，层次分明
</details>

---

### 练习 4: 修改改进 | Improvement

> [!question] 改进以下系统指令
> 将以下指令改进为使用合适的语气控制词：

1. "Cite your sources"
2. "Don't copy song lyrics"
3. "Use thinking blocks"
4. "Be concise"
5. "You can search the web"

<details>
<summary>查看答案</summary>

**答案**:

| 原文 | 改进 | 使用的语气词 |
|:-----|:-----|:------------:|
| "Cite your sources" | "MUST ALWAYS appropriately cite" | MUST, ALWAYS |
| "Don't copy song lyrics" | "CRITICAL: NEVER reproduce song lyrics" | CRITICAL, NEVER |
| "Use thinking blocks" | "strongly consider using thinking blocks" | strongly |
| "Be concise" | "should generally be concise" | should |
| "You can search the web" | "may use web_search when appropriate" | may |

**改进原则**: 明确强制程度，避免模糊表达
</details>

---

## 📚 总结与反思 | Summary & Reflection

> [!abstract] 核心洞察 | Key Insights
> ==语气控制词的三个维度==
>
> **1. 强制程度维度 | Mandatory Level**
> - CRITICAL/MUST/NEVER → 100% 无例外
> - strongly → 90% 极少例外
> - should → 70% 允许例外
> - may/optional → 0-30% 完全可选
>
> **2. 方向维度 | Direction**
> - 正向: MUST, should, may
> - 负向: NEVER, should not, avoid
>
> **3. 一致性维度 | Consistency**
> - ALWAYS: 100% 一致
> - consistently: 高度一致

> [!tip] 学习建议 | Learning Recommendations
> **如何掌握语气控制词？**
>
> 1. **强度层级**: 记住 MUST → strongly → should → may 的层级
> 2. **后果分析**: 违规后果越严重，强制程度越高
> 3. **场景匹配**: 安全/法律用 CRITICAL，风格用 should
> 4. **组合表达**: 理解 "MUST ALWAYS" 的双重强调

> [!warning] 常见错误 | Common Mistakes
> **避免以下错误**:
>
> 1. **过度使用 MUST**: 降低所有规则的重要性
> 2. **强度混淆**: should 和 strongly 的差异
> 3. **忽略方向**: MUST vs MUST NOT
> 4. **滥用 CRITICAL**: 应该仅用于真正关键的规则

---

## 🔗 相关链接 | Related Links

- [[vocabulary-index]] - 词汇总索引
- [[vocabulary-extraction-guide]] - 词汇提取指南
- [[01-Degree-Modifiers]] - 程度修饰语
- [[03-Boundary-Words]] - 边界词
- [[../01-Annotated/search-behavior]] - 搜索行为分析

---

**最后更新 | Last Updated**: 2026-02-06
**下一计划 | Next Review**: 2026-02-13
