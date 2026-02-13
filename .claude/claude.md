# 项目说明：claude-skill

本仓库提供一组可复用的 Claude Skill，用于在 Cursor/Claude 对话中按预设规范完成各类开发任务。

## Claude Skill 用法

### 什么是 Skill？

Skill 是 `.claude/skills/<技能名>/SKILL.md` 中的指令文档。每个 Skill 定义了某类任务（如代码审查、重构、写测试）的执行规则和输出格式。在对话中引用 Skill 后，Claude 会遵循这些规则来协助你。

### 如何引用 Skill？

1. 在输入框输入 `@`，会弹出引用菜单
2. 输入技能名（如 `database_ops`、`code_review`）或选择对应 `SKILL.md` 文件
3. 也可以直接输入完整路径：`@.claude/skills/database_ops/SKILL.md`

引用后，Claude 会在本次对话中应用该 Skill 的指令。

### 示例

- `@code_review` + 粘贴代码 → 按规范进行代码审查
- `@refactor` + 指定文件/函数 → 按重构原则安全重构
- `@testing` + 指定模块 → 按测试实践编写测试
- `@git_commit` + 说明改动 → 生成规范的 commit message
- `@database_ops` + 查询或迁移 → 按 DB 最佳实践处理
- `@debug` + 错误描述/代码 → 按调试流程排查问题
- `@security_check` + 代码片段 → 进行安全审查
- `@documentation` + 说明文档类型 → 按规范编写文档

### 组合引用

可同时引用多个 Skill，例如：`@code_review @security_check`，让 Claude 同时应用代码审查和安全检查的规则。

## 技能列表

| 技能 | 用途 |
|------|------|
| `database_ops` | 数据库查询优化、事务、迁移、安全 |
| `code_review` | 系统化代码审查（正确性、安全性、性能等） |
| `refactor` | 小步、安全的重构 |
| `documentation` | README、API、设计文档写作规范 |
| `testing` | 单元/集成测试实践 |
| `git_commit` | Conventional Commits 格式 |
| `debug` | 系统化问题排查流程 |
| `security_check` | 常见安全漏洞检查 |

更多说明见项目根目录的 `README.md`。
