---
title: "程度修饰语 | Degree Modifiers"
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
  - degree-modifiers
  - adverbs
  - bilingual
related_docs:
  - "[[vocabulary-index]]"
  - "[[vocabulary-extraction-guide]]"
  - "[[../01-Annotated/search-behavior]]"
  - "[[../01-Annotated/thinking-mode]]"
---

# 程度修饰语 | Degree Modifiers

> [!success] 核心要点 | Core Concept
> ==程度修饰语控制执行力度 | Degree Modifiers Control Execution Intensity==
>
> 程度修饰语（Degree Modifiers）是用于精确控制 AI 行为**执行力度、质量和方式**的副词。它们看似普通，但每个词的选择都经过精心设计，用于在**灵活性与精确性**之间取得平衡。
>
> **核心功能 | Core Functions**:
> - **控制执行强度** | Control execution intensity
> - **定义质量标准** | Define quality standards
> - **调节响应风格** | Adjust response style
> - **平衡指令硬度** | Balance directive rigidity

---

## 📊 词汇表 | Vocabulary Table

| 词汇 | 中文 | 强度 | 频率 | 首次来源 | 替代表达 |
|:-----|:-----|:----:|:----:|:---------|:---------|
| appropriately | 适当地 | 中-高 | 高 | claude-4.5 | correctly, properly |
| strategically | 策略性地 | 高 | 中 | claude-4.5 | wisely, intelligently |
| carefully | 仔细地 | 高 | 高 | claude-4.1 | cautiously, thoroughly |
| thoroughly | 彻底地 | 高 | 中 | claude-4.5 | completely, fully |
| naturally | 自然地 | 中 | 高 | claude-4.5 | normally, typically |
| politely | 礼貌地 | 低-中 | 中 | claude-4.5 | courteously, respectfully |
| strongly | 强烈地 | 高 | 高 | claude-4.1 | firmly, emphatically |
| highly | 高度地 | 高 | 低 | claude-3.7 | very, extremely |
| comprehensively | 全面地 | 高 | 中 | claude-4.5 | thoroughly, completely |
| explicitly | 明确地 | 中-高 | 中 | claude-4.5 | clearly, specifically |
| specifically | 具体地 | 中 | 高 | claude-4.5 | particularly, especially |
| substantively | 实质性地 | 中 | 低 | claude-4.5 | meaningfully, significantly |
| significantly | 显著地 | 中 | 中 | claude-3.7 | considerably, notably |
| efficiently | 高效地 | 中 | 低 | claude-code | quickly, effectively |
| proactively | 主动地 | 中 | 低 | claude-4.5 | actively, voluntarily |

---

## 🎯 词源与语用分析 | Etymology & Pragmatic Analysis

### 1. appropriately | 适当地

> [!abstract] 词源分析 | Etymology
> **拉丁语源**: *appropriatus* (ad- "to" + proprius "one's own")
> **本义**: 使某物适合于特定用途或目的
> **AI 语境**: 不仅要求"正确"，还要求"适配语境和风格"

> [!info] 语用功能 | Pragmatic Function
> **作用**: 引用和行为需适配具体场景、用户意图和响应风格
> **替代表达**: correctly (仅强调正确), properly (仅强调规范)
> **为何选择此词**: "appropriately" 涵盖了正确性 + 适配性 + 风格一致性的三层含义

> [!example] 语境对比 | Contextual Comparison
> ```markdown
> ❌ "cite correctly" → 仅关注格式是否正确
> ✅ "appropriately cite" → 格式正确 + 语境适配 + 风格一致
>
> 示例场景:
> - 学术论文: 正式引用格式
> - 闲聊对话: 更自然的提及方式
> - 代码注释: 简洁的来源说明
> ```

> [!tip] 跨文档对比 | Cross-Document Comparison
> | 文档 | 用法 | 差异 |
> |:-----|:-----|:-----|
> | Claude 4.5 | "appropriately cite" | 强调适配性 |
> | Claude 3.7 | "correctly cite" | 强调准确性 |
> | OpenAI | "cite sources" | 中性，无修饰 |

> [!question] 闪卡练习 | Flashcard Exercise
> **Q**: "appropriately cite" vs "cite correctly"?
>
> <details>
> <summary>查看答案</summary>
>
> **appropriately** = 正确性 + 语境适配 + 风格一致<br>
> **correctly** = 仅格式正确性
>
> **关键洞察**: 系统提示词偏好更宽泛的指导原则，允许 AI 根据场景灵活调整
> </details>

---

### 2. strategically | 策略性地

> [!abstract] 词源分析 | Etymology
> **希腊语源**: *strategia* (stratos "army" + agein "to lead")
> **本义**: 将军指挥军队的艺术
> **AI 语境**: 需要深思熟虑、权衡利弊后的决策

> [!info] 语用功能 | Pragmatic Function
> **作用**: 参数选择、工具调用次数、响应长度需要策略性决策
> **替代表达**: wisely (智慧地), intelligently (智能地)
> **为何选择此词**: "strategically" 暗示有明确的目标和权衡过程

> [!example] 语境对比 | Contextual Comparison
> ```markdown
> 用法: "decide strategically how to set n (number of chats to retrieve)"
>
> 策略考量:
> - 信息丰富度 vs 处理效率
> - 用户需求 vs 资源限制
> - 当前结果 vs 潜在收益
>
> ❌ "set n to 20" → 固定规则，无灵活性
> ✅ "decide strategically" → 根据情况动态调整
> ```

> [!tip] 跨文档对比 | Cross-Document Comparison
> | 文档 | 用法 | 场景 |
> |:-----|:-----|:-----|
> | Claude 4.5 | "decide strategically" | 参数选择 |
> | Claude 3.7 | "choose wisely" | 工具使用 |
> | OpenAI | "make good choices" | 行为指导 |

> [!question] 闪卡练习 | Flashcard Exercise
> **Q**: 何时使用 "strategically" vs "carefully"?
>
> <details>
> <summary>查看答案</summary>
>
> **strategically** = 策略决策，涉及权衡和目标考量<br>
> **carefully** = 仔细执行，关注准确性和细节
>
> **示例**:
> - "decide strategically how many searches to run" → 权衡成本和收益
> - "carefully analyze the search results" → 仔细检查每个结果
> </details>

---

### 3. carefully | 仔细地

> [!abstract] 词源分析 | Etymology
> **古英语**: *careful* (care "关注、忧虑" + -ful "充满")
> **本义**: 充满关注的、小心的
> **AI 语境**: 需要特别注意、细致处理的行为

> [!info] 语用功能 | Pragmatic Function
> **作用**: 函数调用后分析、复杂推理、错误诊断时需要仔细思考
> **替代表达**: cautiously (谨慎地), thoroughly (彻底地)
> **为何选择此词**: "carefully" 强调注意力和细节关注，而非谨慎回避

> [!example] 语境对比 | Contextual Comparison
> ```markdown
> 核心用法: "carefully consider whether a thinking block is appropriate"
>
> 思考维度:
> - 是否真正需要推理？
> - 用户是否需要看到思考过程？
> - 思考块是否会增加价值？
>
> ⚠️ 注意: "carefully" 不是 "slowly"
> - 仔细 ≠ 慢速
> - 关注质量，而非速度
> ```

> [!tip] 跨文档对比 | Cross-Document Comparison
> | 文档 | 用法 | 频率 |
> |:-----|:-----|:----:|
> | Claude 4.1 | "carefully consider" | 高 |
> | Claude 4.5 | "carefully analyze" | 中 |
> | OpenAI | "be careful" | 低 |

> [!question] 闪卡练习 | Flashcard Exercise
> **Q**: "carefully" 与 "cautiously" 的区别？
>
> <details>
> <summary>查看答案</summary>
>
> **carefully** = 仔细关注细节，追求准确<br>
> **cautiously** = 谨慎避免风险，偏向保守
>
> **系统提示词选择**: "carefully" 而非 "cautiously"
> → 因为 AI 需要积极解决问题，而非过度保守
> </details>

---

### 4. thoroughly | 彻底地

> [!abstract] 词源分析 | Etymology
> **古英语**: *thorough* (thuruh "through" + -ly)
> **本义**: 完全穿过、彻底完成
> **AI 语境**: 完整、全面、无遗漏

> [!info] 语用功能 | Pragmatic Function
> **作用**: 确保覆盖所有方面，不遗漏重要信息
> **替代表达**: completely (完全地), fully (充分地)
> **为何选择此词**: "thoroughly" 强调过程的完整性

> [!example] 语境对比 | Contextual Comparison
> ```markdown
> 用法: "aim to give a thorough and informative answer"
>
> 对比:
> - thorough: 过程完整，覆盖全面
> - complete: 结果完整，没有缺失
> - comprehensive: 范围广泛，包含多个方面
>
> 示例:
> ❌ "answer completely" → 回答完整（可能简洁）
> ✅ "thoroughly informative" → 全面且信息丰富
> ```

> [!question] 闪卡练习 | Flashcard Exercise
> **Q**: "thoroughly" vs "comprehensively"?
>
> <details>
> <summary>查看答案</summary>
>
> **thoroughly** = 强调过程的完整性（不遗漏）<br>
> **comprehensively** = 强调范围的广泛性（覆盖多方面）
>
> **组合使用**: "thoroughly and comprehensively" = 既完整又全面
> </details>

---

### 5. naturally | 自然地

> [!abstract] 词源分析 | Etymology
> **拉丁语源**: *naturalis* (natura "出生、本性")
> **本义**: 符合本性的、非人为的
> **AI 语境**: 行为符合预期，没有刻意或勉强

> [!info] 语用功能 | Pragmatic Function
> **作用**: 响应和交互应该流畅、符合预期，不突兀或机械
> **替代表达**: normally (正常地), typically (通常地)
> **为何选择此词**: "naturally" 暗示符合人类交互的直觉

> [!example] 语境对比 | Contextual Comparison
> ```markdown
> 核心用法 1: "synthesize information naturally"
> → 综合后的信息应该像自然对话一样流畅
>
> 核心用法 2: "Users naturally reference past conversations"
> → 用户引用过去对话是自然行为，不需要显式指令
>
> 对比:
> ❌ "combine information" → 机械组合
> ✅ "synthesize naturally" → 有机融合
> ```

> [!tip] 双重身份 | Dual Identity
> "naturally" 在不同语境下有不同分类:
>
> | 语境 | 分类 | 功能 |
> |:-----|:-----|:-----|
> | "synthesize naturally" | 程度修饰 | 描述综合方式 |
> | "naturally reference" | 微妙表达 | 自然化用户行为 |

> [!question] 闪卡练习 | Flashcard Exercise
> **Q**: 为何系统提示词说 "Users naturally reference..."？
>
> <details>
> <summary>查看答案</summary>
>
> **答案**: 因为这是**自然化描述**（Naturalization）
>
> **功能**:
> 1. 将常见行为描述为"自然的"
> 2. 暗示 AI 应该预期并支持这种行为
> 3. 避免让用户觉得需要"特殊指令"
>
> **反例**: "Users often mention past topics" → 偶然行为
> **正例**: "naturally reference" → 预期行为
> </details>

---

### 6. politely | 礼貌地

> [!abstract] 词源分析 | Etymology
> **拉丁语源**: *politus* (polire "磨光、修饰")
> **本义**: 经过修饰的、有教养的
> **AI 语境**: 语气友好，但内容可能不受欢迎

> [!info] 语用功能 | Pragmatic Function
> **作用**: 即使传达负面消息，也保持友好语气
> **替代表达**: courteously (客气地), respectfully (恭敬地)
> **为何选择此词**: "politely" 最符合日常交互习惯

> [!example] 语境对比 | Contextual Comparison
> ```markdown
> 核心用法: "politely inform the user that the answer cannot be found"
>
> 关键洞察:
> - "politely" 修饰语气，而非内容
> - 仍然要明确告知无法找到答案
> - 避免模糊或误导性的安慰
>
> ❌ "I'm sorry, maybe try again later" → 过于委婉，不诚实
> ✅ "politely inform: the answer cannot be found" → 礼貌但明确
> ```

> [!question] 闪卡练习 | Flashcard Exercise
> **Q**: "politely" 是否意味着"弱化"坏消息？
>
> <details>
> <summary>查看答案</summary>
>
> **答案**: **不**（No）
>
> **politely inform** ≠ **weaken the message**
>
> **正确理解**:
> - 语气: 友好、尊重
> - 内容: 仍然准确、明确
>
> **示例**:
> ❌ "I can't seem to find that" → 弱化，模糊
> ✅ "The search results do not contain this information" → 礼貌但明确
> </details>

---

### 7. strongly | 强烈地

> [!abstract] 词源分析 | Etymology
> **古英语**: *strang* (strong "强壮" + -ly "副词后缀")
> **本义**: 以强有力的方式
> **AI 语境**: 高优先级，但不是绝对强制

> [!info] 语用功能 | Pragmatic Function
> **作用**: 表达强烈建议，但保留例外空间
> **替代表达**: firmly (坚定地), emphatically (强调地)
> **为何选择此词**: "strongly" 在强度和灵活性之间取得平衡

> [!example] 语境对比 | Contextual Comparison
> ```markdown
> 核心用法: "strongly consider outputting a thinking block"
>
> 强度层级:
> MUST              → 100% 强制，无例外
> strongly prefer   → 90% 建议，有例外
> should            → 70% 建议，允许偏离
> may               → 30% 允许，不推荐
>
> 关键: "strongly" 不是 "must"
> - 如果确定不需要 → 可以不使用 thinking 块
> - 如果不确定     → 强烈倾向于使用
> ```

> [!tip] 跨文档对比 | Cross-Document Comparison
> | 文档 | 用法 | 强度 |
> |:-----|:-----|:----:|
> | Claude 4.1 | "strongly consider" | 高 |
> | Claude 4.5 | "strongly prefer" | 高 |
> | OpenAI | "should" | 中 |
> | Google | "recommended" | 中-低 |

> [!question] 闪卡练习 | Flashcard Exercise
> **Q**: "strongly consider" vs "MUST"?
>
> <details>
> <summary>查看答案</summary>
>
> **MUST** = 绝对强制，违反会出错<br>
> **strongly consider** = 强烈建议，可合理例外
>
> **示例**:
> - MUST: "MUST cite sources" → 不引用 = 违规
> - strongly: "strongly consider thinking" → 不思考可能也可以
>
> **设计理念**: "strongly" 给 AI 留下判断空间
> </details>

---

### 8. comprehensively | 全面地

> [!abstract] 词源分析 | Etymology
> **拉丁语源**: *comprehensivus* (com- "一起" + prehendere "抓住")
> **本义**: 全部抓住、包含所有内容
> **AI 语境**: 覆盖所有相关方面，无遗漏

> [!info] 语用功能 | Pragmatic Function
> **作用**: 对于复杂查询，需要从多个角度全面分析
> **替代表达**: thoroughly (彻底地), completely (完全地)
> **为何选择此词**: "comprehensively" 强调**范围**而非**深度**

> [!example] 语境对比 | Contextual Comparison
> ```markdown
> 用法: "aim to give a thorough and informative answer, even if doing so requires expanding beyond the specific inquiry"
>
> 对比维度:
> - thoroughly: 深度足够，每个方面都深入
> - comprehensively: 范围足够，覆盖所有相关方面
> - completely: 没有缺失，达到100%
>
> 示例场景:
> 问: "如何提高 Python 代码性能？"
>
> ❌ 简单回答: "使用更好的算法"
> ✅ comprehensively: 算法选择 + 数据结构 + 编码技巧 + 工具优化 + ...
> ```

> [!question] 闪卡练习 | Flashcard Exercise
> **Q**: "comprehensively" vs "thoroughly"?
>
> <details>
> <summary>查看答案</summary>
>
> **comprehensively** = 广度优先（覆盖多个方面）<br>
> **thoroughly** = 深度优先（每个方面深入）
>
> **理想状态**: 既 comprehensive 又 thorough
> → "comprehensive and thorough analysis"
> </details>

---

### 9. explicitly | 明确地

> [!abstract] 词源分析 | Etymology
> **拉丁语源**: *explicitus* (ex- "向外" + plicare "折叠")
> **本义**: 完全展开、清晰说明
> **AI 语境**: 清楚表达，没有歧义

> [!info] 语用功能 | Pragmatic Function
> **作用**: 某些行为需要用户明确要求才会执行
> **替代表达**: clearly (清楚地), specifically (具体地)
> **为何选择此词**: "explicitly" 强调**有意表达**而非**清晰度**

> [!example] 语境对比 | Contextual Comparison
> ```markdown
> 核心用法: "unless the user explicitly asks"
>
> 关键区别:
> - explicit: 用户有意识地、清楚地提出要求
> - implicit: 用户暗示或默认期望
>
> 示例:
> ❌ "user might want details" → 隐式期望
> ✅ "explicitly asks for details" → 明确要求
>
> 设计理念: 默认简洁，用户明确要求时才扩展
> ```

> [!tip] 跨文档对比 | Cross-Document Comparison
> | 文档 | 用法 | 条件 |
> |:-----|:-----|:-----|
> | Claude 4.5 | "unless explicitly asked" | 行为触发 |
> | Claude 3.7 | "if requested" | 更弱条件 |
> | OpenAI | "when needed" | AI 判断 |

> [!question] 闪卡练习 | Flashcard Exercise
> **Q**: 为何用 "explicitly asks" 而非 "asks"?
>
> <details>
> <summary>查看答案</summary>
>
> **答案**: 区分明确要求和隐式期望
>
> **explicitly asks**:
> - "Please give me more details"
> - "Show me the full code"
> - "I need all the information"
>
> **隐式期望**（不触发）:
> - "Tell me about X"（可能期望详情但不明确）
> - "What do you think?"（开放问题）
>
> **设计原则**: 避免过度响应，只在用户明确要求时扩展
> </details>

---

### 10. specifically | 具体地

> [!abstract] 词源分析 | Etymology
> **拉丁语源**: *specificus* (species "种类、外观")
> **本义**: 针对特定种类或个体
> **AI 语境**: 精确、具体、非笼统

> [!info] 语用功能 | Pragmatic Function
> **作用**: 指代特定事物，而非一般类别
> **替代表达**: particularly (特别地), especially (尤其)
> **为何选择此词**: "specifically" 强调**精确性**而非**重要性**

> [!example] 语境对比 | Contextual Comparison
> ```markdown
> 用法: "prioritize specific nouns over generic verbs"
>
> 对比:
> - specific: "Python", "OAuth", "San Francisco" → 精确
> - generic: "language", "protocol", "city" → 笼统
>
> 搜索示例:
> ❌ "programming language" → 太泛，结果多
> ✅ "Python" → 具体，结果精确
>
> 设计理念: 具体词汇 → 更相关 → 更准确
> ```

> [!question] 闪卡练习 | Flashcard Exercise
> **Q**: "specifically" vs "especially"?
>
> <details>
> <summary>查看答案</summary>
>
> **specifically** = 具体指定（精确性）<br>
> **especially** = 特别强调（重要性）
>
> **示例**:
> - "specifically Python" → 精确到 Python，不是其他语言
> - "especially Python" → 包括多种语言，但 Python 最重要
>
> **系统提示词用途**: "specifically" 用于搜索和过滤
> </details>

---

### 11. substantively | 实质性地

> [!abstract] 词源分析 | Etymology
> **拉丁语源**: *substantivus* (substantia "本质、实体")
> **本义**: 与本质相关的、重要的
> **AI 语境**: 有实际内容意义的，非形式化的

> [!info] 语用功能 | Pragmatic Function
> **作用**: 区分有实际意义的词汇和形式化词汇
> **替代表达**: meaningfully (有意义地), significantly (显著地)
> **为何选择此词**: "substantive" 强调**内容实体**而非**形式**

> [!example] 语境对比 | Contextual Comparison
> ```markdown
> 核心用法: "substantive/high-confidence keywords"
>
> 对比:
> ✅ Substantive: "robot", "pasta", "OAuth", "machine learning"
> ❌ Non-substantive: "discuss", "talk", "conversation", "yesterday"
>
> 判断标准:
> - Substantive: 有独立意义，能识别具体内容
> - Non-substantive: 仅描述交互形式或时间
>
> 设计理念: 实质性词汇 → 更好的搜索相关性
> ```

> [!question] 闪卡练习 | Flashcard Exercise
> **Q**: 为何 "robot" 是 substantive 而 "discuss" 不是？
>
> <details>
> <summary>查看答案</summary>
>
> **答案**: "substantive" 关注内容实体
>
> **robot** (substantive):
> - 指向具体主题（机器人技术）
> - 在对话中可识别
> - 搜索结果高度相关
>
> **discuss** (non-substantive):
> - 描述交互形式（讨论）
> - 不指向具体主题
> - 搜索结果低相关
>
> **记忆口诀**: Substantive = 有实质内容
> </details>

---

### 12. efficiently | 高效地

> [!abstract] 词源分析 | Etymology
> **拉丁语源**: *efficientem* (ex- "out" + facere "make")
> **本义**: 有效地产生结果
> **AI 语境**: 以最小成本获得最佳结果

> [!info] 语用功能 | Pragmatic Function
> **作用**: 平衡质量和资源使用（时间、token、API 调用）
> **替代表达**: quickly (快速地), effectively (有效地)
> **为何选择此词**: "efficiently" 强调**投入产出比**

> [!example] 语境对比 | Contextual Comparison
> ```markdown
> 用法: "efficiently gather the most recent chats"
>
> 对比:
> - quickly: 速度优先，可能质量不足
> - effectively: 结果优先，可能成本高
> - efficiently: 平衡速度和质量
>
> 示例:
> ❌ 快速但不高效: 调用 20 次获取 100 条聊天（太多）
> ❌ 有效但不高效: 调用 1 次获取 10 条聊天（太少）
> ✅ 高效: 调用 2-3 次获取 30-40 条聊天（平衡）
> ```

> [!question] 闪卡练习 | Flashcard Exercise
> **Q**: "efficiently" 在系统提示词中主要用于什么场景？
>
> <details>
> <summary>查看答案</summary>
>
> **答案**: 资源管理和工具调用优化
>
> **主要场景**:
> 1. **API 调用**: 限制调用次数，同时获取足够信息
> 2. **Token 使用**: 简洁响应，避免冗余
> 3. **响应时间**: 快速响应，不牺牲质量
> 4. **搜索策略**: 使用最少查询获取最佳结果
>
> **核心理念**: Efficiency = 质量 / 成本
> </details>

---

### 13. proactively | 主动地

> [!abstract] 词源分析 | Etymology
> **希腊语源**: *proactive* (pro- "提前" + active "行动")
> **本义**: 提前采取行动
> **AI 语境**: 不等用户请求，主动提供帮助

> [!info] 语用功能 | Pragmatic Function
> **作用**: AI 应该主动识别并满足用户潜在需求
> **替代表达**: actively (积极地), voluntarily (自愿地)
> **为何选择此词**: "proactively" 强调**提前性**和**主动性**

> [!example] 语境对比 | Contextual Comparison
> ```markdown
> 用法: "proactively suggest relevant information"
>
> 对比:
> - reactive: 用户问 → AI 答（被动响应）
> - proactive: AI 预判需求 → 主动提供（主动）
>
> 示例:
> ❌ Reactive: 用户问"需要引用吗？" → AI 答"需要"
> ✅ Proactive: AI 主动说"需要我搜索最新信息吗？"
>
> 设计理念: Proactive = 更好的用户体验
> ```

> [!question] 闪卡练习 | Flashcard Exercise
> **Q**: "proactively" 与 "presumptuously"（冒昧地）的区别？
>
> <details>
> <summary>查看答案</summary>
>
> **答案**: 主动 vs 冒昧
>
> **Proactively** (正面):
> - 预期用户需求
> - 提供有价值的信息
> - 尊重用户选择
>
> **Presumptuously** (负面):
> - 假设用户需求
> - 强加信息
> - 不尊重用户
>
> **边界**: Proactively 提供选项，而非代替用户决策
> - ✅ "需要我搜索吗？"（主动）
> - ❌ "我帮你搜索了"（冒昧）
> </details>

---

## 📊 综合对比矩阵 | Comprehensive Comparison Matrix

### 强度层级对比 | Intensity Hierarchy

| 词汇 | 强度 | 主要功能 | 典型语境 |
|:-----|:----:|:---------|:---------|
| appropriately | 中-高 | 适配性 | 引用、响应风格 |
| strategically | 高 | 策略性 | 参数选择、决策 |
| carefully | 高 | 准确性 | 分析、推理 |
| thoroughly | 高 | 完整性 | 信息覆盖 |
| strongly | 高 | 优先级 | 建议、偏好 |
| comprehensively | 高 | 广度 | 多方面分析 |
| explicitly | 中-高 | 明确性 | 条件触发 |
| specifically | 中 | 精确性 | 搜索、过滤 |
| substantively | 中 | 实质性 | 内容判断 |
| efficiently | 中 | 效率 | 资源管理 |
| proactively | 中 | 主动性 | 用户体验 |
| naturally | 低-中 | 自然性 | 交互风格 |
| politely | 低-中 | 友善度 | 语气控制 |

### 语义场分析 | Semantic Field Analysis

```
完整性语义场:
┌─────────────────────────────────────┐
│ thoroughly        → 深度完整          │
│ comprehensively  → 广度完整          │
│ completely       → 结果完整          │
└─────────────────────────────────────┘

准确性语义场:
┌─────────────────────────────────────┐
│ carefully        → 仔细准确          │
│ appropriately    → 适配准确          │
│ specifically     → 精确具体          │
│ explicitly       → 明确无误          │
└─────────────────────────────────────┘

强度语义场:
┌─────────────────────────────────────┐
│ strategically     → 策略强度         │
│ strongly         → 建议强度          │
│ highly           → 程度强度          │
│ significantly     → 显著强度          │
└─────────────────────────────────────┘
```

---

## 🧪 语境练习 | Contextual Exercises

### 练习 1: 词汇选择 | Vocabulary Selection

> [!question] 选择最合适的程度修饰语
> 为以下场景选择最合适的修饰语：

1. 在函数调用后分析结果: ___ consider the results
2. 决定获取多少条聊天记录: ___ decide how many to retrieve
3. 引用搜索结果: ___ cite your sources
4. 综合多个来源的信息: ___ synthesize the information
5. 告知用户无法找到答案: ___ inform the user

<details>
<summary>查看答案</summary>

**答案**:
1. **carefully** → 需要仔细分析每个结果
2. **strategically** → 需要权衡信息量和效率
3. **appropriately** → 需要适配语境和风格
4. **naturally** → 需要流畅整合，非机械拼接
5. **politely** → 需要保持友好语气

**关键原则**: 匹配功能与修饰语的语义重点
</details>

---

### 练习 2: 程度排序 | Degree Ordering

> [!question] 按强制程度排序
> 将以下词汇短语按强制程度从高到低排序：

1. MUST cite
2. appropriately cite
3. strongly prefer to cite
4. should cite
5. may cite

<details>
<summary>查看答案</summary>

**答案**:

| 排序 | 短语 | 强度 | 说明 |
|:----:|:-----|:----:|:-----|
| 1 | MUST cite | 100% | 绝对强制 |
| 2 | strongly prefer to cite | 90% | 强烈建议 |
| 3 | should cite | 70% | 一般建议 |
| 4 | appropriately cite | 60% | 质量要求 |
| 5 | may cite | 30% | 允许选项 |

**关键洞察**: "appropriately" 不是强制程度，而是质量标准
</details>

---

### 练习 3: 修改改进 | Improvement

> [!question] 改进以下表达
> 将以下表达改进为系统提示词风格（使用合适的程度修饰语）：

1. "搜索后分析结果"
2. "决定参数值"
3. "给用户一个完整的回答"
4. "告诉用户找不到信息"
5. "综合所有信息"

<details>
<summary>查看答案</summary>

**答案**:

| 原文 | 改进 | 使用的修饰语 |
|:-----|:-----|:------------:|
| "搜索后分析结果" | "carefully analyze the search results" | carefully |
| "决定参数值" | "strategically decide on parameter values" | strategically |
| "给用户一个完整的回答" | "give a thorough and informative response" | thoroughly |
| "告诉用户找不到信息" | "politely inform the user" | politely |
| "综合所有信息" | "synthesize information naturally" | naturally |

**改进原则**: 添加精确的程度修饰语，明确执行标准
</details>

---

### 练习 4: 场景应用 | Scenario Application

> [!question] 设计系统指令
> 为以下场景设计包含程度修饰语的系统指令：

**场景**: AI 助手帮助用户调试代码

<details>
<summary>查看答案</summary>

**答案**:

```markdown
代码调试系统指令:

1. **分析阶段**:
   "carefully analyze the error message and code context"

2. **诊断阶段**:
   "thoroughly examine potential causes"

3. **解释阶段**:
   "provide a clear and comprehensive explanation"

4. **解决方案**:
   "strategically suggest fixes based on the issue severity"

5. **跟进阶段**:
   "proactively offer additional debugging tips"

**使用的修饰语**:
- carefully: 仔细分析错误
- thoroughly: 全面检查原因
- comprehensively: 完整解释
- strategically: 策略性建议
- proactively: 主动提供帮助
```

</details>

---

## 📚 总结与反思 | Summary & Reflection

> [!abstract] 核心洞察 | Key Insights
> ==程度修饰语的三个核心维度==
>
> **1. 质量控制维度 | Quality Control**
> - carefully (仔细) → 准确性
> - thoroughly (彻底) → 完整性
> - comprehensively (全面) → 广度
>
> **2. 执行方式维度 | Execution Method**
> - strategically (策略) → 权衡决策
> - efficiently (高效) → 资源优化
> - naturally (自然) → 交互流畅
>
> **3. 交互风格维度 | Interaction Style**
> - appropriately (适配) → 语境敏感
> - politely (礼貌) → 友善语气
> - proactively (主动) → 用户体验

> [!tip] 学习建议 | Learning Recommendations
> **如何掌握这些程度修饰语？**
>
> 1. **分组记忆**: 按语义场分组（完整性、准确性、强度）
> 2. **对比练习**: 对比相似词汇的微妙差异
> 3. **场景应用**: 在具体场景中选择合适的修饰语
> 4. **跨文档验证**: 观察不同公司如何使用相似词汇

> [!warning] 常见错误 | Common Mistakes
> **避免以下错误**:
>
> 1. **过度使用**: 不是每个动词都需要修饰语
> 2. **错误选择**: 匹配修饰语与实际功能
> 3. **忽略语境**: 同一词在不同语境有不同含义
> 4. **强度混淆**: 区分强制程度和质量标准

---

## 🔗 相关链接 | Related Links

- [[vocabulary-index]] - 词汇总索引
- [[vocabulary-extraction-guide]] - 词汇提取指南
- [[02-Tone-Controllers]] - 语气控制词
- [[03-Boundary-Words]] - 边界词
- [[../01-Annotated/search-behavior]] - 搜索行为分析
- [[../01-Annotated/thinking-mode]] - 思维模式详解

---

**最后更新 | Last Updated**: 2026-02-06
**下一计划 | Next Review**: 2026-02-13
