# Generative Agents: Interactive Simulacra of Human Behavior

- **作者**: Joon Sung Park et al. (Stanford)
- **会议**: ICLR 2023 (UIST 2023)
- **链接**: [arXiv:2304.03442](https://arxiv.org/abs/2304.03442)
- **标签**: `#多智能体` `#社会模拟` `#经典`

## 核心贡献

创建了 **斯坦福 AI 小镇**——25 个 AI Agent 在一个数字小镇中自主生活，展现出类人社会行为：

- Agent 会**起床、做早餐、上班、聊天、约会**
- 信息通过 Agent 之间的对话**自然传播**
- 没有脚本，全靠 Agent 自主决策

## 架构三组件

| 组件 | 说明 |
|------|------|
| **记忆流 (Memory Stream)** | 所有经历的时间线，按重要性、相关性、近因性检索 |
| **反思 (Reflection)** | 定期将记忆抽象为更高层的洞察 |
| **规划 (Planning)** | 基于角色和记忆生成日常计划 |

## 影响

- 开创了**多 Agent 社会模拟**研究范式
- 记忆流+反思+规划的架构被后续大量工作沿用
- 展示了 emergent social behavior 的可能性

## 笔记

> 这篇论文证明了"Agent 交互可以产生超越单 Agent 能力的涌现行为"。记忆流的设计尤其值得学习——如何在不同抽象层次管理记忆。
