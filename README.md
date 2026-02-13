# claude-skill

Claude 可复用的技能指令集，存放在 `.claude/skills/` 目录下。每个技能是一组预设指令，可在对话中引用以指导 Claude 按特定方式完成任务。

## Claude Skill 用法

### 什么是 Claude Skill？

Skill 是预先编写好的指令文件（`SKILL.md`），包含某类任务的执行规范。在 Cursor 或 Claude 对话中引用 Skill 后，AI 会遵循其中的规则和流程来协助你。

### 如何引用 Skill？

1. **在对话中输入 `@`**，触发引用菜单
2. **输入技能名称**（如 `database_ops`、`code_review`）或选择对应文件
3. **或直接输入路径**：`@.claude/skills/database_ops/SKILL.md`

引用后，Claude 会加载该 Skill 的指令并在后续回答中应用。

### 使用场景示例

- 代码审查：`@code_review` 请审查这段代码
- 重构代码：`@refactor` 帮我重构这个函数
- 写测试：`@testing` 为这个模块写单元测试
- 写提交信息：`@git_commit` 帮我写 commit message
- 查 Bug：`@debug` 这段代码报错，帮我排查
- 安全检查：`@security_check` 检查这段代码的安全问题
- 数据库相关：`@database_ops` 优化这个查询

### 组合使用

可以同时引用多个 Skill，例如：`@code_review @security_check` 请从代码质量和安全两方面审查。

---

## 目录结构

```
.claude/skills/
├── database_ops/SKILL.md   # 数据库操作
├── code_review/SKILL.md    # 代码审查
├── refactor/SKILL.md       # 重构
├── documentation/SKILL.md  # 文档编写
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