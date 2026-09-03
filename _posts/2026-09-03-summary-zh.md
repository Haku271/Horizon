---
layout: default
title: "Horizon Summary: 2026-09-03 (ZH)"
date: 2026-09-03
lang: zh
---

> 从 5 条内容中筛选出 5 条重要资讯。

---

1. [Paint.NET 发布由 Claude 生成的 Direct2D 净室重写以支持 WINE](#item-1) ⭐️ 8.0/10
2. [Claude Fable/Mythos 5.1 发布，缓存价格下调 75%](#item-2) ⭐️ 7.0/10
3. [llm-gemini 0.34 新增 Gemini 3.8 Flash 支持](#item-3) ⭐️ 6.0/10
4. [Claude 新系统提示词明确拒绝复现歌词](#item-4) ⭐️ 6.0/10
5. [AI 智能体记忆设计：哪些模式有效，哪些会失败](#item-5) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [Paint.NET 发布由 Claude 生成的 Direct2D 净室重写以支持 WINE](https://simonwillison.net/2026/Sep/2/rick-brewster/) ⭐️ 8.0/10

Paint.NET 现在内置了一个从零开始、净室逆向工程重写的 Direct2D 实现，通过 /wine 参数触发，使该应用能够在 WINE 下运行。这个位于 PaintDotNet.Windows.Direct2D1.Managed.dll 中的 18 万行实现主要由 Claude 生成，作者 Rick Brewster 承认其中大部分是未经审查的“氛围编程”代码。 这标志着 AI 辅助软件开发的一个重要里程碑，表明一个主流应用可以发布几乎完全由 LLM 生成的复杂底层子系统。它同时消除了 Paint.NET 在 Linux 上运行的最大障碍，但也引发了关于生产软件中 AI 生成代码的代码审查、信任和长期可维护性的严肃问题。 该重写位于 PaintDotNet.Windows.Direct2D1.Managed.dll 中，通过 /wine 命令行参数激活。Brewster 指出他不得不反复纠正 Claude 在 COM 引用计数（AddRef/Release）方面的错误，并否决了一些糟糕的架构决策，同时称赞了它在逆向 Direct2D 内置效果公式时表现出的不懈努力。

rss · Simon Willison · 9月2日 05:50

**背景**: Direct2D 是微软的硬件加速 2D 图形 API，许多 Windows 应用依赖它进行高性能渲染。WINE 是一个兼容层，通过重新实现 Windows API 让 Windows 软件能在 Linux 等类 Unix 系统上运行，但其 Direct2D 支持历来不完整。净室逆向工程是一种法律上较安全的做法：由一个团队检查原系统并编写规范，再由另一个未接触原始代码的团队独立实现。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Direct2D">Direct2D</a></li>
<li><a href="https://en.wikipedia.org/wiki/Wine_compatibility_layer">Wine compatibility layer</a></li>
<li><a href="https://en.wikipedia.org/wiki/Clean-room_reverse_engineering">Clean-room reverse engineering</a></li>

</ul>
</details>

**标签**: `#AI-assisted development`, `#WINE`, `#Direct2D`, `#reverse engineering`, `#software engineering`

---

<a id="item-2"></a>
## [Claude Fable/Mythos 5.1 发布，缓存价格下调 75%](https://www.latent.space/p/ainews-claude-fablemythos-51-new) ⭐️ 7.0/10

Anthropic 发布了 Claude Fable 5.1 和 Claude Mythos 5.1，这一新的最先进模型系列将提示缓存价格下调了 75%，同时输出 token 数量增加了约 70%。 新的最先进模型与 75% 的缓存降价相结合，直接降低了生产环境 LLM 团队的推理成本，使先进 AI 更加经济实惠，并可能加速整个行业的采用。 Claude Mythos 5.1 与 Fable 5.1 相同，但为受网络安全和生命科学限制影响的经过审查的个人和组织提供更宽松的安全防护；输出 token 增加 70% 可能会部分抵消缓存节省的成本。

rss · Latent Space · 9月2日 07:46

**背景**: 提示缓存会存储重复的提示前缀，使后续请求对已缓存 token 按更低价格计费，通常可在不改变模型输出的情况下将输入成本降低多达 90%。Anthropic 的 Claude 模型系列是 OpenAI GPT 系列的主要竞争对手，Fable/Mythos 的命名用于区分公开版本和受限访问版本。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.anthropic.com/claude-fable-and-mythos-5-1">Introducing Claude Fable 5 . 1 and Claude Mythos 5 . 1 \ Anthropic</a></li>
<li><a href="https://en.wikipedia.org/wiki/Claude_(AI)">Claude (AI) - Wikipedia</a></li>
<li><a href="https://www.digitalapplied.com/blog/prompt-caching-2026-cut-llm-costs-engineering-guide">Prompt Caching in 2026: Cut LLM Costs, Keep Quality</a></li>

</ul>
</details>

**标签**: `#AI`, `#LLM`, `#model release`, `#pricing`, `#Latent Space`

---

<a id="item-3"></a>
## [llm-gemini 0.34 新增 Gemini 3.8 Flash 支持](https://simonwillison.net/2026/Sep/2/llm-gemini/) ⭐️ 6.0/10

Simon Willison 发布了 llm-gemini 0.34，新增对谷歌 Gemini 3.8 Flash 模型的支持，提供低、中、高三档思考级别，并修复了异步响应无法记录已解析模型版本的 bug。 此次更新让 llm-gemini 用户能够立即以 Flash 级别的速度和成本使用 Gemini 3.8 Flash 的高级推理能力，更方便地用于编码和知识型工作。 Gemini 3.8 Flash 支持 100 万 token 上下文窗口、最大 64k 输出 token 以及可调节的思考级别；异步 bug 修复由 Charlie Tonneslan 在 PR #137 中贡献。

rss · Simon Willison · 9月2日 16:39

**背景**: llm-gemini 是 Simon Willison 开发的 llm 命令行工具插件，用于在终端中访问谷歌的 Gemini 模型。Gemini Flash 是谷歌面向高吞吐量任务设计的快速、低成本模型系列，而思考级别控制模型在回答前进行多少推理。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://ai.google.dev/gemini-api/docs/latest-model">What's new in Gemini 3.8 Flash | Gemini API | Google AI for Developers</a></li>
<li><a href="https://deepmind.google/models/gemini/flash/">Gemini 3.8 Flash — Google DeepMind</a></li>
<li><a href="https://en.wikipedia.org/wiki/Gemini_(language_model)">Gemini (language model) - Wikipedia</a></li>

</ul>
</details>

**标签**: `#llm-gemini`, `#Gemini`, `#Google`, `#AI tools`, `#plugin release`

---

<a id="item-4"></a>
## [Claude 新系统提示词明确拒绝复现歌词](https://simonwillison.net/2026/Sep/2/claudes-new-system-prompt/) ⭐️ 6.0/10

Anthropic 更新了 Claude 消费级应用已发布的系统提示词，新增一大段指令，要求 Claude 不得整体或部分复现歌词、诗歌以及书籍和文章中的段落。这一变化出现在 Claude Fable 5 与 Fable 5.1 的差异对比中，同时 Anthropic 还将系统提示词文档重新整理为按模型分页的结构。 这一变化反映出 AI 提供商正面临越来越大的压力，需要降低逐字复现受版权保护作品所带来的侵权风险。由于 Anthropic 公开其系统提示词及修订历史，研究人员和用户可以准确追踪模型行为是如何被引导的，这为外界观察 AI 安全与法律合规决策提供了少见的公开视角。 新指令要求 Claude 即使面对部分复现也要拒绝，例如副歌、记忆点、逐音符写出的旋律，或用户逐行粘贴并声称是自己歌曲的歌词，并且在整个对话剩余部分中都要继续拒绝更窄化或改写后的请求。1929 年之前首次发表的作品可以例外，但 Claude 依据自己对作品年代的了解来判断，不确定时也会拒绝。

rss · Simon Willison · 9月2日 14:16

**背景**: 系统提示词是一组隐藏指令，在任何用户交互开始之前就定义了 AI 模型的行为和限制。Anthropic 公开了 Claude.ai 和 Claude 移动应用的系统提示词，包括历史变更，这在主要 AI 提供商中并不常见。platform.claude.com/docs 网站专门设计为对 LLM 友好，用户可以在任意页面后添加 .md 来获取 Markdown 格式内容，从而便于对提示词变化进行差异对比。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.promptlayer.com/glossary/system-prompt/">What is a System prompt? | PromptLayer</a></li>
<li><a href="https://en.wikipedia.org/wiki/System_prompt">System prompt</a></li>

</ul>
</details>

**标签**: `#Anthropic`, `#Claude`, `#system prompts`, `#AI behavior`, `#copyright`

---

<a id="item-5"></a>
## [AI 智能体记忆设计：哪些模式有效，哪些会失败](https://machinelearningmastery.com/ai-agent-memory-design-what-works-and-what-doesnt/) ⭐️ 6.0/10

MachineLearningMastery 发布了一篇教程式文章，讲解 AI 智能体可靠记忆系统的设计模式，并指出需要避免的常见架构陷阱。 随着 AI 智能体从单轮聊天机器人发展为多步骤自主系统，持久化记忆成为可靠性和用户体验的关键差异点，因此实用的架构指导对构建生产级 LLM 应用的开发者很有价值。 文章区分了状态管理与长期记忆，涵盖基于嵌入的检索、混合记忆和时间线流等模式，并强调记忆写入路径应当非阻塞且具备容错能力。

rss · Machine Learning Mastery · 9月2日 11:49

**背景**: AI 智能体记忆是指让智能体跨交互和会话存储、检索并推理信息的基础设施。常见方法包括用于语义搜索的向量数据库、记录过往经历的情景记忆，以及提炼知识后的语义记忆。一个反复出现的难题是“智能体失忆”，即基于 LLM 的系统在会话之间忘记先前的上下文。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://machinelearningmastery.com/5-architectural-patterns-for-persistent-memory-and-state-in-ai-agents/">5 Architectural Patterns for Persistent Memory and State in AI Agents - MachineLearningMastery.com</a></li>
<li><a href="https://www.varunpratap.com/blog/universal-memory-layer-ai-agents-architecture-patterns">Building a Universal Memory Layer for AI Agents: Architecture Patterns for Scalable State Management</a></li>
<li><a href="https://www.trixlyai.com/blog/technical-14/building-memory-in-ai-agents-design-patterns-and-datastores-that-enable-long-term-intelligence-87">Building Memory in AI Agents: Design Patterns and Datastores That Enable Long-Term Intelligence - Blogs - Trixly AI Solutions</a></li>

</ul>
</details>

**标签**: `#AI agents`, `#memory systems`, `#software architecture`, `#LLM applications`, `#tutorial`

---