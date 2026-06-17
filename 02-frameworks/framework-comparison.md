# 框架对比指南

> 2025 年主流 Agent 框架的对比与选型建议。

## 速览

| 框架 | 发布方 | 最佳场景 | 语言 | 核心特色 |
|------|--------|----------|------|----------|
| [OpenAI Agents SDK](https://github.com/openai/openai-agents-python) | OpenAI | 生产级单/多 Agent | Py/JS | Agent Builder 可视化、ChatKit、Evals |
| [LangGraph](https://github.com/langchain-ai/langgraph) | LangChain | 有状态、复杂分支图 | Py/JS | 图状态机、人机交互、持久化 |
| [CrewAI](https://github.com/crewAIInc/crewAI) | CrewAI | 角色分工团队 | Py | 角色定义、任务委派、轻量 |
| [AutoGen (AG2)](https://github.com/ag2ai/ag2) | Microsoft | 事件驱动多 Agent | Py | 对话驱动、代码生成、调试 |
| [LlamaIndex Workflows](https://github.com/run-llama/llama_index) | LlamaIndex | 数据密集型/RAG | Py/TS | 数据索引、查询引擎、Agent+RAG |
| [Pydantic AI](https://github.com/pydantic/pydantic-ai) | Pydantic | 类型安全 | Py | FastAPI 原生、类型检查、结构化 |
| [Smolagents](https://github.com/huggingface/smolagents) | HuggingFace | 小 Agent 实验 | Py | 轻量、代码执行 |
| [Vercel AI SDK](https://github.com/vercel/ai) | Vercel | Next.js 应用 | TS/JS | 流式、SSR、Edge Runtime |

## 详细分析

### OpenAI Agents SDK
- **核心概念**: Agent + Handoff + Guardrails
- **亮点**: 可视化 Agent Builder、内置 Eval 系统
- **适合**: 想快速上生产、不走弯路

### LangGraph
- **核心概念**: StateGraph + Node + Edge
- **亮点**: 状态管理、分支控制、Human-in-the-loop
- **适合**: 需要精细控制执行流程的复杂应用

### CrewAI
- **核心概念**: Agent + Task + Crew + Process
- **亮点**: 角色定义直觉、Sequential/Hierarchical 流程
- **适合**: 团队协作模拟、内容生成流程

### AutoGen / AG2
- **核心概念**: Agent + Chat + Tool
- **亮点**: 代码生成与执行、多 Agent 辩论
- **适合**: 多 Agent 对话、代码任务

## 选型决策树

```
需要可视化 Agent Builder?
├── 是 → OpenAI Agents SDK
└── 否
    ├── 需要精细图控制?
    │   ├── 是 → LangGraph
    │   └── 否
    │       ├── 角色分工明确?
    │       │   ├── 是 → CrewAI
    │       │   └── 否
    │       │       ├── 数据/RAG 密集型?
    │       │       │   ├── 是 → LlamaIndex
    │       │       │   └── 否
    │       │       │       ├── 类型安全优先?
    │       │       │       │   ├── 是 → Pydantic AI
    │       │       │       │   └── 否
    │       │       │       │       ├── 事件驱动多 Agent?
    │       │       │       │       │   ├── 是 → AutoGen
    │       │       │       │       │   └── 否 → 随便选
```
