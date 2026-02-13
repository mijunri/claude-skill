# claude-skill

可复用的 AI 技能指令集，供集成到任意项目中。

---

## 致 AI：Skill 所在位置与使用方式

本项目包含一组 **Skill** 文件，位于 `.claude/skills/<技能名>/SKILL.md`。每个 SKILL.md 是一份**任务执行规范**，请在相关任务中**主动读取并遵循**其中的指令。

### Skill 路径一览

| 用户需求 / 任务类型 | 应读取的 Skill 文件 |
|-------------------|---------------------|
| 代码审查、review | `.claude/skills/code_review/SKILL.md` |
| 重构代码、refactor | `.claude/skills/refactor/SKILL.md` |
| 编写测试、写测试 | `.claude/skills/testing/SKILL.md` |
| 写 commit message、提交信息 | `.claude/skills/git_commit/SKILL.md` |
| 排查 bug、调试、debug | `.claude/skills/debug/SKILL.md` |
| 数据库操作、SQL、查询优化、迁移 | `.claude/skills/database_ops/SKILL.md` |
| 安全检查、安全审查 | `.claude/skills/security_check/SKILL.md` |
| 写文档、README、API 文档 | `.claude/skills/documentation/SKILL.md` |

### 使用方式

1. 当用户提出与上表匹配的需求时，**先读取对应的 SKILL.md 文件**
2. 按照该文件中的规则、流程和输出格式完成任务
3. 若用户同时涉及多类任务（如「审查并检查安全」），请读取多个 Skill 并综合应用

例如：用户说「帮我审查这段代码」，应读取 `.claude/skills/code_review/SKILL.md`，再按其中的审查维度和输出格式进行回答。

---

## 集成说明（给人看）

将 `.claude/skills/` 目录复制到你的项目中即可。AI 在读取项目 README 后，会知道 Skill 的位置并在相关任务中自动加载。