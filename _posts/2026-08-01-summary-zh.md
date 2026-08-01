---
layout: default
title: "Horizon Summary: 2026-08-01 (ZH)"
date: 2026-08-01
lang: zh
---

> 从 17 条内容中筛选出 11 条重要资讯。

---

1. [十年前的物理 AI 论文获 SIGGRAPH 时间检验奖](#item-1) ⭐️ 9.0/10
2. [DeepSeek V4 Flash 0731：304B 参数、增强代理能力的语言模型](#item-2) ⭐️ 8.0/10
3. [无状态 MCP 2.0 重新点燃兴趣，推出 mcp-explorer 和 datasette-mcp](#item-3) ⭐️ 8.0/10
4. [Oxide and Friends 播客与 Simon Willison 讨论开放权重 AI 革命](#item-4) ⭐️ 8.0/10
5. [smevals：一个评估 AI 模型的小型测试套件](#item-5) ⭐️ 7.0/10
6. [Datasette Agent 0.4a0 引入 browser_task 机制，支持浏览器内执行 JavaScript](#item-6) ⭐️ 7.0/10
7. [GPT-5.6 价格下调 20%-80%：递归自优化使成本四个月内降 13 倍](#item-7) ⭐️ 7.0/10
8. [Simon Willison 发布 llm-mcp-client 0.1a0 早期 alpha 版本](#item-8) ⭐️ 5.0/10
9. [StablyAI 推出 Orca：管理并行编码代理舰队](#item-9) ⭐️ 5.0/10
10. [YC 软件发布多人协作 AI 智能体框架 QM](#item-10) ⭐️ 3.0/10
11. [Block 推出 Buzz：基于 Rust 的蜂巢思维通信平台](#item-11) ⭐️ 3.0/10

---

<a id="item-1"></a>
## [十年前的物理 AI 论文获 SIGGRAPH 时间检验奖](https://mp.weixin.qq.com/s?__biz=MzIzNjc1NzUzMw==&mid=2247908730&idx=2&sn=0b3a81693cb5f92800c95b7fc50939f1) ⭐️ 9.0/10

一篇十多年前的研究论文因在物理 AI 领域的开创性工作获得 SIGGRAPH 时间检验奖，该工作整合了全身控制与灵巧手操作。其开源实现在 GitHub 上已获得 8000 多颗星。 该奖项凸显了早期物理 AI 在当今机器人领域的基础性作用，其中灵巧操作是一项关键挑战。它证实了使用物理仿真训练机器人的长期愿景，这一趋势如今已成为物理 AI 运动的核心。 该研究解决了在物理仿真中协调机器人身体运动与灵巧手动作的问题，使二者能够联合训练。其开源代码库获得了社区广泛支持，表明在实际机器人中具有应用潜力。

rss · 量子位 · 7月31日 06:32

**背景**: SIGGRAPH 是计算机图形学和交互技术的顶级会议，其时间检验奖表彰发表超过十年仍持续产生重大影响的论文。物理 AI 指的是利用物理仿真为虚拟角色或机器人生成逼真行为的方法，如今已成为机器人实际部署前训练的关键手段。灵巧手操作涉及机器人用多指手执行复杂任务，需要精细的运动控制。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.163.com/dy/article/L369OJTE0511DSSR.html">SIGGRAPH 时 间 检 验 奖 揭晓：这项研究，提前十年押中了物理AI</a></li>
<li><a href="https://segmentfault.com/a/1190000046737330">aiera... - SegmentFault 思否</a></li>
<li><a href="https://m.21jingji.com/article/20260702/herald/3b0f90de7e671df4aec070bbf2b75c3d.html">踩着 物 理 AI 的风口，Momenta冲刺IPO - 21财经</a></li>

</ul>
</details>

**标签**: `#SIGGRAPH`, `#Test of Time Award`, `#Physics AI`, `#Robotics`, `#Open Source`

---

<a id="item-2"></a>
## [DeepSeek V4 Flash 0731：304B 参数、增强代理能力的语言模型](https://simonwillison.net/2026/Jul/31/deepseek-v4-flash-0731/#atom-everything) ⭐️ 8.0/10

DeepSeek 发布了 V4 Flash 0731，这是一款拥有 3040 亿参数的模型，大幅增强了代理能力，据 Artificial Analysis 评估，其智能性价比领先。 它目前在 LLMs 中提供了最佳的智能性价比，通过大幅降低成本同时保持高性能，可能使先进 AI 能力的获取更加普及。 该模型定价为每百万输入 tokens 0.14 美元、输出 0.27 美元，模型体量 167GB，在成本效率上超越了更大的对手，如 428B 的 MiniMax M3。不过，图像生成质量可能取决于推理努力级别。

rss · Simon Willison · 7月31日 23:59

**背景**: 代理能力指 AI 自主规划和执行任务的能力。Artificial Analysis 智能指数对模型进行多项基准测试，帕累托线展示了智能与成本的最佳平衡。MiniMax M3 是中国 AI 公司 MiniMax 推出的竞争性大语言模型。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.ibm.com/think/topics/agentic-ai">What is Agentic AI? | IBM</a></li>
<li><a href="https://en.wikipedia.org/wiki/MiniMax_M3">MiniMax M3</a></li>

</ul>
</details>

**标签**: `#AI`, `#Large Language Models`, `#DeepSeek`, `#Agentic Capabilities`, `#Machine Learning`

---

<a id="item-3"></a>
## [无状态 MCP 2.0 重新点燃兴趣，推出 mcp-explorer 和 datasette-mcp](https://simonwillison.net/2026/Jul/31/stateless-mcp/#atom-everything) ⭐️ 8.0/10

2026 年 7 月 28 日，模型上下文协议（MCP）2.0 规范引入了无状态模式，将工具调用简化为单个 HTTP 请求，无需会话管理。受此启发，Simon Willison 发布了用于探测 MCP 服务器的命令行工具 mcp-explorer，以及新的 Datasette MCP 服务器 datasette-mcp。 与赋予代理 shell 访问权限相比，无状态 MCP 降低了安全风险，并减少了实现复杂性，使 LLM 代理工具更易于审计、扩展，且能与较小模型配合。Willison 的工具和对 MCP 的重新倡导可能会加速社区在生产系统中采用 MCP。 无状态 MCP 使用单个 POST 请求，通过 MCP-Protocol-Version 和 Mcp-Method 等头部传递信息，客户端信息嵌入请求体的`_meta`字段。mcp-explorer 是一个用于交互式列举和调用工具的 CLI 工具，而 datasette-mcp 则将 Datasette 作为 MCP 工具服务器暴露。

rss · Simon Willison · 7月31日 23:13

**背景**: MCP 是 Anthropic 制定的开放标准，定义了 LLM 驱动代理访问外部工具的方式。原状态化版本需要两步握手建立会话才能调用工具，增加了开销和扩展难度。虽然 Skills（为代理提供终端和 curl 访问）因其灵活性而流行，但安全顾虑使人们重新关注 MCP 可审计的细粒度工具控制。

**标签**: `#MCP`, `#stateless`, `#LLM agents`, `#tools`, `#specification`

---

<a id="item-4"></a>
## [Oxide and Friends 播客与 Simon Willison 讨论开放权重 AI 革命](https://simonwillison.net/2026/Jul/31/oxide-and-friends/#atom-everything) ⭐️ 8.0/10

2026 年 7 月 31 日发布的这期播客邀请了 Simon Willison，回顾了前一周的动荡事件，包括 Kimi K3 证明开放权重模型能与闭源模型匹敌、意外的网络安全攻击，以及一份由多位 AI 领袖签署的关于开放权重模型的公开信，而 Anthropic 明显缺席。 这场讨论突显了开放权重模型正在快速缩小与闭源系统的差距，加剧了关于 AI 政策、国家安全和行业领导权的辩论，这些将影响 AI 未来的发展和可及性。 这期播客在发布时已显过时，因为仅在几天后就出现了 DeepSeek V4 Flash 0731 和 Anthropic 自身的网络安全事件，突显了 AI 发展的惊人速度。节目中跑题讨论了从 Golden Gate Claude 到野生火鸡攻击和铅-犯罪假说等各种话题。

rss · Simon Willison · 7月31日 21:33

**背景**: 开放权重模型公开其训练得到的权重，允许任何人下载并在自己的基础设施上运行，这与仅通过 API 访问的专有模型不同。Kimi K3 是中国公司月之暗面（Moonshot AI）开发的 2.8 万亿参数模型，于 2026 年 7 月达到前沿性能。政策争论的焦点在于 Anthropic 警告的独裁政权滥用风险与开放权重促进 AI 创新民主化之间的权衡。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://hai.stanford.edu/ai-definitions/what-is-an-open-weight-model">What is an Open-Weight Model? - Stanford HAI</a></li>
<li><a href="https://www.anthropic.com/news/position-open-weights-models">Our position on open-weights models \ Anthropic</a></li>
<li><a href="https://en.wikipedia.org/wiki/Kimi_K3">Kimi K3</a></li>

</ul>
</details>

**标签**: `#AI`, `#open weight models`, `#podcast`, `#AI policy`, `#machine learning`

---

<a id="item-5"></a>
## [smevals：一个评估 AI 模型的小型测试套件](https://simonwillison.net/2026/Jul/31/smevals/#atom-everything) ⭐️ 7.0/10

Prime Radiant 开源了 smevals，一个用于创建和运行小型评估套件的工具，可比较不同 AI 模型的配置，包括提示和测试框架。 这为复杂的评估框架提供了一个实用、轻量级的替代方案，让开发者和研究人员能快速评估模型在特定任务上的表现。 smevals 使用 YAML 配置文件定义评估，将运行与评分分离，并支持通过 Web 服务器或静态 HTML 报告查看结果。它定义了术语：评估、任务、配置、运行、评分器、检查和自定义检查脚本。

rss · Simon Willison · 7月31日 21:15

**背景**: 评估框架用于系统地测试 AI 模型的能力。`uvx` 是 uv Python 包管理器中的一个命令，可以无需显式安装即运行 Python 工具。Prime Radiant 是由 Jesse Vincent 创办的实用 AI 研究实验室。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://simonwillison.net/2026/Jul/31/smevals/">smevals—a small eval suite for evaluating models, prompts ...</a></li>
<li><a href="https://docs.astral.sh/uv/getting-started/installation/">uv is an extremely fast Python package and project manager, written in...</a></li>

</ul>
</details>

**标签**: `#AI evaluation`, `#LLM`, `#tooling`, `#open-source`, `#testing`

---

<a id="item-6"></a>
## [Datasette Agent 0.4a0 引入 browser_task 机制，支持浏览器内执行 JavaScript](https://simonwillison.net/2026/Jul/31/datasette-agent/#atom-everything) ⭐️ 7.0/10

Datasette Agent 的 0.4a0 版本新增了 `await context.browser_task()` 机制，使得代理工具能够直接在用户浏览器中运行自定义 JavaScript 代码。 这扩展了 Datasette Agent 的能力，使其能进行浏览器端动态交互（如 DOM 操作、调用客户端 API），对于 LLM 工具调用工作流和基于浏览器的代理具有重要意义。 该功能通过工具插件中的 `await context.browser_task()` 调用，目前处于 alpha 阶段，因此稳定性和文档可能有限。

rss · Simon Willison · 7月31日 14:14

**背景**: Datasette Agent 是一个基于大语言模型的 Datasette 助手，采用工具调用模式，通过生成 SQL 回答问题。新增的 browser_task 机制允许插件在浏览器中运行 JavaScript，将服务端代理逻辑与客户端交互连接起来。LLM 工具调用是一种让模型调用外部函数的设计模式，虽然已有 agent-browser 等浏览器自动化工具，但此功能直接集成到了 Datasette 生态中。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://agent.datasette.io/">Datasette Agent : an AI assistant for Datasette to help explore and...</a></li>
<li><a href="https://github.com/datasette/datasette-agent">GitHub - datasette/ datasette - agent : An LLM-powered agent for...</a></li>
<li><a href="https://medium.com/@yasir_siddique/tool-calling-for-llms-a-detailed-tutorial-a2b4d78633e2">Tool Calling for LLMs: A Detailed Tutorial - Medium</a></li>

</ul>
</details>

**标签**: `#datasette`, `#llm-tool-use`, `#agent`, `#browser`, `#release`

---

<a id="item-7"></a>
## [GPT-5.6 价格下调 20%-80%：递归自优化使成本四个月内降 13 倍](https://www.latent.space/p/ainews-gpt-56-price-cut-by-20-80) ⭐️ 7.0/10

OpenAI 将 GPT-5.6 的价格下调了 20%至 80%，而达到 GPT-5.4 级别智能的成本在短短四个月内下降了 13 倍，据报道这得益于包括蒸馏在内的递归自优化技术。 如此大幅的成本降低可能使先进 AI 的获取更加民主化，让初创公司和研究人员能够更广泛地采用，同时表明通过自动化改进循环，AI 模型正迅速变得更便宜、更高效。 此次降价适用于 GPT-5.6，13 倍的提升是相对于 GPT-5.4 智能的成本而言的。具体的递归自优化方法可能涉及知识蒸馏，即让较小的模型从较大的教师模型那里学习。

rss · Latent Space · 7月31日 04:40

**背景**: 人工智能中的递归自改进是指系统能够优化自身算法或后继者，可能带来快速的能力提升。在机器学习中，蒸馏是一种技术，通过训练一个紧凑的“学生”模型来模仿大型“教师”模型，从而降低推理成本并保持性能。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Recursive_self-improvement">Recursive self-improvement - Wikipedia</a></li>
<li><a href="https://cacm.acm.org/news/is-recursive-self-improvement-really-here/">Is Recursive Self-Improvement Really Here?</a></li>

</ul>
</details>

**标签**: `#AI`, `#Distillation`, `#Cost Reduction`, `#Large Language Models`, `#Self-Optimization`

---

<a id="item-8"></a>
## [Simon Willison 发布 llm-mcp-client 0.1a0 早期 alpha 版本](https://simonwillison.net/2026/Jul/31/llm-mcp-client/#atom-everything) ⭐️ 5.0/10

Simon Willison 发布了 llm-mcp-client 0.1a0，这是一个早期的 alpha 客户端，将模型上下文协议（MCP）与大型语言模型（LLM）集成，通过标准化方式连接外部工具和数据源。 该版本使开发者能更轻松地构建利用 MCP 的 AI 应用，有望加速该协议在不同 LLM 生态系统中的采用，并简化与外部系统的集成。 作为 alpha 版本，该客户端可能尚不稳定，主要用于实验；详细使用信息可参考链接的博客文章。

rss · Simon Willison · 7月31日 23:03

**背景**: 模型上下文协议（MCP）是由 Anthropic 于 2024 年 11 月推出的开放标准，旨在标准化 LLM 连接外部数据和工具的方式。该协议随后被 OpenAI 和 Google DeepMind 等主要 AI 提供商采用。Simon Willison 是一位知名开发者，以其在 Datasette 以及 LLM 和数据生态系统中的其他工具而闻名。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Model_Context_Protocol">Model Context Protocol</a></li>
<li><a href="https://modelcontextprotocol.io/docs/getting-started/intro">What is the Model Context Protocol (MCP)? - Model Context Protocol</a></li>

</ul>
</details>

**标签**: `#llm`, `#model-context-protocol`, `#mcp`, `#tools`, `#release`

---

<a id="item-9"></a>
## [StablyAI 推出 Orca：管理并行编码代理舰队](https://github.com/stablyai/orca) ⭐️ 5.0/10

StablyAI 的 Orca 是一个新的 TypeScript 应用程序，使开发者能够在桌面和移动平台上编排和管理并行的编码代理舰队。 它允许用户使用自己的订阅同时运行多个编码 AI 代理，可能提升处理复杂多代理任务的开发者的生产力。随着 AI 辅助编码成为主流，代理编排工具的重要性日益增加。 Orca 被描述为支持任何编码代理的代理开发环境（ADE）。它使用 TypeScript 构建，在过去 24 小时内有 45 次代码推送和 1 个拉取请求，尽管星标数较低，但显示开发活跃。

ossinsight · stablyai · 8月1日 01:28

**背景**: 多代理系统涉及多个 AI 代理并行工作以更高效地完成任务。像 GitHub Copilot 或自主编码器这样的编码代理可以组合处理项目的不同方面。Orca 似乎简化了跨设备管理这类代理的过程。

**标签**: `#TypeScript`, `#AI Agents`, `#Agent Orchestration`, `#Developer Tools`, `#Multi-Agent Systems`

---

<a id="item-10"></a>
## [YC 软件发布多人协作 AI 智能体框架 QM](https://github.com/yc-software/qm) ⭐️ 3.0/10

来自 YC 软件的开源项目 QM 在 GitHub 上出现，提供了一个多人智能体框架，让团队能够在隔离的工作空间中与 AI 智能体协作。该项目在过去 24 小时内获得了 6 颗星，表明早期关注。 该项目代表了企业环境中协作式 AI 的转变，允许多个人类用户和智能体在限定记忆和权限下一起工作。其开源、模型无关的方法减少了供应商锁定，并可能降低初创公司在日常工作中采用 AI 智能体的门槛。 QM 为每个员工提供隔离的工作区，并支持多种 AI 后端，包括 Pi、OpenCode、Codex 和 Claude Code。它具有限定范围的记忆、文件、密钥链、权限、计划任务、Web 应用和持久沙箱，并以开源形式发布以便定制。

ossinsight · yc-software · 8月1日 01:28

**背景**: 智能体框架（Agent Harness）是管理大语言模型（LLM）工具使用、记忆和执行环境的软件基础设施，使其能够作为自主智能体运行。与单智能体设置不同，多人框架在共享上下文中协调多个用户和智能体，通常具有隔离和协作功能。这一概念类似于 Microsoft Agent Framework，但侧重于基于团队的 AI 交互。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/yc-software/qm">GitHub - yc-software/qm: Multiplayer agent harness for work · GitHub</a></li>
<li><a href="https://www.startuphub.ai/ai-news/artificial-intelligence/2026/yc-qm-agent-harness-a-collaborative-ai-shift">YC QM Agent Harness: A Collaborative AI Shift | StartupHub.ai</a></li>
<li><a href="https://en.wikipedia.org/wiki/Agent_harness">Agent harness - Wikipedia</a></li>

</ul>
</details>

**标签**: `#TypeScript`, `#multiplayer`, `#agent`, `#harness`, `#low-activity`

---

<a id="item-11"></a>
## [Block 推出 Buzz：基于 Rust 的蜂巢思维通信平台](https://github.com/block/buzz) ⭐️ 3.0/10

Block 公司开源了名为 Buzz 的“蜂巢思维通信平台”，该项目使用 Rust 语言编写，近期在 GitHub 上获得了 5 个星标。该平台包含一个 Tauri 桌面客户端和一个以代理（Agent）为先的命令行界面，其桌面版本于 2026 年 7 月中旬达到 v0.4.24。 Buzz 代表了对基于 Nostr 协议、可供人类与 AI 代理共同使用的自托管协作工作空间的重要探索。这可能会影响开源社区和组织构建安全、可互操作的通信工具的方式。 Buzz 采用 Apache 2.0 许可证，使用中继服务器架构来存储和索引已签名的 Nostr 事件，并支持通过桌面客户端、工作流和命令行工具进行连接。该项目大量使用 Rust 语言，其中继组件开发活跃，近期还包含了智能 HTTP 的 Git 修复。

ossinsight · block · 8月1日 01:28

**背景**: “蜂巢思维”平台旨在促进集体智能和通信，通常用于分布式群体。Nostr 是一个去中心化社交协议，使用加密密钥和中继器，具有抗审查特性。Block 公司（前身为 Square）是一家专注于金融服务和开源开发的技术公司。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/block/buzz">GitHub - block/buzz: A hive mind communication platform</a></li>
<li><a href="https://www.explainx.ai/blog/block-buzz-nostr-agent-workspace-humans-agents-july-2026">Block Buzz — Nostr Agent Workspace (2026) | explainx.ai Blog</a></li>
<li><a href="https://essamamdani.com/blog/block-buzz-self-hosted-agent-workspace-guide-2026">Block Buzz: The Self-Hosted Workspace Where AI Agents Are ...</a></li>

</ul>
</details>

**标签**: `#communication`, `#rust`, `#platform`, `#open-source`

---