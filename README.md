# claude-skill

Claude 可复用的技能指令集，存放在 `.claude/skills/` 目录下。

## 目录结构

```
.claude/skills/
├── database_ops/SKILL.md   # 数据库操作
├── code_review/SKILL.md    # 代码审查
├── refactor/SKILL.md       # 重构
├── documentation/SKILL.md   # 文档编写
├── testing/SKILL.md        # 测试编写
├── git_commit/SKILL.md     # Git 提交
├── debug/SKILL.md          # 调试
└── security_check/SKILL.md # 安全审查
```

## 可用技能

| 技能 | 路径 | 用途 |
|------|------|------|
| 数据库操作 | `database_ops` | 查询优化、事务、安全、迁移 |
| 代码审查 | `code_review` | 系统化代码审查 |
| 重构 | `refactor` | 安全、小步的重构指导 |
| 文档编写 | `documentation` | README、API、设计文档规范 |
| 测试编写 | `testing` | 单元/集成测试实践 |
| Git 提交 | `git_commit` | 规范的 commit message 格式 |
| 调试 | `debug` | 系统化问题排查方法 |
| 安全审查 | `security_check` | 常见安全漏洞检查 |

## 使用方式

在对话中引用技能，例如：`@database_ops` 或 `@.claude/skills/database_ops/SKILL.md`