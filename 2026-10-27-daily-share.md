---
title: "2026-10-27 AI编程技巧"
published: 2026-10-27 10:01:07 +0800
description: "2026年10月27日 AI编程技巧，包含最新教程动态"
image: "https://images.xxapi.cn/images/acg/pc/bMIpXcp90YeJAdOUdgiHui4W.jpg"
tags:
  - 编程
  - 教程
  - 提示词
  - 每日分享
  - AI生成
category: "教程"
---

# 2026年10月27日 AI编程技巧

## 今日概要

According to the sources, Cursor is an AI-powered code editor that offers advanced features like Composer, which allows users to generate, modify, and apply code changes globally within a project. Unlike GitHub Copilot, Cursor's Composer enables users to manually select context and apply changes directly to files, offering more control and flexibility. Cursor also includes an Agent mode that assists in setting up project environments and managing dependencies. The system prompts in Cursor are designed to optimize interactions and ensure the AI's responses are contextually relevant and high-quality.

---

### 1. 简单说一下 GitHub Copilot 和 Cursor 的差别，以及为什么我觉得 Cursor 要更好 | 宝玉的分享

第二个是通过提示词添加、重构、删除新功能

很多人在用 AI 编辑器只用了自动补全修改的功能，而通过提示词让 AI 帮你生成代码的功能用的比较少或者不会用，这就相当于让 AI 编辑器的能力只发挥了一小部分，真正体现智能的地方就是通过提示词对项目全局修改。

GitHub Copilot 和 Cursor 都可以通过两种方式唤出写提示词的窗口：CMD + I 或者侧边栏的 AI Chat。GitHub Copilot 的 CMD + I 这个快捷键功能没有太多人知道，因为 VSCode 上没有明显提示，很多人不知道，Cursor 在选中代码后有提示相对好一点。

但是 Cursor 又有两个功能键 CMD + K 和 CMD + I，有一些细微差别，建议默认选择 CMD + I 这个，也叫 Composer。

这个提示词撰写窗口对于 GitHub Copilot 和 Cursor 来说，有个根本性的差别，包括 Windsurf 也没有的，就是上下文内容的手动选择。对于 GitHub Copilot 来说，它是根据你打开的 Tab 标签来“猜测”你的上下文，但这很难猜准，而 Cursor 可以让你手动选择你想要的上下文，在Composer中通过+号或者 @ 去附加代码。对于专业程序员来说，手动控制上下文这非常非常重要！因为在修改代码时，肯定少不了要引用现有的代码，参考其API，参考其代码结构等等，虽然你也可以手动复制进去，但是如果你可以方便的选择那是最好的。

回归到提示词工程，要让提示词效果好核心有两点：

1. 指令清晰
2. 上下文充分 [...] 回归到提示词工程，要让提示词效果好核心有两点：

1. 指令清晰
2. 上下文充分

如果你自己作为专业程序员不能精确控制上下文，寄希望于 AI 帮你选择上下文，现阶段还是不靠谱的，这点 Cursor 是做的非常好的。如果你还没有用过 Cursor 的 Composer 或者 Composer 的手动选择代码作为上下文的功能，一旦你习惯了，你再也受不了 GitHub Copilot 和 WIndsurf 这些帮你“猜”上下文代码的 AI 编辑器。

第三个是 Agent 或者说智能体的功能

GitHub Copilot 的 Chat，如果你用过就知道，它只能给出修改建议，生成参考代码，无法帮你直接应用修改，你需要手动去复制粘贴创建代码。

Cursor 的 Chat，默认也不会，但是你可以在代码上点击“Apply”链接应用代码到相应的文件。

GitHub Copilot 的 Composer，只能修改当前文件代码，不能应用到其他文件位置。

Cursor 的 Composer，它可以在项目全局添加、删除和修改代码，你只要review一下修改就可以应用这些修改，不满意也可以拒绝或者局部拒绝。

Cursor 的 Composer，现在有两个模式：Normal 和 Agent，Normal 就是简单的根据指令和上下文生成代码、应用修改。Agent 则可以像一个机器人一样，根据你的指令去分析代码，去安装需要添加的包，当然需要你自己确认。这个 Agent 功能在你创建新项目达环境的时候特别实用，一步步帮你把包都安装好了，直接就可以运行。

Agent 功能 Windsurf 做的非常好，Cursor 可能是借鉴的 Windsurf，GitHub Copilot 据说也要推出了。

来源：[https://baoyu.io/blog/github-copilot-vs-cursor](https://baoyu.io/blog/github-copilot-vs-cursor)

---

### 2. GitHub - Omnls/system-prompts-and-models-of-ai-tools-chinese: AI编程工具中文提示词合集，包含Cursor、Antigravity、VSCode Agent等多种AI编程工具的提示词，为中文开发者提供AI辅助编程参考资源。持续更新中文编程Rules和最新AI编程提示词。 · GitHub

| Factory（Droid） | Factory（Droid） |  |  |
| Fellou | Fellou |  |  |
| GitHub Copilot（VSCode） | GitHub Copilot（VSCode） |  |  |
| Gizmo AI | Gizmo AI |  |  |
| Google（Gemini、Jules） | Google（Gemini、Jules） |  |  |
| Grok（xAI） | Grok（xAI） |  |  |
| Hermes | Hermes |  |  |
| Hume（语音AI） | Hume（语音AI） |  |  |
| Indus AI | Indus AI |  |  |
| JetBrains（Junie） | JetBrains（Junie） |  |  |
| Kagi（搜索AI） | Kagi（搜索AI） |  |  |
| Leap（AI开发） | Leap（AI开发） |  |  |
| Lovable（AI全栈开发） | Lovable（AI全栈开发） |  |  |
| Manus（AI Agent） | Manus（AI Agent） |  |  |
| Meta（Llama） | Meta（Llama） |  |  |
| Microsoft（Copilot） | Microsoft（Copilot） |  |  |
| MiniMax | MiniMax |  |  |
| Misc | Misc |  |  |
| Mistral（Le Chat） | Mistral（Le Chat） |  |  |
| MultiOn（浏览器Agent） | MultiOn（浏览器Agent） |  |  |
| Notion（AI） | Notion（AI） |  |  | [...] . ├── Anthropic（Claude）/ # Claude 全系列（20个文件已翻译） │ ├── Core_Models/ # 核心模型提示词 │ ├── Features/ # 功能特性提示词 │ └── raw/ # 原始系统消息 ├── OpenAI（ChatGPT）/ # GPT 系列（5个文件已翻译） │ └── Core_Models/ # GPT-5.x 系列 ├── Grok（xAI）/ # Grok 系列（3个文件已翻译） │ ├── Core_Models/ # 基础模型 │ ├── Features/ # Grok Build 完整系统 │ └── Personalities/ # 个性化设置 ├── Google（Gemini、Antigravity）/ # Google AI 工具 ├── Microsoft（Copilot）/ # Copilot CLI ✅ ├── Meta（Llama）/ # Meta AI ✅ ├── Cline（VS Code插件）/ # Cline 完整系统 ✅ ├── Cursor（代码编辑器）/ # Cursor Composer ✅ ├── Sourcegraph（Amp）/ # Amp CLI ✅ ├── Notion（AI）/ # Notion AI ✅ ├── Comet Assistant/ # Comet 系统 ✅ ├── StackBlitz（Bolt.new）/ # Bolt.new ✅ ├── Factory（Droid）/ # Factory Droid ✅ ├── Hume（语音AI）/ # Hume Voice ✅ ├── MultiOn（浏览器Agent）/ # MultiOn ✅ ├── 字节跳动（豆包、Trae）/ # 字节系工具 ✅ ├── AWS（Kiro）/ # AWS [...] ## 🚀 收录内容

本项目当前收录了 40+ 主流及新兴 AI 编程工具的系统提示词和模型设计资料：

### 核心大模型（已完整翻译 ✅）

 Anthropic Claude 系列: Claude 3.7, Claude 4.6 (Opus/Sonnet), Claude Code, Claude Cowork
 OpenAI GPT 系列: GPT-5.2/5.3/5.4 (Thinking & Instant)
 xAI Grok 系列: Grok 4.0, Grok Build (完整工程系统)
 Google Gemini: Gemini 3.5 Flash, Gemini CLI
 Meta AI: Llama 系列对话系统

### 代码编辑器与 IDE 工具（已翻译 ✅）

 Cursor: Composer Agent 2.0
 Cline: VS Code 插件完整系统
 Microsoft Copilot: CLI 命令行工具
 Sourcegraph Amp: 代码搜索增强
 Windsurf: AI 编程环境
 VS Code Agent: 多模型支持

### AI 编程助手（部分翻译）

 Cognition Devin: 自主编程 Agent
 Replit: 在线编程平台
 StackBlitz Bolt.new: 快速原型工具 ✅
 Factory Droid: 工程 Agent ✅

### 企业与效率工具（已翻译 ✅）

 Notion AI: 文档智能助手
 Comet Assistant: 开发效率工具
 Perplexity: 搜索增强

### 国内厂商工具

 字节跳动: 豆包、Trae ✅
 阿里巴巴: Qoder 系列
 腾讯: CodeBuddy
 智谱: Z.ai
 月之暗面: Kimi

来源：[https://github.com/Omnls/system-prompts-and-models-of-ai-tools-chinese](https://github.com/Omnls/system-prompts-and-models-of-ai-tools-chinese)

---

### 3. "AI 辅助编程实战：从Copilot 到Cursor 的2026 年效率工具 ...

提示词技巧好的提示词能显著提升AI 输出质量: 差的提示词: 写一个排序函数好的提示词… 1. 支持泛型,可以排序任意类型的数组2. 接受比较函数作为参数3.

来源：[https://zhuanlan.zhihu.com/p/2022614703696823950](https://zhuanlan.zhihu.com/p/2022614703696823950)

---

### 4. 拆解 Cursor 系统提示词：2000 字背后的 AI 调教艺术 - 文章 - 开发者社区 - 火山引擎

[](

登录注册

首页AI 大模型体验中心AI 大模型体验中心AI 大模型体验中心Agent 评测集Agent 评测集Agent 评测集AI 案例广场AI 案例广场AI 案例广场火山杯大赛学习中心

去发布

首页AI 大模型体验中心AI 大模型体验中心AI 大模型体验中心动手实验室动手实验室动手实验室Agent 评测集Agent 评测集Agent 评测集AI 案例广场AI 案例广场AI 案例广场学习中心

社区

# 拆解 Cursor 系统提示词：2000 字背后的 AI 调教艺术

予贝

予贝

AI

大模型向量数据库云存储

点击👇关注我 学习更多AI知识

大家好，我是予贝

今天在技术群里看到有人转发了 Cursor 的系统提示词，这个提示词，代表了当前 AI 助手设计的最高水准。

当我们在 Cursor 中敲下第一行代码，一个 2000 字的提示词已经在背后默默工作。

今天我们来拆解它，看看顶级 AI 是如何被"调教"的。

提示词如下，本提示词源自云中江树，在此向大佬致以诚挚谢意。 [...] 标签中用户在每条消息中的指令。  1. 2. 3. 4. 5. 6. 7. 8. _file、grep\__search时，总是并行运行所有命令。宁可最大化并行工具调用，也不要运行太多顺序工具。 当收集关于某个主题的信息时，在你的思考中提前规划搜索，然后一起执行所有工具调用。例如，以下所有情况都应使用并行工具调用： - 搜索不同模式（imports、usage、definitions）应该并行进行 - 使用不同正则表达式模式的多个grep搜索应该同时运行 - 读取多个文件或搜索不同目录可以一次性完成 - 结合codebase\__search以获得全面结果 - 任何你提前知道要查找什么的信息收集 在进行工具调用之前，简要考虑：我需要什么信息来完全回答这个问题？然后一起执行所有这些搜索，而不是等待每个结果再规划下一个搜索。大多数时候，可以使用并行工具调用而不是串行。只有当你真正需要工具A的输出来确定工具B的使用时，才能使用串行调用。 默认并行：除非你有特定原因说明操作必须串行（A的输出是B的输入所必需），否则总是同时执行多个工具。这不仅仅是优化——这是预期行为。记住并行工具执行比串行调用快3-5倍，显著改善用户体验。 如果你对用户请求的答案不确定或不知道如何满足他们的请求，你应该收集更多信息。这可以通过额外的工具调用、询问澄清问题等方式来完成... 例如，如果你执行了语义搜索，结果可能无法完全回答用户的请求，或值得收集更多信息，请随时调用更多工具。 如果你执行了可能部分满足用户查询的编辑，但你不确定，请在结束你的回合之前收集更多信息或使用更多工具。 如果你能自己找到答案，倾向于不要求助用户。 进行代码更改时，除非被要求，否则绝不向用户输出代码。相反，使用代码编辑工具之一来实现更改。 确保你生成的代码可以立即被用户运行，这是极其重要的。为确保这一点，请仔细遵循以下指令： [...] 这是代码引用的唯一可接受格式。格式为```startLine:endLine:filepath，其中startLine和endLine是行号。

使用相关工具（如果可用）回答用户的请求。检查每个工具调用的所有必需参数是否已提供或可以从上下文合理推断。如果没有相关工具或缺少必需参数的值，请要求用户提供这些值；否则继续工具调用。如果用户为参数提供了特定值（例如在引号中提供），确保准确使用该值。不要为可选参数编造值或询问。仔细分析请求中的描述性术语，因为它们可能指示应包含的必需参数值，即使没有明确引用。

```
五大调教艺术：从笨拙到智能 -------------### 1. 角色塑造的艺术：用否定句划清边界
```

"绝不向用户输出代码，除非被要求"  
 "绝不创建文件，除非绝对必要"  
 "绝不主动创建文档文件"

```
"绝不" "我可以" "你不是服务员，不要端盘子；你不是收银员，不要收钱。你只负责做菜。"### 2. 执行优化的艺术：并行思维的革命
```

你问一个问题  
 AI思考  
 AI回答  
 你问下一个问题  
 重复...

```
 而 Claude Sonnet 4 被训练成这样工作： 
```

你问一个复杂问题  
 AI同时启动多个"思考进程"  
 并行处理所有相关子问题  
 整合后给出完整答案

```
"并行工具执行比串行调用快 3-5 倍"### 3. 质量控制的艺术：用约束创造自由
```

"绝不" 出现了 8 次  
 "必须" 出现了 12 次  
 "总是" 出现了 6 次  
 "从不" 出现了 4 次

```
 为什么需要这么多约束？ 因为 AI 就像一个极其聪明但没有常识的孩子。你不告诉他什么不能做，他会做出让你哭笑不得的事情。 比如，如果不加约束，AI 可能会： 
```

来源：[https://developer.volcengine.com/articles/7538285627641430059](https://developer.volcengine.com/articles/7538285627641430059)

---

### 5. 深度解析 Cursor（逐行解析系统提示词、分享高效制定 Cursor Rules 的技巧...）

## ` instead of responding if you need to read a file”。当遇到编码任务时，模型现在会补全出“read_file(‘index.py’)</assistant>”，我们（客户端）则会再次输入提示词“<tool>… full contents of index.py …</tool><assistant>`”并要求其继续补全文本。虽然本质上仍是自动补全，但大语言模型已能借此与外界及外部系统互动了。

### 

b. write_file(full_path: str, content: str)

c. run_command(command: str)

4.   优化内部提示词（Prompts）：例如“你是一位编码专家”、“不要假设，请使用工具”等

总的来看，核心流程基本就是这些了。真正的难点在于设计提示词和工具链，确保它们能稳定可靠地工作。 如果完全按照上述描述来构建，系统虽能勉强运行，但会频繁出现语法错误、幻觉问题（hallucinations）且相当不稳定。

### ：在这些编程工具中建议积极使用 @folder/@file（优先提供更明确的上下文，以获取更快更准确的响应）。

   搜索代码可能很复杂，尤其对于“我们在哪里实现了认证功能相关的代码？”这类语义查询。我们没有让智能体精通编写搜索正则表达式（regexes），而是选择在索引阶段使用一个编码器大模型（encoder LLM）将整个代码库索引到向量数据库（vectorstore）中，从而将文件内容及其功能嵌入到向量中。在查询时，另一个大语言模型会根据相关性对文件进行重排序和过滤。这确保了主智能体在询问认证功能代码相关问题时能获得“完美”的结果。 [...] 操作建议 (Tip)：你无法直接将提示词发送给应用模型（apply-model）。类似“别乱删代码”或“别随意增删注释”的建议完全无效，因为这些问题本质上是应用模型（apply-model）工作机制的固有产物。 应该让主智能体获得更多控制权，例如在指令中明确要求：“在 edit_file 指令中提供完整的文件内容”
       操作建议 (Tip)：应用模型处理超大文件时缓慢且易错，务必将文件拆分至每部分小于 500 行代码
       操作建议 (Tip)：lint 反馈对智能体具有极高价值，应投资构建能提供高质量建议的增强型 linter2。使用编译型语言和静态类型语言能提供更丰富的 lint 时反馈（lint-time feedback）
       操作建议 (Tip)：使用唯一的文件名（不要在代码库中使用多个不同的 page.js 文件，最好改用 foo-page.js、bar-page.js 等），在文档中应使用完整的文件路径，并将高频修改的代码段（hot-paths）集中到同一文件或文件夹中，以降低编辑工具的操作歧义

   选用擅长在此类智能体（Agent）工作流中编写代码的模型（而非仅具备通用编码能力）。这就是 Anthropic 模型在 Cursor 等 AI 编程工具中表现出色的原因 —— 它们不仅代码质量高，更擅长将编程任务拆解为这种类型的工具调用（tool calls）。

       操作建议 (Tip)：选用模型时，不应仅关注“编码能力”，应优先选择专门为智能体驱动型编程工具（agentic IDEs）优化的模型。 目前（据我所知）能有效评估此能力的唯一排行榜是 WebDev Arena 3。 [...] 关注

原创 2025-06-18 10:21:56 4k 阅读AI 写同款·GEO 优化›

> 编者按： 我们今天为大家带来的这篇文章，作者的观点是：只有深入理解 AI 编程工具的底层原理和能力边界，才能真正驾驭这些工具，让它们成为提升开发效率的“外挂神器”。
> 
> 
> 本文从 LLM 的基础工作机制出发，解释了 Cursor 等工具本质上是 VSCode 的复杂封装，通过聊天界面、工具集（如 read_file、write_file 等）和精心设计的提示词来实现智能编程辅助。作者还逐行解析了 Cursor 的系统提示词，分析了其中的工程设计细节。此外，作者还提供了制定高效 Cursor Rules 的具体指导，强调 Cursor Rules 应该像百科词条般详实，而非简单的命令列表。

作者 | Shrivu Shankar

编译 | 岳扬

透彻了解 Cursor、Windsurf和 Copilot这类 AI 编程工具的运作原理细节，能大大提升你的开发效率，并让这些工具在不同场景下都更加稳定地工作 —— 尤其在庞大、复杂的代码库中。当人们难以让 AI 编程工具高效工作时，往往是把它们当成了传统工具来使用，却忽略了一个关键：只有清楚这些工具的先天不足和最佳应对策略，才能真正驾驭它们。一旦摸透这些工具的运作逻辑和能力边界，它们就会化身成为提升开发效率的“外挂神器”。在我写作此文时，我约 70% 的代码1都由 Cursor 产出。

在本文，我将深入解析这些 AI 编程工具的实际运行原理、Cursor 的系统提示词，以及如何优化你的编码方式与 Cursor rules。

来源：[https://blog.csdn.net/Baihai_IDP/article/details/148733687](https://blog.csdn.net/Baihai_IDP/article/details/148733687)

---

