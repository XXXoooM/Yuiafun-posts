---
title: "2026-10-06 AI编程技巧"
published: 2026-10-06 10:01:03 +0800
description: "2026年10月06日 AI编程技巧，包含最新教程动态"
image: "https://images.xxapi.cn/images/acg/pc/image_374_8ac1ba9a.jpg"
tags:
  - 编程
  - 教程
  - 提示词
  - 每日分享
  - AI生成
category: "教程"
---

# 2026年10月06日 AI编程技巧

## 今日概要

The sources provide insights into Cursor Copilot's prompt techniques and usage. They emphasize setting negative and positive directives to constrain AI behavior, ensuring AI uses only provided tools and reads files instead of guessing answers. They highlight the importance of context understanding, making code changes efficiently, and prioritizing user queries. The sources also discuss the need for AI to generate runnable code, handle errors, and use memory functions effectively. Additionally, they mention the significance of designing effective prompts and tool chains to ensure stable and reliable AI programming tool performance.

---

### 1. 扒了下 Cursor 的提示词，被狠狠惊艳到了！如果让你开发一个 AI 编程工具（比如 Cursor），你觉得最大的难点 - 掘金

💡 这一段提示词中，我们能学到几个技巧：

 通过设定负面指令（大写的 NEVER）和正面指令（大写的 ALWAYS），强化了对 AI 的行为约束。
 通过 “切勿调用未明确提供的工具”、“仅使用标准的工具调用格式和可用的工具”、“读取文件而不是猜测或编造答案” 尽可能地消除 AI 的幻觉。
 在合适的场景给 AI 放权，不用让它频繁找用户确认。

我印象很深刻，刚开始用 AI Agent 的时候，有一次我睡觉前让 AI 跑个大任务，结果第二天发现 AI 在等我确认需不需要安装依赖。。。合着卡了一晚上啥都没干！

#### maximize\_context\_understanding

这部分的作用是告诉 AI 如何进行思考和信息收集、最大限度地理解上下文，核心原则是 全面 和 深入：

 在回答前，必须通过工具或提问确保掌握了完整的上下文。
 要追溯每个符号的定义和用法，确保完全理解。
 强制 AI 使用多种不同措辞进行多次搜索，确保信息的完备性。

💡 其中，最后一点是我认为非常值得学习的，就跟我们程序员遇到 Bug 时一样，一个关键词可能无法搜索到我们想要的答案，就要多尝试几组关键词，得到足够多的信息后问题才更容易解决。

💡 这部分内容也是 思维链 CoT（Chain-of-Thought） 和 ReAct（推理执行） 的体现，给 AI 规划了一套具体、可执行的信息收集分析流程，让 AI 先尽可能思考、获取到足够的信息之后，再具体执行。

#### making\_code\_changes

这个模块的作用是 规范 AI 修改代码的行为： [...] #### making\_code\_changes

这个模块的作用是 规范 AI 修改代码的行为：

 禁止直接在聊天中输出代码，必须通过代码编辑工具来实现更改。这样做就避免了对话框的空间被大量的代码块占据。
 强调生成的代码必须是 可立即运行的，要求 AI 自动处理好依赖、导入等所有前置条件。否则生成一堆没法用的代码的话，体验就很差了。不过这里也只是一个约束罢了，毕竟谁能保证一次性写出的代码 100% 能运行呢？
 为 AI 设定了处理错误的循环机制，尝试修复最多3次，如果失败就向用户求助。

💡 对于 AI 编程工具来说，这段提示词非常重要。想象一下，如果已经生成了一个 5000 行代码的文件，结果用户只需要修改文件中的某一行代码，难道要重新把这 5000 行代码输出一遍么？更高效的方式肯定是提供给 AI 一个支持 “字符串替换” 的代码编辑工具，可以让 AI 只修改部分代码，不仅输出效率更高、修改更精准可控，还有利于对比修改前后的代码。

#### summarization

这部分比较简短，只添加了一个约束 —— AI 应该处理最重要的查询。

这其实是强行调整 AI 的注意力焦点。随着对话进行，用户可能会提出新的、更优先的需求，有了这段提示词，AI 可以转移任务重心，优先处理用户的核心诉求。

就好比我正在处理一个工作，老板突然说：“别干了，出去团建去！”，那我不可能还继续干之前的工作对吧。

#### memories

这段提示词虽然很长，但核心的功能是为了让 AI 正确使用 Cursor 的对话记忆功能，了解一下就好。

### 3、支持的工具

Tools 模块的内容非常长，占了整个提示词的 80%，但其实很好理解，就是给 AI 提供各种各样的工具，并且将每个工具的作用、用法、注意事项给 AI 描述清楚。 [...] 比如鱼皮说一遍 “记得点赞三连”，你可能不以为然，所以这里我要说第二遍 “求你点赞三连”，但你可能还是没有被打动，所以我要说第三遍 “在你没有点赞三连之前，请你先点赞三连”。

💡 还有个类似的技巧叫 Re-Reading 重读，又称 Re2。其实就是复读机，通过让模型重新阅读一遍问题来提高推理能力，有 文献 印证了它的效果。

### 2、操作约束

接下来的提示词就是在教 AI 做事。

分为 6 个部分，每个部分都是用一组对称的 HTML 标签括了起来，结构非常清晰。

#### communication

见名知意，这里就是在告诉 AI “怎么说话”，便于用户理解。

规定了 AI 的响应要使用 Markdown 格式，以及如何格式化文件名、函数名，如何使用定界符来展示数学公式。

💡 统一输出格式不仅能帮助用户阅读，而且也有利于后续对输出文本的处理。

鱼皮之前带大家做的 AI 零代码应用生成平台项目 中，提示词内也约定了输出格式：

#### tool\_calling

这是整个提示词中非常关键的约束部分，是 AI 使用工具时必须要遵守的原则。

比如：

 禁止 AI 在和用户交流时直接提及工具名称。
 鼓励 AI 优先通过调用工具获取信息，而不是直接向用户提问，避免一些无意义的交互影响用户的体验。
 一旦制定计划，应立即执行，无需等待用户确认。这也是 AI 经常出现的情况，制定计划之后总是会结束会话并询问用户是否执行。
 在不确定代码库结构或文件内容时，必须使用工具读取信息，禁止猜测。

💡 这一段提示词中，我们能学到几个技巧：

来源：[https://juejin.cn/post/7547547103166595122](https://juejin.cn/post/7547547103166595122)

---

### 2. 10个使用Cursor进行AI编程时的提示词技巧

示例第一步提示词：“设计一个Python 函数来读取一个文件，并将其中每一行的内容反转。” 第二步提示词：“写出实现逻辑步骤。” 第三步提示词：“根据上述逻辑

来源：[https://x.com/AlchainHust/status/1852009724369342529](https://x.com/AlchainHust/status/1852009724369342529)

---

### 3. 深度解析 Cursor（逐行解析系统提示词、分享高效制定 Cursor Rules 的技巧...）

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

### 4. 五大提示词优化方案，让Cursor 生成代码准确率提升90%

"Cursor AI代码生成存在版本适配、资源虚构、逻辑错误三大幻觉问题。本文通过五大提示词优化方案，将代码准确率从48%提升至94%：1)绑定项目环境参数

来源：[https://cloud.tencent.com/developer/article/2685595](https://cloud.tencent.com/developer/article/2685595)

---

### 5. 免费AI编程助手实测对比：Copilot / Codeium / Cursor / Tabby - 声网

## 界面与交互

Copilot和Codeium在IDE中表现为智能提示：编辑时自动弹出建议框，用户可按Tab/Enter接受补全；Copilot Chat或Codeium Chat通过侧边栏或命令行界面进行对话。Cursor的UI类似VS Code，左侧边栏有Chat入口，Tab补全在编辑区出现，其它功能通过快捷键触发。Tabby的使用则与Copilot类似：在IDE中调用Tabby命令或快捷键即可获得补全和问答。响应速度与资源占用：Copilot和Codeium均使用云端模型推理，响应速度取决于网络和服务器负载，一般数百毫秒内返回建议，几乎不占用本地算力。Codeium宣传“闪电般的速度”；Cursor默认也是连接远端模型，需网速良好。Tabby运行时则需本地或私有GPU资源支持，模型大小不同导致速度差异：使用较大模型时可能略慢，但在有高速GPU的情况下体验仍然流畅。总的来说，Tabby本地部署对硬件要求最高，而前三者基本可在普通开发机（i5/16GB）上流畅运行。

### 联网需求与隐私

Copilot、Codeium和Cursor的AI计算都在厂商云端进行，必须联网使用，而且代码片段会发送到服务器；其中Copilot和Cursor都声明遵守SOC 2等标准保护数据隐私，但仍需信任提供商。Codeium官方强调其服务基于自研模型，不收集用户代码或个人信息，不会使用GPL等非许可代码进行训练。Tabby则完全本地运行，不依赖外部API，用户代码和请求都存储在自己搭建的服务器中，隐私由用户自行控制。

## 模型与部署 [...] ### 相关文章

 零成本开发！试试这6个免费的API接口平台
 声网博客开张大吉！首发征文活动，好礼拿不停
 6款免费语音AI工具推荐，涵盖ASR、TTS与VAD全链路
 为机器人装上“眼睛”：声网视觉理解技术如何重塑家庭陪伴新范式
 2026 年1月 GitHub 最受欢迎的十大开源 AI 项目全解析
 GitHub Copilot 教程：提示词、技巧和用例

### 在声网，连接无限可能

想进一步了解「对话式 AI 与 实时互动」？欢迎注册，开启探索之旅。

注册体验

本博客为技术交流与平台行业信息分享平台，内容仅供交流参考，文章内容不代表本公司立场和观点，亦不构成任何出版或销售行为。

热门产品

对话式 AI 引擎

对话式 AI 开发套件

语音通话

视频通话

低延迟直播

实时消息

热门场景

对话式 AI

智能硬件

在线教育

Demo 下载

RTE 体验馆

RTE 健康看板

生态合作

声选计划

新闻中心

安全合规

企业责任

400 632 6626

加入我们

开发者实践教程 对话式 AI 引擎 一站式出海解决方案 智能硬件解决方案 [...] ### Codeium

Exafunction公司推出的AI代码助手，以深度学习模型为驱动，可实现代码补全、代码生成、错误修复、重构、解释等功能。目前号称支持70多种编程语言，兼容VS Code、Vim/Neovim、Sublime Text、Atom、Emacs等40多种编辑器。Codeium提供智能的单行/多行补全和函数级生成，并能根据自然语言指令生成代码；其 Chat 功能（插件中通过输入 #chat 启动）可回答问题、解释代码或执行重构命令；搜索功能（#search）可查询项目或在线资源的API示例。Codeium主打“极速”体验，据称补全建议质量先进且生成速度非常快。

### Cursor

一个独立的AI编程编辑器（Fork自VS Code），由AnySphere公司开发。Cursor集成了Cursor Tab（智能补全）和内置AI Chat两大核心功能。Cursor Tab提供类似Copilot的自动补全，但强调多行连续补全能力：按一次Tab可补全当前行，再按一次可以跳到下一段落继续补全，非常适合批量重构或参数变更等场景。据用户测试，Cursor补全的连贯性和准确度优于GitHub Copilot。Cursor的AI Chat功能内置在编辑器中，可使用 @File、@Folder、@Codebase、@Doc、@Web、@Git 等指令获取不同范围的上下文，直接提问项目问题并一键将生成的修改应用到代码中。此外，Cursor支持自然语言的命令式修改（如在终端或代码内输入快捷键生成/重构代码），还有如“Composer 模式”自动拆分组件、代码审查等高级功能。

### Tabby

来源：[https://www.shengwang.cn/blog/blogdetail/free-ai-code-assistant](https://www.shengwang.cn/blog/blogdetail/free-ai-code-assistant)

---

