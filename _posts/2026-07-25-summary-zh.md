---
layout: default
title: "Horizon Summary: 2026-07-25 (ZH)"
date: 2026-07-25
lang: zh
---

> 从 14 条内容中筛选出 11 条重要资讯。

---

1. [sglang v0.5.16 发布：DSpark 推测解码与 Inkling 多模态 MoE 支持](#item-1) ⭐️ 9.0/10
2. [黑森林实验室发布 FLUX 3 多模态模型，性能超越 Seedance 2.0 等主流模型](#item-2) ⭐️ 9.0/10
3. [Anthropic 发布 Claude Opus 5：深思熟虑、主动且成本减半的模型](#item-3) ⭐️ 8.0/10
4. [AMD 能否打破 CUDA 护城河？AMD Advancing AI 2026](#item-4) ⭐️ 8.0/10
5. [微信 WeLM 617B MoE 提出隐式扩展路径，或为 AI 第三条扩展定律](#item-5) ⭐️ 7.0/10
6. [有状态与无状态智能体设计权衡概览](#item-6) ⭐️ 5.0/10
7. [新型 JavaScript 浏览器支持人类与 AI 智能体并行使用](#item-7) ⭐️ 5.0/10
8. [video-shotcraft: 面向 Remotion 的 AI 镜头配方库](#item-8) ⭐️ 5.0/10
9. [OmniRoute 免费网关：聚合 160+AI 提供商，引入令牌压缩](#item-9) ⭐️ 5.0/10
10. [基于 Claude Code 的 AI 驱动求职框架](#item-10) ⭐️ 5.0/10
11. [Block 的 Rust 通信平台 Buzz 在 GitHub 上走红，单日获星 12 颗](#item-11) ⭐️ 3.0/10

---

<a id="item-1"></a>
## [sglang v0.5.16 发布：DSpark 推测解码与 Inkling 多模态 MoE 支持](https://github.com/sgl-project/sglang/releases/tag/v0.5.16) ⭐️ 9.0/10

sglang v0.5.16 引入了 DSpark——一种置信度驱动的推测解码算法，在 DeepSeek-V4-Pro 上达到 383.7 tok/s，并新增了对 Inkling 的支持，这是一个 9750 亿参数的多模态混合专家模型，拥有 100 万 token 上下文，在 Blackwell GPU 上实现高达 171.0 tok/s 的解码速度。 DSpark 通过自适应调度验证显著提高了推理吞吐量，而 Inkling 的支持则能够服务于具有超长上下文的大规模多模态模型。这些进步推动了大型语言模型推理效率的边界，并扩展了 sglang 面向下一代 AI 工作负载的能力。 DSpark 以块为单位半自回归地生成草稿，并根据草稿的置信度调整验证窗口大小。Inkling 混合了滑动窗口、全注意力和 Mamba2 线性注意力，并包含 NVFP4 MoE 及可选的视觉/音频塔。其他改进包括 GLM-5.2 DSA 缓存层分割将每 rank 的 KV 内存减少 74%，以及 ReplaySSM 推测解码的内存占用减少 6.4 倍。

github · Qiaolin-Yu · 7月25日 00:13

**背景**: 推测解码通过使用小型草稿模型提出多个 token，然后由大型目标模型并行验证，从而加速大型语言模型推理。混合专家（MoE）模型每个 token 只激活一部分专家子网络，从而实现庞大的参数量但计算量适中。NVIDIA Blackwell 是最新的 GPU 架构，专为 AI 工作负载设计，相比前代产品有显著的性能提升。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2607.05147">[2607.05147] DSpark: Confidence-Scheduled Speculative Decoding with Semi-Autoregressive Generation</a></li>
<li><a href="https://thinkingmachines.ai/news/introducing-inkling/">Inkling: Our Open-Weights Model - Thinking Machines Lab</a></li>
<li><a href="https://en.wikipedia.org/wiki/Blackwell_(microarchitecture)">Blackwell (microarchitecture) - Wikipedia</a></li>

</ul>
</details>

**标签**: `#sglang`, `#speculative-decoding`, `#llm-inference`, `#multimodal`, `#inference-optimization`

---

<a id="item-2"></a>
## [黑森林实验室发布 FLUX 3 多模态模型，性能超越 Seedance 2.0 等主流模型](https://www.latent.space/p/ainews-black-forest-labs-flux-3-multimodal) ⭐️ 9.0/10

黑森林实验室发布了 FLUX 3 多模态流模型，可联合学习图像、视频和音频，据称性能超越了 Seedance 2.0、Gemini Omni 和 Grok Imagine。此外还推出了机器人视频动作模型 FLUX-mimic。 这一成就使黑森林实验室在多模态人工智能领域占据领先地位，有望加速视频生成、机器人和世界模型的应用，并加剧与谷歌、字节跳动等巨头的竞争。 FLUX 3 基于 Self-Flow 架构，使用数千万小时通用视频和数十万小时操作视频训练，可从文本提示生成图像或最长 20 秒的带音频视频，目前处于早期访问阶段。

rss · Latent Space · 7月24日 04:30

**背景**: 多模态流模型可学习跨数据类型的统一表征。Seedance 2.0 是字节跳动的逼真文本转视频模型；Gemini Omni 是谷歌的多模态模型；Grok Imagine 是 xAI 的图像生成模型。黑森林实验室此前发布了 FLUX 图像生成模型，FLUX 3 则扩展到了视频和音频领域。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://bfl.ai/blog/flux-3">FLUX 3 - Real World Models: Towards Multimodal Flow Models as the ...</a></li>
<li><a href="https://venturebeat.com/technology/black-forest-labs-launches-flux-3-capable-of-generating-images-and-20-second-video-with-audio-but-in-limited-release-to-start">Black Forest Labs launches FLUX 3 capable of generating images and 20-second video with audio — but in limited release to start | VentureBeat</a></li>
<li><a href="https://en.wikipedia.org/wiki/Seedance_2.0">Seedance 2.0</a></li>

</ul>
</details>

**标签**: `#multimodal`, `#AI models`, `#flow models`, `#computer vision`, `#generative AI`

---

<a id="item-3"></a>
## [Anthropic 发布 Claude Opus 5：深思熟虑、主动且成本减半的模型](https://simonwillison.net/2026/Jul/24/introducing-claude-opus-5/#atom-everything) ⭐️ 8.0/10

Anthropic 发布了新模型 Claude Opus 5，它既深思熟虑又积极主动，以一半的价格达到了接近前沿模型 Claude Fable 5 的智能水平，目前位居 Artificial Analysis 排行榜首位。 该模型将成本降至前沿模型 Fable 5 的一半，使先进 AI 能力更容易获取，同时引入主动推理和更好的网络安全漏洞检测能力，有望为更广泛的应用场景普及尖端 AI。 Claude Opus 5 的价格与其前代 Opus 4.8 相同，并提供一个成本翻倍的“快速模式”。它展现了显著的主动性，例如在无法直接查看图纸的情况下，自行构建计算机视觉管道来重建 3D 模型。此外，根据其系统卡，它不易受到提示注入攻击。

rss · Simon Willison · 7月24日 23:48

**背景**: Anthropic 是一家人工智能研究公司，以其 Claude 系列大型语言模型闻名。Claude Fable 5 是最新的前沿模型，性能顶尖但成本较高。Opus 系列模型则定位为更经济的替代方案。Artificial Analysis 排行榜是一个广泛引用的基准，用于比较 LLM 的性能和价格。提示注入是一种安全漏洞，攻击者在用户输入中嵌入恶意指令以操纵模型行为。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/spaces/ArtificialAnalysis/LLM-Performance-Leaderboard">LLM Performance Leaderboard - a Hugging Face Space by ArtificialAnalysis</a></li>
<li><a href="https://en.wikipedia.org/wiki/Claude_Fable_5">Claude Fable 5</a></li>
<li><a href="https://www.anthropic.com/claude/fable">Claude Fable \ Anthropic</a></li>

</ul>
</details>

**社区讨论**: Simon Willison 表示尚未测试但反响积极。Boris Cherny 强调，根据系统卡显示，Opus 5 是目前最不易被提示注入的模型，这与主动性和安全性改进相符。人们对它的性能和高性价比感到兴奋，但对其漏洞检测能力提升而未训练利用的问题也持谨慎态度。

**标签**: `#AI`, `#Claude`, `#Anthropic`, `#LLM`, `#model release`

---

<a id="item-4"></a>
## [AMD 能否打破 CUDA 护城河？AMD Advancing AI 2026](https://newsletter.semianalysis.com/p/can-amd-break-the-cuda-moat-amd-advancing) ⭐️ 8.0/10

AMD 通过代理核生成自动化 GPU 内核优化，并提供高达 105% 的金融工程折扣来挑战英伟达 CUDA 的统治地位，但面临内部开发集群不稳定和下一代 Helios MI455X 系统生产爬坡的困境。 如果成功，AMD 的多管齐下的策略可以多样化 AI 加速器市场、降低成本并减少对英伟达专有 CUDA 生态系统的依赖；然而，持续的软硬件障碍可能会延迟企业广泛采用。 代理核生成使用大语言模型自动编写和优化 GPU 内核，可能缩小与 CUDA 的软件差距；Helios MI455X 每个机架配备 72 个 GPU 和 31 TB HBM4 内存，但生产爬坡问题可能影响交付时间；AMD 的“高达 105% 的折扣”可能涉及捆绑、回扣或融资激励，而不仅仅是降价。

rss · Semianalysis · 7月25日 00:33

**背景**: 英伟达的 CUDA 是已成为 AI 开发事实标准的并行计算平台，形成了将开发者锁定在英伟达硬件上的“护城河”。AMD 的 ROCm 软件栈历来难以匹敌 CUDA 的成熟度和库生态系统。代理核生成是一种新兴的 AI 技术，可自动创建高度优化的 GPU 代码，这可能帮助 AMD 快速改善软件兼容性和性能。Helios MI455X 是 AMD 即将推出的机架级 AI 系统，专为大规模训练和推理设计。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://cuda-agent.github.io/">CUDA Agent | Large-Scale Agentic RL for CUDA Kernel Generation</a></li>
<li><a href="https://www.amd.com/en/blogs/2026/amd-launches-helios-the-highest-performing-rackscale-ai-infrastructure-solution.html">AMD Launches Helios™: The Highest Performing Rackscale AI ...</a></li>

</ul>
</details>

**标签**: `#AMD`, `#CUDA`, `#AI hardware`, `#software optimization`, `#competitive analysis`

---

<a id="item-5"></a>
## [微信 WeLM 617B MoE 提出隐式扩展路径，或为 AI 第三条扩展定律](https://mp.weixin.qq.com/s?__biz=MzI3MTA0MTk1MA==&mid=2652714734&idx=1&sn=7e98659aa2ab44778c0d5587a1aa8a84) ⭐️ 7.0/10

微信 AI 团队为其 6170 亿参数 MoE 模型 WeLM 提出了一种新颖的“隐式扩展”方法，声称这代表了 AI 的第三条扩展定律，超越了模型规模和数据扩展的范畴。 这可能重塑大语言模型的扩展方式，在不单纯增加参数或数据的情况下提升性能，为更高效、更强大的 AI 系统开辟道路。 该方法利用 MoE 架构和隐式计算，可能通过将推理步骤直接嵌入序列来实现；但信息来自新闻聚合平台，并非正式论文，细节有限。

rss · 新智元 · 7月24日 04:33

**背景**: Mixture-of-Experts（MoE）将模型拆分为多个专门的“专家”子模型，各自处理不同输入，从而在相似计算量下使用更多参数。经典的扩展定律（如 Kaplan 等，2020）表明，模型性能随模型大小、数据集大小和计算量的增加而可预测地提升。所谓的“第三条扩展定律”可能指推理时的扩展或推理步骤数量的扩展。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Mixture_of_experts">Mixture of experts - Wikipedia</a></li>
<li><a href="https://arxiv.org/abs/2001.08361">[2001.08361] Scaling Laws for Neural Language Models - arXiv.org Revisiting Scaling Laws for Language Models: The Role of Data ... Scaling Law Of Language Models - Towards Data Science New Approach to Scaling Laws Could Change How AI Models Are ... Densing law of LLMs - Nature Machine Intelligence Temporal Scaling Law for Large Language Models</a></li>

</ul>
</details>

**标签**: `#large-language-models`, `#mixture-of-experts`, `#scaling-laws`, `#AI-research`, `#WeChat`

---

<a id="item-6"></a>
## [有状态与无状态智能体设计权衡概览](https://machinelearningmastery.com/stateful-vs-stateless-agent-design-tradeoffs-for-scalable-agentic-systems/) ⭐️ 5.0/10

一篇新的入门文章阐述了有状态与无状态智能体设计的核心权衡，重点关注状态管理如何影响可扩展性和部署。 随着 AI 智能体变得更加自主且被广泛部署，有状态与无状态设计之间的选择直接影响系统的可扩展性、可靠性和运维复杂性。 有状态智能体在交互过程中保持持久记忆和上下文，支持个性化和长时间运行的任务；而无状态智能体独立处理每个请求，简化了扩展和故障恢复。

rss · Machine Learning Mastery · 7月24日 12:44

**背景**: AI 智能体系统是基于大语言模型的自主、目标导向程序。状态管理——即智能体是否记住过去的交互——是影响可扩展性、可靠性和实现复杂性的基础设计决策。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/AI_agent">AI agent - Wikipedia</a></li>
<li><a href="https://www.letta.com/blog/stateful-agents">Stateful Agents: The Missing Link in LLM Intelligence | Letta</a></li>
<li><a href="https://avahi.ai/glossary/stateless-agent-design/">What is Stateless Agent Design in AI?</a></li>

</ul>
</details>

**标签**: `#agentic-systems`, `#software-architecture`, `#state-management`, `#scalability`, `#ai-engineering`

---

<a id="item-7"></a>
## [新型 JavaScript 浏览器支持人类与 AI 智能体并行使用](https://github.com/citrolabs/ego-lite) ⭐️ 5.0/10

GitHub 仓库 citrolabs/ego-lite 成为趋势项目，提出了一个基于 JavaScript 的浏览器，旨在支持人类和 AI 智能体同时使用。 这样的浏览器可以简化 AI 智能体辅助完成网页任务时的人类工作流程，在同一会话中操作，可能减少在不同浏览器实例之间切换的上下文开销。 该仓库处于早期阶段，使用 JavaScript 编写，目前缺乏详细的技术文档，其实现方法尚不明确。

ossinsight · citrolabs · 7月25日 01:24

**背景**: AI 浏览器智能体是能够自动浏览网页、填写表单和抓取数据的工具，通常作为单独的扩展或无头浏览器运行。像 hydro13/tandem-browser 这样的“协作”浏览器将 AI 直接嵌入到相同的浏览器环境中，与人类用户共享标签页、Cookie 和会话。ego-lite 似乎也旨在提供类似的共享浏览体验。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/hydro13/tandem-browser">hydro13/tandem-browser: AI-Human symbiotic browser - GitHub</a></li>
<li><a href="https://www.firecrawl.dev/blog/best-browser-agents">11 Best AI Browser Agents in 2026 - firecrawl.dev</a></li>

</ul>
</details>

**标签**: `#browser`, `#AI agents`, `#JavaScript`, `#developer tools`, `#early-stage`

---

<a id="item-8"></a>
## [video-shotcraft: 面向 Remotion 的 AI 镜头配方库](https://github.com/Vincentwei1021/video-shotcraft) ⭐️ 5.0/10

Vincentwei1021 的 video-shotcraft 仓库提供了 106 个镜头配方卡和 161 个动态预览，作为一个模板用于使用 Remotion 创建电影级产品视频，并明确设计为与 Claude Code 和 Codex 等 AI 编码工具配合使用。 该集成简化了 AI 辅助视频制作，使开发者和内容创作者无需深入了解 Remotion 即可快速生成复杂的动画和镜头，可能降低程序化视频创作的门槛。 该模板已可用于生产，使用 TypeScript 编写，但采用度有限（24 小时内 7 颗星），表明仍处于早期关注阶段。它利用 Remotion 基于 React 和服务器端渲染视频的能力，AI 编码助手可以将镜头配方作为上下文来生成视频代码。

ossinsight · Vincentwei1021 · 7月25日 01:24

**背景**: Remotion 是一个开源框架，允许开发者使用 React 和 CSS、Canvas、WebGL 等网络技术以编程方式创建视频。Claude Code 和 Codex 是 AI 驱动的编码助手；来自 Anthropic 的 Claude Code 和来自 OpenAI 的 Codex 可以理解自然语言提示和代码上下文来生成或编辑代码。该仓库充当桥梁，提供结构化的‘镜头配方’，供这些 AI 工具用于组合视频序列。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://grokipedia.com/page/Remotion">Remotion</a></li>
<li><a href="https://www.remotion.dev/docs/ai/">Building with Remotion and AI | Remotion | Make videos programmatically</a></li>
<li><a href="https://grokipedia.com/page/Claude_Code">Claude Code</a></li>

</ul>
</details>

**标签**: `#AI`, `#video-generation`, `#Remotion`, `#Claude-Code`, `#Codex`

---

<a id="item-9"></a>
## [OmniRoute 免费网关：聚合 160+AI 提供商，引入令牌压缩](https://github.com/diegosouzapw/OmniRoute) ⭐️ 5.0/10

开源项目 OmniRoute 发布，作为一个免费 AI 网关，它通过单一 API 端点聚合了超过 160 个人工智能服务提供商，并采用 RTK 和 Caveman 堆叠压缩技术来节省令牌，同时支持智能自动故障转移。 它简化了开发者集成多种 AI 模型的复杂度并降低了 API 调用成本，其免费层产品尤其降低了使用多样化模型的门槛。 其堆叠压缩声称可节省 15-95%的令牌，但独立基准测试显示 Caveman 仅节省约 8.5%，且 RTK 的压缩效果被系统提示开销部分抵消；此外，它还支持 MCP/A2A 协议、多模态 API，并提供桌面/PWA 界面。

ossinsight · diegosouzapw · 7月25日 01:24

**背景**: AI 网关是集成多个 AI 服务的中间件，提供统一 API 和管理功能。RTK 和 Caveman 等令牌压缩技术通过过滤工具输出来减少输入令牌数，但独立基准测试显示实际节省效果有限。模型上下文协议（MCP）是连接 AI 应用与外部工具的开放标准，而智能体间协议（A2A）则用于不同 AI 智能体之间的通信。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.ibm.com/think/topics/ai-gateway">What is an AI gateway? - IBM</a></li>
<li><a href="https://github.com/mikeruhl/rtk-vs-caveman/blob/main/RESULTS.md">rtk-vs-caveman/RESULTS.md at main · mikeruhl/rtk-vs-caveman</a></li>
<li><a href="https://modelcontextprotocol.io/">What is the Model Context Protocol ( MCP )? - Model Context Protocol</a></li>

</ul>
</details>

**标签**: `#AI Gateway`, `#TypeScript`, `#Free`, `#Open Source`, `#Aggregator`

---

<a id="item-10"></a>
## [基于 Claude Code 的 AI 驱动求职框架](https://github.com/MadsLorentzen/ai-job-search) ⭐️ 5.0/10

新的 TypeScript 框架 MadsLorentzen/ai-job-search 使用 Claude Code 自动化简历定制、求职信撰写和面试准备。 该工具展示了 AI 代理在个人生产力中的实际应用，可能减少求职中的手动工作。 该框架需要用户 fork 仓库并提供个人资料，然后使用 Claude Code 评估职位并生成定制申请材料。

ossinsight · MadsLorentzen · 7月25日 01:24

**背景**: Claude Code 是 Anthropic 开发的 AI 编程助手，能理解和修改代码库。该框架利用 Claude Code 的能力自动化求职任务，代表了 AI 个人生产力工具的日益增长趋势。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Claude_Code">Claude Code</a></li>
<li><a href="https://claude.com/product/claude-code">Claude Code by Anthropic | AI Coding Agent, Terminal, IDE</a></li>

</ul>
</details>

**标签**: `#AI`, `#job-search`, `#automation`, `#TypeScript`, `#Claude`

---

<a id="item-11"></a>
## [Block 的 Rust 通信平台 Buzz 在 GitHub 上走红，单日获星 12 颗](https://github.com/block/buzz) ⭐️ 3.0/10

名为'block/buzz'的 GitHub 仓库在过去 24 小时内获得了 12 颗星标，该项目被描述为'一个蜂巢思维通信平台'，由 Block 公司开发，基于 Rust 语言。 该项目可能代表了一种利用集体智能的新型通信范式，而 Block 采用 Rust 进行开发则凸显了该语言在构建可扩展平台方面的成熟度，这可能会吸引更多开发者探索类似架构。 仓库显示有 31 次代码推送和 1 个开放的拉取请求，表明开发活跃，但项目描述极少，具体功能尚不明确。

ossinsight · block · 7月25日 01:24

**背景**: Block 公司以其 Square 支付系统和 Cash App 等产品闻名，此前已开源了多个 Rust 项目，例如'core'和'librdkafka'。'蜂巢思维'一词通常指集体智慧，这暗示该平台可能支持群组通信或协作决策。

**标签**: `#rust`, `#communication-platform`, `#open-source`, `#block`

---