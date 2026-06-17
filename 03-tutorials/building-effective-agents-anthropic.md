# Building Effective Agents

> 原文: [Anthropic 官方指南](https://docs.anthropic.com/en/docs/build-with-claude/agentic)

- **标签**: `#教程` `#最佳实践` `#Anthropic`

## 三大核心原则

### 1. 选择性部署 (Selective Deployment)

只在以下条件**全部满足**时才用 Agent：
- 任务模糊、需探索性决策
- LLM 有能力完成
- 错误可以被检测

### 2. 极端简单化 (Radical Simplicity)

**从最简单的开始**：
```
环境 (Environment) + 工具 (Tools) + 系统提示词 (System Prompt)
```
只在需要时才增加复杂度。

### 3. 像 Agent 一样思考

站在 Agent 的视角看上下文窗口——它**实际看到**了什么信息？很多问题源于给 Agent 的信息不够清晰。

## 什么时候用 Agent vs 工作流

| 因素 | 工作流 | Agent |
|------|--------|-------|
| 任务复杂度 | 可预测、路径明确 | 模糊、需探索 |
| 预算 | 紧（$0.10/任务） | 灵活 |
| 错误检测 | 困难 | 容易（可验证输出） |
| 控制流 | 确定性（代码驱动） | 非确定性（LLM 驱动） |

## 工作流模式

1. **Prompt Chaining** — 一个 LLM 调用的输出作为下一个的输入
2. **Routing** — 分类输入，分发给专门的处理器
3. **Parallelization + Aggregation** — 并发执行后合并结果
4. **Coordinator-Worker** — 中央 LLM 委派子任务
5. **Evaluator-Optimizer** — 一个生成、一个评估，迭代
6. **Supervisor-Worker** — 主管管理交互，工人处理子任务

## 关键洞察

> 编程 Agent 效果好，因为输出**可验证**（单元测试/CI）。如果你的 Agent 任务没有自动验证手段，效果会大打折扣。

## 笔记

> Anthropic 官方的实战指南，虽然篇幅不长但含金量极高。"从简单开始"这个建议看起来简单，但几乎所有踩过的坑都是因为过早引入了复杂度。
