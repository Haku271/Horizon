---
layout: default
title: "Horizon Summary: 2026-09-10 (ZH)"
date: 2026-09-10
lang: zh
---

> 从 17 条内容中筛选出 9 条重要资讯。

---

1. [Quoting Calif Research](#item-1) ⭐️ 9.0/10
2. [(AINews) OpenAI reports Navier-Stokes singularity find in 88 hours using Astra-next, roughly 10,000 agents and 130B tokens (>$40M), a contender for second ever Millennium Prize awarded](#item-2) ⭐️ 9.0/10
3. [vLLM v0.29.0 将 Model Runner V2 设为默认并新增多款模型](#item-3) ⭐️ 8.0/10
4. [免训练 LoRA 合并框架：单样本校准、零推理开销](#item-4) ⭐️ 7.0/10
5. [AI 对日常生活的影响仍处于早期阶段](#item-5) ⭐️ 7.0/10
6. [机器人在哪里思考：端侧推理与数据中心推理的权衡](#item-6) ⭐️ 7.0/10
7. [使用 MLflow 对 Scikit-LLM 实验进行版本管理与跟踪的教程](#item-7) ⭐️ 5.0/10
8. [Simon Willison 推出浏览器版 .blend 查看器并实验 AI 生成法贝热彩蛋](#item-8) ⭐️ 4.0/10
9. [Sam Altman 欢迎 Paul 加入 OpenAI 从事 AI 安全工作](#item-9) ⭐️ 3.0/10

---

<a id="item-1"></a>
## [Quoting Calif Research](https://simonwillison.net/2026/Sep/10/calif-research/) ⭐️ 9.0/10

Calif Research announces WeWorm, the first zero-click worm spreading through WeChat calls on iOS and Android, developed in about two days with AI assistance.

rss · Simon Willison · 9月10日 00:56

**标签**: `#security`, `#zero-click`, `#AI-assisted-exploit`, `#mobile-security`, `#WeChat`

---

<a id="item-2"></a>
## [(AINews) OpenAI reports Navier-Stokes singularity find in 88 hours using Astra-next, roughly 10,000 agents and 130B tokens (>$40M), a contender for second ever Millennium Prize awarded](https://www.latent.space/p/ainews-openai-reports-navier-stokes) ⭐️ 9.0/10

OpenAI reportedly used ~10,000 agents and 130B tokens to find a Navier-Stokes singularity in 88 hours, potentially qualifying for a Millennium Prize.

rss · Latent Space · 9月9日 05:04

**标签**: `#AI`, `#mathematics`, `#Navier-Stokes`, `#OpenAI`, `#scientific-discovery`

---

<a id="item-3"></a>
## [vLLM v0.29.0 将 Model Runner V2 设为默认并新增多款模型](https://github.com/vllm-project/vllm/releases/tag/v0.29.0) ⭐️ 8.0/10

vLLM v0.29.0 将 Model Runner V2 设为所有模型的默认执行核心，完成了从池化模型开始的推广。该版本还新增了对 Hy4-preview、Qwen3.8-Flash-Next、GraniteSWA 和 Kimi K3 NVFP4 检查点等模型的支持，并引入了批量分片采样和 CUDA 图内存分析。 作为使用最广泛的 LLM 推理引擎之一，vLLM 向 Model Runner V2 的架构转变及其性能优化可显著降低生产 AI 系统的服务延迟和内存占用。新增的模型支持还使组织能够更高效地部署腾讯 770B MoE 和 Kimi K3 等前沿模型。 Model Runner V2 现在包含用于 KV 缓存自动调整的 CUDA 图内存分析、将每步 logits 内存降低 1/TP 的批量分片采样，以及 EAGLE/MTP 草稿预填充前的 DP 同步跳过。MRV1 仍用于少数 ROCm 模型和 MRV2 尚不支持的功能，同时十个已弃用的模型架构被移除，属于破坏性变更。

github · khluu · 9月9日 08:54

**背景**: vLLM 是一个用于高吞吐量 LLM 推理和服务的开源库，在生产 AI 部署中被广泛采用。Model Runner V2 是对 vLLM 执行核心的重新设计，引入了模块化模型逻辑、GPU 原生输入准备、稳定的持久批处理和异步优先调度，以解决原始 V1 设计中积累的技术债务。CUDA 图通过捕获 GPU 操作来减少内核启动开销，而内存分析有助于自动调整 KV 缓存大小以获得最佳性能。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://docs.vllm.ai/en/latest/design/model_runner_v2/">Model Runner V2 Design Document - vLLM</a></li>
<li><a href="https://vllm.ai/blog/2026-03-24-mrv2">Model Runner V2: A Modular and Faster Core for vLLM</a></li>
<li><a href="https://kimbodo.com/reduce-llm-inference-cost-and-latency-with-new-open-weights-vllm-mrv2-and-llama-cpp-kernel-optimizations/">Reduce LLM Inference Cost and Latency with... | Kimbodo AI Research</a></li>

</ul>
</details>

**标签**: `#vLLM`, `#LLM inference`, `#release`, `#AI infrastructure`, `#model serving`

---

<a id="item-4"></a>
## [免训练 LoRA 合并框架：单样本校准、零推理开销](https://mp.weixin.qq.com/s?__biz=MzIzNjc1NzUzMw==&mid=2247920779&idx=3&sn=18f5eb81b14b5d60903503df5a463897) ⭐️ 7.0/10

一个免训练的 LoRA 合并框架被公布，该框架将合并问题重新定义为信号路由，而非参数算术。它只需要一个校准样本，并且不会增加推理开销。 该方法可以显著简化和加速多个微调 LoRA 适配器的部署，使模型定制在资源受限环境和实时应用中更加实用。 该框架被描述为免训练，仅需一个校准样本，且推理开销为零。不过，ICML'26 的说法似乎为时过早或未经证实，且来源是一篇推广性质的微信公众号文章。

rss · 量子位 · 9月9日 11:12

**背景**: LoRA（低秩适配）是一种流行的高效微调大语言模型技术，通过训练小型低秩适配矩阵而非更新全部模型参数来实现。合并多个 LoRA 适配器通常涉及参数组合，这可能计算成本高昂或导致性能下降。现有合并方法多依赖参数算术或聚类，而该新框架将合并视为信号路由问题。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2409.16167">[2409.16167] Merging LoRAs like Playing LEGO: Pushing the Modularity of LoRA to Extremes Through Rank-Wise Clustering</a></li>
<li><a href="https://llamafactory.readthedocs.io/en/latest/getting_started/merge_lora.html">Model Saving, LoRA Merging, and Quantization - LlamaFactory</a></li>

</ul>
</details>

**标签**: `#LoRA`, `#model-merging`, `#efficient-ML`, `#ICML`, `#fine-tuning`

---

<a id="item-5"></a>
## [AI 对日常生活的影响仍处于早期阶段](https://www.interconnects.ai/p/when-will-average-people-feel-ais) ⭐️ 7.0/10

Nathan Lambert 提出，我们正处于一场可能持续一个世纪的复合型 AI 革命的不到五年阶段，并讨论了 AI 行业应如何管理这一发展轨迹。 这一观点重新设定了对 AI 普及的预期，表明 AI 对普通人的变革性影响可能需要数十年而非数年，这可能影响投资、政策和公众对 AI 的认知。 Lambert 将 AI 进展视为一种复合型革命而非单一事件，意味着早期的基础设施和研究收益会随时间累积；文章侧重于行业管理，而非具体的技术基准。

rss · Interconnects · 9月9日 11:01

**背景**: AI 普及的时间线在研究人员和评论者中存在争议：一些人预计日常生活会很快被颠覆，而另一些人则认为，像电力或互联网这样的通用技术带来的重大社会变革需要数十年才能显现。Nathan Lambert 是一位知名的 AI 评论员，以撰写 AI 政策、研究和行业动态文章而闻名。

**标签**: `#AI adoption`, `#technology impact`, `#AI industry`, `#future of AI`, `#commentary`

---

<a id="item-6"></a>
## [机器人在哪里思考：端侧推理与数据中心推理的权衡](https://newsletter.semianalysis.com/p/where-does-a-robot-think-on-device) ⭐️ 7.0/10

SemiAnalysis 发布了一篇分析文章，探讨机器人 AI 推理在端侧设备上直接运行与卸载到数据中心基础设施之间的架构权衡。 推理位置的选择会影响物理 AI 系统的延迟、隐私、可靠性和成本，并将在人形机器人和工业自动化规模扩大时塑造机器人开发者的产品设计方式。 这篇文章讨论了一个及时的机器人系统架构问题，但所提供的摘录内容过于有限，无法评估其完整技术深度或所讨论的具体基准测试。

rss · Semianalysis · 9月9日 20:53

**背景**: 端侧推理是指 AI 模型在机器人机载计算机等本地硬件上运行，避免了网络往返，但受限于功耗和算力。数据中心推理将数据发送到功能强大的远程服务器，提供更强的计算能力，但会引入延迟和对网络连接的依赖。对于必须对物理环境做出实时反应的机器人来说，这种权衡尤为关键。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://grokipedia.com/page/Local_inference">Local inference</a></li>
<li><a href="https://datacentersx.com/datacenter-inference.html">Data Center Inference Overview | DatacentersX</a></li>
<li><a href="https://www.nvidia.com/en-us/industries/robotics/">NVIDIA AI Robotics – From Simulation to Deployment</a></li>

</ul>
</details>

**标签**: `#robotics`, `#AI inference`, `#edge computing`, `#datacenter`, `#systems architecture`

---

<a id="item-7"></a>
## [使用 MLflow 对 Scikit-LLM 实验进行版本管理与跟踪的教程](https://machinelearningmastery.com/versioning-and-tracking-scikit-llm-experiments/) ⭐️ 5.0/10

Machine Learning Mastery 发布了一篇教程，展示如何使用 Scikit-LLM 和 MLflow 构建、跟踪、比较并注册集成了大语言模型的 scikit-learn 流水线。 该教程填补了 ML 从业者的一个实际空白：他们希望将基于大语言模型的组件引入标准 scikit-learn 工作流，同时保留实验跟踪和模型注册能力。 该教程涵盖 Scikit-LLM 与 scikit-learn 流水线的集成，以及 MLflow 的日志记录、对比和模型注册等功能，但并未在现有开源项目之外引入新的工具或方法。

rss · Machine Learning Mastery · 9月9日 12:00

**背景**: scikit-learn 是一个广泛使用的开源 Python 机器学习库，而 Scikit-LLM 是一个允许用户将 ChatGPT 等大语言模型集成到 scikit-learn 工作流中的项目。MLflow 是一个用于管理机器学习生命周期的开源平台，包括实验跟踪、打包、部署和模型注册。将这些工具结合使用，可以让从业者把基于大语言模型的文本分析步骤作为可复现、可跟踪的 ML 流水线的一部分来处理。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Scikit-learn">Scikit-learn</a></li>
<li><a href="https://github.com/fnnx-ai/scikit-llm">GitHub - fnnx-ai/scikit-llm: Seamlessly integrate LLMs into ...</a></li>
<li><a href="https://grokipedia.com/page/MLflow">MLflow</a></li>

</ul>
</details>

**标签**: `#MLOps`, `#scikit-learn`, `#LLM`, `#MLflow`, `#experiment-tracking`

---

<a id="item-8"></a>
## [Simon Willison 推出浏览器版 .blend 查看器并实验 AI 生成法贝热彩蛋](https://simonwillison.net/2026/Sep/9/blender-viewer/) ⭐️ 4.0/10

Simon Willison 发布了一个基于浏览器的 .blend URL 查看器，可直接在网页中渲染 Blender 文件，并用它展示了一个由 GPT-6 Astra 根据 ChatGPT Images 2.5 参考图生成的法贝热彩蛋模型。 这展示了一种将 AI 图像生成、AI 辅助 Blender 建模和浏览器 3D 预览结合起来的实用工作流，有望降低无需安装 Blender 即可分享和查看 3D 资产的门槛。 该查看器通过 jsDelivr 解析 GitHub URL 来加载 .blend 文件，示例模型包含 783,764 个顶点、1,446,560 个三角形和 17 种材质，预览中材质为近似效果，未应用的修改器会被省略。

rss · Simon Willison · 9月9日 23:58

**背景**: Blender 是一款免费开源的 3D 图形套件，其原生 .blend 格式用于存储模型、动画和场景。GPT-6 Astra 是 OpenAI 于 2026 年 9 月发布的大语言模型，具备编码和计算机操作能力；ChatGPT Images 2.5 是 OpenAI 最新的图像生成模型。法贝热彩蛋最初是为俄国沙皇制作的华丽珠宝彩蛋。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Blend_(file_format)">Blend (file format)</a></li>
<li><a href="https://en.wikipedia.org/wiki/GPT-6_Astra">GPT-6 Astra</a></li>
<li><a href="https://chatgpt.com/features/images/">ChatGPT Images 2.5 | AI Image Generator</a></li>

</ul>
</details>

**标签**: `#blender`, `#ai-image-generation`, `#personal-project`, `#tooling`

---

<a id="item-9"></a>
## [Sam Altman 欢迎 Paul 加入 OpenAI 从事 AI 安全工作](https://twitter.com/sama/status/tweet-2097776310940569783) ⭐️ 3.0/10

Sam Altman 在 X 上发布了一条简短消息，欢迎一位名叫 Paul 的人，感谢他过去对 AI 安全的贡献，并表示很高兴能再次共事。该帖子没有说明 Paul 的具体职位、头衔或入职时间。 这条消息表明 OpenAI 正在引入或重新启用一位具有 AI 安全经验的人，这可能意味着在业界围绕 AI 风险展开广泛讨论的背景下，OpenAI 继续或重新关注安全问题。但由于缺乏职位细节，实际影响仍不明确。 该帖子没有包含任何技术细节、具体职位名称，也没有关于 Paul 的背景或职责的信息。这只是一条纯社交性质的欢迎消息，信息量有限。

twitter · Sam Altman · 9月9日 19:57

**背景**: Sam Altman 是 OpenAI 的首席执行官，OpenAI 是 ChatGPT 及其他大型语言模型背后的公司。AI 安全是该领域的重要议题，涉及确保 AI 系统可靠运行且不造成伤害的努力。OpenAI 领导层的人事公告往往受到关注，因为该公司与安全相关的团队曾经历引人注目的离职和招聘。

**标签**: `#AI safety`, `#OpenAI`, `#personnel announcement`, `#Sam Altman`

---