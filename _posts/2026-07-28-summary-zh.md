---
layout: default
title: "Horizon Summary: 2026-07-28 (ZH)"
date: 2026-07-28
lang: zh
---

> 从 13 条内容中筛选出 8 条重要资讯。

---

1. [月之暗面发布 2.8 万亿参数 Kimi K3 模型，采用修改版 MIT 许可](#item-1) ⭐️ 8.0/10
2. [AI 代理持久化记忆与状态的五种架构模式](#item-2) ⭐️ 7.0/10
3. [西蒙·威利森谈 AI 工具从聊天模式向代理系统的转变](#item-3) ⭐️ 6.0/10
4. [综述提出五个方向，减少 3DGS 显存占用](#item-4) ⭐️ 6.0/10
5. [img2threejs 将参考图像转换为程序化 Three.js 3D 模型](#item-5) ⭐️ 6.0/10
6. [OpenMinis：即将推出的跨平台 AI 智能体应用的占位仓库](#item-6) ⭐️ 3.0/10
7. [全新 JavaScript 设计语言 'Impeccable' 旨在提升 AI 辅助设计](#item-7) ⭐️ 3.0/10
8. [QwenPaw 自托管 AI 助手获 5 颗 GitHub 星](#item-8) ⭐️ 3.0/10

---

<a id="item-1"></a>
## [月之暗面发布 2.8 万亿参数 Kimi K3 模型，采用修改版 MIT 许可](https://simonwillison.net/2026/Jul/27/kimi-k3/#atom-everything) ⭐️ 8.0/10

月之暗面（Moonshot AI）发布了其拥有 2.8 万亿参数的 Kimi K3 模型权重。该模型采用修改版 MIT 许可，要求大型商业实体进行署名，并对大型模型服务业务施加额外限制。 此次发布使得一个大规模、有竞争力的模型可供研究和商业使用，但限制性许可可能限制大型云服务商和科技公司的采用，引发关于开放权重模型治理的讨论。 模型权重在 Hugging Face 上总计 1.56TB。许可比 K2 的署名要求更严格，要求过去 12 个月收入超过 2000 万美元的模型服务业务需另行签订协议，月之暗面称其为“开放权重”而非“开源”。

rss · Simon Willison · 7月27日 23:39

**背景**: 月之暗面是一家中国 AI 初创公司，以 Kimi 系列大语言模型闻名。2025 年发布的 Kimi K2 模型引入了修改版 MIT 许可，要求月活用户超 1 亿或月收入超 2000 万美元的商业实体进行署名。“开放权重”一词用来区分那些权重公开但许可受限、不完全开源的模型。

**标签**: `#AI`, `#LLM`, `#Open Source`, `#Model Release`, `#Licensing`

---

<a id="item-2"></a>
## [AI 代理持久化记忆与状态的五种架构模式](https://machinelearningmastery.com/5-architectural-patterns-for-persistent-memory-and-state-in-ai-agents/) ⭐️ 7.0/10

该文章介绍了五种用于管理 AI 代理持久化记忆和状态的架构模式，以确保在长期部署中的一致性。 持久化记忆对于长时间运行的自主代理至关重要，这些模式为构建可靠、有状态的 AI 系统提供了结构化方法。 这些模式解决了状态一致性、错误恢复和可扩展性等挑战，但具体实现细节取决于所选框架和用例。

rss · Machine Learning Mastery · 7月27日 12:00

**背景**: AI 代理通常需要记住过去的交互并维护内部状态以有效执行任务。如果没有持久化记忆，代理在会话之间或发生故障后会丢失上下文，从而限制其在实际应用中的用途。

**标签**: `#AI Agents`, `#Persistent Memory`, `#Software Architecture`, `#LLMs`, `#State Management`

---

<a id="item-3"></a>
## [西蒙·威利森谈 AI 工具从聊天模式向代理系统的转变](https://simonwillison.net/2026/Jul/27/an-opinionated-guide-to-which-ai-to-use-to-do-stuff/#atom-everything) ⭐️ 6.0/10

西蒙·威利森观察到，伊桑·莫里克的人工智能工具指南已经从推荐 ChatGPT 和 Claude 等聊天模型，转向强调能够自主完成数小时人类工作的代理系统。他指出了 ChatGPT Work 和 Claude Cowork 等模式命名令人困惑，并提到谷歌的 Gemini Spark 尚未证明自身价值。 这篇评论反映了行业向代理人工智能发展的更广泛趋势，这种技术有望自动化复杂任务并提高生产力。命名混乱凸显了用户在日益碎片化的人工智能工具环境中面临的导航挑战。 一个关键点是，ChatGPT 移动端上的“Work”模式允许其代码解释器容器访问互联网，而在桌面应用中，“Work”实质上只是 Codex 的一个简化界面。这些模式在不同平台和产品间的区别并不直观。

rss · Simon Willison · 7月27日 21:55

**背景**: 代理系统是一种能够以最少人工监督自主执行多步骤任务的人工智能设计，与简单的聊天交互不同。伊桑·莫里克是一位以实用人工智能使用指南而闻名的教授和人工智能评论员。文中提到的工具包括 ChatGPT Work（用于编码和数据分析的模式）、Claude Cowork（Claude 的类似功能）以及 Gemini Spark（谷歌的代理助手）。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://datadrivenblogs.medium.com/when-ai-starts-acting-a-look-at-agentic-systems-d19817013a54">When AI Starts Acting: A Look at Agentic Systems | Medium</a></li>
<li><a href="https://support.google.com/gemini/answer/17094507?hl=en-CA&co=GENIE.Platform=Android">Use Gemini Spark to manage your tasks & workflows in Gemini Apps...</a></li>

</ul>
</details>

**标签**: `#AI tools`, `#agentic AI`, `#LLM`, `#industry trends`, `#commentary`

---

<a id="item-4"></a>
## [综述提出五个方向，减少 3DGS 显存占用](https://mp.weixin.qq.com/s?__biz=MzIzNjc1NzUzMw==&mid=2247907517&idx=3&sn=47197285f42f0199832d9f5b6612b961) ⭐️ 6.0/10

一篇综述论文归纳了五个研究方向，旨在缓解 3D 高斯泼溅每个场景高达 700MB 的显存占用问题。 这解决了在消费级 GPU 和移动设备上部署 3DGS 的关键瓶颈，有望使实时新视角合成在 VR、游戏和数字孪生等应用中更加普及。 该综述将现有和潜在的解决方案划分为五个方法类别，为后续研究提供了结构化的路线图。

rss · 量子位 · 7月27日 03:31

**背景**: 3D 高斯泼溅（3DGS）是一种从多视角图像实时渲染辐射场的近期技术。它用数百万个各向异性的 3D 高斯函数表示场景，每个高斯包含位置、形状、颜色和不透明度等参数。尽管渲染速度快，但大量高斯会占用数百兆的 GPU 显存，限制了可扩展性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/3D_Gaussian_splatting">3D Gaussian splatting</a></li>

</ul>
</details>

**标签**: `#3D Gaussian Splatting`, `#Memory Optimization`, `#Computer Vision`, `#Survey`, `#Graphics`

---

<a id="item-5"></a>
## [img2threejs 将参考图像转换为程序化 Three.js 3D 模型](https://github.com/img2threejs/img2threejs) ⭐️ 6.0/10

GitHub 仓库 img2threejs 推出了一款基于 Python 的工具，能够利用程序化生成技术，将参考图像转换为纯代码、可动画的 Three.js 3D 模型。 这种方法为传统的图像转 3D 技术提供了一种节省 token 的替代方案，有望降低计算成本，并使基于网页的 3D 内容创作更加普及。 该工具是一个早期项目，用 Python 编写，专注于“质量把关”的程序化工作流程，但其当前影响力和社区采用度有限。

ossinsight · img2threejs · 7月28日 01:19

**背景**: Three.js 是一个流行的 JavaScript 库，用于在网页浏览器中渲染 3D 图形。程序化生成是一种通过算法自动创建数据的技术，常用于自动生成 3D 模型和纹理，这可以带来更小的文件体积和更丰富的内容。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Three.js">Three.js</a></li>
<li><a href="https://en.wikipedia.org/wiki/Procedural_generation">Procedural generation</a></li>

</ul>
</details>

**标签**: `#3D`, `#image-to-3D`, `#Three.js`, `#procedural-generation`, `#Python`

---

<a id="item-6"></a>
## [OpenMinis：即将推出的跨平台 AI 智能体应用的占位仓库](https://github.com/OpenMinis/OpenMinis) ⭐️ 3.0/10

一个名为 OpenMinis 的新 GitHub 仓库出现，预告了一款即将推出的开源跨平台 AI 智能体应用，但目前尚未包含任何源代码。 该公告预示着开源 AI 智能体领域可能迎来新参与者，为对自主 AI 工具感兴趣的开发者和用户提供一个潜在的跨平台选择。 该仓库目前只是一个占位符，在过去 24 小时内仅获得 6 个星标和 0 次复刻，且没有任何代码、文档或技术细节。

ossinsight · OpenMinis · 7月28日 01:19

**背景**: AI 智能体是一种能够代表用户执行任务、做出决策并与环境交互的自主软件程序。跨平台应用旨在运行于 Windows、macOS 和 Linux 等多种操作系统上，从而可能扩大其用户基础。

**标签**: `#AI`, `#Agent`, `#CrossPlatform`, `#OpenSource`, `#Trending`

---

<a id="item-7"></a>
## [全新 JavaScript 设计语言 'Impeccable' 旨在提升 AI 辅助设计](https://github.com/pbakaus/impeccable) ⭐️ 3.0/10

一个名为 'pbakaus/impeccable' 的新开源项目出现在 GitHub 上，它被描述为一种旨在让 AI 工具更擅长设计的 JavaScript 设计语言。 该项目探索了 AI 与设计系统的交叉领域，可能为 AI 生成或优化用户界面提供一种结构化方法，从而简化开发者和设计师的工作流程。 该项目处于非常早期的阶段，使用 JavaScript 编写，过去一天仅获得 5 个星标，表明这是一个新兴概念，尚无成熟社区或经过验证的实用性。

ossinsight · pbakaus · 7月28日 01:19

**背景**: “设计语言”是一套指导产品视觉外观的规则和原则，例如谷歌的 Material Design。该项目的名称 'Impeccable' 及其描述可能暗指包豪斯运动，这所著名的设计学院以其功能性、极简主义和“无可挑剔”的工艺而闻名。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.goodreads.com/author/quotes/64267.Nicholas_Fox_Weber">Quotes by Nicholas Fox Weber (Author of The Bauhaus Group)</a></li>
<li><a href="https://dianamosher.com/from-our-house-to-bauhaus-five-questions-with-jerelyn-hanrahan-founder-of-atelier-on-spring-gallerie/">From Our House to Bauhaus: Five Questions with Jerelyn Hanrahan ...</a></li>

</ul>
</details>

**标签**: `#AI`, `#design`, `#JavaScript`, `#open-source`, `#tools`

---

<a id="item-8"></a>
## [QwenPaw 自托管 AI 助手获 5 颗 GitHub 星](https://github.com/agentscope-ai/QwenPaw) ⭐️ 3.0/10

由 agentscope-ai 创建的 QwenPaw 个人 AI 助手项目在过去 24 小时内获得了 5 颗 GitHub 星，显示出开发者社区的初步关注。 尽管关注度有限，该项目突显了市场对自托管 AI 解决方案日益增长的需求，这些方案优先考虑用户隐私和数据控制，尤其在聊天助手领域。 该项目使用 Python 编写，可部署在本地或云端，支持多种聊天应用，并具备易于扩展的功能。

ossinsight · agentscope-ai · 7月28日 01:19

**标签**: `#AI-assistant`, `#open-source`, `#Python`, `#self-hosted`, `#chat-apps`

---