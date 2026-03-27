# 04. Architecture

## 架构目标

构建一个“可控、可测、可评估”的 Agent 系统分层架构。

## 推荐分层

1. Prompt Layer  
   负责提示词模板、上下文管理、策略注入。

2. Agent Orchestrator  
   负责任务拆解、流程编排、状态管理与异常处理。

3. Tool Layer  
   负责外部工具与系统能力调用（检索、数据库、API 等）。

4. Evaluation Harness  
   负责自动化测试集执行、结果对比、评分产出。

5. Metrics & Observability  
   负责日志、追踪、告警、性能和成本看板。

## 图示约定

请将架构图放置在：`diagrams/architecture.png`。
