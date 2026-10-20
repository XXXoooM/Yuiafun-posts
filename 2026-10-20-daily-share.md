---
title: "2026-10-20 AI编程技巧"
published: 2026-10-20 10:09:32 +0800
description: "2026年10月20日 AI编程技巧，包含最新教程动态"
image: "https://images.xxapi.cn/images/acg/pc/t019e416757e3068bd0.jpg"
tags:
  - 编程
  - 教程
  - 提示词
  - 每日分享
  - AI生成
category: "教程"
---

# 2026年10月20日 AI编程技巧

## 今日概要

The sources provide information on AI programming tools like Cursor and GitHub Copilot, highlighting their features and use cases. Cursor, integrated with VS Code, offers code prediction and AI-assisted coding through natural language queries, enhancing development efficiency. GitHub Copilot, on the other hand, is integrated into Office 365 and Edge for broader applications like document writing. The sources suggest Cursor is more suited for coding scenarios due to its context understanding and AI-driven code generation and optimization features.

---

### 1. Cursor AI 编程实战-总篇 附提示词代码

Title: Cursor AI 编程实战-总篇 附提示词代码
# Cursor AI 编程实战-总篇 附提示词代码. ## Cursor AI 编程实战：用 Prompt 与 Rules 把「能用」变成「好用」. > **摘要**：AI 辅助编程常见痛点是幻觉、风格漂移与上下文理解浅。本文从团队内部实践提炼出一套可复用方法：**输出质量 ≈ 结构化 Prompt + 项目级 Rules**。文中给出可直接复制的大段提示词模板、`.mdc` 规则写法与第三方对接案例流程。文中涉及公司内部框架与坐标已做**脱敏**（以 `com.yourorg.platform`、`Platform*`、`platform-*` 等代替），读者请按自身技术栈替换。. **关键词**：Cursor、Prompt Engineering、Cursor Rules、AI 编程、软件工程. **连载与文件**：同一内容另有 **三篇拆分稿**（便于 CSDN 分开发布）：`CSDN分篇-01-Prompt与案例总结.md`、`CSDN分篇-02-Rules与分层上-Adapter-App.md`、`CSDN分篇-03-Domain-Infrastructure-策略全文.md`。第四节内的短代码块已标为 **速查 A–E**，避免与 **附录 E**（Adapter/App 全文）、**附录 F**（Domain/Infrastructure/策略全文）混淆。. **Cursor 输出质量 ≈ 精确、可执行的 Prompt + 有效、可继承的 Rule 约束**. 下文分两部分：**Prompt 工程化**与 **Rules 体系化**，并附完整可复制片段（已脱敏）。. #### 2.1 三层架构：目标 → 背景 → 要求. 2.   **背景**：业务约束、技术栈、文档路径、相关模块。. 3.   **要求**：步骤拆解、禁止项、输出格式、质量检查点。. #### 2.2 延伸学习. #### 3.1 技术方案生成. # 技术方案生成 Cursor 提示词. - 需求文档已明确定义了功能改动和业务需求，文档路径为：/docs/prd/*_prd.md. #### 3. ## 3. ## 4. ## 6. ### 6.3 对象设计. # 代码生成 Cursor 提示词. - 需求文档已明确定义业务需求和功能规格，文档路径为：/docs/prd/*_prd.md. 路径：**Cursor Settings → Rules → User Rules**。作用所有项目。. 以下将企业内部 Maven 坐标、Starter 命名、二方搜索组件版本线及事务注解等，统一替换为 **`com.yourorg.platform.*`、`platform-*`、`platform-v2`、`PlatformTransactional`** 等占位符，便于公开发表；读者落地时请改回各自公司的真实坐标与 API 名称。. #### Adapter 层. *   **文件命名**：以 `*Adapter` 或 `*Controller` 结尾. #### Domain 层. #### Infrastructure 层. *   各层包路径包含层次标识：adapter、app、domain、infrastructure、spi. log.info("开始处理订单，订单号：{}", order.getOrderNo());. log.info("订单处理完成，订单号：{}", order.getOrderNo());. *   Image 37分享复制链接 分享到 QQ 分享到新浪微博 Image 38 Image 39扫一扫. _AI_ _编程_ _实战_：_Cursor_ 避坑指南与高效 _提示词_ 设计. 【_AI_】使用 _Cursor_ 和 _AI_ _编程_ 生成的VUE前端框架. _Cursor_ 黑科技：_AI_ _编程_ _实战_——用 _AI_ 写 _代码_ 的革命性工具. 摘要：本文介绍 _AI_ _编程_ 工具 _Cursor_ 如何变革开发流程。_Cursor_ 结合VSCode功能和 _AI_ 辅助，支持智能补全、自然语言生成 _代码_、跨文件协作等特性。通过构建Vue+SpringBoot用户管理系统案例，展示其快速生成实体类、Repository、Controller的能力，以及自动创建Vue组件和表单的实践。文章还探讨了 _AI_ 重构功能，并分析 _Cursor_ 在提升效率、辅助学习方面的优势，同时指出仍需人工审查生成 _代码_。最后强调 _Cursor_ 作为开发"第二大脑"的价值，为开发者提供高效 _编程_ 新范式. _AI_ _编程_ 工具 _cursor_ _实战_. _Cursor_ 是由Anysphere公司开发的一款 _AI_ _代码_ 编辑器，支持多种 _编程_ 语言如Python、Java和JavaScript。它能够通过自然语言输入自动生成 _代码_，并具备 _代码_ 理解、重构和优化的能力。_Cursor_ 的主要功能包括 _代码_ 提示补全和交互式聊天，后者可以回答问题并自动生成 _代码_。本文介绍了使用cusor开发一个excel合并功能的 _实战_ 情况，全程 _AI_ 工具自动生成，无手写一行 _代码_。. 本文介绍了 _AI_ _编程_ 助手 _Cursor_ 的使用经验和技巧。_Cursor_ 是一款基于GPT模型的智能 _代码_ 编辑器，支持 _代码_ 生成、解释、优化和重构等功能。文章详细讲解了 _Cursor_ 的安装配置、基础使用方法，并提供了项目初始化、_代码_ 调试和学习新技术的 _实战_ 技巧。此外，还分享了与 _AI_ 对话的技巧、_代码_ 审查方法以及分阶段的学习路径建议。作者指出，合理使用 _AI_ _编程_ 助手能显著提高 _编程_ 效率、加速学习过程并提升 _代码_ 质量，但强调 _AI_ 是辅助工具而非替代品。最后展望了 _AI_ _编程_ 的发展趋势，鼓励程序员拥抱 _AI_ 技术以提升自身能力。. 【_Cursor_ 黑科技 _AI_ _编程_ _实战_】. 《_Cursor_ _AI_ _编程_ 工具 _实战_ 指南》摘要： _Cursor_ 是一款智能 _代码_ 编辑器，支持Python等主流语言，提供 _代码_ 生成与自动补全功能。安装需下载对应系统版本，配置环境变量并验证。_AI_ _代码_ 生成 _实战_ 中，应选择合适工具（如Copilot）、编写清晰提示、严格验证生成 _代码_。典型应用包括数据预处理、API开发等场景，需注意 _代码_ 安全性与性能优化。建议结合人工审查，将 _AI_ 生成 _代码_ 纳入规范开发流程。. _Cursor_ _AI_ _编程_ _-_ 详细教程. _Cursor_ 官网：https://www._cursor_.com/ja _Cursor_ 文档：_Cursor_ – Welcome to _Cursor_ _Cursor_ 论坛：Weekly _-_ _Cursor_ _-_ Community Forum。. _提示词_ 工程是优化大语言模型输出的关键技术，其核心原理在于通过结构化指令引导 _AI_ 生成更精准、可控的内容。在 _AI_ _编程_ 领域，高质量的 _提示词_ 能显著提升 _代码_ 生成质量与开发效率。通过定义明确的角色、任务、上下文与输出格式，开发者可以将模糊需求转化为 _AI_ 可执行的精确指令。_cursor_ _-_ prompts仓库系统化地实践了这一理念，它采用场景化分类和社区驱动模式，为 _代码_ 生成、重构、调试等高频开发任务提供了经过优化的 _提示词_ 模板。这些模板不仅降低了使用门槛，更通过工程化整理，帮助开发者将 _AI_ _编程_ 助手从简单的补全工具升级为高效协作的. _cursor_ _实战_ _-_ _-_ _AI_ 生成五子棋游戏案例（零 _代码_）. _cursor_ _编程_ 入门，_Ai_ _编程_ 实践。. _AI_ _编程_ 神器 _Cursor_：_代码_ 生成到重构全解析. _AI_ _编程_ 工具 _Cursor_ 实现自然语言到 _代码_ 的跨越式转换，深度集成GPT _-_ 4等大模型。核心功能包括：1）智能 _代码_ 生成，如通过简单提示创建HTTP服务器；2）上下文感知补全，自动完善数据库查询等 _代码_；3）跨语言支持，一键生成Python/JS/Go等算法实现。实测效率提升40%，支持从原型开发到 _代码_ 重构全流程，重塑"思考优先于编码"的开发者工作模式。_Cursor_ 代表 _编程_ 工具从行级补全到模块级生成的范式跃迁，使开发者更专注于业务逻辑而非实现细节。. _Cursor_ _AI_ _编程_ 效率提升：_提示词_ 工程与 _代码_ 生成工具箱 _实战_. 上一篇： Cursor AI 编程实战（篇三）：Domain、Infrastructure 与策略模式 下一篇： 库存快照报表升级实战：SQL 窗口函数 + 分区管理（MySQL 8.0）.

来源：[https://blog.csdn.net/heyongjin22/article/details/161089480](https://blog.csdn.net/heyongjin22/article/details/161089480)

---

### 2. 掌握提示工程：GitHub Copilot与AI编程助手-CSDN博客

# 掌握提示工程：GitHub Copilot与AI编程助手. 最新推荐文章于 2025-12-09 16:15:28 发布. 于 2025-04-09 11:39:30 发布. CC 4.0 BY-SA版权. 版权声明：本文为博主原创文章，遵循 CC 4.0 BY-SA 版权协议，转载请附上原文出处链接和本声明。. ### 背景简介. 在当今数字化时代，编程和软件开发正变得日益重要。随着人工智能（AI）技术的发展，我们见证了AI在编程领域的应用日益广泛。提示工程（Prompt Engineering）作为一种策略，被用来引导大型语言模型（LLMs）以生成所需的内容。而GitHub Copilot，作为一种AI编程助手，正在改变开发者的日常工作方式。. #### 提示工程的艺术. #### 安全与隐私. #### 自主AI代理与RAG技术. #### GitHub Copilot. GitHub Copilot是AI编程助手领域的佼佼者，提供先进的代码建议、创建和解释能力，显著提高开发者的工作效率。Copilot提供了个人版、企业版和企业版三种订阅模式，以满足不同规模企业的需求。它支持多行函数建议、测试生成加速和敏感代码模式筛选等功能，是开发者不可或缺的工具。. #### 使用案例：编程硬件与电商平台. ### 总结与启发. 提示工程不仅是一门科学，还涉及创造力和直觉。通过结构化的提示设计，我们可以更有效地引导大型语言模型生成所需的输出。GitHub Copilot作为一款AI编程助手，其在AMD和Shopify等公司的成功应用案例，证明了它在提升工作效率和代码质量方面的巨大潜力。对于开发者来说，这不仅仅是一个工具，而是一个改变工作方式的创新力量。. 在未来，随着AI技术的持续进步，我们可以预见，类似GitHub Copilot的工具将在软件开发行业中扮演越来越重要的角色。企业需要明智地处理与这些工具相关的安全和隐私问题，同时要拥抱多样性与包容性，以确保在AI辅助编程的浪潮中保持领先地位。. *AI**编程**助手*入门指南：*GitHub* *Copilot*、Cursor*与*Claude的安装*与*基础使用. *AI**编程**助手*入门指南：*GitHub* *Copilot*、Cursor*与*Claude的安装*与*基础使用. 从*GitHub*\_Trending/sy/system\_prompts\_leaks学*AI**协作**:**提示词*设计*与*团队... *GitHub*\_Trending/sy/system\_prompts\_leaks是一个收集各类*AI*系统*提示词**(*SystemPrompts*)*的开源项目,涵盖了Anthropic、Open*AI*、Google等多家知名*AI*公司的产品*提示词*。这些*提示词*是*AI*工具的"操作手册",直接影响*AI*的行为和输出质量。 项目结构清晰,主要分为以下几个目录*:* Anthropic/*:* 包含. 【*GitHub*项目推荐--*AI* *助手**提示词*库】【转载】\_*github* *提示词*-CSDN... 或许,你*与*高效使用 *AI* 之间只差一个优质的 Prompt*(**提示词**)*。今天要介绍的*GitHub*开源项目 - Awesome ChatGPT Prompts,正是解决这个痛点的利器。 01 这个项目是什么来头? 由土耳其开发者 Fatih Kadir Akın 发起的AwesomeChatGPT Prompts项目,目前已在 *GitHub* 获得超过12万星标。 它系统整理了 160+ 经过验证的优... *AI**编程**助手*：从*GitHub* *Copilot*到代码*生成*优化. *GitHub* *Copilot*是由*GitHub*和Open*AI*联合开发的一款*AI**编程**助手*，它基于Open*AI*的Codex模型，通过分析大量的开源代码进行训练，能够理解代码的上下文和逻辑，为开发者提供智能的代码补全、函数*生成*、文档注释等建议。表格示例：*GitHub* *Copilot*核心功能功能描述代码补全根据当前代码的上下文，自动补全代码片段函数*生成*根据开发者输入的函数名或描述，自动*生成*函数的实现文档注释*生成*根据函数的名称和参数，自动*生成*文档字符串，帮助维护代码文档代码优化建议。. *GitHub* *Copilot*：*AI**编程**助手*的架构演进*与*真实世界影响. *GitHub*\_Trending/sy/system\_prompts\_leaks项目资源整合*:*打造个人*AI*提 ... *GitHub*\_Trending/sy/system\_prompts\_leaks是一个开源的*AI*系统*提示词*集合项目,包含了Anthropic、Open*AI*、Google等主流*AI*服务商的最新*提示词*模板。项目采用分类化目录结构,将*提示词*按*AI*厂商、功能类型和应用场景进行三维组织,确保用户能够快速定位所需资源。 核心价值 ... *AI**提示词**Github*开源项目集合目录\_*ai**提示词*教程开源仓库. 仓库链接*:* https*:*//*github*.com/Agenta-*AI*/agenta 描述*:* 一个面向LLM开发者的开源平台,集成了*提示词*管理、评估和部署功能,支持快速迭代。 特点*:* 全栈式工具,强调*工程*化应用,适合团队*协作*。 PromptBench 仓库链接*:* https*:*//*github*.com/microsoft/PromptBench ... 5分钟上手*GitHub* *Copilot*：*AI**编程**助手*实战指南. *GitHub* *Copilot*显著减少了重复编码工作，但其核心价值是作为“智能*助手*”而非“替代者”。合理利用*AI*工具，结合开发者自身经验，才能实现效率最大化。尝试一下，在评论区分享你的*Copilot*使用体验吧！. *AI**编程**助手*横向评测：*GitHub* *Copilot* vs CodeWhisperer vs Cursor. *AI**编程**助手*对比测评：*GitHub* *Copilot*、CodeWhisperer和Cursor在软件测试领域的应用表现。文章从测试脚本*生成*、数据构造和持续集成三个维度，对三大工具进行深度评估。结果显示：*Copilot*在测试框架支持上表现最佳，CodeWhisperer*与*AWS云服务集成最优，Cursor则擅长通过自然语言交互*生成*测试用例。针对不同团队需求给出选型建议，并预测未来*AI*测试工具将向用例自愈、数据治理等方向发展，测试*工程*师需转向更高阶的质量策略设计工作。. *AI*代码*生成*工具：*GitHub* *Copilot*、Tabnine*与*Cursor实战指南. 嗨，欢迎来到我的 CSDN 博客小天地！一名深耕多年的技术发烧友。在这里，我将把日常工作中积累的宝贵经验，从复杂架构设计的精妙之处，到代码优化的实战技巧，毫无保留地分享给大家。. *AI*代码*生成*工具：*GitHub* *Copilot*、Tabnine*与*Cursor实战指南. *AI**编程*辅助工具实战指南：*GitHub* *Copilot*、Cursor和Trae的深度对比*与*应用. *AI**编程*辅助工具是将人工智能技术*与**编程*环境相结合的工具，它们能够理解代码的逻辑和结构，提供实时的代码补全、*生成*、错误修复和优化建议。这些工具极大地提高了开发效率，减少了重复性工作，帮助开发者专注于更有创意和价值的开发任务。. 探索*AI**编程*新时代：*GitHub* *Copilot*如何重塑开发者工作效率. *GitHub* *Copilot*以其非凡的*AI*支持，在提高代码质量和开发效率方面展现出巨大的潜力。在*编程*的各个领域，从Web开发到数据科学，再到教育培训，*Copilot*都是开发者不可或缺的强力*助手*。在这个*AI*赋能的新时代，开发者应充分利用技术赋予的便利，加速创新，让*编程*更简单、更有趣。未来已经到来，让我们共同见证并拥抱这一变化。. Awesome *GitHub* *Copilot*：超级定制化*AI**编程**助手*工具集. 团队规范：针对特定技术和编码实践的团队指令项目专用：*增强**GitHub* *Copilot*在特定项目中的行为表现自动应用：安装后自动应用于*Copilot*行为角色专用模式：如Azure架构师、*安全*专家、代码审查员等专用模式工具集成：集成代码库、终端命令、测试工具等多种开发工具上下文感知：为特定任务和工作流提供*增强*的上下文感知协助。. 软件*工程**AI**编程*工具对比分析：*GitHub* *Copilot*、Codeium*与*Tabnine在代码*生成*、补全及*协作*中的应用*与*优势综述. *AI**编程*工具如*GitHub* *Copilot*、Codeium和Tabnine应运而生，它们通过智能代码*生成*、补全、错误检测等功能，大幅提升了*编程*效率和代码质量。*GitHub* *Copilot*以其强大的代码*生成*能力和广泛的*编程*语言支持著称，适用于追求... 【软件开发领域】*AI*...

来源：[https://blog.csdn.net/weixin_29050829/article/details/147119600](https://blog.csdn.net/weixin_29050829/article/details/147119600)

---

### 3. Cursor和copilot哪个好用 Cursor怎么写提示词-Cursor中文网站

Title: Cursor和copilot哪个好用 Cursor怎么写提示词-Cursor中文网站
发布时间：2026/05/25 09:50:36. **软件版本：**Cursor 1.1.3. 随着AI技术的发展，很多程序员借助AI辅助编程提高开发效率，Cursor和Copilot都是非常优秀的辅助编程工具。不少用户在纠结选择使用哪一款作为自己的“主力”工具。如果选择使用Cursor，应该怎么编写提示词呢？本文将为大家介绍Cursor和Copilot哪个好用，Cursor怎么写提示词的相关内容。. Cursor和Copilot是两款不同的AI工具，两者都是依靠AI大模型提供辅助，但是集成方式、使用场景等不同，在编程场景，我更推荐大家使用Cursor。下面我就详细为大家介绍一下二者的区别。. Cursor基于VS Code开发的代码编辑器，可以直接编辑代码工程，并且支持从VS Code导入配置，如果你是前端开发工程师，那么Cursor更适合你，因为是在原来开发的基础上，引入了AI辅助的场景，操作流程、调试方式、快捷键使用几乎相同，可以无感切换到Cursor做开发。. Copilot是微软推出的AI工具，主要集成到Office 365系列产品和Edge浏览器，一般用于协助编写Word文档等场景，对于开发场景，可以使用对话功能，发送代码让Copilot分析，无法直接在编写代码时提供预测。. Cursor具备上下文理解能力，能理解整个项目的代码，适合用于编写代码或者重构项目。按下Tab键能保留预测的代码，AI对话模式能直接生成代码文件，在Java开发时，Controller层编写的接口，能自动生成service、mapper等文件，极大提高开发效率。. Cursor内置AI聊天界面，可以以“自然语言”的形式询问代码错误、请求建议等。按下快捷键【CMD+K】可以快速调出AI聊天界面，可以根据语言描述检索代码工程，找出需要修改的代码块，并且给出高质量的代码，按下【CMD+Y】即可保留Cursor生成的代码。. 在代码开发场景，Cursor表现得更加智能、专业、好用，上文着重介绍了Cursor的代码预测与AI对话编写代码的两个功能点，这是Copilot不具备的功能，所以如果你想要使用一款开发工具提升开发效率，那么Cursor是更好用的一款。. 在编写复杂逻辑时，我们可以选中相关代码块，按下快捷键【CMD+K】并输入提示词（如“优化这段代码”），Cursor即可调用AI功能优化代码。例如下面这段计算两数之和的代码中，原本使用了变量接收计算后的结果最终返回，优化后直接返回两数之和，代码更加简洁，省去了很多不必要的内存占用。代码中的红色底表示Cursor即将删除的行，绿色为Cursor编写的代码行，按下【CMD+Y】即可保留Cursor修改意见。. 如果不知道代码写在哪里，我们可以按下【CMD+L】打开AI聊天功能，并且在此处编写提示词描述功能需求，Cursor可以检索当前代码工程内所有的文件，按下【CMD+Y】接受Cursor的修改意见。例如下图所示，在任意界面调出AI聊天功能，提示词是【请帮我把button界面的介绍删除】，Cursor会检索工程内的代码段，并将其删除。. 以上就是Cursor和Copilot哪个好用，Cursor怎么写提示词的相关内容。在编程开发场景，Cursor相比于Copilot，支持代码预测以及AI对话辅助编程，能大幅提高开发效率。并且本文还为大家介绍了Cursor编写提示词的两种方式，希望对你有所帮助。.

来源：[https://www.cursorcn.com/jiaocheng/cur-wohcnd.html](https://www.cursorcn.com/jiaocheng/cur-wohcnd.html)

---

### 4. Vibe Coding提示词生成器 - Cursor和Copilot的AI编程提示词 | NxCode

Title: Vibe Coding提示词生成器 - Cursor和Copilot的AI编程提示词 | NxCode
# AI编程提示词生成器. 描述您的应用想法，我们将为您喜爱的AI编程工具生成完美的提示词。支持Cursor、Copilot、Claude、Bolt.new等。. ## 1选择您的AI编程工具. ## 2描述您的应用想法. ## 3添加关键功能(可选). ## 4选择技术栈(可选). ### Vibe Coding 技巧. ## 什么是Vibe Coding？. Vibe Coding是一种软件开发技术，您用自然语言描述想要构建的内容，AI工具为您生成代码。它被柯林斯词典评为2025年度词汇，彻底改变了开发者和非开发者构建软件的方式。Cursor、GitHub Copilot、Claude和Bolt.new等流行工具让您能在几分钟内从想法变成可运行的代码。. 这个免费的提示词生成器帮助您为任何AI编程工具创建优化的提示词。只需描述您的应用想法，选择您喜欢的工具，即可获得结构完美的提示词，帮助您从AI编程助手获得更好的结果。. ### Related Tools. Compare top AI coding toolsApp Cost Calculator. Estimate development costsNo-Code 可行性检测器. Check if no-code works for you. ## Related Tools. 🪙AI Token Calculator🤖AI Model Comparison⚡AI Builder Cost Comparison📊AI Agent ROI Calculator.

来源：[https://www.nxcode.io/zh/tools/vibe-coding-prompt-generator](https://www.nxcode.io/zh/tools/vibe-coding-prompt-generator)

---

### 5. GitHub - Omnls/system-prompts-and-models-of-ai-tools-chinese: AI编程工具中文提示词合集，包含Cursor、Antigravity、VSCode Agent等多种AI编程工具的提示词，为中文开发者提供AI辅助编程参考资源。持续更新中文编程Rules和最新AI编程提示词。 · GitHub

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

