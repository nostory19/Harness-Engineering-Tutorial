# Harness Engineering: 从原理到落地的全栈教程

> 一个从 0 到 1 系统讲解 Harness Engineering（AI 工程化新范式）的开源指南。  
> 覆盖：起源 → 核心思想 → 系统设计 → 实战 → 对比分析。

## ❓ 为什么需要 Harness Engineering？

随着 LLM / Agent 技术的发展，传统开发模式逐渐暴露问题：

- Prompt 工程难以维护
- Agent 行为不可控
- 多工具调用混乱
- 缺乏可观测性和评估体系

Harness Engineering 的核心目标是：

> 让 AI 系统“可控、可测试、可评估、可演化”。

一句话：Dont't ask what your agents can do for you. Ask what you can do for your agnet.

## 🧩 什么是 Harness Engineering？

Harness Engineering 是一种围绕 AI / Agent 构建的工程方法论，强调：

- 对 AI 行为进行约束（Harness）
- 建立可测试的执行环境
- 引入评估（Evaluation）机制
- 实现可复现与可持续优化

它可以被理解为：

- AI 领域的 DevOps 实践方法
- 面向 Agent 系统的测试与评估框架

【不是给AI拴上锁链让它寸步难行，而是给它一条可靠的缰绳，让它能自由奔跑，却不会失控。】

## 🕰️ 技术起源

Harness Engineering（驾驭工程）是 2025 年至 2026 年间逐渐兴起的 AI 工程新范式。它的诞生并非一蹴而就，而是经历了多个独立技术方向逐步融合、演进的过程。

### 概念提出与行业关注

这一概念的明确提出始于 2026 年初：

- HashiCorp 联合创始人 Mitchell Hashimoto 最早使用该术语，描述其利用 AI Agent 进行软件开发的方法。
- 随后，OpenAI 在 2026 年 2 月发布[《Harness engineering: leveraging Codex in an agent-first world》](https://openai.com/zh-Hans-CN/index/harness-engineering/)一文，分享团队在五个月内、仅靠 3-7 名工程师、借助 Codex AI Agent 构建 100 万行代码产品的内部实验。
- 紧接着，Martin Fowler 和 Thoughtworks 的专家 Birgitta Böckeler 也进行了专门解读，将其归纳为更清晰的工程框架。

### 演进路径
![path](./diagrams/HCHoBfpWsAATUzk.jfif)

从演进路径来看，Harness Engineering 是对此前几个工程阶段的自然承接与整合：

- **Prompt Engineering（提示词工程，约 2022-2023 年）**：最初，人们主要关注如何通过优化提示词，让大语言模型输出更符合预期的单次结果。这个阶段的核心是“人类下指令，AI 执行单次任务”。
- **Context Engineering（上下文工程，约 2024-2025 年）**：随着应用复杂化，人们发现仅靠提示词不够，还需要为 AI 提供正确的知识和上下文（如通过 RAG 检索增强生成），使其能基于更充分的信息做决策。这个阶段的核心是“人类提供知识，AI 基于知识执行”。
- **Harness Engineering（驾驭工程，2026 年至今）**：当 AI 从单次对话走向需要多步推理、工具调用、长期自主执行的复杂任务时（如 OpenAI Codex 构建百万行级应用），仅靠提示词和上下文已无法解决可靠性、可控性和可维护性问题。于是，行业逐渐形成共识，需要一套更系统的工程方法，将架构约束、反馈闭环、可观测性和持续评估整合起来，为 AI Agent 构建一个既能自主发挥能力、又能在安全边界内可靠工作的“驾驭系统”。

### 归纳

因此，Harness Engineering 最终可以理解为：在上述各方向（提示词、上下文、评估、可观测性等）基础上，进一步融合架构约束（Architectural Constraints）与熵管理（Entropy Management）等实践，形成以“约束 + 测试 + 评估”为核心的工程体系，目标是让 AI 智能体能够在复杂、长周期的任务中稳定、可靠地运行。

最终演化为：**Harness Engineering（约束 + 测试 + 评估）**。

## 🧠 核心思想
![harness](./diagrams/HDF0MuzaMAMSEam.jfif)

Harness Engineering 重点解决以下五类问题：

1. **控制（Control）**：如何限制 LLM 的行为边界？
2. **测试（Testing）**：如何验证 AI 输出正确性？
3. **评估（Evaluation）**：如何量化系统质量？
4. **可复现（Reproducibility）**：如何保证结果稳定？
5. **可演进（Iteration）**：如何持续优化？

## 🏗️ 系统架构

![architecture](./diagrams/)

核心模块通常包括：

- Prompt Layer
- Agent Orchestrator
- Tool Layer
- Evaluation Harness
- Metrics & Observability

> 说明：当前仓库预留了架构图位置，你可以后续在 `diagrams/architecture.png` 中补充图示。
## 基础篇

### 文章教程

| 文章地址 | 作者 |
| --- | --- | 
| [Harness Engineering 是什么？从上下文工程到驾驭工程](https://cloud.tencent.com/developer/article/2645208) |[mixlab](https://cloud.tencent.com/developer/user/1628742) | 
| ["Harness Engineering" is going to blow up](https://x.com/dotey/status/2027156511555027252)| 宝玉|
|  | |
|  | |

### 必读
| 文章地址 | 作者 |
| --- | --- |
| [Harness engineering: leveraging Codex in an agent-first world](https://openai.com/zh-Hans-CN/index/harness-engineering/)| OpenAI|
|[Exploring Gen AI](https://martinfowler.com/articles/exploring-gen-ai/harness-engineering.html) | Martin Fowler| 
|[Harness Engineering Is Cybernetics](https://x.com/odysseus0z/status/2030416758138634583) |George|
|[The Anatomy of an Agent Harness](https://x.com/Vtrivedy10/status/2031408954517971368) | Viv|
|[Harness capabilities](https://docs.langchain.com/oss/python/deepagents/harness) | Langchain docs |

### 学习资源
* [Reliable AI Systems](https://www.to2d.xyz/)


## ⚙️ 实战教程入口

本仓库提供完整实践路径：

- 🧪 Step 1：构建基础 Agent → `docs/05-practice.md`
- 🧪 Step 2：加入工具调用 → `examples/`
- 🧪 Step 3：构建 Harness（核心） → `examples/`
- 🧪 Step 4：评估系统 → `examples/`
- 🧪 Step 5：优化与对比 → `docs/06-advanced.md`

## ⚔️ Harness Engineering vs 其他范式

| 技术 | 特点 | 问题 |
| --- | --- | --- |
| Prompt Engineering | 简单、上手快 | 不可控、难维护 |
| Fine-tuning | 任务适配精准 | 成本高、迭代慢 |
| Agent Engineering | 灵活、扩展强 | 行为不稳定 |
| ✅ Harness Engineering | 可控 + 可评估 + 可演进 | 学习成本较高 |

结论：Harness Engineering 是走向工业级 AI 系统的关键一步。

## 📊 Demo

你可以在后续版本中展示如下内容：

- 输入：用户问题
- 输出：Agent 推理路径 + 最终结果
- 指标：准确率 / 一致性 / latency / 成本

建议补充 GIF 或截图，提升可读性和传播效果。

## 🗺️ 学习路径

推荐阅读顺序：

1. `docs/01-introduction.md`
2. `docs/02-origin.md`
3. `docs/03-core-concepts.md`
4. `docs/04-architecture.md`
5. `docs/05-practice.md`
6. `docs/06-advanced.md`
7. `docs/07-comparison.md`

## 🛠️ 技术栈

- Python / FastAPI
- LangGraph / LangChain
- OpenAI / LLM API
- Redis / Vector DB
- Evaluation Framework（可自研）

## 🤝 Contributing

欢迎通过以下方式参与共建：

- 提交实战案例（examples）
- 补充评估方法（metrics / eval）
- 优化系统架构与工程模板
- 完善教程文档与图示

你可以先阅读各模块 `README` 或文档章节，再提交 PR。

## ⭐ 如果这个项目对你有帮助

请给一个 Star ⭐，这对项目持续迭代非常重要。
