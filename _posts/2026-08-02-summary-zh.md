---
layout: default
title: "Horizon Summary: 2026-08-02 (ZH)"
date: 2026-08-02
lang: zh
---

> 从 9 条内容中筛选出 5 条重要资讯。

---

1. [OpenAI 的 Astra 模型以每个不到 2000 美元成本解决十个十年未解数学难题](#item-1) ⭐️ 8.0/10
2. [OpenAI 总裁：员工反感收到同事 ChatGPT 机器人发来的任务请求](#item-2) ⭐️ 7.0/10
3. [Datasette Apps 0.2a0 新增代理调试功能](#item-3) ⭐️ 6.0/10
4. [DeepSeek V4-Flash 0731 低调发布，增强代理能力](#item-4) ⭐️ 3.0/10
5. [YC 支持的 QM：开源多玩家智能体框架](#item-5) ⭐️ 3.0/10

---

<a id="item-1"></a>
## [OpenAI 的 Astra 模型以每个不到 2000 美元成本解决十个十年未解数学难题](https://simonwillison.net/2026/Aug/1/ten-advances-in-mathematics/#atom-everything) ⭐️ 8.0/10

OpenAI 宣布，其即将推出的“Astra”模型的一个内部版本解决了十个长期悬而未决的数学问题，每个问题至少十年未有进展，且每个问题的解决成本不到 2000 美元（基于 GPT-5.6 Sol 代币定价）。 这展示了 AI 驱动的数学研究成果本急剧下降，直接与 Anthropic 最近的类似成就形成竞争，并预示着 AI 可能成为解决硬核科学问题的主要工具。 OpenAI 发布了证明的 Lean 4 形式化表述、描述解决方案的论文，以及一份由 LLM 生成的、重构推理过程的 PDF，但未公开所使用的具体提示词，且失败的尝试次数未知。

rss · Simon Willison · 8月1日 20:34

**背景**: 此消息紧随 Anthropic 最近展示其“Mythos Preview”模型发现密码学漏洞之后。OpenAI 的“Astra”模型系列专为长时间运行的复杂任务设计，并已向美国政策制定者进行了展示。其成本基于 OpenAI 的 GPT-5.6 Sol 模型定价，该模型输入价格为每百万 token 5 美元，输出价格为每百万 token 30 美元。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://the-decoder.com/openai-announces-its-next-major-model-astra-by-dropping-ten-previously-unsolved-math-solutions/">OpenAI announces its "next major model" Astra by dropping ten previously unsolved math solutions</a></li>
<li><a href="https://openrouter.ai/openai/gpt-5.6-sol">GPT - 5 . 6 Sol - API Pricing & Benchmarks | OpenRouter</a></li>
<li><a href="https://www.kucoin.com/news/flash/openai-developing-new-ai-model-astra-for-long-term-tasks">OpenAI is developing a new AI model called Astra for long-term tasks. | KuCoin</a></li>

</ul>
</details>

**社区讨论**: 作者 Simon Willison 对未成功的尝试次数表示怀疑，并指出许多数学家正经历一场类似于“深蓝”时刻的“精神危机”，而另一些人如陶哲轩则设想了一个“大数学”的未来，由 AI 处理技术性的繁重工作。

**标签**: `#AI`, `#mathematics`, `#OpenAI`, `#research-breakthrough`, `#theoretical-computer-science`

---

<a id="item-2"></a>
## [OpenAI 总裁：员工反感收到同事 ChatGPT 机器人发来的任务请求](https://simonwillison.net/2026/Aug/1/greg-brockman/#atom-everything) ⭐️ 7.0/10

OpenAI 总裁兼联合创始人格雷格·布罗克曼透露，OpenAI 员工不喜欢收到同事的 ChatGPT 机器人发来的任务请求，即使他们乐意直接帮助那位同事。 这一观察揭示了 AI 采纳中的一个关键人为因素：人们重视直接的人际关系，并将 AI 中介的任务委派视为冷漠的行为，若不加以解决，可能会阻碍 AI 在职场中的融合。 这一洞见来自布罗克曼对 OpenAI 内部文化的个人观察，员工将 ChatGPT 接入 Slack，这凸显了人们更希望 AI 增强而非取代人际互动。

rss · Simon Willison · 8月1日 22:29

**背景**: ChatGPT 是 OpenAI 开发的生成式 AI 聊天机器人，可集成到 Slack 等工作场所工具中以实现通信自动化。格雷·布罗克曼是 OpenAI 的关键人物，该公司以开发大型语言模型而闻名。'AI 委派'的概念是指使用 AI 代理代表人类执行任务，这有时会在社交层面引发摩擦。

**标签**: `#ai-ethics`, `#human-ai-interaction`, `#workplace-ai`, `#openai`, `#generative-ai`

---

<a id="item-3"></a>
## [Datasette Apps 0.2a0 新增代理调试功能](https://simonwillison.net/2026/Aug/1/datasette-apps/#atom-everything) ⭐️ 6.0/10

Datasette Apps 0.2a0 版本为 Datasette Agent 引入了两个新工具：app_debug()，允许代理通过隐藏的 iframe 使用 JavaScript 无痕打开并测试应用；以及 app_list()，用于列出用户可编辑的应用列表。 此次更新增强了 Datasette Agent 的集成，实现了无需人工干预即可自动测试和管理 Datasette Apps，为 Datasette 生态系统中更稳健的代理驱动开发工作流铺平了道路。 app_debug() 工具将应用加载到一个设置了 opacity: 0 和 pointer-events: none 的 iframe 中，使其不可见且不可交互，然后执行代理提供的 JavaScript 进行测试。它利用了 datasette-agent 0.4a0 中新的 browser_task() 机制。此版本为 alpha 版，功能可能尚处于实验阶段。

rss · Simon Willison · 8月1日 21:23

**背景**: Datasette 是一个用于探索和发布数据的开源工具，数据通常存储在 SQLite 中。Datasette Agent 是一个 AI 驱动的助手插件，帮助用户与数据进行交互。Datasette Apps 允许用户创建交互式数据应用。代理可以创建和修改这些应用，本次发布为代理提供了自动调试和列出应用的新工具。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://datasette.io/blog/2026/datasette-agent/">Datasette Agent, an extensible AI assistant for Datasette - Datasette Blog</a></li>
<li><a href="https://agent.datasette.io/">Datasette Agent: an AI assistant for Datasette to help explore and analyze data in SQLite</a></li>

</ul>
</details>

**标签**: `#datasette`, `#developer-tools`, `#ai-agents`, `#testing`, `#release-notes`

---

<a id="item-4"></a>
## [DeepSeek V4-Flash 0731 低调发布，增强代理能力](https://www.latent.space/p/ainews-not-much-happened-today-038) ⭐️ 3.0/10

AI 简讯提到今天是平静的一天，除了 DeepSeek V4-Flash 0731 发布，该模型是 DeepSeek 的更新版本，具有增强的代理能力，取代了预览版。 此更新提升了 AI 代理性能，可能以具有竞争力的价格实现更复杂的自主任务，有利于构建代理应用的开发者。 它是一个稀疏混合专家模型，在 2840 亿总参数中激活 130 亿参数，各平台定价约为每百万输入 tokens 0.09–0.14 美元。

rss · Latent Space · 8月1日 01:38

**背景**: DeepSeek 是一家以打造高效模型闻名的中国 AI 公司。‘Flash’变体可能优先考虑速度和成本效益。混合专家架构每次推理只激活部分参数，平衡了性能和计算成本。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/deepseek-ai/DeepSeek-V4-Flash-0731">deepseek-ai/DeepSeek-V4-Flash-0731 · Hugging Face</a></li>
<li><a href="https://artificialanalysis.ai/models/deepseek-v4-flash">DeepSeek V4 Flash 0731 (max) - Intelligence, Performance & Price Analysis</a></li>

</ul>
</details>

**标签**: `#AI`, `#newsletter`, `#DeepSeek`, `#low-effort`

---

<a id="item-5"></a>
## [YC 支持的 QM：开源多玩家智能体框架](https://github.com/yc-software/qm) ⭐️ 3.0/10

开源多玩家智能体框架 yc-software/qm 在过去 24 小时内获得了 5 个星标和 2 次分叉。 这体现了 YC 支持的一种工具，让初创公司能协调多个 AI 智能体进行协作，符合多智能体系统日益增长的趋势。 该仓库使用 TypeScript 编写，采用 MIT 许可证，于 2026 年 7 月发布。最近有一次推送但没有拉取请求，表明处于早期开发阶段。

ossinsight · yc-software · 8月2日 01:26

**背景**: 多玩家智能体框架允许多个 AI 智能体像人类团队一样协作，协调和委派工作。它们属于更广泛的智能体 AI 运动，利用大语言模型驱动复杂的多步骤工作流。QM 专门面向希望部署 AI 智能体集群的初创公司。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.everydev.ai/tools/qm-agent-harness">QM - Open Source Multiplayer Agent Harness | EveryDev.ai</a></li>
<li><a href="https://www.neura.market/blog/multiplayer-agent-harness-how-ai-orchestrates-team-work-in-2026">Multiplayer Agent Harness : How AI Orchestrates... | Neura Market</a></li>

</ul>
</details>

**标签**: `#TypeScript`, `#agent`, `#multiplayer`, `#open-source`, `#developer-tools`

---