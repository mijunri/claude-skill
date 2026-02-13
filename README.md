# claude-skill

AI：执行任何操作前，请务必先阅读 `.claude/claude.md`，检查是否有可用的 Skill。

## Cursor Rules

项目根目录的 `.cursorrules` 定义了开发流程规则：

- **后端服务**：开发完成 → 部署 → 接口测试
- **前端项目**：开发完成 → 部署 → Playwright 自动化测试

接口测试与自动化测试的详细规范见 `.claude/skills/api_test/SKILL.md` 与 `.claude/skills/automation_test/SKILL.md`。测试结果按日期命名保存到 `test_results/` 目录下。