# Cheng-Wei Paperwriting Style

[English](README.md) | 中文说明

`cheng-wei-paperwriting-style` 是一个用于 Codex 的英文科研论文润色 skill。它的目标不是改科研故事，也不是替你编机制或结果，而是在不改变原意、数据、引用、模型、证据边界和不确定性的前提下，把英文论文语言改得更像成熟科研论文：更克制、更具体、更有证据感，也更少 AI 味。

这个 skill 的风格规则来自 2025 年以前、与北京大学程强和中科院动物所魏妥相关的合法可分析论文材料。它只提取高层级写作习惯，例如句式、动词选择、连接词、段落节奏和 claim 的强弱控制，不复制原文句子，也不上传或内置 PDF 全文。

## 适用场景

适合用于润色：

- 英文论文段落
- Abstract、Introduction、Results、Discussion
- Cover letter
- Response to reviewers
- 生物医学、转化医学、肿瘤、免疫、纳米递送、mRNA/LNP 相关写作
- 已有科学内容正确，但语言显得泛泛、模板化、过度宣传或 AI 味明显的文本

最适合的使用方式是：你已经确定科学信息和引用大体正确，只需要把英文表达打磨成更自然、更像论文的版本。

## 不适合做什么

这个 skill 不应该用于：

- 编造机制、结果、实验设计、统计数据、引用或临床意义
- 把原文中的弱 claim 改成强 claim
- 替代专业审稿、统计审查或期刊语言编辑
- 模仿或复制来源论文中的独特句子
- 使用未授权的付费全文
- 把 mRNA-LNP 领域词汇强行塞进无关主题

## 核心工作原则

### 1. 先保护科学含义

润色前必须保留：

- 数字、单位、样本量、时间点、剂量、百分比和统计描述
- 引用位置，以及引用和 claim 的对应关系
- 基因、蛋白、疾病、组织、器官、细胞类型、动物模型和实验方法名称
- 证据层级，例如 in vitro、ex vivo、in vivo、preclinical、clinical、computational 或 review-based
- 不确定性强度，例如 `may`、`could`、`suggest`、`demonstrate`、`significantly` 等

也就是说，语言可以变，但科学含义、证据范围和 claim 强度不能偷偷改变。

### 2. 使用 Cheng-Wei 式科研英文语感

这个 skill 总结出的英文写作特征包括：

- 喜欢具体主语，例如 `The results`、`This strategy`、`These findings`、`We`、`LNPs`、`The formulation`
- 喜欢准确研究动词，例如 `developed`、`designed`、`engineered`、`evaluated`、`enabled`、`enhanced`、`revealed`、`confirmed`、`suggested`
- 多数句子控制在 18-30 个词左右
- 主动语态和被动语态平衡使用：作者行为多用主动，方法、检测和观察多用被动
- 连接词克制使用，例如 `However`、`Here`、`Notably`、`Together`、`Overall`
- 段落结尾倾向于有限度的推论，而不是泛泛地说“具有巨大潜力”

### 3. 去除 AI 式英文痕迹

它会重点处理这些问题：

- 删除 `In recent years`、`With the rapid development of` 这类空泛开头
- 把抽象赞美改成具体科学含义
- 避免 `shows great promise`、`plays a vital role` 这类没有信息量的套话
- 减少堆叠形容词和没有数据支撑的强化词
- 拆开承载太多 claim 的长句
- 让段落逻辑更像“问题-设计-证据-有限推论”，而不是宣传稿

## 三种使用模式

### `polish`

适合想要明显提升语言质量和论文感的时候。它会在不改变科学含义的基础上，让句子更紧凑、更自然、更有科研写作节奏。

示例：

```text
Use cheng-wei-paperwriting-style in polish mode to revise this paragraph:

[粘贴英文段落]
```

### `conservative`

适合已经接近定稿、最怕改错含义的时候。这个模式只做较小幅度改动，优先保证原意、引用和 claim 强度。

示例：

```text
Use cheng-wei-paperwriting-style in conservative mode. Keep all claims and citations unchanged:

[粘贴英文段落]
```

### `diagnose`

适合先诊断一段英文为什么像 AI 写的，再决定是否重写。

示例：

```text
Use cheng-wei-paperwriting-style in diagnose mode. Explain what makes this paragraph sound AI-generated and suggest fixes:

[粘贴英文段落]
```

## 推荐输出格式

在 `polish` 或 `conservative` 模式下，建议输出：

1. Revised text
2. 简短说明：只有当原文涉及 claim、引用、数字或不确定性时，才说明哪些地方需要特别注意

在 `diagnose` 模式下，建议输出：

1. 主要 AI 味问题
2. 修改建议
3. 如果用户需要，再给一个修改版本

## 安装方式

本地 Codex 使用时，把整个目录放到：

```text
~/.codex/skills/cheng-wei-paperwriting-style/
```

入口文件必须是：

```text
~/.codex/skills/cheng-wei-paperwriting-style/SKILL.md
```

安装后，新开一个 Codex 对话或刷新 skills 列表，然后可以直接这样调用：

```text
Use cheng-wei-paperwriting-style to polish this manuscript paragraph...
```

## 仓库结构

```text
cheng-wei-paperwriting-style/
├── SKILL.md
├── agents/
│   └── openai.yaml
└── references/
    ├── corpus_inventory.md
    ├── rewrite_checklist.md
    └── style_profile.md
```

各文件作用：

- `SKILL.md`：Codex skill 的主说明和硬性规则
- `agents/openai.yaml`：可选的界面元数据
- `references/corpus_inventory.md`：论文清单、纳入规则和全文可用性状态
- `references/style_profile.md`：从语料中总结出的高层级英文写作风格
- `references/rewrite_checklist.md`：保留原意和去 AI 味的检查清单

## 语料基础

当前版本主要参考了用户提供且可合法分析的 2025 年以前材料，包括：

- Luo et al., 2024, `ACS Nano`
- Fei et al., 2024, `Advanced Materials`
- Lin et al., 2023, `Biophysics Reports`
- Wei et al., 2022, `Life Medicine`
- Dilliard et al., 2021, `PNAS`
- Cheng et al., 2020, `Nature Nanotechnology` author manuscript
- 一篇 2024 年 `Chinese Science Bulletin` 中文综述，主要用于结构理解，不用于决定英文句法

完整论文清单、纳入理由和访问状态见 `references/corpus_inventory.md`。

## 写作规则摘要

使用这个 skill 润色时，应按这个顺序处理：

1. 先识别原文主 claim，并保持不变
2. 把句子主语改得更具体
3. 用更准确的研究动词或结果动词替代模糊动词
4. 保持 hedging 强度不变
5. 把过长句拆成 18-30 词左右的科研句
6. 只在有助于逻辑时添加连接词
7. 段落结尾用有限推论，不写过度宣传式结论

## 使用示例

```text
Use cheng-wei-paperwriting-style in polish mode. Preserve all claims, citations, cell types, animal models, and uncertainty levels. Do not add new mechanisms or references.

[粘贴英文论文段落]
```

## 安全和版权说明

这个仓库只包含 skill 指令、风格总结和论文清单，不包含 PDF 原文，也不包含从论文中抽取出的受版权保护全文。后续如果扩充语料，应只使用开放获取版本、PMC 版本、出版社允许的作者稿，或用户本人提供的合法副本。

这个 skill 是语言层面的论文润色工具。除非用户明确要求进行科学内容修改，否则它不应该改变科学内容；如果发现原文 claim 证据不足或可能过度，应提示用户，而不是静默改成事实。
