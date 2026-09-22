---
title: "2026-09-22 AI编程技巧"
published: 2026-09-22 10:01:18 +0800
description: "2026年09月22日 AI编程技巧，包含最新教程动态"
image: "https://images.xxapi.cn/images/acg/pc/T50A1dPaG4YwQdtGg4ceFCzQ.jpg"
tags:
  - 编程
  - 教程
  - 提示词
  - 每日分享
  - AI生成
category: "教程"
---

# 2026年09月22日 AI编程技巧

## 今日概要

Cursor is an AI-powered code editor with advanced features like intelligent code completion and integrated AI chat. It supports multiple programming languages and offers tools for code review and documentation. Cursor aims to enhance coding efficiency and productivity.

---

### 1. 扒了下 Cursor 的提示词，被狠狠惊艳到了！如果让你开发一个 AI 编程工具（比如 Cursor），你觉得最大的难点 - 掘金

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

💡 这一段提示词中，我们能学到几个技巧：

我印象很深刻，刚开始用 AI Agent 的时候，有一次我睡觉前让 AI 跑个大任务，结果第二天发现 AI 在等我确认需不需要安装依赖。。。合着卡了一晚上啥都没干！

#### maximize\_context\_understanding

这部分的作用是告诉 AI 如何进行思考和信息收集、最大限度地理解上下文，核心原则是 全面 和 深入：

💡 其中，最后一点是我认为非常值得学习的，就跟我们程序员遇到 Bug 时一样，一个关键词可能无法搜索到我们想要的答案，就要多尝试几组关键词，得到足够多的信息后问题才更容易解决。

💡 这部分内容也是 思维链 CoT（Chain-of-Thought） 和 ReAct（推理执行） 的体现，给 AI 规划了一套具体、可执行的信息收集分析流程，让 AI 先尽可能思考、获取到足够的信息之后，再具体执行。

#### making\_code\_changes

这个模块的作用是 规范 AI 修改代码的行为： [...] ### 整体结构分析

整体来看，这个提示词分为三大模块：角色定义、操作约束、和支持的工具。

就跟我们塑造一个游戏角色一样，先知道你是谁、你能做什么、你要做什么；再开始给角色点技能、教他怎么做；最后给角色持续买装备、教他怎么用，越来越强。

💡 我们写提示词也可以按照这个思路，让 AI 先从宏观上理解它的身份和目标，再到微观上遵循每一步的行动规范。

下面我们依次分析每个模块。

### 1、角色定义

提示词：

这段提示词上来就定义了：

💡 这也是典型的提示词编写技巧，通过明确角色、背景和目的，确保 AI 生成的内容聚焦于某个具体的领域和场景，提升输出的有效性。

接着往下看：

“你必须一直运行到完全解决用户的问题” 这里进一步明确了 AI 的角色，并且赋予 AI Agent 的持续运行模式，让 AI 有能力处理复杂、多步骤的任务。

💡 不知道大家有没有注意到，这段内容的表达有点冗余，多次重复了 “继续工作”、“解决查询”。这也是写 Prompt 常用的一种手段，我们知道，AI 跟人一样，在接受信息比较多的情况下，很可能会忘记一部分内容、或者忽略掉一些重点。通过从不同的角度 反复强调 同一个事情，能够强化 AI 的理解、保证这段内容的权重，也能在一定程度上消除 AI 理解 Prompt 时的歧义。

比如鱼皮说一遍 “记得点赞三连”，你可能不以为然，所以这里我要说第二遍 “求你点赞三连”，但你可能还是没有被打动，所以我要说第三遍 “在你没有点赞三连之前，请你先点赞三连”。

💡 还有个类似的技巧叫 Re-Reading 重读，又称 Re2。其实就是复读机，通过让模型重新阅读一遍问题来提高推理能力，有 文献 印证了它的效果。

### 2、操作约束

接下来的提示词就是在教 AI 做事。 [...] #### making\_code\_changes

这个模块的作用是 规范 AI 修改代码的行为：

💡 对于 AI 编程工具来说，这段提示词非常重要。想象一下，如果已经生成了一个 5000 行代码的文件，结果用户只需要修改文件中的某一行代码，难道要重新把这 5000 行代码输出一遍么？更高效的方式肯定是提供给 AI 一个支持 “字符串替换” 的代码编辑工具，可以让 AI 只修改部分代码，不仅输出效率更高、修改更精准可控，还有利于对比修改前后的代码。

#### summarization

这部分比较简短，只添加了一个约束 —— AI 应该处理最重要的查询。

这其实是强行调整 AI 的注意力焦点。随着对话进行，用户可能会提出新的、更优先的需求，有了这段提示词，AI 可以转移任务重心，优先处理用户的核心诉求。

就好比我正在处理一个工作，老板突然说：“别干了，出去团建去！”，那我不可能还继续干之前的工作对吧。

#### memories

这段提示词虽然很长，但核心的功能是为了让 AI 正确使用 Cursor 的对话记忆功能，了解一下就好。

### 3、支持的工具

Tools 模块的内容非常长，占了整个提示词的 80%，但其实很好理解，就是给 AI 提供各种各样的工具，并且将每个工具的作用、用法、注意事项给 AI 描述清楚。

由于工具较多，在最外层将工具通过 `namespace` 命名空间进行分类，包括 `functions` 和 `multi_tool_use`，为 AI 提供了一个清晰的工具层级。

`namespace`
`functions`
`multi_tool_use`

命名空间下有很多工具，比如代码库搜索工具：

💡 从这个模块中，我们能学到一些小技巧。

来源：[https://juejin.cn/post/7547547103166595122](https://juejin.cn/post/7547547103166595122)

---

### 2. GitHub - InfyEdge/system-prompts-and-models-of-ai-tools-chinese: AI编程工具中文提示词合集，包含Cursor、Antigravity、VSCode Agent等多种AI编程工具的提示词，为中文开发者提供AI辅助编程参考资源。持续更新中文编程Rules和最新AI编程提示词。 · GitHub

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

来源：[https://github.com/InfyEdge/system-prompts-and-models-of-ai-tools-chinese](https://github.com/InfyEdge/system-prompts-and-models-of-ai-tools-chinese)

---

### 3. 【2025最新】Cursor vs GitHub Copilot 终极对比：AI编程助手王者之争 - Cursor IDE 博客

学习曲线平缓
 在熟悉的VS Code中使用
 丰富的代码示例和解释
 活跃的社区支持
 免费的学生版本

## 【高级技巧】最大化AI编程效率

### Cursor高级使用技巧

1. 优化Composer提示词：

```
// 好的提示词示例 "创建一个React组件，包含用户头像、姓名和状态指示器，支持在线/离线状态切换，使用TypeScript和Tailwind CSS" // 避免的提示词 "做一个用户组件" 
```

1. 项目级配置优化：

```

json

```
// .cursor/settings.json{"cursor.ai.model":"gpt-4","cursor.ai.maxTokens": 4000,"cursor.ai.temperature":0.3}
```

```

### GitHub Copilot高级使用技巧

1. 优化代码注释：

```

javascript

```
// 创建一个防抖函数，延迟300ms，用于搜索输入// 支持取消上一次调用，返回Promise function debouncefunc, delay// Copilot会生成高质量的防抖实现
```

```

1. 利用Chat功能：

 使用`/explain`解释复杂代码
 使用`/fix`修复错误
 使用`/tests`生成测试用例

## 【成本优化】如何降低AI编程成本

### 💰 个人开发者省钱策略

1. GitHub Copilot学生免费版：

    使用学校邮箱申请
    完全免费，功能完整
    适合学生和教育工作者
2. 开源项目免费使用：

    维护开源项目可免费使用
    需要GitHub认证
    适合开源贡献者
3. 使用laozhang.ai中转API： [...] GitHub Copilot独有创新：

 Copilot Chat：集成在IDE中的AI对话
 代码解释：解释复杂代码逻辑
 测试生成：自动生成单元测试
 文档生成：自动生成代码文档
 漏洞检测：识别潜在安全问题

创新功能实用性评分：

| 创新功能 | Cursor评分 | Copilot评分 | 实用性 |
 ---  --- |
| 自然语言编程 | 9/10 | 7/10 | 极高 |
| 项目理解 | 9/10 | 6/10 | 高 |
| 代码解释 | 7/10 | 8/10 | 高 |
| 测试生成 | 6/10 | 8/10 | 中 |
| 安全检测 | 5/10 | 8/10 | 高 |

胜出者：Cursor - 在创新性和前瞻性方面领先

## 【场景分析】不同用户群体推荐

### 🎯 个人开发者推荐

选择Cursor的情况：

 主要使用JavaScript/TypeScript/Python
 专注于单一大型项目开发
 喜欢尝试新技术和工具
 对价格不太敏感
 需要深度的项目理解能力

选择GitHub Copilot的情况：

 使用多种编程语言
 在多个IDE间切换工作
 预算有限，追求性价比
 需要快速上手，学习成本低
 经常参与开源项目

### 🏢 团队/企业推荐

选择Cursor的情况：

 团队规模较小（5-20人）
 主要开发Web应用
 团队技术水平较高
 愿意投入时间学习新工具

选择GitHub Copilot的情况：

 大型团队或企业
 多语言、多平台开发
 需要严格的安全合规
 已有GitHub企业账户
 需要详细的管理和审计功能

### 🚀 初学者推荐

强烈推荐GitHub Copilot：

 学习曲线平缓
 在熟悉的VS Code中使用
 丰富的代码示例和解释
 活跃的社区支持
 免费的学生版本

来源：[https://www.cursor-ide.com/blog/cursor-vs-github-copilot-ultimate-comparison-2025](https://www.cursor-ide.com/blog/cursor-vs-github-copilot-ultimate-comparison-2025)

---

### 4. AI编程之Cursor使用技巧及一些思考

网上也能找到一些不错的提示词总结，比如awesome-cursorrules。我试着将仓库特定的规则告诉它，比如代码风格，比如一些工具或编译等，这都有助于我们未来更好的与AI沟通。

这个过程中，其实我们还可以偷懒，甚至`.cursorrules`也是由AI来写的，它基于README或code base，可以帮我们完成一个初稿，我们自己再补充完善一些，未来这就是喂给AI的一部分提示词了。我在想，若是能够不断编辑完善rules，比如如何写一个测试用例，如何写注释，如何写一个模块，那么真的很可能取得不错效果，这一块我应该未来还会持续有更多实践，特别是工作中会经常和某几个仓库打交道，必然有些成熟的惯例是AI能轻松学去的吧：） Cursor Rules

## Cursor的其它实践

### 单元测试

有一些工作是我们平常自己厌烦的，但是咱们的AI助手可是任劳任怨，比如写更多单测。我们自己写平常会有两大问题，用例想不完全以及偷懒覆盖不足。这种目标性比较确定的事情，在Cursor中是比较容易完成的，当然前提是你的代码比较规范，也有一些可参考的示例。

也有些场景生成的代码不太符合预期，那么如何写出AI友好的用例/代码呢？我看Behavior Driven Development (BDD)挺不错，它强调行为，而不是实现，所以可以更聚焦于功能，而不是实现细节。有这种代码框架后，细节刚好AI可以补全，而咱们只需要关注于功能（即用例）。在Go语言中，可以借助于`Ginkgo`()，它支持BDD框架。你看着感受一下会不会AI友好些： [...] 未来如何在更多场景中使用AI来帮助完善单测是值得探讨的事情，希望有更多实践后能和大家分享更多心得体会。

### Code Review

没想到吧，AI除了帮你写代码，当然也能帮你评审代码。随着不停的听着各种AI刷爆排行榜，那么我也期待它们能帮我把控更多的风险。我尝试将工作中的一些比较隐蔽的BUG，通过Cursor来评审，发现它确实能发现一些问题，甚至一些我们组内多人评审都漏掉的问题。我不由得想，如果大家提交代码前，都有一个这么强力的助手帮你先看看本次改动，提供一些参考建议，那么提交的代码质量会更高，也更有信心。

任劳任怨的AI，它不会因为一次修改几百处而眼花缭乱，它只会默默的遵从你的指定帮你检查。所以给CR的提示词也比较关键，这里我们可以看一下网上的一些总结ai prompts for code reviews。不过我感觉不同团队或项目最好有自己定制的CR规则，比如就写在`.cursorrules`文件中，这样更有针对性。

这里有点小技巧，我们在Cursor中提交代码前，可以`@git`选择`PR (Diff with Main Branch)` ，这样Cursor会基于当前的diff来评审，而不是基于整个仓库。模型上我建议你选择更强的模型，比如`claude-3.5-sonnet`或者`o1-mini`等。

我最近拿了一个较复杂的提交来让AI进行Code Review，使用claude-3.5-sonnet模型以及4o都没有发现问题，但我切换到o1-mini，它能够发现。我又试了一下国产最近大火的DeekSeek V3，也能够发现问题。给国产模型点个赞！所以作为CR使用，面对复杂的场景我们就别节约这点消耗啦：）

## 其它AI Code Editor [...] 惊艳到我的是，我让其重构一段代码，它同时尝试修复相关lint，发现protobuf的proto有修改，自动去编译proto，它先尝试命令`make proto`，发现报错了。 接着分析我的Makefile，察觉到是基于Earthly来构建的，并且发现了`make code`命令可以生成相关协议，接着自动执行编译与修复工作。一切就绪后，给我生成了一个不错的Commit Message，并自动提交了。这期间我就是看它表演，时而让我确认一下要执行的命令，我面带微笑点确定，又一次有点忧伤。

### YOLO模式

在使用Agent模式时，当遇到需要在计算机上执行一些命令时，有时会询问于你，要使用者主动点确定，主要是隐私等考虑。但有时我们想更快捷认为可以授权它去做点事，这便是Yolo功能的出现背景，要使用此功能则需要0.44+的版本。相对开启Agent，Yolo这个相当于一个配置，说是一种模式略显牵强。当前默认是不开启Yolo的，显式的为了安全起见，我们还是可以配置允许它自动执行哪些命令，白名单或黑名单都支持。

在启用YOLO后，Agent模式下工作会更加自动化，多数时候已经可以“围观”机器工作了。这个模式我使用的经验倒不是特别多，有时候似乎有些低效的循环，但未来价值可期。

### 定制化`.cursorrules`

写文章时再查了一下，前几天更新的0.45版本又一次提升了.cursorrules文件的定制能力，它支持了多仓库级的rules配置，未来研究一下实际效果。我们先说两种使用方式：

1. 全局的Rules For AI。在`Cursor`的设置中可直接输入，可以配置一些全局规则，比如我就让它回复使用中文，但是代码注释使用英文，效果很明显。
2. 在根目录定义`.cursorrules`文件，在它上面写上你想告诉Cursor的一些提示词。

来源：[https://gameapp.club/post/2025-01-26-programming-with-cursor](https://gameapp.club/post/2025-01-26-programming-with-cursor)

---

### 5. 免费AI编程助手实测对比：Copilot / Codeium / Cursor / Tabby

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

