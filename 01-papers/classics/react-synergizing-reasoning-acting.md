# ReAct: Synergizing Reasoning and Acting in Language Models

- **作者**: Shunyu Yao et al. (Princeton)
- **会议**: ICLR 2023
- **链接**: [arXiv:2210.03629](https://arxiv.org/abs/2210.03629)
- **标签**: `#经典` `#ReAct` `#推理` `#行动`

## 核心贡献

提出 **ReAct (Reasoning + Acting)** 范式，将推理轨迹与行动步骤交织在一起，让 LLM 交替进行：

```
思考 (Thought) → 行动 (Action) → 观察 (Observation) → 思考 → ...
```

## 为什么重要

- 几乎所有现代 Agent 框架（LangGraph、AutoGen、CrewAI 等）都基于 ReAct
- 解决了纯推理（CoT）无法与环境交互、纯行动无法推理的问题

## 关键发现

| 范式 | 优势 | 劣势 |
|------|------|------|
| CoT (只推理) | 逻辑连贯 | 无法获取外部信息 |
| Act (只行动) | 能与环境交互 | 缺乏推理规划 |
| **ReAct (推理+行动)** | **两者兼顾** | 需要更多 Token |

## 笔记

> 这是 AI Agent 领域**必须精读**的论文。理解 ReAct 循环是理解所有现代 Agent 的基础。
