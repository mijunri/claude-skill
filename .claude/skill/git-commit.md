# Git Commit Skill

协助编写规范的 Git 提交信息：

## 提交信息格式

```
<type>(<scope>): <subject>

<body>

<footer>
```

## Type 类型

- `feat` - 新功能
- `fix` - Bug 修复
- `docs` - 文档更新
- `style` - 代码格式（不影响逻辑）
- `refactor` - 重构
- `perf` - 性能优化
- `test` - 测试相关
- `chore` - 构建/工具变更

## 规范

- **subject**: 50 字以内，祈使句，如 "add user login" 而非 "added user login"
- **body**: 说明为什么改、改了什么（可选）
- **footer**: 关联 issue，如 `Closes #123`（可选）

## 示例

```
feat(auth): add JWT token refresh mechanism

Implement automatic token refresh when access token expires.
Refresh token is stored in httpOnly cookie for security.
```
