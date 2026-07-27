---
layout: default
title: "Horizon Summary: 2026-07-27 (ZH)"
date: 2026-07-27
lang: zh
---

> 从 13 条内容中筛选出 8 条重要资讯。

---

1. [vLLM v0.26.0 发布：支持 Inkling 模型与性能提升](#item-1) ⭐️ 8.0/10
2. [调查揭示大语言模型 API 折扣访问的非法市场](#item-2) ⭐️ 7.0/10
3. [MonkeyOCRv2 以 0.7B 参数实现 17 语言文档解析最佳性能](#item-3) ⭐️ 6.0/10
4. [OmniRoute：免费 AI 网关，聚合 290+提供商，支持 Token 压缩](#item-4) ⭐️ 6.0/10
5. [block/buzz: 基于 Rust 的早期蜂巢思维通信平台](#item-5) ⭐️ 4.0/10
6. [Floci 作为基于 Java 的轻量级 AWS 本地模拟器替代方案出现](#item-6) ⭐️ 4.0/10
7. [QwenPaw：AgentScope-AI 的易安装个人 AI 助手](#item-7) ⭐️ 4.0/10
8. [Instatic：一个自托管可视化 CMS 在 GitHub 上获得 7 星](#item-8) ⭐️ 3.0/10

---

<a id="item-1"></a>
## [vLLM v0.26.0 发布：支持 Inkling 模型与性能提升](https://github.com/vllm-project/vllm/releases/tag/v0.26.0) ⭐️ 8.0/10

vLLM v0.26.0 引入了对全新 Inkling 模型家族的支持、针对 DeepSeek-V4 的性能优化、生成模型的 fp32 lm_head 以及灵活的注意力后端选择，共包含来自 212 位贡献者的 411 次提交。 该版本扩展了 vLLM 与 Inkling 等前沿模型的兼容性，降低了 DeepSeek-V4 的服务成本和延迟，并通过 fp32 lm_head 提高了输出精度，对代码生成和推理任务尤其有益。 Inkling 是一个 MoE Transformer，总参数 975B，活跃参数 41B，现已全面支持 LoRA 和 NVFP4 量化。NVFP4 是 NVIDIA 的 4 位浮点格式，用于高效推理；同时为 Inkling 启用了多令牌预测（MTP）推测解码。

github · khluu · 7月27日 01:06

**背景**: Inkling 是 Thinking Machines Lab 的首个开放权重模型，从头训练耗时不到九个月。多令牌预测是一种先进的推测解码技术，每次前向预测多个未来令牌，在不损失质量的情况下提高吞吐量。NVFP4 专为 Blackwell GPU 设计，在低位时提供比 INT4 更好的精度。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://thinkingmachines.ai/news/introducing-inkling/">Inkling: Our Open-Weights Model - Thinking Machines Lab</a></li>
<li><a href="https://developer.nvidia.com/blog/introducing-nvfp4-for-efficient-and-accurate-low-precision-inference/">Introducing NVFP4 for Efficient and Accurate Low-Precision ...</a></li>

</ul>
</details>

**标签**: `#LLM inference`, `#open-source`, `#performance optimization`, `#model support`, `#release`

---

<a id="item-2"></a>
## [调查揭示大语言模型 API 折扣访问的非法市场](https://simonwillison.net/2026/Jul/26/relay-market/#atom-everything) ⭐️ 7.0/10

Matt Lenhard 的调查揭露了一个市场，转售商通过滥用免费试用、窃取凭证以及使用 one-api 和 new-api 等开源代理软件，提供折扣的大语言模型 API 访问。 这个非法生态系统给 API 提供商和开发者带来了财务风险，因为未受保护的端点可能被利用来牟利，同时也凸显了为 API 密钥设置更严格消费上限的迫切需求。 该市场主要活跃于中国，买家寻求廉价令牌、绕过地理限制或为模型蒸馏收集数据。所使用的开源工具本是合法的负载均衡器，却被重新用于欺诈。

rss · Simon Willison · 7月26日 19:30

**背景**: 像 OpenAI 这样的 LLM 提供商按令牌数量对 API 使用收费。像 one-api 这样的代理软件旨在管理和负载均衡多个 API 密钥。欺诈者汇集通过非法手段（如盗刷信用卡或拒付攻击）获得的密钥，并以折扣价转售访问权限，从而形成了 AI 服务的黑市。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://simonwillison.net/2026/Jul/26/relay-market/">An Inside Look at the Relay Market Powering Token Resellers and...</a></li>
<li><a href="https://github.com/songquanpeng/one-api/blob/main/README.en.md">one-api/README.en.md at main · songquanpeng/one-api</a></li>

</ul>
</details>

**标签**: `#LLM`, `#API security`, `#fraud`, `#token reselling`, `#open source`

---

<a id="item-3"></a>
## [MonkeyOCRv2 以 0.7B 参数实现 17 语言文档解析最佳性能](https://mp.weixin.qq.com/s?__biz=MzIzNjc1NzUzMw==&mid=2247907283&idx=2&sn=5df8a52712c79f67232ca9672d4cc34e) ⭐️ 6.0/10

MonkeyOCRv2 是一个全新的开源视觉文本基础模型，仅用 0.7B 参数就在 17 种语言的文档解析中达到顶尖水平，突显了高效的参数利用能力。 这证明通过更智能的架构，小模型可与大模型匹敌，使高级文档 AI 更易获取，并能在资源受限的边缘设备上部署。 该模型基于包含 1.13 亿张图像的 MonkeyDoc v2 数据集训练，覆盖 17 种语言，通过联合学习文本生成和像素级重建产生文档原生的视觉表示。

rss · 量子位 · 7月26日 04:30

**背景**: 文档解析是从扫描件或图像中提取文字和结构的技术。AI 中，OCR 模型通常参数规模达数十亿，参数数量衡量模型大小和能力。MonkeyOCRv2 表明即使 0.7B 的小模型也能表现优异，挑战了模型一味做大的趋势。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/html/2607.11562">MonkeyOCRv2: A Visual-Text Foundation Model for Document AI</a></li>
<li><a href="https://github.com/Yuliang-Liu/MonkeyOCRv2">GitHub - Yuliang-Liu/MonkeyOCRv2: MonkeyOCRv2 Vision Encoder — A Document-Native Visual Backbone</a></li>

</ul>
</details>

**标签**: `#OCR`, `#multilingual`, `#small models`, `#document parsing`, `#open-source`

---

<a id="item-4"></a>
## [OmniRoute：免费 AI 网关，聚合 290+提供商，支持 Token 压缩](https://github.com/diegosouzapw/OmniRoute) ⭐️ 6.0/10

名为 OmniRoute 的开源项目在 GitHub 上成为趋势，24 小时内获得 5 颗星。它提供单一 API 端点，可访问超过 290 个 LLM 提供商和 500 多个模型，并具备配额感知自动回退和 RTK+Caveman 令牌压缩等功能。 OmniRoute 通过聚合提供商、在配额耗尽时自动切换以及通过压缩降低 15-95%的 Token 成本，简化了多模型 AI 集成。这可以降低开发者的门槛并减少运营支出。 这个 MIT 许可的 TypeScript 项目声称支持主流编码助手（如 Claude Code、Cursor 等）以及 MCP/A2A 协议。令牌压缩采用 RTK（命令输出优化）和 Caveman（文本压缩），但鉴于早期阶段，500 多名贡献者的说法似乎带有宣传性质。

ossinsight · diegosouzapw · 7月27日 01:45

**背景**: AI 网关为多个大语言模型 (LLM) API 提供统一接口，简化开发。配额感知回退在使用限制达到时将请求路由到替代提供商，避免服务中断。RTK 和 Caveman 是令牌节省技术：RTK 压缩命令输出，Caveman 压缩自然语言文本。MCP（模型上下文协议）和 A2A（智能体对智能体）是 AI 智能体通信的新兴标准。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://proxmox-scripts.com/posts/omniroute/">OmniRoute | Proxmox VE Scripts</a></li>
<li><a href="https://github.com/dd3ok/caveman-rtk-benchmark">GitHub - dd3ok/caveman-rtk-benchmark · GitHub</a></li>

</ul>
</details>

**标签**: `#ai-gateway`, `#llm-tools`, `#open-source`, `#typescript`, `#api-aggregation`

---

<a id="item-5"></a>
## [block/buzz: 基于 Rust 的早期蜂巢思维通信平台](https://github.com/block/buzz) ⭐️ 4.0/10

项目 block/buzz 是一个用 Rust 编写的蜂巢思维通信平台，在过去 24 小时内获得了 9 个 GitHub 星标和 17 次代码推送，显示出活跃的早期开发，但尚未有分支。 现在评估其更广泛的影响还为时过早，但该项目探索了集体智能和分布式通信，利用 Rust 的性能和安全性打造一个可能新颖的平台。 该仓库除了一句话描述外没有列出具体功能或文档，低参与度（9 颗星，0 分支）表明它处于非常早期的实验阶段。

ossinsight · block · 7月27日 01:45

**背景**: '蜂巢思维'指的是个体共享思想和决策的集体意识。旨在实现蜂巢思维的通信平台通常包含实时消息、投票和协作功能。Rust 是一种系统编程语言，以其内存安全和无垃圾回收的并发性而闻名，非常适合构建可靠、高性能的分布式系统。该项目托管在 GitHub 的'block'组织下，该组织可能与 Block 公司（Square 和 Cash App 背后的技术公司）有关，但此关联在提供的资料中未得到确认。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/block/buzz">GitHub - block/buzz: A hive mind communication platform · GitHub</a></li>
<li><a href="https://en.wikipedia.org/wiki/Rust_(programming_language)">Rust (programming language)</a></li>

</ul>
</details>

**标签**: `#rust`, `#hive-mind`, `#communication`, `#open-source`, `#trending`

---

<a id="item-6"></a>
## [Floci 作为基于 Java 的轻量级 AWS 本地模拟器替代方案出现](https://github.com/floci-io/floci) ⭐️ 4.0/10

GitHub 仓库 floci-io/floci 作为现有 AWS 本地模拟器的轻量级 Java 替代方案受到关注，在过去 24 小时内获得了 6 颗星。 它为开发人员提供了一个可能更快、始终免费且无需凭据的本地 AWS 开发反馈循环，这可以简化测试并降低云成本。 Floci 使用 Java 编写，声称可以在几毫秒内在本地运行 AWS、Azure 和 GCP 服务，无需账户或遥测。

ossinsight · floci-io · 7月27日 01:45

**背景**: 像 LocalStack 这样的 AWS 本地模拟器允许开发者在自己的机器上模拟 AWS 云服务以进行测试，从而避免使用真实的 AWS 账户和相关成本。Floci 定位为一个更快、更轻量的替代方案，同时也支持 Azure 和 GCP。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/floci-io/floci">GitHub - floci - io / floci : Light, fluffy, and always free - The AWS Local...</a></li>
<li><a href="https://floci.io/">Floci — Local Cloud Emulators</a></li>
<li><a href="https://www.localstack.cloud/localstack-for-aws">LocalStack for AWS</a></li>

</ul>
</details>

**标签**: `#AWS`, `#emulator`, `#Java`, `#local-development`, `#serverless`

---

<a id="item-7"></a>
## [QwenPaw：AgentScope-AI 的易安装个人 AI 助手](https://github.com/agentscope-ai/QwenPaw) ⭐️ 4.0/10

QwenPaw 是一个新的开源个人 AI 助手，内置本地运行时，无需 API 密钥或云依赖，并支持多种聊天应用。 它降低了个人 AI 部署的门槛，使用户能够在本地运行功能齐全且可扩展的助手，契合了对注重隐私、自托管 AI 工具日益增长的需求。 QwenPaw 的本地运行时不依赖云服务，并可与 Ollama、LM Studio 及超过 14 个云提供商集成，实现灵活的模型选择。

ossinsight · agentscope-ai · 7月27日 01:45

**背景**: AgentScope-AI 是 AgentScope 2.0 背后的组织，这是一个生产就绪的开源智能体框架，具备事件驱动和权限系统。QwenPaw 是在此生态基础上构建的个人助手应用，强调易于安装和本地运行。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/agentscope-ai/QwenPaw">GitHub - agentscope-ai/ QwenPaw : Your Personal AI Assistant; easy to...</a></li>
<li><a href="https://github.com/agentscope-ai/agentscope">GitHub - agentscope-ai/agentscope: Build and run agents you ...</a></li>
<li><a href="https://agentscope.io/">AgentScope — Where Agents Come Alive</a></li>

</ul>
</details>

**标签**: `#AI assistant`, `#Python`, `#open-source`, `#chatbot`, `#personal assistant`

---

<a id="item-8"></a>
## [Instatic：一个自托管可视化 CMS 在 GitHub 上获得 7 星](https://github.com/CoreBunch/Instatic) ⭐️ 3.0/10

Instatic 是一个用 TypeScript 编写的自托管可视化 CMS，在过去 24 小时内在 GitHub 上获得了 7 星，声称可在一分钟内完成设置。 这表明对具有可视化编辑功能的自托管开发者友好型 CMS 工具的兴趣持续存在，这些工具让用户在不牺牲易用性的前提下控制数据并进行定制。 Instatic 使用 TypeScript 构建，旨在快速部署，并提供用于内容管理的可视化界面，但其目前极少的关注度表明它处于早期开发阶段且测试有限。

ossinsight · CoreBunch · 7月27日 01:45

**背景**: 可视化 CMS 提供拖放界面用于编辑网站内容，弥合了开发者与内容创作者之间的鸿沟。自托管意味着软件在您自己的基础设施上运行，让您完全拥有数据和控制配置。流行的开源替代品包括 Strapi（无头 TypeScript CMS）和 TinaCMS（一个可视化的、基于 Git 的 CMS）。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://strapi.io/">Strapi - Open-Source TypeScript Headless CMS</a></li>
<li><a href="https://dev.to/builderio/what-is-a-visual-headless-cms-aka-visual-cms-19cb">What is a Visual Headless CMS (aka Visual CMS )? - DEV Community</a></li>
<li><a href="https://tina.io/">TinaCMS – GitHub’s #1 Headless CMS , powered by an awesome...</a></li>

</ul>
</details>

**标签**: `#CMS`, `#TypeScript`, `#self-hosted`, `#trending-repo`

---