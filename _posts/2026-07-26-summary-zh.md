---
layout: default
title: "Horizon Summary: 2026-07-26 (ZH)"
date: 2026-07-26
lang: zh
---

> 从 13 条内容中筛选出 10 条重要资讯。

---

1. [vLLM v0.26.0 发布：新增 Inkling 模型及 DeepSeek-V4 优化](#item-1) ⭐️ 8.0/10
2. [Ruff v0.16.0 将默认 lint 规则扩展至 413 条](#item-2) ⭐️ 7.0/10
3. [清华与腾讯提出树状 Rollout 降低大模型后训练成本](#item-3) ⭐️ 7.0/10
4. [Claude Opus 5 以一半价格实现 Fable 级性能](#item-4) ⭐️ 7.0/10
5. [开源框架利用 Claude AI 自动化求职申请](#item-5) ⭐️ 6.0/10
6. [供人类与 AI 代理并行的浏览器 Ego-Lite](#item-6) ⭐️ 5.0/10
7. [OmniRoute：集成 290+服务商的免费 MIT 许可 AI 网关](#item-7) ⭐️ 5.0/10
8. [开源机器人吸尘器 OOMWOO 在 GitHub 上获得关注](#item-8) ⭐️ 5.0/10
9. [block/buzz：面向人类与 AI 的开源蜂巢思维平台](#item-9) ⭐️ 4.0/10
10. [Orca：管理并行编程代理的 TypeScript 工具](#item-10) ⭐️ 4.0/10

---

<a id="item-1"></a>
## [vLLM v0.26.0 发布：新增 Inkling 模型及 DeepSeek-V4 优化](https://github.com/vllm-project/vllm/releases/tag/v0.26.0) ⭐️ 8.0/10

vLLM v0.26.0 发布，新增对 Inkling 多模态 MoE 模型系列的支持，针对 DeepSeek-V4 在多种硬件上的性能优化（例如专用路由内核和融合 top-k 偏置内核），以及通过 head_dtype 选项使用 fp32 lm_head 以提升准确性；还带来了灵活的注意力后端按 KV 缓存组选择、成熟的 KV 缓存卸载至二级存储、以及扩展的 Rust 前端和多模态功能。 这些改进使 vLLM 更快、更准确，并能支持更多类型的模型，为 DeepSeek-V4 等新一代稀疏模型和 Inkling 等多模态模型的大规模推理降低延迟、提升吞吐量，对 LLM 服务社区具有重要意义。 值得关注的技术细节：专用 DeepSeek-V4 路由内核带来 2.94%端到端 TPOT 提升，fused_topk_bias 内核实现 1.5-2 倍加速，以及通过 head_dtype 选项使用 fp32 lm_head；注意力后端可按 KV 缓存组选择；KV 缓存卸载支持对象存储二级层并具备数据并行副本感知能力。

github · khluu · 7月25日 10:38

**背景**: vLLM 是一个高性能开源 LLM 推理引擎，广泛用于部署大型语言模型。推测性解码通过并行生成候选令牌进行加速。Hopper 是 NVIDIA 专为 AI 设计的 GPU 架构（H100/H200）。DeepSeek-V4 是一个大型稀疏混合专家语言模型，Inkling 是由 Thinking Machines Lab 开发的总参数 975B 的多模态 MoE 模型。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.baseten.co/library/inkling/">Inkling | Model library</a></li>
<li><a href="https://thinkingmachines.ai/news/introducing-inkling/">Inkling : Our Open-Weights Model - Thinking Machines Lab</a></li>
<li><a href="https://arxiv.org/html/2603.05451v1">FlashAttention-4: Algorithm and Kernel Pipelining Co-Design for Asymmetric Hardware Scaling</a></li>

</ul>
</details>

**标签**: `#LLM serving`, `#open-source`, `#vLLM`, `#performance optimization`, `#release`

---

<a id="item-2"></a>
## [Ruff v0.16.0 将默认 lint 规则扩展至 413 条](https://simonwillison.net/2026/Jul/25/ruff/#atom-everything) ⭐️ 7.0/10

Ruff v0.16.0 于 7 月 23 日发布，将默认 lint 规则从 59 条增加到 413 条。新默认规则可捕获语法错误和即时运行时错误等严重问题。 该更新导致依赖未固定版本的 Ruff 的项目在 CI 中大量失败，但通过提前捕获更多问题，显著提升了代码质量。作为广泛使用的 Python lint 工具，这一变更影响众多开发者，推动提高编码标准。 自 v0.1.0 上次调整默认规则集以来，Ruff 规则总数从 708 增至 968，许多新默认规则可检测严重 bug。lint 输出可供开发者和自动化编程代理使用，并提供自动修复功能。

rss · Simon Willison · 7月25日 22:44

**背景**: Ruff 是一个用 Rust 编写的高性能 Python 代码检查与格式化工具，由近期被 OpenAI 收购的 Astral 开发。代码检查工具能在运行前静态分析代码，发现潜在错误和风格问题。默认规则集指无需配置即启用的检查项，此前仅保守启用 59 条，此次扩充至 413 条以提升开箱即用的代码质量。

**标签**: `#python`, `#linting`, `#developer-tools`, `#ci-cd`, `#ruff`

---

<a id="item-3"></a>
## [清华与腾讯提出树状 Rollout 降低大模型后训练成本](https://mp.weixin.qq.com/s?__biz=MzIzNjc1NzUzMw==&mid=2247907199&idx=3&sn=db62b221aeb50a9dfff1af69803b2787) ⭐️ 7.0/10

清华大学与腾讯提出一种新式 Rollout 方法，将智能体轨迹视为树结构，动态分配计算预算而非平均分摊到提示词，从而降低大语言模型后训练的高昂成本。 大模型后训练（尤其是智能体模型）计算开销极大；这种树状方法有望大幅削减训练成本，让小型团队也能负担先进 AI 开发，并加速高性价比 AI 智能体的落地。 该方法将智能体轨迹视为分支树而非平坦序列，能选择性扩展高价值路径，避免在无潜力的分支上浪费算力——其思想类似于将蒙特卡洛树搜索应用于 RLHF 或 GRPO 训练流程。

rss · 量子位 · 7月25日 04:40

**背景**: 在大模型后训练中，“Rollout”指从提示词生成的响应或动作序列，常用于强化学习（如 RLHF、GRPO）提供训练信号。对于语言智能体，轨迹可能跨越多次工具交互。传统 Rollout 为每个提示词分配均等算力，而树状 Rollout 在不同分支间共享计算、剪枝低潜力路径，从而提升效率——类似于棋类游戏中的树搜索。清华与腾讯的这项工作专门针对智能体轨迹，其中的决策点自然形成树结构。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2605.02913">[2605.02913] Generate, Filter, Control, Replay: A Comprehensive Survey of Rollout Strategies for LLM Reinforcement Learning</a></li>
<li><a href="https://min.news/en/tech/eea6d780b18a13830bdf969bfad174b4.html">Alibaba AutoNavi proposes Tree -GRPO to efficiently solve the problem...</a></li>

</ul>
</details>

**标签**: `#LLM`, `#post-training`, `#cost-efficiency`, `#agent-trajectory`, `#rollout`

---

<a id="item-4"></a>
## [Claude Opus 5 以一半价格实现 Fable 级性能](https://www.latent.space/p/ainews-claude-opus-5-fable-level) ⭐️ 7.0/10

Anthropic 发布了 Claude Opus 5，这一蒸馏模型据称性能比肩旗舰 Fable 系列，但价格仅为其一半。 这一突破大幅降低了获取前沿 AI 的成本，使更多开发者和企业能够负担得起高性能模型。 Opus 5 通过模型蒸馏技术实现 Fable 级性能，以现有 Opus 级别定价（Fable 一半的价格）提供同等能力。

rss · Latent Space · 7月25日 07:25

**背景**: Anthropic 的 Claude 模型包含多个层级；Opus 通常兼顾性能与成本，而 Fable 是能力最强但价格昂贵的模型。模型蒸馏将 Fable 等大模型的知识迁移到 Opus 5 等小模型，在保持性能的同时降低推理成本。该技术已被广泛用于创建高效、可部署的模型。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://fable5.io/">Fable 5 AI — Independent Model Guide & Prompt Workspace</a></li>
<li><a href="https://en.wikipedia.org/wiki/Model_distillation">Model distillation</a></li>

</ul>
</details>

**标签**: `#Anthropic`, `#Claude`, `#model-distillation`, `#AI-model-release`, `#pricing`

---

<a id="item-5"></a>
## [开源框架利用 Claude AI 自动化求职申请](https://github.com/MadsLorentzen/ai-job-search) ⭐️ 6.0/10

新的开源 TypeScript 框架 MadsLorentzen/ai-job-search 利用 Claude AI 自动调整简历、撰写求职信并评估职位匹配度。 该工具可以大幅缩短求职申请时间，但如果被广泛采用，也会引发关于招聘真实性和公平性的担忧。 基于 Claude Code 构建，用户 Fork 仓库并填写个人资料，AI 即可处理后续工作。使用 TypeScript 编写，除集成外无内在技术新颖性。

ossinsight · MadsLorentzen · 7月26日 01:27

**背景**: Claude 是 Anthropic 开发的大型语言模型系列，以其对安全性和宪法式人工智能的关注而闻名。Claude Code 是一种代理编码工具，可以理解代码库、编辑文件并运行命令，因此适合自动执行求职申请等复杂工作流。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Claude_(AI)">Claude (AI)</a></li>
<li><a href="https://claude.com/product/claude-code">Claude Code by Anthropic | AI Coding Agent, Terminal, IDE</a></li>

</ul>
</details>

**标签**: `#AI`, `#job-search`, `#automation`, `#TypeScript`, `#Claude`

---

<a id="item-6"></a>
## [供人类与 AI 代理并行的浏览器 Ego-Lite](https://github.com/citrolabs/ego-lite) ⭐️ 5.0/10

Citro Labs 开源了 ego-lite，一款基于 Chromium 的桌面浏览器，使人类用户和 AI 代理能在同一浏览器中并行工作，代理在隔离的 Spaces 中运行。 该工具降低了将 AI 代理融入日常网络任务的门槛，有望简化工作流，让代理自动执行数据收集、表单填写等浏览器操作，而用户继续正常浏览。 ego-lite 支持任何 AI 代理（如 Claude Code、Cursor），并保持登录会话，允许代理访问需要认证的网站。它使用 JavaScript 开发，遵循 MIT 许可证，完全开源。

ossinsight · citrolabs · 7月26日 01:27

**背景**: 随着 AI 代理自主网络交互能力增强，它们通常依赖无头浏览器或自动化框架。ego-lite 提供了一个共享的可视化浏览器，代理在独立的标签页或 Spaces 中工作，用户可监控和控制操作，利用现有浏览器会话和凭证，而不影响个人标签页。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://lite.ego.app/">Fastest Browser for AI Agents to Run Web Automation | ego ( lite )</a></li>
<li><a href="https://www.everydev.ai/tools/ego-lite">ego ( lite ) - Browser for AI Agents | EveryDev.ai</a></li>
<li><a href="https://git.hubp.de/citrolabs/ego-lite">GitHub - citrolabs/ ego - lite : The best browser for both you and your AI...</a></li>

</ul>
</details>

**标签**: `#browser`, `#AI agents`, `#parallel work`, `#JavaScript`, `#open-source`

---

<a id="item-7"></a>
## [OmniRoute：集成 290+服务商的免费 MIT 许可 AI 网关](https://github.com/diegosouzapw/OmniRoute) ⭐️ 5.0/10

新推出了一款名为 OmniRoute 的开源 AI 网关，采用 MIT 许可证，通过单一端点统一接入 290 多家 AI 服务商和 500 多个模型，并具备自动故障转移和节省 token 的压缩功能。 OmniRoute 简化了与多个 AI 服务的集成，降低了开发者的成本和复杂性。其 token 压缩技术（RTK 和 Caveman）可大幅降低 API 使用开销，使 AI 更易用且高效。 该网关支持 Claude Code、Cursor 和 Copilot 等流行编程工具，并包含基于配额的自动故障转移以防服务中断。RTK 压缩可将命令输出 token 减少 60-90%，而 Caveman 压缩则以语义方式缩减上下文而不丢失含义。

ossinsight · diegosouzapw · 7月26日 01:27

**背景**: AI 网关是路由请求到不同 AI 模型提供商的中间件，提供统一 API。token 压缩至关重要，因为 LLM 按 token 收费，减少 token 数量直接降低成本。RTK（Rust Token Killer）是一个基于 Rust 的工具，用于过滤和压缩命令行输出以用于 LLM。Caveman 压缩是一种剥离可预测语法、仅保留关键事实内容的方法。Agent2Agent（A2A）协议允许不同 AI 代理进行通信和协作。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://dashen-tech.com/en/dev-tools/rtk-token-killer-guide-2026/">RTK Complete Guide: Rust-Powered LLM Token Compression Tool...</a></li>
<li><a href="https://github.com/wilpel/caveman-compression">GitHub - wilpel/caveman-compression: Caveman Compression is a semantic compression method for LLM contexts. It removes predictable grammar while preserving the unpredictable, factual content that defines meaning. · GitHub</a></li>
<li><a href="https://a2a-protocol.org/latest/">A 2 A Protocol</a></li>

</ul>
</details>

**标签**: `#AI`, `#gateway`, `#open-source`, `#API`, `#TypeScript`

---

<a id="item-8"></a>
## [开源机器人吸尘器 OOMWOO 在 GitHub 上获得关注](https://github.com/makerspet/oomwoo) ⭐️ 5.0/10

makerspet/oomwoo 开源吸尘器机器人项目在单日内获得了 6 颗星，表明社区兴趣正在上升。 该项目通过提供开源、可自制的替代方案，使机器人吸尘器技术大众化，让用户能够定制和维修自己的设备。 OOMWOO 采用 Python 实现，具有模块化设计，包括激光雷达、吸风扇和可接触的 I/O 板，便于爱好者和开发者上手。

ossinsight · makerspet · 7月26日 01:27

**背景**: 像 OOMWOO 这样的开源硬件项目使爱好者能够构建和修改通常由专有技术主导的设备，从而促进创新并降低成本。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://oomwoo.com/">OOMWOO — the open-source robot vacuum you build yourself</a></li>
<li><a href="https://github.com/makerspet/oomwoo/">GitHub - makerspet/ oomwoo : Open-source vacuum robot cleaner</a></li>

</ul>
</details>

**标签**: `#open-source`, `#robotics`, `#python`, `#vacuum-cleaner`, `#iot`

---

<a id="item-9"></a>
## [block/buzz：面向人类与 AI 的开源蜂巢思维平台](https://github.com/block/buzz) ⭐️ 4.0/10

Block 公司发布了基于 Rust 的开源平台 block/buzz，让人类与 AI 代理在共享工作空间中协作，过去 24 小时内在 GitHub 上获得了 12 颗星。 它反映了将 AI 代理作为积极协作者而非被动工具的趋势，可能重新塑造团队工作和决策的方式。 该平台可自行托管，被描述为“蜂巢思维”通信工具，过去一天内有 31 次推送和 1 个拉取请求，表明开发活跃。

ossinsight · block · 7月26日 01:27

**背景**: Block（前身为 Square）一直开源 AI 工具如 Goose；Buzz 创建了一个人类与 AI 代理共享房间的工作空间，体现了集体智能的概念。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://block.xyz/inside/introducing-buzz-where-humans-and-agents-work-together">Block - Introducing Buzz: where humans and agents work together</a></li>
<li><a href="https://github.com/block/buzz">GitHub - block/buzz: A hive mind communication platform · GitHub</a></li>
<li><a href="https://stacker.news/items/1529631">buzz: A hive mind communication platform - Block \ stacker news</a></li>

</ul>
</details>

**社区讨论**: 在 Stacker News 上，一些用户将 Buzz 视为早期项目的继承者，称赞其可自行托管的设计和 AI 代理与人类共享空间的新颖方法。

**标签**: `#rust`, `#communication`, `#p2p`, `#platform`

---

<a id="item-10"></a>
## [Orca：管理并行编程代理的 TypeScript 工具](https://github.com/stablyai/orca) ⭐️ 4.0/10

StablyAI 发布了 orca，一个基于 TypeScript 的工具，允许开发者在桌面和移动平台上同时运行和编排多组并行编程代理。 orca 进入了编程代理编排这一新兴领域，提供了跨平台的代理管理能力，但由于社区采用率低，目前影响有限。 orca 用 TypeScript 开发，自称 ADE（可能指代理开发环境），支持用户使用自己的订阅运行代理。该仓库在 24 小时内获得 6 颗星和 53 次推送，表明开发活跃但关注度低。

ossinsight · stablyai · 7月26日 01:27

**背景**: ADE 通常指应用开发环境，但在此处可能意为代理开发环境。并行编程代理是指多个 AI 代理同时处理编码任务，开发者则充当编排者。这种多代理方法因能高效处理复杂代码库而日益流行。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.pcmag.com/encyclopedia/term/ade">Definition of ADE | PCMag</a></li>
<li><a href="https://addyosmani.com/blog/code-agent-orchestra/">AddyOsmani.com - The Code Agent Orchestra - what makes multi-agent coding work</a></li>

</ul>
</details>

**标签**: `#ai-agents`, `#developer-tools`, `#typescript`, `#open-source`, `#agent-orchestration`

---