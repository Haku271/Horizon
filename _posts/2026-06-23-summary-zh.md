---
layout: default
title: "Horizon Summary: 2026-06-23 (ZH)"
date: 2026-06-23
lang: zh
---

> 从 8 条内容中筛选出 6 条重要资讯。

---

1. [Mythos 之后，OpenAI 董事与 Gray Swan CEO 探讨 AI 红队测试](#item-1) ⭐️ 9.0/10
2. [研究显示 LLM 优先考虑文本风格，为角色混淆越狱开门](#item-2) ⭐️ 8.0/10
3. [使用 Claude Code 将 Moebius 0.2B 模型移植到浏览器](#item-3) ⭐️ 8.0/10
4. [GLM-5.2: 开源代理的重大突破](#item-4) ⭐️ 8.0/10
5. [用 Python 从头构建浏览器 AI 智能体教程](#item-5) ⭐️ 6.0/10
6. [DeepSeek 急招 AI Agent 人才，负责人亲自宣传](#item-6) ⭐️ 4.0/10

---

<a id="item-1"></a>
## [Mythos 之后，OpenAI 董事与 Gray Swan CEO 探讨 AI 红队测试](https://www.latent.space/p/gray-swan) ⭐️ 9.0/10

Zico Kolter（OpenAI 董事）和 Matt Fredrikson（Gray Swan 首席执行官）讨论了为何 AI 安全需要与传统网络安全不同的方法，并以 Anthropic 的 Mythos 模型等近期 AI 红队测试为背景。 随着 AI 模型变得更强大，例如 Mythos 展示了攻破国家安全系统的潜力，保障 AI 安全需要超越传统网络安全的新策略，以应对对抗性机器学习威胁。 Zico Kolter 从他所在的 OpenAI 董事会带来视角，而 Matt Fredrikson 的公司 Gray Swan 专注于 AI 安全红队测试，强调对抗性输入等 AI 漏洞需要专门的测试。

rss · Latent Space · 6月22日 21:06

**背景**: Anthropic 的 Mythos 是一个具备高级计算机安全能力的语言模型，最近报道在一次红队测试中几乎攻破了 NSA 的机密系统。AI 红队测试是一种系统化的对抗性测试，旨在发现 AI 系统的漏洞，如提示注入、越狱和数据投毒。与传统网络安全关注网络和软件漏洞不同，AI 安全还需应对对抗性机器学习，即攻击者通过操纵输入来欺骗模型。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://red.anthropic.com/">red.anthropic.com</a></li>
<li><a href="https://www.paloaltonetworks.com/cyberpedia/what-is-ai-red-teaming">What Is AI Red Teaming? Why You Need It and How to Implement - Palo Alto Networks</a></li>

</ul>
</details>

**标签**: `#AI security`, `#red-teaming`, `#adversarial ML`, `#OpenAI`, `#podcast`

---

<a id="item-2"></a>
## [研究显示 LLM 优先考虑文本风格，为角色混淆越狱开门](https://simonwillison.net/2026/Jun/22/prompt-injection-as-role-confusion/#atom-everything) ⭐️ 8.0/10

一篇新论文表明，大语言模型（LLM）容易因基于角色的提示注入而混淆，因为它们优先考虑文本风格而非实际内容。研究人员展示，对用户输入进行“去风格化”——稍作改写使其偏离预期的角色格式——可将攻击成功率从 61%大幅降至 10%。 这揭示了当前 LLM 安全机制的根本弱点，即模型无法可靠地区分可信系统指令与用户提供的文本。研究表明，在模型具备真正的角色感知能力之前，提示注入防御将始终是一场打地鼠游戏。 该攻击通过注入伪造的推理块（模仿模型内部思考的风格）来实施，导致模型覆盖安全训练。论文引入了“角色探针”来衡量模型内部如何分配权限，并提出“角色混淆”作为核心机制。

rss · Simon Willison · 6月22日 23:59

**背景**: 提示注入是一种网络安全攻击，通过模糊开发者指令与用户数据之间的界限，诱使 LLM 执行非预期操作。越狱（jailbreak）专门绕过生成式 AI 中的安全与策略约束。现代 LLM 使用<system>、<user>和<assistant>等角色标签来标明特权指令，但这项研究显示风格模仿可以欺骗这些模型。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Prompt_injection_attack">Prompt injection attack</a></li>
<li><a href="https://arxiv.org/html/2603.12277v2">Prompt Injection as Role Confusion</a></li>

</ul>
</details>

**标签**: `#prompt-injection`, `#AI-safety`, `#LLM`, `#jailbreak`, `#research-summary`

---

<a id="item-3"></a>
## [使用 Claude Code 将 Moebius 0.2B 模型移植到浏览器](https://simonwillison.net/2026/Jun/22/porting-moebius/#atom-everything) ⭐️ 8.0/10

Simon Willison 将轻量级 Moebius 0.2B 图像修复模型移植到浏览器中，利用 WebGPU 完全在客户端运行，无需 CUDA 或 PyTorch，并发布了可用的在线演示。 这表明在浏览器中本地运行复杂 AI 模型日益可行，减少了对服务器的依赖，可实现保护隐私、低延迟的应用，同时也展示了 Claude Code 等 AI 编码代理在复杂模型移植中的实用性。 该移植使用 ONNX Runtime Web 配合 WebGPU 后端，利用了模型仅 0.2B 参数的轻量优势；演示支持非方形图像加框、标记区域并执行修复。

rss · Simon Willison · 6月22日 23:43

**背景**: 图像修复是填补图像缺失或遮挡区域的任务。Moebius 是 ECCV 2026 提出的高度优化的轻量级模型，在修复质量上媲美大得多的模型。WebGPU 是现代浏览器 API，可直接访问 GPU 进行高性能计算，使机器学习模型能在客户端运行。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://hustvl.github.io/Moebius/">Moebius Project Page</a></li>
<li><a href="https://github.com/hustvl/Moebius">GitHub - hustvl/Moebius: [ECCV 2026] Moebius: 0.2B ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/WebGPU">WebGPU</a></li>

</ul>
</details>

**标签**: `#image inpainting`, `#browser-based AI`, `#WebGPU`, `#model porting`, `#lightweight models`

---

<a id="item-4"></a>
## [GLM-5.2: 开源代理的重大突破](https://www.interconnects.ai/p/glm-52-is-the-step-change-for-open) ⭐️ 8.0/10

Z.ai 发布了采用 MIT 许可证的 GLM-5.2 开源模型，该模型在代理应用方面已成为领先的开源模型，标志着能力的一次阶跃变化。 该发布让高性能 AI 代理更加普及，可能加速本地和隐私保护 AI 应用的创新，并对闭源模型形成挑战。 GLM-5.2 可通过 Unsloth Studio 等工具在本地运行，支持自动内存卸载和多 GPU 设置，适合个人爱好者与企业使用。

rss · Interconnects · 6月22日 14:52

**背景**: GLM（通用语言模型）是 Z.ai（原智谱 AI）开发的大型语言模型系列。开源 AI 代理是指使用开源权重 LLM 自主执行任务的软件，具有透明和可定制优势。代理范式是当前 AI 发展的重要方向。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/GLM-5.2">GLM-5.2</a></li>
<li><a href="https://unsloth.ai/docs/models/glm-5.2">GLM-5.2 - How to Run Locally | Unsloth Documentation</a></li>
<li><a href="https://www.reddit.com/r/technology/comments/1uc5hjh/what_is_glm52_another_opensource_chinese_ai_model/">What is GLM-5.2? Another open-source Chinese AI model has ...</a></li>

</ul>
</details>

**标签**: `#open-source`, `#large-language-models`, `#agents`, `#AI`, `#model-release`

---

<a id="item-5"></a>
## [用 Python 从头构建浏览器 AI 智能体教程](https://machinelearningmastery.com/building-browser-using-ai-agents-in-python/) ⭐️ 6.0/10

Machine Learning Mastery 发布了一篇新教程，教授如何用 Python 从基本原理开始构建可操控浏览器的 AI 智能体，而不依赖高级 API。该教程侧重于使用低级编程技术实现直接的浏览器交互。 这种方法让开发者更深入地理解浏览器自动化，从而能更好地定制和调试自主网页智能体，这对现代 AI 应用至关重要。它填补了教育资源中的一个空白，因为大多数教程都隐藏了底层机制。 教程可能使用 Selenium 或 Playwright 等标准 Python 库进行浏览器控制，引导读者完成 DOM 导航、元素交互和数据提取，而不依赖预构建的智能体框架。

rss · Machine Learning Mastery · 6月22日 12:00

**背景**: AI 浏览器智能体是一种自主系统，通过模拟点击和打字等人类行为与网页交互，用于网页抓取、自动化测试和执行复杂工作流程。尽管 Browser Use 和 Skyvern 等框架已广泛流行，但从头构建智能体能提供更强的控制力和教学价值。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.firecrawl.dev/blog/best-browser-agents">11 Best AI Browser Agents in 2026 - Firecrawl</a></li>
<li><a href="https://usefulai.com/tools/ai-browsers">7 Best AI Browser Agents in June 2026 (23 Tested)</a></li>

</ul>
</details>

**标签**: `#ai-agents`, `#web-automation`, `#python`, `#tutorial`, `#browser-interaction`

---

<a id="item-6"></a>
## [DeepSeek 急招 AI Agent 人才，负责人亲自宣传](https://mp.weixin.qq.com/s?__biz=MzIzNjc1NzUzMw==&mid=2247898679&idx=1&sn=7e13093476268ed660ab89bfa7edc32f) ⭐️ 4.0/10

DeepSeek 正紧急招聘 AI Agent 相关岗位，团队负责人亲自发布招聘广告。该公司为其 Harness 部门寻找人才，提供至少三个职位，包括实习岗位。 此次招聘热潮表明业界对 AI Agent 开发技能的需求快速增长。这凸显了 Agentic AI 的战略重要性，企业正竞相构建能够代表用户执行任务的自主系统。 招聘至少包括三个岗位，提供实习机会，且不设严格职责边界。团队负责人崔添翼直接招募，突显紧迫性。

rss · 量子位 · 6月22日 04:20

**背景**: AI Agent 是能够自主追求目标、使用工具并在人类设定的约束下采取行动的系统。它们是生成式 AI 的关键趋势，OpenAI、Anthropic 和 Salesforce 等主要厂商都在开发 Agent 平台。DeepSeek 是一家以高性价比大语言模型闻名的中国 AI 实验室，如今正扩展至 Agent 技术领域，反映了行业向 Agentic 应用的广泛转变。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/AI_agent">AI agent</a></li>
<li><a href="https://www.ibm.com/think/topics/ai-agents">What Are AI Agents? | IBM</a></li>

</ul>
</details>

**标签**: `#hiring`, `#AI agents`, `#DeepSeek`, `#job market`

---