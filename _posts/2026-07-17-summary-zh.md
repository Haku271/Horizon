---
layout: default
title: "Horizon Summary: 2026-07-17 (ZH)"
date: 2026-07-17
lang: zh
---

> 从 14 条内容中筛选出 9 条重要资讯。

---

1. [Firefox 编译为 WebAssembly 在 Chrome 中运行](#item-1) ⭐️ 8.0/10
2. [Linus Torvalds 声明 Linux 并非反 AI 项目](#item-2) ⭐️ 8.0/10
3. [Thinking Machines Lab 发布 Inkling：975B 参数多模态开放权重模型，采用 Apache 2.0 许可](#item-3) ⭐️ 8.0/10
4. [Kimi K3：月之暗面推出的 2.8 万亿参数开源模型与鹈鹕基准测试](#item-4) ⭐️ 7.0/10
5. [GPT-5.6 Codex 漏洞可导致用户主目录被误删](#item-5) ⭐️ 7.0/10
6. [Lila Sciences 打造数据中心式实验室，旨在革新 AI 驱动发现](#item-6) ⭐️ 7.0/10
7. [WebAssembly 编译的 Mermaid 转彩色 ASCII 艺术工具](#item-7) ⭐️ 6.0/10
8. [OpenAI 官方发布 8 个 ChatGPT 使用技巧](#item-8) ⭐️ 5.0/10
9. [用 Ollama 在 15 分钟内运行本地 AI 模型](#item-9) ⭐️ 5.0/10

---

<a id="item-1"></a>
## [Firefox 编译为 WebAssembly 在 Chrome 中运行](https://simonwillison.net/2026/Jul/16/firefox-in-webassembly/#atom-everything) ⭐️ 8.0/10

Puter 将 Firefox 的 Gecko 引擎编译为 WebAssembly，通过 233MB 的 gecko.wasm 文件和基于代理的网络连接，使整个浏览器在 Chrome 中运行。 该演示突破了 WebAssembly 的极限，证明复杂的桌面级应用程序可以完全在浏览器沙箱中运行，这可能会带来新的跨平台和安全浏览解决方案。 选择 Gecko 是因为其强大的单进程支持。所有网络流量通过 Wisp WebSocket 代理协议经由 Puter 的服务器中转，并支持端到端加密。AI 辅助开发使用了价值约 2.5 万美元的 Claude Opus 和 Fable 代币，但由于订阅计划实际成本较低。

rss · Simon Willison · 7月16日 23:34

**背景**: WebAssembly (Wasm) 是一种可移植的二进制格式，允许用 C/C++ 等语言编写的代码在浏览器中以接近原生的速度运行。Mozilla 的 Gecko 是 Firefox 的布局引擎。由于网页无法打开任意 TCP 连接，该演示使用基于 WebSocket 的代理协议 (Wisp) 来传输网络流量。将像 Gecko 这样庞大的代码库编译为 Wasm 是一项重大的工程壮举，而近期 AI 编码工具的进步使这变得更加可行。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/MercuryWorkshop/wisp-protocol">GitHub - MercuryWorkshop/wisp-protocol: Wisp is a low-overhead, easy to implement protocol for proxying multiple TCP/UDP sockets over a single websocket. · GitHub</a></li>
<li><a href="https://www.anthropic.com/claude/fable">Claude Fable \ Anthropic</a></li>
<li><a href="https://puter.com/">Puter</a></li>

</ul>
</details>

**标签**: `#WebAssembly`, `#Firefox`, `#browser`, `#compilation`, `#WebSocket`

---

<a id="item-2"></a>
## [Linus Torvalds 声明 Linux 并非反 AI 项目](https://simonwillison.net/2026/Jul/16/linus-torvalds/#atom-everything) ⭐️ 8.0/10

Linux 内核最高维护者 Linus Torvalds 在 Linux Media 邮件列表中明确表示，Linux 不是一个反 AI 项目。他宣称 AI 显然是一种有用的工具，并邀请持不同意见者分叉项目或离开。 这一声明直接回应了开源社区中关于 AI 在软件开发中角色的持续争论，树立了重要先例。它表明全球最具影响力的开源项目不会拒绝 AI 的参与，可能影响其他大型项目的相关政策。 Torvalds 承认 AI 的实用性在一年前可能还不那么明确，但如今已毋庸置疑，同时指出关于 AI 的其他问题（如最终的经济影响）仍然存在。该消息发布于 Linux 内核邮件列表上的一次讨论中。

rss · Simon Willison · 7月16日 13:26

**背景**: Linus Torvalds 于 1991 年创建了 Linux，并至今担任其最高维护者，对内核合并内容拥有最终决定权。开源社区对于 AI 生成的代码存在分歧，一些项目因版权或质量问题而禁止使用。分叉（Fork）是开源领域的常见做法，指复制项目并在新领导下独立开发。

**标签**: `#linux`, `#open-source`, `#ai`, `#linus-torvalds`, `#software-development`

---

<a id="item-3"></a>
## [Thinking Machines Lab 发布 Inkling：975B 参数多模态开放权重模型，采用 Apache 2.0 许可](https://www.latent.space/p/ainews-thinkys-inkling-975b-a41b) ⭐️ 8.0/10

由前 OpenAI 首席技术官米拉·穆拉蒂创立的 Thinking Machines Lab 发布了 Inkling，这是一个拥有 9750 亿参数、采用混合专家架构的多模态模型，并基于宽松的 Apache 2.0 许可开放权重，同时计划推出一个较小的 2760 亿参数版本。 该发布标志着美国实验室推出的最大开放权重模型，为中国的开放模型提供了一个强大且可商用的替代方案，增强了美国开源人工智能生态系统。 Inkling 采用混合专家架构，激活参数为 410 亿，使用 45 万亿文本、图像、音频和视频标记进行训练，旨在通过 Tinker 平台作为定制微调的坚实基础，但其训练数据文档较为有限。

rss · Latent Space · 7月16日 06:18

**背景**: 混合专家（MoE）是一种神经网络架构，通过多个专门的子模型（专家）根据不同输入选择性激活，在庞大模型规模下实现更低的每次推理计算量。开放权重模型公开发布训练后的参数，允许任何人使用、微调或部署。Apache 2.0 是一种宽松的开源许可证，允许商业使用、修改和分发。Thinking Machines Lab 由前 OpenAI 首席技术官米拉·穆拉蒂于 2025 年创立。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.ghacks.net/2026/07/16/thinking-machines-lab-releases-inkling-a-975-billion-parameter-open-weights-ai-model-under-apache-2-0/">Thinking Machines Lab Releases Inkling, a 975 Billion Parameter Open Weights AI Model Under Apache 2.0 - gHacks Tech News</a></li>
<li><a href="https://en.wikipedia.org/wiki/Mixture_of_experts">Mixture of experts - Wikipedia</a></li>
<li><a href="https://huggingface.co/blog/moe">Mixture of Experts Explained</a></li>

</ul>
</details>

**标签**: `#open-source`, `#large-language-models`, `#multimodal`, `#AI-release`, `#Apache-2.0`

---

<a id="item-4"></a>
## [Kimi K3：月之暗面推出的 2.8 万亿参数开源模型与鹈鹕基准测试](https://simonwillison.net/2026/Jul/16/kimi-k3/#atom-everything) ⭐️ 7.0/10

月之暗面（Moonshot AI）发布了 Kimi K3，一个拥有 2.8 万亿参数的开源模型，有望于 2026 年 7 月 27 日开放权重。该模型在多项基准测试中表现出色，尤其是在 Arena.ai 前端代码排行榜上位居榜首，不过它也是中国 AI 实验室迄今最昂贵的模型。 作为首个开源 3 万亿参数级别的模型，Kimi K3 标志着开源模型规模的重要里程碑，直接挑战了闭源巨头。其高价表明中国 AI 实验室正开始与西方服务商在高端模型市场直接竞争。 尽管规模庞大，Kimi K3 的推理输出 token 数比前代 K2.6 减少了 21%，但每百万 token 输入 3 美元、输出 15 美元的定价使其成为中国开源模型中最贵的。在 Simon Willison 的鹈鹕骑自行车基准测试中，它生成了细节丰富的 SVG 图片，花费 0.25 美元。

rss · Simon Willison · 7月16日 20:19

**背景**: “鹈鹕骑自行车基准测试”是由开发者 Simon Willison 创立的一个非正式大语言模型测试，要求模型生成一幅鹈鹕骑自行车的 SVG 图像，用以评估其遵循创意指令和编写代码的能力。开源权重模型（如 Kimi K3 承诺的那样）公开其模型参数，允许用户下载和使用，但可能不包括训练数据和代码，这与完全开源的 AI 有所不同。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://grokipedia.com/page/Pelican_on_a_bicycle_AI_benchmark">Pelican on a bicycle (AI benchmark)</a></li>
<li><a href="https://hai.stanford.edu/ai-definitions/what-is-an-open-weight-model">What is an Open-Weight Model? - Stanford HAI</a></li>

</ul>
</details>

**标签**: `#AI`, `#LLM`, `#Open-Source`, `#Moonshot AI`, `#Benchmark`

---

<a id="item-5"></a>
## [GPT-5.6 Codex 漏洞可导致用户主目录被误删](https://simonwillison.net/2026/Jul/16/bad-codex-bug/#atom-everything) ⭐️ 7.0/10

Thibault Sottiaux 报告了 GPT-5.6 Codex 的一个漏洞：在无沙箱保护的情况下运行时，模型在尝试覆盖 $HOME 环境变量时会错误地删除用户的主目录。 该漏洞凸显了编程智能体中一个关键的 AI 安全风险：模型的“无心之失”可能导致不可逆的数据丢失，这强调了在自主软件工程工具中采用沙箱和审查机制的必要性。 该删除行为具体发生在启用“完全访问模式”、关闭自动审查，且模型试图通过修改 $HOME 来设置临时目录，却错误地删除了原始主目录路径的情况下。

rss · Simon Willison · 7月16日 17:45

**背景**: OpenAI Codex 是一套用于自动化软件任务的 AI 编程智能体。$HOME 环境变量在类 Unix 系统中指向用户的个人目录。沙箱是一种安全技术，通过隔离程序来防止其影响主机系统，而在报告的场景中该保护措施缺失。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Sandbox_(computer_security)">Sandbox (computer security) - Wikipedia</a></li>
<li><a href="https://www.baeldung.com/linux/home-variable-user-tilde">Where and How Are the User $HOME Environment Variable and Tilde Set? | Baeldung on Linux</a></li>
<li><a href="https://grokipedia.com/page/OpenAI_Codex">OpenAI Codex</a></li>

</ul>
</details>

**标签**: `#generative-ai`, `#coding-agents`, `#codex`, `#ai-safety`, `#software-engineering`

---

<a id="item-6"></a>
## [Lila Sciences 打造数据中心式实验室，旨在革新 AI 驱动发现](https://www.latent.space/p/the-lab-of-the-future-should-feel) ⭐️ 7.0/10

Lila Sciences 正在构建像数据中心一样运作的自动化实验室，利用机器人和 AI 生成海量科学训练数据，用于生命、化学和材料科学领域的突破。 该模式通过大规模生成高质量实验数据，可大幅加速科学发现，有望彻底改变药物发现和材料设计等领域，标志着向 AI 驱动的研究基础设施转变。 Lila 的实验室被设计为自主、自驱动的环境，AI 模型在其中设计、进行并重新设计实验；该公司定位在 AI、机器人和生命科学的交叉点，但源材料未透露具体技术实现细节。

rss · Latent Space · 7月16日 13:30

**背景**: 自驱动实验室（SDL）是将 AI 与机器人自动化相结合、自主进行实验并做出数据驱动决策的系统，旨在加速科学方法。传统科研常因数据有限且异构而阻碍 AI 模型训练。将实验室视为数据中心的理念，正是为了满足大规模、高质量实验数据的需求以推动 AI 发现。Lila Sciences 位于瑞士，瑞士是制药和生命科学行业的主要中心，拥有诺华和罗氏等公司，这提供了人才和工业需求。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.lila.ai/">LILA | Scientific Superintelligence</a></li>
<li><a href="https://pubs.acs.org/doi/10.1021/acs.chemrev.4c00055">Self-Driving Laboratories for Chemistry and Materials Science | Chemical Reviews</a></li>
<li><a href="https://en.wikipedia.org/wiki/Life_sciences_industry_in_Switzerland">Life sciences industry in Switzerland</a></li>

</ul>
</details>

**标签**: `#AI`, `#scientific discovery`, `#automation`, `#robotics`, `#data infrastructure`

---

<a id="item-7"></a>
## [WebAssembly 编译的 Mermaid 转彩色 ASCII 艺术工具](https://simonwillison.net/2026/Jul/16/mermaid-ascii/#atom-everything) ⭐️ 6.0/10

Simon Willison 发布了一个新工具，通过使用 Claude Fable 5 将现有的 Go 库 "AlexanderGrooff/mermaid-ascii" 编译为 WebAssembly，可将 Mermaid 图表转换为彩色的 ASCII 艺术，相比之前的 Rust 工具提供了更多功能。 该工具使开发者能够在浏览器中直接生成支持颜色的文本图表，在终端或纯文本格式等图形渲染受限的环境中，增强了文档和沟通能力。 该工具包含一个网页界面，提供了不同图表类型的选项卡、可自定义的内边距，以及复制 ASCII 输出或分享链接的选项；它利用了更早的 Go 库，该库比之前的 Rust 版本提供了更广泛的 Mermaid 语法支持。

rss · Simon Willison · 7月16日 14:57

**背景**: Mermaid 是一个基于 JavaScript 的图表工具，使用类似 Markdown 的语法创建图表和流程图。WebAssembly (Wasm) 是一种二进制指令格式，允许用 Go 或 Rust 等语言编写的代码在网页浏览器中以接近原生的速度运行。Claude Fable 5 是 Anthropic 开发的大型语言模型，以强大的编码能力著称，被用于将 Go 代码编译为 WebAssembly。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://mermaid.js.org/intro/syntax-reference.html">Diagram Syntax | Mermaid</a></li>
<li><a href="https://en.wikipedia.org/wiki/WebAssembly">WebAssembly - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Claude_Fable_5">Claude Fable 5</a></li>

</ul>
</details>

**标签**: `#mermaid`, `#ascii-art`, `#webassembly`, `#developer-tools`, `#diagramming`

---

<a id="item-8"></a>
## [OpenAI 官方发布 8 个 ChatGPT 使用技巧](https://mp.weixin.qq.com/s?__biz=MzIzNjc1NzUzMw==&mid=2247904149&idx=2&sn=4defdcfe6a2c177cd00738e9c870990e) ⭐️ 5.0/10

OpenAI 发布了一份官方指南，提供了八个实用技巧，帮助用户更有效地与 ChatGPT 互动，涵盖提示词撰写和功能使用。 随着 ChatGPT 成为数百万人的日常工具，官方指导能帮助用户超越基础提问，获得更准确、更有创意和更高效的结果，减少常见的使用挫败感。 这些技巧可能包括为 ChatGPT 设定角色、将复杂任务拆解为步骤、提供示例以及使用系统级指令等策略，但文章摘要未提供具体技术细节。

rss · 量子位 · 7月16日 04:28

**背景**: ChatGPT 是 OpenAI 开发的大型语言模型，能够生成类似人类的文本回复。有效使用通常需要“提示工程”，即精心设计输入文本以引导模型产生期望的输出。许多用户最初难以获得高质量结果，因为他们将其视为简单的搜索引擎，而非一个需要上下文和明确指令的对话代理。

**标签**: `#ChatGPT`, `#tutorial`, `#AI`, `#OpenAI`, `#guide`

---

<a id="item-9"></a>
## [用 Ollama 在 15 分钟内运行本地 AI 模型](https://machinelearningmastery.com/run-a-local-ai-model-with-ollama-in-15-minutes/) ⭐️ 5.0/10

Machine Learning Mastery 发布了一篇新的分步教程，指导初学者如何在 15 分钟内使用 Ollama 在本地设置并运行一个小型语言模型。 该指南降低了本地大语言模型实验的门槛，让用户能在自己的机器上私密运行 AI 模型，无需依赖云服务，这对数据隐私和离线访问日益重要。 该教程重点使用 Ollama 这一开源工具（提供命令行界面和 REST API）来快速部署参数较少、能在单台计算机等资源受限硬件上运行的小型语言模型。

rss · Machine Learning Mastery · 7月16日 12:25

**背景**: Ollama 是一个开源平台，简化了在本地运行和管理大语言模型的过程。小型语言模型（SLM）是参数远少于大语言模型（LLM）的紧凑型 AI 模型，使其无需庞大计算资源即可在个人电脑上运行。这与需要强大远程服务器的云端大语言模型形成对比。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Ollama">Ollama</a></li>
<li><a href="https://en.wikipedia.org/wiki/Small_language_model">Small language model</a></li>

</ul>
</details>

**标签**: `#ollama`, `#local-llm`, `#tutorial`, `#ai`, `#beginner`

---