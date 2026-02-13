# claude-skill

Claude 可复用的技能指令集，存放在 `.claude/skill/` 目录下。

## 可用技能

| 技能 | 文件 | 用途 |
|------|------|------|
| 代码审查 | `code-review.md` | 系统化代码审查（正确性、安全性、性能等） |
| 重构 | `refactor.md` | 安全、小步的重构指导 |
| 文档编写 | `documentation.md` | README、API、设计文档规范 |
| 测试编写 | `testing.md` | 单元/集成测试实践 |
| Git 提交 | `git-commit.md` | 规范的 commit message 格式 |
| 调试 | `debug.md` | 系统化问题排查方法 |
| 安全审查 | `security-check.md` | 常见安全漏洞检查 |

## 使用方式

在对话中引用技能，例如：`@code-review` 或 `@.claude/skill/code-review.md`