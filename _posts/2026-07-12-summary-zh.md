---
layout: default
title: "Horizon Summary: 2026-07-12 (ZH)"
date: 2026-07-12
lang: zh
---

> 从 11 条内容中筛选出 2 条重要资讯。

---

1. [vLLM v0.25.0 发布：Model Runner V2 成默认，移除 PagedAttention](#item-1) ⭐️ 8.0/10
2. [sqlite-utils 4.1 新增 --code 选项，支持 Python 代码生成行数据](#item-2) ⭐️ 5.0/10

---

<a id="item-1"></a>
## [vLLM v0.25.0 发布：Model Runner V2 成默认，移除 PagedAttention](https://github.com/vllm-project/vllm/releases/tag/v0.25.0) ⭐️ 8.0/10

vLLM v0.25.0 将 Model Runner V2 设为所有稠密模型的默认执行路径，移除了旧版 PagedAttention 实现，并使 Transformers 后端性能与原生 vLLM 持平。同时新增了对 LLaVA-OneVision-2 等模型的支持，并引入了针对异构词表的通用推测解码方法。 作为广泛使用的 LLM 推理引擎，vLLM 向 MRv2 的架构迁移及其移除奠基性技术 PagedAttention，标志着推理效率和代码库现代化的重大演进。Transformers 后端的性能持平在保证速度的同时拓宽了模型兼容性，惠及整个开源 LLM 部署生态。 MRv2 现支持 EVS、实时嵌入、Mamba 混合模型前缀缓存，以及兼容完整 CUDA 图的动态推测解码。新的通用推测解码（TLI）允许使用不同词表的草稿模型，该版本包含来自 232 位贡献者的 558 次提交。

github · khluu · 7月11日 20:06

**背景**: vLLM 是一个高吞吐量 LLM 推理引擎，以 PagedAttention 闻名，该技术类似虚拟内存，以非连续块管理 KV 缓存来减少浪费。Model Runner V2 是重新设计的内部执行引擎，比最初的 V1 更清晰、更模块化。推测解码通过使用较小的草稿模型提议多个 token，再由主模型并行验证，从而加速推理。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://docs.vllm.ai/en/latest/design/model_runner_v2/">Model Runner V2 Design Document - vLLM</a></li>
<li><a href="https://en.wikipedia.org/wiki/PagedAttention">PagedAttention</a></li>
<li><a href="https://speculative-decoding.github.io/">COLING 2025 Tutorial: Speculative Decoding for Efficient LLM ...</a></li>

</ul>
</details>

**标签**: `#vLLM`, `#LLM-serving`, `#release`, `#performance`, `#model-support`

---

<a id="item-2"></a>
## [sqlite-utils 4.1 新增 --code 选项，支持 Python 代码生成行数据](https://simonwillison.net/2026/Jul/11/sqlite-utils/#atom-everything) ⭐️ 5.0/10

sqlite-utils 4.1 为 insert 和 upsert 命令新增 --code 选项，允许用户通过 Python 代码定义 rows() 函数或可迭代对象，直接在命令行生成要插入的行数据。此外还加入了 --type 列类型覆盖、drop-index 命令以及 query 命令的标准输入支持。 此次更新通过支持内联 Python 代码作为数据源，简化了数据导入流程，减少了对中间文件的依赖。--type 选项解决了 CSV/TSV 用户长期面临的痛点，例如需要将邮政编码等看似整数的数据保留为 TEXT 类型。 --code 选项接受 Python 代码字符串或指向 .py 文件的路径，该文件需包含 rows() 函数或 rows 可迭代对象。--type 选项使用 --type 列名 类型 的语法，在创建表时覆盖自动检测的类型。drop-index 命令支持 --ignore 参数，可在索引不存在时不报错。

rss · Simon Willison · 7月11日 23:50

**背景**: sqlite-utils 是一个用于操作 SQLite 数据库的 Python 命令行工具和库，常用于数据工程与探索。insert 命令用于添加新行，upsert 则根据主键冲突执行插入或更新。此前版本已支持通过 Python 代码进行数据转换，--code 选项是这一模式的自然延伸。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://sqlite-utils.datasette.io/en/stable/cli.html">sqlite - utils command - line tool - sqlite - utils</a></li>
<li><a href="https://sqlite-utils.datasette.io/">sqlite - utils</a></li>
<li><a href="https://sqlite.org/lang_upsert.html">UPSERT</a></li>

</ul>
</details>

**标签**: `#sqlite`, `#python`, `#cli-tools`, `#data-engineering`, `#release-notes`

---