---
layout: default
title: "Horizon Summary: 2026-09-11 (ZH)"
date: 2026-09-11
lang: zh
---

> 从 13 条内容中筛选出 5 条重要资讯。

---

1. [任意 Nix 软件包，在浏览器中直接运行](#item-1) ⭐️ 8.0/10
2. [Shopify 放弃 React Native，回归原生 Swift 与 Kotlin](#item-2) ⭐️ 7.0/10
3. [一次辞职重新点燃了广泛的 AI 安全担忧](#item-3) ⭐️ 7.0/10
4. [分析数据中心表后供电面临的挑战](#item-4) ⭐️ 6.0/10
5. [将传统机器学习与智能体推理相结合](#item-5) ⭐️ 5.0/10

---

<a id="item-1"></a>
## [任意 Nix 软件包，在浏览器中直接运行](https://simonwillison.net/2026/Sep/10/trynix/) ⭐️ 8.0/10

trynix.dev 利用 qemu-wasm 在浏览器中完整运行一个 x86_64 Linux 虚拟机，用户可以通过 URL 地址启动过去 13 年中的任意 Nix 软件包。Farid Zakaria 还推出了 trynix-preview，这是一个 GitHub Action，会在拉取请求中评论一个链接，让用户无需服务器即可在浏览器中启动该 PR 的构建。 这种方法将 Nix 的可复现性与基于浏览器的虚拟化结合起来，使历史软件包环境可以通过 URL 即时访问和分享。它可能显著改善代码审查流程和可复现构建，让开发者无需本地配置即可测试精确的软件包版本。 该虚拟机由 qemu-wasm 驱动，这是一个使用 TCG 移植到浏览器中的 QEMU 系统模拟器，可以启动如 2017 年的 Python 3.6.2 等软件包。trynix-preview GitHub Action 无需服务器，仅需浏览器即可启动拉取请求的构建。

rss · Simon Willison · 9月10日 23:44

**背景**: Nix 是一个纯函数式软件包管理器，将软件包视为不可变值，确保在不同系统上构建的可复现性。QEMU 是一个广泛使用的系统模拟器，可以运行完整的操作系统，而 qemu-wasm 是 QEMU 到 WebAssembly 的实验性移植，使其能够在网页浏览器中运行。WebAssembly 是一种二进制指令格式，允许在浏览器中高性能地执行代码。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/ktock/qemu-wasm">GitHub - ktock/qemu-wasm: QEMU on browser · GitHub</a></li>
<li><a href="https://en.wikipedia.org/wiki/Nix_(package_manager)">Nix (package manager)</a></li>
<li><a href="https://archive.fosdem.org/2025/schedule/event/fosdem-2025-6290-running-qemu-inside-browser/">FOSDEM 2025 - Running QEMU Inside Browser</a></li>

</ul>
</details>

**标签**: `#nix`, `#webassembly`, `#virtualization`, `#reproducible-builds`, `#devtools`

---

<a id="item-2"></a>
## [Shopify 放弃 React Native，回归原生 Swift 与 Kotlin](https://simonwillison.net/2026/Sep/10/shopify-react-native/) ⭐️ 7.0/10

Shopify 宣布将其移动应用从 React Native 迁回独立的 Swift 和 Kotlin 代码库，推翻了 2020 年采用跨平台方案的决策。该公司表示，AI 编码代理现在已能承担足够的实现、翻译、测试和审查工作，因此维护两套原生代码库不再像过去那样成本高昂。 这是一个重要的行业信号，因为 Shopify 是 React Native 的重要采用者和开源贡献者，其转向可能影响其他正在权衡跨平台与原生开发的公司。其新颖的理由——AI 代理降低了双代码库的维护成本——可能重塑工程团队评估技术选型的方式。 Shopify 维护着三个重要的 React Native 库：react-native-skia 和 flash-list 正在寻找新的归宿，而 restyle 因用户群体较小，将于 2026 年底归档。文章对 React Native 在 Shopify 使用的六年期间给予了充分肯定，称其是一个出色的平台。

rss · Simon Willison · 9月10日 21:11

**背景**: React Native 是 Meta 开发的开源框架，允许开发者使用 JavaScript 和 React 构建 iOS 和 Android 应用，同时仍可访问原生平台能力。原生开发意味着分别用 Swift 编写 iOS 应用、用 Kotlin 编写 Android 应用，历史上这需要重复开发功能并维护两套代码库。Shopify 在 2020 年采用 React Native，就是为了避免重复构建相同功能，并让开发者能够跨技术栈工作。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/React_Native">React Native</a></li>
<li><a href="https://en.wikipedia.org/wiki/Kotlin">Kotlin</a></li>

</ul>
</details>

**标签**: `#mobile development`, `#React Native`, `#Shopify`, `#AI agents`, `#software architecture`

---

<a id="item-3"></a>
## [一次辞职重新点燃了广泛的 AI 安全担忧](https://www.interconnects.ai/p/one-resignation-turned-the-embers) ⭐️ 7.0/10

AI 行业的一次高调辞职加剧了人们对 AI 的既有担忧，使原本缓慢发酵的顾虑迅速演变为更大范围的公开讨论。 该事件的重要性在于，它表明有影响力的 AI 机构中的人事变动能够迅速影响公众认知以及围绕 AI 安全的政策讨论。 消息来源是一位受人尊敬的 AI 评论员，但现有内容非常有限，没有说明辞职者姓名、所属机构或辞职的具体情况。

rss · Interconnects · 9月10日 15:28

**背景**: 随着先进模型能力不断增强，AI 安全已成为重要议题，研究人员和高管有时会因在 AI 发展速度或安全性问题上存在分歧而离开所在机构。

**标签**: `#AI`, `#resignation`, `#AI safety`, `#industry news`, `#commentary`

---

<a id="item-4"></a>
## [分析数据中心表后供电面临的挑战](https://newsletter.semianalysis.com/p/what-is-so-hard-about-behind-the) ⭐️ 6.0/10

SemiAnalysis 发布了分析文章的第一部分，探讨数据中心采用表后（BTM）供电模式所面临的技术和经济障碍，并将“愚蠢的科学实验”与“印钞机”两种模式进行对比。 随着 AI 工作负载推动前所未有的电力需求，表后发电正从应急备用转变为核心增长引擎，其可行性与经济性对数据中心行业的扩张至关重要。 文章副标题暗示了投机性、实验性的表后项目与商业上可行且利润丰厚的部署之间的区别，但所提供的摘录中并未包含完整的技术细节。

rss · Semianalysis · 9月10日 14:28

**背景**: 表后供电是指在用户电表一侧、就地发电或储能的模式，绕过或补充传统电网。对数据中心而言，这可以包括位于设施内部或附近的燃气轮机、太阳能、电池或其他发电资产。表后供电传统上仅用于应急备用，如今正被考虑作为主要电源，以克服电网并网延迟和容量限制。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://datacenterhawk.com/resources/market-insights/behind-the-meter-power-solutions-the-data-center-industry-s-new-reality">Behind-the-Meter Power Solutions: The Data Center Industry's ...</a></li>
<li><a href="https://www.datacenterdynamics.com/en/opinions/behind-the-meter-power-the-new-backbone-of-data-center-growth/">Behind-the-meter power: The new backbone of data center ...</a></li>
<li><a href="https://www.datacenterknowledge.com/energy-power-supply/why-data-centers-produce-their-own-power">Why Data Centers Are Turning to Behind-the-Meter Power</a></li>

</ul>
</details>

**标签**: `#datacenters`, `#energy`, `#power infrastructure`, `#behind-the-meter`, `#semianalysis`

---

<a id="item-5"></a>
## [将传统机器学习与智能体推理相结合](https://machinelearningmastery.com/how-to-combine-traditional-machine-learning-with-agentic-reasoning/) ⭐️ 5.0/10

Machine Learning Mastery 发布了一篇教程，解释传统机器学习在哪些方面达到极限，以及智能体推理如何与之互补，从而构建能力更强的 AI 系统。 随着智能体 AI 成为重要行业趋势，理解如何将其与成熟的机器学习流程相结合，可以帮助从业者构建既能从数据中学习又能自主行动的系统。 该文章属于教程类内容，并非新颖的研究贡献，且没有提供社区评论或讨论来评估其参与度和可信度。

rss · Machine Learning Mastery · 9月10日 12:00

**背景**: 传统机器学习通常从固定数据集中学习模式以进行预测，而智能体推理使 AI 系统能够追求目标、使用工具并以一定自主性执行多步骤任务。智能体推理通常将大语言模型与规划、记忆和工具使用相结合。该文章假设读者熟悉基本的机器学习概念，并有兴趣将其扩展到更自主的 AI 系统。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Agentic_AI">Agentic AI</a></li>
<li><a href="https://www.glean.com/blog/a-complete-guide-to-agentic-reasoning">A complete guide to agentic reasoning</a></li>
<li><a href="https://www.ibm.com/think/topics/agentic-reasoning">What Is Agentic Reasoning? | IBM</a></li>

</ul>
</details>

**标签**: `#machine learning`, `#agentic AI`, `#tutorial`, `#AI systems`, `#reasoning`

---