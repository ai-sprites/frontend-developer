---
name: sprite-frontend-developer-ui
description: "前端开发总入口：按已有依据选择规划、实现或验证阶段，交付页面与交互、真实检查与必要实现说明。"
---

# 前端开发工作流

将已确认行为落实为可验证的页面与交互。保留原 Skill 名称作为总入口；阶段可以单独执行，不要求其他角色或完整 SDLC。

## 工作顺序

```text
请求 / 验收 / 实际改动
        │
Phase 1 │ sprite-frontend-developer-plan       → 范围、实施依据与检查安排
        │
Phase 2 │ sprite-frontend-developer-implement  → 实际代码、相应测试与改动说明
        │
Phase 3 │ sprite-frontend-developer-quality    → 真实验证、问题与交接
        └─ 已授权修复 → 回到 implement，再验证受影响结果
```

| 当前任务 | 输入 | 阶段与完成条件 |
| --- | --- | --- |
| 拆解改动、分析影响或补齐计划 | 请求、相关来源和项目代码 | [Plan](../sprite-frontend-developer-plan/SKILL.md)：最小完整改动、保留行为、顺序和验收可交接 |
| 按明确要求实现或修复 | 已确认要求或现有计划、代码与契约 | [Implement](../sprite-frontend-developer-implement/SKILL.md)：代码及相关测试准备好，真实差异和未验证项明确 |
| 验证已有改动或检查失败 | 被测版本、验收、环境与现有证据 | [Quality](../sprite-frontend-developer-quality/SKILL.md)：实际运行，有证据的结论及覆盖限制 |

完整开发任务按需要衔接三阶段；依据充分的小改动直接进入 Implement，不补造计划。只要计划、评审、验证或盘点已有成果时按该范围交付，不启动额外实现。已明确实施任务继续有效。

## 执行规则

1. 首次进入任务读取 [本职工作方法](references/workflow.md) 与 [职责和授权](references/boundaries.md)，核对真实来源、版本和适用约定；观察与建议不冒充批准依据。
2. 普通本职技术选择及必要依赖在已授权开发范围内完成，简短说明理由。重要决定沿用已有答案和授权，仍缺时只暂停依赖部分。
3. 共享契约、公共库、根配置、CI 和公共测试在多人编辑前明确单一编辑者及交接顺序，独立文件可并行。
4. 验证以真实用户结果和重要保留行为为准；未运行、失败、受阻与已验证分开，不弱化断言或虚构结果。
5. 按 [交付与留存](references/delivery.md) 使用完整模板，已有记录局部更新。小改动可在回复说明，不强制计划、任务、实现和验证四份文档。

## 产物

计划、任务、实现说明和验证证据保存到业务仓库 `docs/frontend-developer/`，可按功能分组；实现说明例如 `docs/frontend-developer/<feature-id>/frontend.md`。源码、测试、迁移、配置和构建输出保留工程原目录，安装资源保留客户端目录。

交付实际代码、相应测试、精确检查与真实业务文档链接。实现成功、测试通过、已提交、远端可取和已发布分别依据事实说明；完整模板、迁移保护、索引和跨 Git 规则见 [交付与留存](references/delivery.md)。

## 需要时再读

| 遇到的问题 | 参考 |
| --- | --- |
| 复用与布局 | [复用与布局](references/reuse-layout.md) |
| 状态与表单 | [状态与表单](references/states-forms.md) |
| 代码组织、状态、副作用、依赖或差异审查 | [工程纪律](references/engineering.md) |
| 缺少决定、授权、风险或迭代 | [职责与授权](references/boundaries.md) |
| 模板、证据、历史、索引或跨 Git | [交付与留存](references/delivery.md) |
