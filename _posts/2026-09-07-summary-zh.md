---
layout: default
title: "Horizon Summary: 2026-09-07 (ZH)"
date: 2026-09-07
lang: zh
---

> 从 12 条内容中筛选出 7 条重要资讯。

---

1. [OpenAI 拥抱编码智能体与递归自我改进](#item-1) ⭐️ 8.0/10
2. [DNS 主要成为诈骗传播渠道，新 gTLD 域名滥用率高达 10% 至 20%](#item-2) ⭐️ 7.0/10
3. [Simon Willison：从零重写很少能解决技术债务](#item-3) ⭐️ 7.0/10
4. [OpenAI 联合创始人 Greg Brockman 宣布进入 AGI 时代](#item-4) ⭐️ 7.0/10
5. [Greg Brockman 推荐用 Astra 检查科学论文](#item-5) ⭐️ 7.0/10
6. [报道称 GPT-6 已完成训练，更强模型即将发布](#item-6) ⭐️ 6.0/10
7. [Sam Altman 转发一条指向 Jakub 的神秘帖子](#item-7) ⭐️ 3.0/10

---

<a id="item-1"></a>
## [OpenAI 拥抱编码智能体与递归自我改进](https://simonwillison.net/2026/Sep/6/research-acceleration-the-view-inside-openai/) ⭐️ 8.0/10

OpenAI 公布了内部数据，显示每位研究人员在编码智能体上的日均支出从 2026 年 2 月接近零增长到 8 月底约 600 美元。公司还引入了递归自我改进（RSI）作为 AGI 的新表述，并在研究加速文章和首席科学家 Jakub Pachocki 的文章《An Alien Mind》中进行了讨论。 这一内部视角证实了智能体工程已成为 OpenAI 自身研究流程的核心，标志着整个行业正加速转向 AI 辅助软件开发。将 AGI 的框架转向递归自我改进，也把领域焦点重新引向能够自我增强能力的系统，这对 AI 安全和发展时间表具有重大影响。 图表显示 2026 年 7 月下旬出现急剧加速，Simon Willison 推测这可能与内部获得后来发布为 GPT-6 Astra 的模型访问权限时间吻合。OpenAI 的文章中直接使用 RSI 缩写而未展开说明，表明该术语在公司内部已被视为既定概念。

rss · Simon Willison · 9月6日 23:57

**背景**: 递归自我改进是一种假设性过程，即 AI 系统通过重写自身代码来增强能力，可能引发智能爆炸。编码智能体是能够生成并执行代码、进行测试并在最少人工指导下独立迭代的 AI 工具。智能体工程是指借助此类编码智能体开发软件的实践，这一趋势在 2026 年显著加速。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Recursive_self-improvement">Recursive self-improvement</a></li>
<li><a href="https://www.technologyreview.com/2026/08/18/1142188/ai-recursive-self-improvement/">AI’s recursive self-improvement might not come so quickly after all | MIT Technology Review</a></li>
<li><a href="https://simonwillison.net/guides/agentic-engineering-patterns/what-is-agentic-engineering/">What is agentic engineering? - Agentic Engineering Patterns - Simon Willison's Weblog</a></li>

</ul>
</details>

**标签**: `#OpenAI`, `#AI agents`, `#recursive self-improvement`, `#software engineering`, `#AGI`

---

<a id="item-2"></a>
## [DNS 主要成为诈骗传播渠道，新 gTLD 域名滥用率高达 10% 至 20%](https://simonwillison.net/2026/Sep/6/the-purpose-of-dns-is-to-spread-scams/) ⭐️ 7.0/10

Terence Eden 认为 DNS 主要是诈骗的传播渠道，并引用 Interisle 报告指出，2025 年新增 gTLD 注册量为 8500 万个，其中 850 万个在 2025 年 5 月前已被列入拦截名单。 如果新注册的 gTLD 域名中有 10% 至 20% 被用于滥用，这表明互联网基础设施存在系统性缺陷，将影响全球普通用户、企业和网络安全工作。 Interisle 报告估计 10% 的滥用率可能是下限，实际数字可能接近 20%，这意味着大约每五个新注册的 gTLD 域名中就有一个可能是诈骗。

rss · Simon Willison · 9月6日 14:40

**背景**: gTLD 是指 .com、.net、.org 等通用顶级域名，由 ICANN 协调的域名系统进行管理。ICANN 是负责协调 DNS 根区注册和域名政策的全球多利益相关方组织，据报道多年来一直在讨论 DNS 滥用问题。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/GTLD">GTLD</a></li>
<li><a href="https://en.wikipedia.org/wiki/ICANN">ICANN</a></li>

</ul>
</details>

**标签**: `#DNS`, `#cybersecurity`, `#domain-abuse`, `#internet-infrastructure`, `#scams`

---

<a id="item-3"></a>
## [Simon Willison：从零重写很少能解决技术债务](https://simonwillison.net/2026/Sep/6/theres-no-limit-to-how-bad-code-can-get/) ⭐️ 7.0/10

Simon Willison 发表评论指出，从零重写系统很少奏效，因为旧系统仍是不断变化的目标，而新团队则面临不切实际的期望。他建议通过自动化测试和有针对性的重构来加固旧系统。 这挑战了当技术债务变得难以承受时，工程管理中常见的“推倒重来”的本能反应。其重要性在于，失败的重写往往会让组织同时维护两套生产系统，浪费大量精力，并积累更多技术债务。 Willison 描述了一种失败模式：旧系统因开发人员没有改进动力而持续累积债务，而新团队发现没有人完全理解被替换系统的行为和范围。他引用 Will Larson 的文章《Migrations: the sole scalable fix to tech debt》作为最负责任的解决方案。

rss · Simon Willison · 9月6日 09:08

**背景**: 技术债务指因选择快速、简单的方案而非更优的长期方案，而导致的未来返工成本。“绿地”项目指不受现有代码约束、从零开始构建。绞杀榕模式和渐进式迁移是逐步替换遗留系统的替代方案，而非一次性全部重写。

**标签**: `#technical debt`, `#software engineering`, `#rewrites`, `#systems design`, `#engineering management`

---

<a id="item-4"></a>
## [OpenAI 联合创始人 Greg Brockman 宣布进入 AGI 时代](https://twitter.com/gdb/status/tweet-2096721633876771094) ⭐️ 7.0/10

OpenAI 联合创始人 Greg Brockman 在 X 上发帖称，我们现在正进入 AGI 时代——无论你认为它来自当前模型、上一个模型还是下一个模型——并将这一里程碑归功于紧密合作伙伴。 OpenAI 联合创始人公开宣称 AGI 已经到来，这是一个重要的行业信号，可能影响投资者预期、公众认知以及各 AI 实验室的竞争定位。 Brockman 的表述刻意模糊了哪个模型构成 AGI，也没有提供任何技术基准或定义，使得这一说法留有解释和争论空间。

twitter · Greg Brockman · 9月6日 22:06

**背景**: AGI（通用人工智能）指的是在大多数具有经济价值的任务上能够达到或超越人类表现的 AI 系统，但目前尚无统一定义。OpenAI 历来将 AGI 定义为在大多数有经济价值的工作中超越人类的系统。这一术语已成为 OpenAI、Anthropic 等主要 AI 实验室之间竞争的焦点。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.bloomberg.com/news/features/2026-09-04/what-is-agi-openai-anthropic-race-for-artificial-general-intelligence">What Is AGI ? OpenAI, Anthropic Race for Artificial... - Bloomberg</a></li>

</ul>
</details>

**社区讨论**: 该帖子获得了数千点赞和数百条回复，讨论可能分为两派：一派庆祝这一里程碑，另一派则质疑当前模型是否真正符合任何严格的 AGI 定义。

**标签**: `#AGI`, `#OpenAI`, `#AI milestones`, `#industry commentary`, `#artificial intelligence`

---

<a id="item-5"></a>
## [Greg Brockman 推荐用 Astra 检查科学论文](https://twitter.com/gdb/status/tweet-2096486220918657164) ⭐️ 7.0/10

知名 AI 人物 Greg Brockman 分享了 Astra 作为检查科学论文的工具，并特别强调其在医学领域的应用。这条推文获得了 1448 个赞和 95 条回复，引起了广泛关注。 来自 AI 领域关键人物的背书表明，AI 辅助科研验证正在成为一个实用且高价值的应用场景。这可能加速透明化、智能体式分析工具在科学和医学界的采用。 Astra 是一种面向透明研究分析的智能体模式（Agentic Schema），提供 Python CLI 和 SDK，用于验证、论文管理和证据核查。推文本身缺乏技术细节，但其底层工具专为结构化、透明的研究工作流而设计。

twitter · Greg Brockman · 9月6日 06:30

**背景**: Astra 由 LightconeResearch 组织开发，包含一套规范和一个工具层。工具仓库 astra-tools 提供验证、命令行访问、论文管理和证据核查功能。它通过 PyPI 分发，方便 Python 用户安装使用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/LightconeResearch/astra-tools/blob/main/README.md">astra-tools/README.md at main · LightconeResearch/astra-tools</a></li>
<li><a href="https://pypi.org/project/astra-tools/">astra-tools · PyPI</a></li>
<li><a href="https://github.com/LightconeResearch/astra-tools">GitHub - LightconeResearch/astra-tools: SDK for ASTRA ...</a></li>

</ul>
</details>

**标签**: `#AI`, `#scientific-research`, `#paper-review`, `#Astra`, `#tooling`

---

<a id="item-6"></a>
## [报道称 GPT-6 已完成训练，更强模型即将发布](https://mp.weixin.qq.com/s?__biz=MzIzNjc1NzUzMw==&mid=2247919381&idx=2&sn=004cb0657b179aa89107176ebfa950aa) ⭐️ 6.0/10

一则简短报道称 GPT-6 已经完成训练，并且更强大的模型很快会发布，同时澄清因安全问题暂停训练的并非 GPT-6，而是未来的某个模型。 如果属实，这表明 OpenAI 正在加快模型发布节奏，并可能已经在准备超越 GPT-6 的下一代模型，这将加剧大语言模型领域的竞争，并引发对安全审查时间表的质疑。 该说法来自二手来源，缺乏技术细节或可验证的信息，且报道明确指出被暂停训练的模型是未来的某个模型，而非 GPT-6。

rss · 量子位 · 9月6日 04:00

**背景**: GPT-6 是 OpenAI 大语言模型系列的下一代产品，继 GPT-4 和 GPT-5 之后。OpenAI 此前曾因安全问题暂停或推迟模型发布，而关于训练进展的传闻通常会在官方公告之前流传。讨论中提到的 Sora 指的是 OpenAI 的文本生成视频模型，该模型已于 2026 年 4 月关闭。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/GPT-6_Astra">GPT-6 Astra</a></li>
<li><a href="https://en.wikipedia.org/wiki/Sora_(OpenAI)">Sora (OpenAI)</a></li>

</ul>
</details>

**社区讨论**: 社区讨论内容很少，只有一条关于 Sora 被忽视的讽刺评论和一个招聘信息，对 GPT-6 的说法几乎没有实质性补充。

**标签**: `#OpenAI`, `#GPT-6`, `#AI news`, `#large language models`, `#rumors`

---

<a id="item-7"></a>
## [Sam Altman 转发一条指向 Jakub 的神秘帖子](https://twitter.com/sama/status/tweet-2096647371983880383) ⭐️ 3.0/10

Sam Altman 发布了一条推文，仅写道“来自 Jakub 的一篇重要帖子：”，但没有附上任何细节、链接预览或所引用帖子的具体内容。 由于 Sam Altman 拥有大量关注者，即使是一条模糊的指引也可能为被引用的作者带来大量关注，但缺乏上下文限制了对该帖子实际重要性的判断。 这条推文没有包含任何技术细节、引用文字或可用的链接，因此无法核实 Jakub 的帖子实际说了什么。

twitter · Sam Altman · 9月6日 17:11

**背景**: Sam Altman 是 OpenAI 的首席执行官，经常使用 X（原 Twitter）分享或放大来自研究人员、工程师以及 AI 社区其他人士的帖子。“Jakub”很可能指与 OpenAI 相关的知名研究员 Jakub Pachocki，但这条推文本身并未确认这一点。

**标签**: `#twitter`, `#sam-altman`, `#jakub`, `#vague`, `#low-value`

---