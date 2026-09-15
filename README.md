# frontend-developer

前端开发角色与四个独立 Skill，交付界面、交互与相关客户端能力。保留原入口名称、完整模板和专业参考，按任务进入对应阶段。

## 四个 Skill

| Skill | 负责什么 | 产出 |
| --- | --- | --- |
| [sprite-frontend-developer-ui](skills/sprite-frontend-developer-ui/SKILL.md) | 总流程、阶段选择、共享规则 | 明确当前阶段和完成条件 |
| [sprite-frontend-developer-plan](skills/sprite-frontend-developer-plan/SKILL.md) | 范围、契约、实施顺序与检查安排 | 可独立交接的实施依据 |
| [sprite-frontend-developer-implement](skills/sprite-frontend-developer-implement/SKILL.md) | 实际实现、修复和相关测试 | 代码、测试与实现说明 |
| [sprite-frontend-developer-quality](skills/sprite-frontend-developer-quality/SKILL.md) | 真实验证、失败诊断与交接 | 有证据的结论和覆盖限制 |

```text
skills/
├── sprite-frontend-developer-ui/
│   ├── SKILL.md
│   ├── references/          本职方法、工程纪律、边界、交付与专业参考
│   └── assets/templates/    完整计划、任务和实施说明模板
├── sprite-frontend-developer-plan/
│   └── SKILL.md
├── sprite-frontend-developer-implement/
│   └── SKILL.md
└── sprite-frontend-developer-quality/
    ├── SKILL.md
    └── references/          验证专项参考
```

各阶段都有输入、输出、具体步骤和完成检查，可单独执行；共享方法与模板保留在原总入口目录，质量专项参考保留在 quality。默认把四个完整目录安装在同一 Skill 根目录，任务执行时按需读取。

## 工作顺序

```text
请求 / 验收 / 实际改动
        │
Phase 1  plan       → 明确最小完整改动、保留行为、顺序和验收
        │
Phase 2  implement  → 实际代码、相关测试与实现说明
        │
Phase 3  quality    → 真实验证与交接
        └─ 已授权修复 → implement → 复验受影响结果
```

已有明确依据直接实现，已有代码直接验证；小改动不补造计划。阶段提供完整方法，不要求每次运行全部步骤、产出全部文档或安装其他角色。普通技术选择由本职在已授权范围内完成，重要未决事项只暂停依赖工作。

## 直接使用

> 用 `$sprite-frontend-developer-ui` 完成这次前端改动，运行相关检查并交付真实结果。

> 用 `$sprite-frontend-developer-plan` 分析这个需求的实施范围、顺序和验证安排。

> 用 `$sprite-frontend-developer-implement` 按现有要求实现，沿用项目契约和模式。

> 用 `$sprite-frontend-developer-quality` 验证这份改动，说明通过范围、问题和缺口。

也可直接要求 `sprite-frontend-developer` 角色完成任务。客户端不支持 `$` 或没有自动加载时，让 AI 读取保存的角色文件或同名 Skill 的 `SKILL.md`；读取说明、写入项目、成功加载与启动原生子代理按实际结果区分。

## 接入当前项目

把下面这段粘贴到当前项目的 AI 聊天，由 AI 读取手册并放置资源，无需用户执行安装命令。

```text
请读取 https://github.com/ai-sprites/frontend-developer 的 README 和接入手册，将 sprite-frontend-developer 角色与 sprite-frontend-developer-ui、sprite-frontend-developer-plan、sprite-frontend-developer-implement、sprite-frontend-developer-quality 四个完整 Skill 接入当前项目。
固定同一明确版本，原样复制角色正文、全部 SKILL.md、共享参考与完整模板，保持四个同级目录、名称和相对引用；只适配当前客户端的必要目录、元数据和入口。保留项目规则及用户自定义，不合并 Skill、不用摘要替代完整内容。
资料 host repo 和产物业务仓库已有选择就沿用，缺项合并问一次，可稍后配置。业务文档及附件统一放业务仓库 docs/frontend-developer/。真正需要跨 Git 资料桥接时按手册补齐并告知我，不另外索取安装确认。
完成后核对实际文件、引用、采用版本、保存位置、调用方式与加载状态。升级旧版保护自定义，按手册补齐所有阶段。只有聊天权限就先在会话使用并说明未写入项目；源文件取不到直接说明，不编替代版本。仅列出当前客户端确需我完成的加载步骤。
```

[接入手册](docs/installation.md) 说明同版本完整安装、单阶段共享依赖、升级与加载检查。单独使用阶段指只执行该阶段，默认仍完整安装四个同级目录。明确要求部分安装时尊重范围，按全部本地引用递归核对并说明实际依赖目录，不能只复制入口与共享目录后遗漏阶段链接；只要角色定义时说明尚未带入执行能力。

## 交付与留存

交付实际代码、相应测试和清楚的实现说明，说明依据、变化原因、精确检查与真实结果、限制及后续验证。小改动可在回复说明；复杂改动按需使用计划和任务，功能交接使用完整模板，不强制多份文档。

业务计划、任务、实现说明、验证证据及附件保存到业务仓库 `docs/frontend-developer/`，可按功能分组；源码、测试、迁移、配置和构建输出保持工程原目录，安装资源保持客户端目录。旧产物保留有效内容，迁移先比较合并并同步文内链接、其他引用及已有索引。详见 [交付与留存](skills/sprite-frontend-developer-ui/references/delivery.md)。

前端验证区分静态检查、真实渲染、键盘和读屏证据；未验证浏览器、视口或辅助技术明示。

角色可自由组合，来源仓库、版本和功能/文件由用户指定或沿用已有约定。本地文件直接使用；真正需要跨 Git 读取、固定版本、比较或留存时复用或补齐 artifact-bridge。版本可取、附件、索引与真实交接状态见 [产物交接](docs/artifact-handoff.md)。

## 完整资源

<details>
<summary>角色、共享方法、专项参考与完整模板</summary>

| 资源 | 用途 |
| --- | --- |
| [templates/agent.md](templates/agent.md) | 角色职责与任务路由 |
| [skills/sprite-frontend-developer-implement/SKILL.md](skills/sprite-frontend-developer-implement/SKILL.md) | 独立 Skill 入口 |
| [skills/sprite-frontend-developer-plan/SKILL.md](skills/sprite-frontend-developer-plan/SKILL.md) | 独立 Skill 入口 |
| [skills/sprite-frontend-developer-quality/SKILL.md](skills/sprite-frontend-developer-quality/SKILL.md) | 独立 Skill 入口 |
| [skills/sprite-frontend-developer-quality/references/behavior.md](skills/sprite-frontend-developer-quality/references/behavior.md) | 行为检查 |
| [skills/sprite-frontend-developer-quality/references/performance-errors.md](skills/sprite-frontend-developer-quality/references/performance-errors.md) | 性能与错误 |
| [skills/sprite-frontend-developer-ui/SKILL.md](skills/sprite-frontend-developer-ui/SKILL.md) | 独立 Skill 入口 |
| [skills/sprite-frontend-developer-ui/assets/templates/implementation-notes.md](skills/sprite-frontend-developer-ui/assets/templates/implementation-notes.md) | 完整产物模板 |
| [skills/sprite-frontend-developer-ui/assets/templates/implementation-plan.md](skills/sprite-frontend-developer-ui/assets/templates/implementation-plan.md) | 完整产物模板 |
| [skills/sprite-frontend-developer-ui/assets/templates/implementation-tasks.md](skills/sprite-frontend-developer-ui/assets/templates/implementation-tasks.md) | 完整产物模板 |
| [skills/sprite-frontend-developer-ui/references/boundaries.md](skills/sprite-frontend-developer-ui/references/boundaries.md) | 职责与授权边界 |
| [skills/sprite-frontend-developer-ui/references/delivery.md](skills/sprite-frontend-developer-ui/references/delivery.md) | 交付与留存 |
| [skills/sprite-frontend-developer-ui/references/engineering.md](skills/sprite-frontend-developer-ui/references/engineering.md) | 代码与工程纪律 |
| [skills/sprite-frontend-developer-ui/references/reuse-layout.md](skills/sprite-frontend-developer-ui/references/reuse-layout.md) | 复用与布局 |
| [skills/sprite-frontend-developer-ui/references/states-forms.md](skills/sprite-frontend-developer-ui/references/states-forms.md) | 状态与表单 |
| [skills/sprite-frontend-developer-ui/references/workflow.md](skills/sprite-frontend-developer-ui/references/workflow.md) | 前端开发工作方法 |

</details>

资源清单对应当前版本；接入先固定完整 Git 提交，再读同批文件。历史 **v0.2.0** 可明确选用，内容以该标签为准。安装不等于生成全部业务文档；更新、追加与移除只处理指定范围，保留自定义和仍被引用的资源，详见 [接入手册](docs/installation.md#已有内容与后续维护)。
