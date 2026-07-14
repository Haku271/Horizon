---
layout: default
title: "Horizon Summary: 2026-07-14 (ZH)"
date: 2026-07-14
lang: zh
---

> 从 6 条内容中筛选出 5 条重要资讯。

---

1. [DOOMQL：用 SQLite 作为完整游戏引擎的类 Doom 游戏](#item-1) ⭐️ 7.0/10
2. [在 GitHub Actions 中利用 UV_EXCLUDE_NEWER 实现缓存友好的 uvx 用法](#item-2) ⭐️ 6.0/10
3. [Datasette GitHub 代码频率图显示 AI 辅助编码激增](#item-3) ⭐️ 6.0/10
4. [构建 AI 代理时应避免的常见反模式](#item-4) ⭐️ 6.0/10
5. [Destructive Command Guard：阻止 AI 代理危险命令的 Rust 工具](#item-5) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [DOOMQL：用 SQLite 作为完整游戏引擎的类 Doom 游戏](https://simonwillison.net/2026/Jul/13/doomql/#atom-everything) ⭐️ 7.0/10

Peter Gostev 开发了 DOOMQL，一款 Python 终端游戏，其中 SQLite 通过 SQL 查询处理所有游戏逻辑——包括移动、碰撞、渲染和战斗，甚至包含一个使用递归 CTE 实现的光线追踪器。 该项目创造性地将 SQLite 重新构想为实时游戏引擎，展示了 SQL 超越传统数据存储的表达能力，并启发了数据库技术的非传统用途。 该游戏以 Python 终端脚本运行，将状态存储在 SQLite 数据库文件中，并使用一个包含递归 CTE 的大型 SQL 查询进行光线追踪渲染；还可以通过 Datasette Web 应用进行可视化。

rss · Simon Willison · 7月13日 22:34

**背景**: SQLite 是一种轻量级、基于文件的数据库引擎，广泛用于应用程序的本地数据存储。递归 CTE（公用表表达式）允许 SQL 查询引用自身，从而实现光线追踪等迭代计算。Datasette 是一个用于探索和发布 SQLite 数据库的工具，其新的 Apps 插件支持直接运行 SQL 查询的自定义 HTML/JavaScript 界面。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://digg.com/tech/iuhrpvcu">Peter Gostev builds a Doom-like raycasting engine entirely in SQLite - Digg</a></li>
<li><a href="https://buildagameengine.com/serialization/serialization-with-sqlite">Serialization with SQLite - Build a Game Engine</a></li>

</ul>
</details>

**标签**: `#sqlite`, `#game-development`, `#python`, `#experimental`, `#terminal`

---

<a id="item-2"></a>
## [在 GitHub Actions 中利用 UV_EXCLUDE_NEWER 实现缓存友好的 uvx 用法](https://simonwillison.net/2026/Jul/14/uvx-github-actions-cache/#atom-everything) ⭐️ 6.0/10

西蒙·威利森分享了一种在 GitHub Actions 中使用 uvx 的缓存友好模式：将 UV_EXCLUDE_NEWER 环境变量设为特定日期并加入缓存键，从而让工具版本解析基于该日期，并通过更新日期来控制缓存失效。 该技巧通过避免每次工作流运行时都从 PyPI 重复下载 Python 工具和依赖项来缩短 CI/CD 流水线运行时间，同时仍允许通过日期进行有计划的升级。 该模式在工作流开头设置 UV_EXCLUDE_NEWER: "2026-07-12"，并将该日期用作 GitHub Actions 缓存键的一部分；将日期向后推移会使缓存失效，并触发更新到较新的工具版本。

rss · Simon Willison · 7月14日 00:56

**背景**: uvx 是 uv Python 包管理器的一个命令，可在隔离环境中直接运行工具而无需手动安装。UV_EXCLUDE_NEWER 是一个环境变量，它将依赖解析限制为在给定日期之前发布的包版本，从而提高可重现性。GitHub Actions 缓存通常用于存储依赖项，通过重用之前下载的文件来加速工作流执行。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://docs.astral.sh/uv/reference/cli/">Commands | uv</a></li>
<li><a href="https://docs.astral.sh/uv/reference/settings/">Settings | uv</a></li>

</ul>
</details>

**标签**: `#github-actions`, `#python`, `#caching`, `#uvx`, `#devops`

---

<a id="item-3"></a>
## [Datasette GitHub 代码频率图显示 AI 辅助编码激增](https://simonwillison.net/2026/Jul/13/datasette-code-frequency/#atom-everything) ⭐️ 6.0/10

Simon Willison 查看了他的 Datasette 项目在 GitHub 上的代码频率图，发现 2026 年的代码添加和删除量出现剧烈激增，他将其归因于使用了编码代理和 Opus 4.8、GPT-5.5、Fable 5、GPT-5.6 Sol 等 AI 模型。 这提供了一个具体、数据驱动的例子，展示了先进的 AI 编码工具如何显著提高开发者产出，引发了关于 AI 在软件工程生产力中作用的讨论。 该图表显示 2026 年某一周的高峰为 37,022 次添加和 9,528 次删除，而此前的峰值较小。这仅是单个项目的观察，未控制项目阶段或个人时间分配等其他因素。

rss · Simon Willison · 7月13日 21:45

**背景**: Datasette 是 Simon Willison 开发的一个用于探索和发布数据的开源工具。GitHub 的代码频率图可视化了一个仓库每周添加和删除的代码行数，通常反映开发活动。编码代理和所提及的大型语言模型正越来越多地用于辅助或自动化编程任务。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://simonwillison.net/2026/Jul/13/datasette-code-frequency/">datasette code - frequency chart on GitHub | Simon Willison’s Weblog</a></li>
<li><a href="https://wpnews.pro/news/datasette-code-frequency-chart-on-github">datasette code - frequency chart on GitHub — Web Pulse</a></li>
<li><a href="https://stackoverflow.com/questions/73474250/github-code-frequency-graph-scale-problem-after-initial-commit">git - github code frequency graph scale problem... - Stack Overflow</a></li>

</ul>
</details>

**标签**: `#productivity`, `#ai-assisted-coding`, `#open-source`, `#datasette`, `#github-metrics`

---

<a id="item-4"></a>
## [构建 AI 代理时应避免的常见反模式](https://machinelearningmastery.com/building-ai-agents-here-are-some-anti-patterns-to-avoid/) ⭐️ 6.0/10

Machine Learning Mastery 上的一篇文章列举了开发 AI 代理时应避免的特定反模式，并强调代理系统在生产环境中会不断变化。 随着基于代理的系统在生产中日益普及，这些指导有助于从业者避开常见的设计和运维陷阱，从而构建更健壮、更易维护的 AI 代理。 文章侧重于代理系统在生产环境中动态变化特性相关的反模式，但摘要中未提供这些模式的具体示例或技术细节。

rss · Machine Learning Mastery · 7月13日 12:00

**背景**: AI 代理是能够感知环境并采取行动以实现目标的自主软件实体。为生产环境构建此类代理会面临状态管理、处理意外输入以及确保长期可靠行为等挑战。反模式是指针对反复出现的问题所采用的常见但无效的解决方案。

**标签**: `#AI Agents`, `#Anti-Patterns`, `#Production ML`, `#Software Engineering`, `#Best Practices`

---

<a id="item-5"></a>
## [Destructive Command Guard：阻止 AI 代理危险命令的 Rust 工具](https://github.com/Dicklesworthstone/destructive_command_guard) ⭐️ 6.0/10

一款名为 Destructive Command Guard 的新 Rust 工具已发布，旨在防止 AI 代理无意中执行危险的 git 和 shell 命令。 随着 AI 代理越来越多地用于自动化编程和系统操作，该工具降低了意外破坏的风险，提升了安全性和可靠性。 该工具用 Rust 编写，专门针对危险的 git 操作（如强制推送）和 shell 命令，但其初始版本未完整记录所拦截命令的具体列表和集成细节。

ossinsight · Dicklesworthstone · 7月14日 01:14

**背景**: 像 GPT-4 和 Copilot 这样的 AI 编程助手能根据提示执行 shell 命令，但缺乏安全措施时，它们可能运行 `git push --force` 或 `rm -rf` 等破坏性命令，导致严重数据丢失。Destructive Command Guard 充当保护层，在执行前拦截此类命令。

**标签**: `#rust`, `#security`, `#ai-agents`, `#developer-tools`, `#git`

---