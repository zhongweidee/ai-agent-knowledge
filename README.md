# AI Agent 知识库

> 从理论到实践的 AI Agent 知识体系构建。

## 目录结构

```
01-papers/         论文阅读笔记
  ├── surveys/     顶级综述
  └── classics/    经典单篇论文
02-frameworks/     Agent 框架对比与指南
03-tutorials/      构建教程与最佳实践
04-glossary/       术语表
05-tools/          常用工具与资源
06-references/     外部参考链接
```

## 快速导航

### 📚 必读综述

| 综述 | 年份 | 核心贡献 |
|------|------|----------|
| [Agent AI: Surveying the Horizons of Multimodal Interaction](01-papers/surveys/li-agent-ai-survey.md) | 2024 | 李飞飞团队，80页多模态 Agent 框架 |
| [LLM based Autonomous Agents](01-papers/surveys/llm-autonomous-agents-survey.md) | 2023 | 奠基性综述，感知-记忆-行动框架 |
| [Model-Native Agentic AI](01-papers/surveys/model-native-agentic-ai.md) | 2025 | Pipeline→Model-Native 范式转变 |
| [From LLM Reasoning to Autonomous AI Agents](01-papers/surveys/reasoning-to-agents-review.md) | 2025 | 60+ Benchmark，10+ 领域应用 |
| [Agentic AI: Multi-Agent Architectures](01-papers/surveys/agentic-ai-systematic-survey.md) | 2026 | 六维度统一分类法 |

### ⭐ 经典论文

| 论文 | 领域 | 重要性 |
|------|------|--------|
| **ReAct** (Yao et al., 2023) | 推理+行动 | 几乎所有现代 Agent 的基础 |
| **Chain-of-Thought** (Wei et al., 2022) | 推理 | CoT 推理奠基之作 |
| **Tree of Thoughts** (Yao et al., 2023) | 推理 | 多路径搜索推理 |
| **Generative Agents** (Park et al., 2023) | 多智能体 | 斯坦福 AI 小镇 |
| **AutoGen** (Microsoft, 2023) | 多智能体 | 微软多 Agent 对话框架 |
| **Toolformer** (Schick et al., 2023) | 工具使用 | LLM 自学使用工具 |
| **CoALA** (2024) | 认知架构 | 语言 Agent 认知架构理论框架 |
| **MemGPT** (2023) | 记忆 | LLM 分层记忆管理 |

### 🔧 框架速览

| 框架 | 最适合 | 语言 |
|------|--------|------|
| **OpenAI Agents SDK** | 生产级 Agent | Py/JS |
| **LangGraph** | 有状态、分支图 | Py/JS |
| **CrewAI** | 角色分工团队 | Py |
| **AutoGen (AG2)** | 事件驱动多 Agent | Py |
| **LlamaIndex Workflows** | 数据密集型/RAG | Py/TS |
| **Pydantic AI** | 类型安全 | Py |
| **Vercel AI SDK** | Next.js 应用层 | TS/JS |

## 推荐阅读顺序

```
入门 ──→ 李飞飞综述 + ReAct
  │
  ├──→ CoALA + Generative Agents（建立框架认知）
  │
  ├──→ Model-Native 综述（把握前沿方向）
  │
  ├──→ Anthropic《Building Effective Agents》（实战）
  │
  └──→ 按需深入：工具 / 多智能体 / 记忆 / 安全
```
