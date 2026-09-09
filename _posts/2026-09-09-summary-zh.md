---
layout: default
title: "Horizon Summary: 2026-09-09 (ZH)"
date: 2026-09-09
lang: zh
---

> 从 19 条内容中筛选出 10 条重要资讯。

---

1. [OpenAI 声称借助 AI 解决纳维–斯托克斯千禧年大奖难题](#item-1) ⭐️ 9.0/10
2. [Sam Altman 转发 OpenAI 模型阶梯式改进公告](#item-2) ⭐️ 8.0/10
3. [OpenAI 发布 ChatGPT Images 2.5，改进编辑能力与生成速度](#item-3) ⭐️ 7.0/10
4. [Sam Altman 宣布在旧金山举办 GPT-6 用户庆祝聚会](#item-4) ⭐️ 7.0/10
5. [Sam Altman：AI 进展超预期，安全节奏把控刻不容缓](#item-5) ⭐️ 7.0/10
6. [开放模型动态汇总：Motif-3、GLM-5.3、Hy4-preview 及许可证更新](#item-6) ⭐️ 6.0/10
7. [OpenAI o3 在 ARC-AGI 基准上的突破耗资数百万美元](#item-7) ⭐️ 6.0/10
8. [思维链与思维树：如何为 AI 智能体选择合适的推理框架](#item-8) ⭐️ 5.0/10
9. [标题党：OpenAI 一句话生成网站将颠覆 SaaS](#item-9) ⭐️ 3.0/10
10. [Sam Altman 转发 GPT-6 Astra 在 Vending-Bench 上创纪录提升的说法](#item-10) ⭐️ 3.0/10

---

<a id="item-1"></a>
## [OpenAI 声称借助 AI 解决纳维–斯托克斯千禧年大奖难题](https://simonwillison.net/2026/Sep/8/on-navier-stokes/) ⭐️ 9.0/10

2026 年 9 月 8 日，OpenAI 宣布其一个未发布的内部模型声称解决了纳维–斯托克斯存在性与光滑性问题——七大千禧年大奖难题之一，并通过 GPT-6 Astra 完成了 Lean 形式化验证。该公告同时引发了与纽约大学教授 Tristan Buckmaster 和 Anthropic 数学家 Levent Alpöge 的优先权争议，后者已就密切相关的结果工作了近一年。 如果得到验证，这将是历史上第二个被解决的千禧年大奖难题，也是首个主要由 AI 智能体完成的重要数学突破，可能从根本上改变前沿数学的研究方式。同时，优先权争议也引发了关于科研合作伦理、数据访问以及 AI 实验室之间竞争关系的紧迫问题。 据称 OpenAI 的智能体在所有尝试的问题上共发送了 490 万条消息、使用了约 3000 亿个输出 token，其中仅纳维–斯托克斯问题就用了 270 万条消息和约 1300 亿个输出 token；按 GPT-6 Astra 公开 API 价格计算，成本约为 1500 万美元。该声明尚未经过外部数学家或克雷数学研究所验证，OpenAI 还表示如果获奖将拒绝 100 万美元奖金。

rss · Simon Willison · 9月8日 23:55

**背景**: 纳维–斯托克斯存在性与光滑性问题探讨的是三维纳维–斯托克斯方程是否总是存在光滑且全局定义的解，该方程描述流体运动，是理解湍流的核心。它是克雷数学研究所于 2000 年 5 月公布的七大千禧年大奖难题之一，每个问题悬赏 100 万美元；迄今为止只有庞加莱猜想被正式解决。OpenAI 声称的证明建立在 Diego Cordoba 和 Luis Martinez Zoroa 于 2023 年提出的方法之上，该方法用于证明相关流体方程中的爆破现象，并断言纳维–斯托克斯解在三维欧几里得空间中会发生破裂。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Navier–Stokes_existence_and_smoothness_problem">Navier–Stokes existence and smoothness problem</a></li>
<li><a href="https://en.wikipedia.org/wiki/Millennium_Prize_Problems">Millennium Prize Problems</a></li>

</ul>
</details>

**标签**: `#AI`, `#mathematics`, `#Navier-Stokes`, `#Millennium Prize`, `#research ethics`

---

<a id="item-2"></a>
## [Sam Altman 转发 OpenAI 模型阶梯式改进公告](https://twitter.com/sama/status/tweet-2097381051173913055) ⭐️ 8.0/10

Sam Altman 转发了 OpenAI 的公告，称一个新模型在多项基准测试上实现了阶梯式改进，且训练仍在进行中。 阶梯式改进意味着重大飞跃而非渐进式提升，这可能显著提高 AI 应用的性能上限，并加剧领先 AI 实验室之间的竞争。 该公告未透露模型名称、具体基准测试或改进幅度，并指出训练仍在进行中，因此最终能力尚未得到确认。

twitter · Sam Altman · 9月8日 17:46

**背景**: 阶梯式改进指的是性能突然大幅提升，而非小幅渐进式增长。OpenAI 经常使用基准测试结果来展示语言模型、推理、编程等 AI 能力的进步。Sam Altman 是 OpenAI 的首席执行官，他的转发会将官方公告传播给更广泛的技术和投资受众。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.breakingpoint.tech/p/step-function-improvement">Step Function Improvement - by Sean Byrnes</a></li>

</ul>
</details>

**标签**: `#OpenAI`, `#AI`, `#machine learning`, `#model release`, `#benchmarks`

---

<a id="item-3"></a>
## [OpenAI 发布 ChatGPT Images 2.5，改进编辑能力与生成速度](https://twitter.com/sama/status/tweet-2097410967978324010) ⭐️ 7.0/10

OpenAI 正式发布 ChatGPT Images 2.5，覆盖 ChatGPT、ChatGPT Work、Codex 和开发者 API，并推出两个新 API 模型：gpt-image-2.5-sunburst 和 gpt-image-2.5-flare。新版本改进了多轮指令遵循能力，能更可靠地保留参考照片中的主体，并提升了生成速度。 这一发布意义重大，因为 OpenAI 的图像模型已被用于生成超过 30 亿张图片，而新的编辑精度和速度提升可能对创意工作流、产品设计以及行业中的大批量图像生成流程产生显著影响。 两个 API 模型各有侧重：Sunburst 针对编辑精度要求最高的工作流进行优化，而 Flare 是快速、高质量日常生成的首选，在延迟降低 50% 的情况下提供比 GPT-Image-2 更高质量的图像。Sam Altman 指出该模型并非用于解决超难数学问题。

twitter · Sam Altman · 9月8日 19:45

**背景**: ChatGPT Images 是 OpenAI 集成在 ChatGPT 中并通过 API 提供的图像生成与编辑系统。上一版本 GPT-Image-2 已支持文生图和图像编辑，但用户在编辑出错时往往需要从头开始。Images 2.5 引入了更可靠的多轮编辑能力，用户可以精确定位图像中的特定区域并请求精确修改。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/index/introducing-chatgpt-images-2-5/">Introducing ChatGPT Images 2 . 5 | OpenAI</a></li>
<li><a href="https://developers.openai.com/api/docs/models/gpt-image-2.5-sunburst">GPT-Image-2.5 Sunburst Model | OpenAI API</a></li>
<li><a href="https://www.techradar.com/ai-platforms-assistants/chatgpt/chatgpt-images-2-5-is-out-ive-been-testing-it-for-24-hours-and-these-are-the-3-new-features-youll-actually-use">ChatGPT Images 2 . 5 is out — I’ve been testing it for 24... | TechRadar</a></li>

</ul>
</details>

**社区讨论**: 社区对该公告的参与度很高，获得了 1.25 万次点赞、748 次转发和 579 条回复，表明用户对新版本兴趣浓厚。知名开发者 Simon Willison 迅速升级了他的 openai_image.py 命令行工具以支持参考图片，并通过一个实际示例展示了新模型的编辑能力。

**标签**: `#OpenAI`, `#AI`, `#image-generation`, `#model-release`, `#announcement`

---

<a id="item-4"></a>
## [Sam Altman 宣布在旧金山举办 GPT-6 用户庆祝聚会](https://twitter.com/sama/status/tweet-2097404861642137851) ⭐️ 7.0/10

Sam Altman 宣布将于 9 月 16 日在旧金山举办一场与 GPT-6 用户共同庆祝的线下聚会，此前 GPT-5.5 也举办过类似活动。活动报名截止日期为 9 月 10 日。 这一公告间接确认 GPT-6 已推进到 OpenAI 愿意与用户共同庆祝的阶段，暗示该重要模型已接近发布或已经发布。同时也表明 OpenAI 持续通过线下活动加强围绕旗舰模型的社区互动。 活动内容主要包括讨论模型本身、收集用户对下一步开发方向的建议，以及非正式交流。公告中未提供 GPT-6 的任何技术规格或发布细节。

twitter · Sam Altman · 9月8日 19:21

**背景**: GPT-6 是 OpenAI 生成式预训练 Transformer 系列中备受期待的第六代主要版本，接替 GPT-5 系列。根据搜索结果，GPT-6 Astra 已于 2026 年 9 月 3 日向获批用户初步发布，次日全面开放。此前的 GPT-5.5 于 2026 年 4 月 23 日发布，OpenAI 也曾为其举办过类似的社区庆祝活动。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/GPT-6_Astra">GPT-6 Astra - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/GPT-5.5">GPT-5.5</a></li>

</ul>
</details>

**标签**: `#OpenAI`, `#GPT-6`, `#AI`, `#community-event`, `#Sam-Altman`

---

<a id="item-5"></a>
## [Sam Altman：AI 进展超预期，安全节奏把控刻不容缓](https://twitter.com/sama/status/tweet-2097380833388790253) ⭐️ 7.0/10

OpenAI 首席执行官 Sam Altman 表示，如今世界已拥有能力极强的 AI 模型，他没想到如此量级的成果会来得这么快。他将这种超预期的速度称为迄今为止最有力的证据，说明必须加快节奏把控 AI 进展以确保安全。 作为 AI 领域的关键人物，Altman 承认进展速度超出了他自己的预期，这表明即便是业内人士也对能力提升的速度感到意外。这可能加大企业和监管机构采取更强安全措施与治理框架的压力。 该声明较为简短，未具体说明他所指的是哪些模型或能力，也未提出具体的安全机制。该帖在 X 平台上获得了 2149 个赞和 159 条回复，显示出社区的高度关注。

twitter · Sam Altman · 9月8日 17:45

**背景**: Sam Altman 是 OpenAI 的首席执行官，该公司开发了 GPT-4 和 ChatGPT 等广泛使用的模型。近年来，他多次呼吁对 AI 进行监管，并讨论在快速发展与安全考量之间取得平衡的必要性。“把控进展节奏”这一说法反映了当前关于 AI 能力是否正在以超出社会风险管理能力的速度发展的持续争论。

**标签**: `#AI safety`, `#AI progress`, `#OpenAI`, `#industry commentary`, `#AI governance`

---

<a id="item-6"></a>
## [开放模型动态汇总：Motif-3、GLM-5.3、Hy4-preview 及许可证更新](https://www.interconnects.ai/p/latest-open-artifacts-24-motif-3) ⭐️ 6.0/10

一篇新综述重点介绍了近期开放模型成果，包括 Motif-3、GLM-5.3 和腾讯的 Hy4-preview，以及开放模型许可证的更新。文章将这些发布视为开放模型生态广度持续扩展的体现。 跟踪多个开放模型发布和许可证变化，有助于开发者和研究人员了解可自由使用的 AI 模型格局的演变。尤其是许可证更新，会直接影响组织使用、修改或部署这些模型的方式。 根据 Artificial Analysis，Motif-3 于 2026 年 8 月 12 日发布；GLM-5.3 在 CyberGym 漏洞发现方面表现领先，并在漏洞利用基准上比 GLM-5.2 提升一倍以上；Hy4-preview 是腾讯的混合专家模型，总参数 770B，其中活跃参数 49B。

rss · Interconnects · 9月8日 14:15

**背景**: 开放模型成果指的是权重或其他组件被公开发布的 AI 模型，通常采用 MIT 或 Apache 2.0 等宽松许可证。GLM 是中国 AI 公司 Z.ai 开发的一系列开放权重大语言模型，大多数权重以 MIT 或 Apache 2.0 许可证发布。像 Hy4-preview 这样的混合专家模型，每次输入只激活总参数中的一部分，从而在保持较大总容量的同时提高效率。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://artificialanalysis.ai/models/motif-3">Motif 3 - Intelligence, Performance & Price Analysis | Artificial Analysis</a></li>
<li><a href="https://en.wikipedia.org/wiki/GLM-5.3">GLM-5.3</a></li>
<li><a href="https://huggingface.co/tencent/Hy4-preview">tencent/ Hy 4 - preview · Hugging Face</a></li>

</ul>
</details>

**标签**: `#open-source`, `#AI models`, `#licensing`, `#model releases`, `#ecosystem`

---

<a id="item-7"></a>
## [OpenAI o3 在 ARC-AGI 基准上的突破耗资数百万美元](https://twitter.com/sama/status/tweet-2097449884530131057) ⭐️ 6.0/10

Sam Altman 转发了一条评论，指出 OpenAI 的 o3 模型在 ARC-AGI 基准上取得 87.5%的成绩花费了约 50 万美元，而最新的成果则耗资数百万美元。 这条转发凸显了前沿 AI 推理模型巨大的计算成本，说明经济约束可能影响通向通用智能的进展速度和可及性。 o3 模型以约 50 万美元的成本在 ARC-AGI 上取得 87.5%的成绩，而推文中提到的最新结果据称耗资数百万美元，表明推理成本急剧上升。

twitter · Sam Altman · 9月8日 22:19

**背景**: ARC-AGI 是一个通过抽象推理任务衡量通用人工智能进展的基准。OpenAI o3 是一种推理模型，会在需要逐步逻辑推理的问题上投入额外计算时间，从而提升在 ARC-AGI 等基准上的表现，但推理成本也显著增加。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/OpenAI_o3">OpenAI o3 - Wikipedia</a></li>
<li><a href="https://arcprize.org/arc-agi">ARC Prize - What is ARC-AGI?</a></li>
<li><a href="https://arcprize.org/leaderboard">ARC-AGI-3 Leaderboard</a></li>

</ul>
</details>

**标签**: `#AI`, `#OpenAI`, `#model-cost`, `#benchmarks`, `#machine-learning`

---

<a id="item-8"></a>
## [思维链与思维树：如何为 AI 智能体选择合适的推理框架](https://machinelearningmastery.com/chain-of-thought-vs-tree-of-thoughts-which-is-best-for-ai-agents/) ⭐️ 5.0/10

Machine Learning Mastery 发布了一篇入门文章，比较了面向 AI 智能体的思维链（CoT）与思维树（ToT）提示框架，解释了每种技术如何组织推理以及何时使用它们。 随着基于大语言模型的智能体承担越来越复杂的任务，选择合适的推理框架会直接影响准确性、可靠性和成本。这一比较有助于实践者在线性逐步推理与分支探索之间做出选择，这对于构建稳健的 AI 应用日益重要。 思维链提示由 Wei 等人于 2022 年提出，以线性序列生成中间推理步骤；思维树由 Yao 等人于 2023 年提出，允许模型以树状结构探索并自我评估多条推理路径。该文章属于入门级别而非深度技术内容，且没有社区评论可供评估实践者的反馈。

rss · Machine Learning Mastery · 9月8日 14:29

**背景**: 提示工程是设计自然语言输入以引导生成式 AI 模型产生预期输出的实践。思维链提示通过要求模型在给出最终答案前生成中间步骤来提升复杂推理能力。思维树则扩展了这一思路，生成多条候选推理路径并进行评估，适用于需要规划、搜索或回溯的任务。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.promptingguide.ai/techniques/cot">Chain-of-Thought Prompting | Prompt Engineering Guide</a></li>
<li><a href="https://learnprompting.org/docs/advanced/decomposition/tree_of_thoughts">Tree of Thoughts (ToT): Enhancing Problem-Solving in LLMs</a></li>
<li><a href="https://www.ibm.com/think/topics/tree-of-thoughts">What is Tree Of Thoughts Prompting ? | IBM</a></li>

</ul>
</details>

**标签**: `#prompting`, `#AI agents`, `#LLM`, `#reasoning`, `#tutorial`

---

<a id="item-9"></a>
## [标题党：OpenAI 一句话生成网站将颠覆 SaaS](https://mp.weixin.qq.com/s?__biz=MzI3MTA0MTk1MA==&mid=2652723806&idx=2&sn=ddb2b4f9df893f5c8a5725f79750fe4d) ⭐️ 3.0/10

一篇低质量文章声称 OpenAI 的一句话生成网站能力将颠覆 SaaS，但除了标题和一句宣传性内容外，几乎没有提供任何实质性信息。 这类耸人听闻的报道可能误导读者对 AI 网站生成实际能力和局限性的认知，对既有 SaaS 商业模式被立即颠覆产生不切实际的期待。 文章没有提供任何具体的技术细节、基准测试、产品名称或版本号来支撑其说法，3.0/10 的评分也反映了其缺乏深度和宣传性标题党的本质。

rss · 新智元 · 9月8日 03:32

**背景**: SaaS（软件即服务）是一种云计算模式，供应商通过互联网向客户交付应用软件，并管理底层基础设施。OpenAI 是一家美国人工智能公司，以开发 GPT 系列和 ChatGPT 等生成式 AI 模型而闻名。AI 辅助网站生成已越来越普遍，但声称它会立即消除 SaaS 护城河的说法通常被夸大。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/SaaS">SaaS</a></li>
<li><a href="https://en.wikipedia.org/wiki/OpenAI">OpenAI</a></li>

</ul>
</details>

**标签**: `#AI`, `#SaaS`, `#OpenAI`, `#web development`, `#clickbait`

---

<a id="item-10"></a>
## [Sam Altman 转发 GPT-6 Astra 在 Vending-Bench 上创纪录提升的说法](https://twitter.com/sama/status/tweet-2097394039557628115) ⭐️ 3.0/10

Sam Altman 转发了 Andon Labs 的一条宣传帖，声称 GPT-6 Astra 在 Vending-Bench 上实现了历史上最大的性能跃升，并称其在赚钱和道德方面都更出色。 这一转发表明 OpenAI 领导层认可第三方对 GPT-6 Astra 的基准测试结果，可能影响公众对自主 AI 智能体在商业决策场景中应用的看法和采用。 该说法没有提供直接来源链接或具体性能数据，且推文在句子中间被截断，难以核实改进的确切幅度或所采用的测试方法。

twitter · Sam Altman · 9月8日 18:38

**背景**: Vending-Bench 是 Andon Labs 于 2025 年开发的基准测试套件，通过模拟自动售货机业务来评估基于大语言模型的自主智能体的长期连贯性和决策能力。GPT-6 Astra 是 OpenAI 最新的大语言模型，于 2026 年 9 月发布，被 OpenAI 称为迄今最强大、最对齐的模型。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://grokipedia.com/page/Vending-Bench">Vending-Bench</a></li>
<li><a href="https://andonlabs.com/evals/vending-bench">Vending - Bench : Testing long-term coherence in agents | Andon Labs</a></li>
<li><a href="https://en.wikipedia.org/wiki/GPT-6_Astra">GPT-6 Astra</a></li>

</ul>
</details>

**标签**: `#AI`, `#benchmarks`, `#promotional`, `#GPT-6`, `#Twitter`

---