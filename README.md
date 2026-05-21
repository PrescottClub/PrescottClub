<!-- ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ -->
<!--        🌌  TERENCE · PRESCOTTCLUB · v5.3  🌌                    -->
<!-- ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ -->

<div align="center">

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:7C3AED,50:22D3EE,100:F472B6&height=220&section=header&text=Terence%20·%20PrescottClub&fontSize=52&fontColor=FFFFFF&animation=fadeIn&fontAlignY=40" />

<a href="https://github.com/PrescottClub">
<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=700&size=22&duration=3000&pause=800&color=7C3AED&background=00000000&center=true&vCenter=true&width=580&height=45&lines=AI+Application+Engineer;Agent+Builder+and+Context+Crafter;Eval-Driven+and+Shipping-First" alt="Typing SVG" />
</a>

<br/>

<img src="https://img.shields.io/badge/🧭_Since-2017-7C3AED?style=for-the-badge&labelColor=0D1117" />
<img src="https://img.shields.io/badge/📍_Shanghai-China-22D3EE?style=for-the-badge&labelColor=0D1117" />
<img src="https://img.shields.io/badge/🛠️_Focus-Agentic_System-F472B6?style=for-the-badge&labelColor=0D1117" />

<br/><br/>

[![Profile views](https://komarev.com/ghpvc/?username=PrescottClub&color=7C3AED&style=for-the-badge&label=VIEWS)](https://github.com/PrescottClub)
[![GitHub followers](https://img.shields.io/github/followers/PrescottClub?label=Followers&style=for-the-badge&color=22D3EE&labelColor=0D1117)](https://github.com/PrescottClub)

</div>

---

## <img src="https://media.giphy.com/media/hvRJCLFzcasrR4ia7z/giphy.gif" width="28" /> 关于我

我是 **Terence**，一名专注于 **AI 应用层 (Application Layer)** 与 **Agent 工程化** 的全栈工程师。

拥有九年工程经验（Java/Spring → Python/FastAPI → AI Native），过去两年将全部精力投入在 **Agent / RAG / LLM 的生产环境落地**。我不做底层模型训练，我解决的是模型到产品之间的最后一公里：**把大模型从“偶尔惊艳的玩具”变成“稳定交付的工业级产品”**。

- ⚔️ **核心优势**：懂后端的严谨（高并发/微服务），也懂 LLM 的脾气（非确定性/幻觉），能用工程手段驯服概率程序。
- 🎯 **当前专注**：Agent Harness 编排设计、Agentic RAG 检索增强架构、基于 LLM-as-Judge 的评测驱动开发 (EDD)。

---

## ⚡ 能力模型与技术栈

作为 AI 应用工程师，我的能力闭环涵盖了从底层编排到前端交付的全链路：

### 🤖 Agent 编排 (Agent Harness)
> **Stack**: `LangGraph` · `OpenAI Agents SDK` · `MCP (Model Context Protocol)`

不依赖脆弱的纯自然语言 Prompt 链，而是构建基于**状态机**的智能体工作流。支持多智能体协作、工具调用的 Schema 强校验、执行中断与 Human-in-the-loop 人工介入。

### 🔍 检索增强架构 (Agentic RAG)
> **Stack**: `LlamaIndex` · `Qdrant` · `pgvector` · `GraphRAG` · `BGE-Reranker`

告别“Embedding 一把梭”。落地 Query Rewriting (意图重写)、Hybrid Retrieval (BM25+Dense)、知识图谱多跳推理与 Rerank 兜底，让检索更贴近真实业务分布。

### 🧩 上下文工程 (Context Engineering)
> **Stack**: `Mem0` · `Zep` · `Prompt Caching`

精细化治理 LLM 上下文窗口。落地 System / Tools / Memory 分层设计；通过摘要与关键事实表实现长对话压缩；利用 Prompt Caching 优化首字延迟与 Token 成本。

### 🧪 评测驱动开发 (Eval-Driven Development)
> **Stack**: `promptfoo` · `Ragas` · `DeepEval` · `Langfuse`

**无 Eval，不上线**。建立 Golden Set 基准测试；在 CI/CD 接入 LLM-as-Judge 自动化评分（幻觉率、相关性、任务完成度）；通过线上 Trace 采样持续扩充测试集。

### ⚙️ 全栈交付与工程基建 (Full-Stack Delivery)
> **Stack**: `Python/FastAPI` · `TypeScript/Vue3` · `LiteLLM` · `Vercel AI SDK`

实现流式输出 (Streaming UI / SSE) 与生成式 UI (Generative UI)；搭建 AI Gateway (多模型路由、Fallback 降级、限流)；提供高可用的前后端工程基建。

<br/>

<div align="center">
  <img src="https://go-skill-icons.vercel.app/api/icons?i=python,typescript,vue,react,tailwind,vite,java,go&perline=8&theme=dark" />
  <br/>
  <img src="https://go-skill-icons.vercel.app/api/icons?i=fastapi,spring,postgres,redis,docker,kubernetes,aws,vercel&perline=8&theme=dark" />
</div>

---

## 🧠 我的工程方法论

### 我怎么做 Agent 编排
我用 **LangGraph 状态机 + MCP** 搭 Agent Harness。选它不是因为流行，是因为：
- 状态机天然支持中断和恢复——线上 Agent 不能跑飞了没人管。
- MCP 把工具定义标准化了，换模型不用重写 tool schema。
- 每一步 trace 都落库，出了问题能精确定位到哪一跳炸的。

### 我怎么管上下文
不调单条 Prompt，我管的是**整个上下文窗口的生命周期**：
- 长对话不 truncate，用摘要 + 关键事实表压缩。
- Prompt Caching 命中率是我盯的核心成本指标。
- 每条线上失败的 trace，都是下一轮 Few-shot 的弹药。

### 我怎么保证质量
我把 LLM 应用当**概率程序**对待，不靠手感调 Prompt：
- 每次 Prompt / Retrieval 的改动，必须过 promptfoo 回归，不达标不合并。
- 线上 Langfuse 采样自动回流，eval 测试集越跑越大。
- 幻觉率、P95 延迟、用户满意度三条红线，过了才上。

---

## 📊 GitHub Stats

<div align="center">

<img height="165em" src="https://github-readme-stats-sigma-five.vercel.app/api?username=PrescottClub&show_icons=true&theme=tokyonight&include_all_commits=true&count_private=true&hide_border=true&bg_color=0D1117&title_color=7C3AED&icon_color=22D3EE&text_color=E6EDF3&ring_color=F472B6" />
<img height="165em" src="https://github-readme-stats-sigma-five.vercel.app/api/top-langs/?username=PrescottClub&layout=compact&langs_count=6&theme=tokyonight&hide_border=true&bg_color=0D1117&title_color=7C3AED&text_color=E6EDF3" />

<br/><br/>

<img src="https://streak-stats.demolab.com?user=PrescottClub&theme=tokyonight&hide_border=true&background=0D1117&ring=7C3AED&fire=F472B6&currStreakLabel=22D3EE&sideLabels=E6EDF3&dates=6B7280" alt="GitHub Streak" />

<br/><br/>

<img src="https://github-readme-activity-graph.vercel.app/graph?username=PrescottClub&custom_title=Contribution%20Activity&bg_color=0D1117&color=7C3AED&line=22D3EE&point=F472B6&area_color=1F2937&title_color=E6EDF3&area=true&hide_border=true&radius=8" alt="Contribution Graph" width="100%" />

</div>

---

## 📫 Connect

<div align="center">

<a href="mailto:jger8276@gmail.com">
  <img src="https://img.shields.io/badge/📧_Email-jger8276%40gmail.com-D14836?style=for-the-badge&labelColor=0D1117" />
</a>&nbsp;
<a href="https://github.com/PrescottClub">
  <img src="https://img.shields.io/badge/🐙_GitHub-PrescottClub-181717?style=for-the-badge&labelColor=0D1117" />
</a>

<br/><br/>

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=16&duration=2800&pause=900&color=22D3EE&background=00000000&center=true&vCenter=true&width=580&height=36&lines=Build+-+Eval+-+Ship+-+Observe+-+Iterate" alt="Loop" />

<br/><br/>

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:F472B6,50:22D3EE,100:7C3AED&height=120&section=footer" />

</div>