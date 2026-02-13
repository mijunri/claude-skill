---
name: environment
description: 项目环境配置规范。使用 .env 存实际环境配置，dev.env 存开发环境配置；project.yaml 存项目名与 GitHub 路径。
---

# 项目环境配置 Skill

处理项目环境配置时遵循以下规范。

## 项目信息

| 文件 | 用途 | 是否提交 |
|------|------|----------|
| `project.yaml` | 项目名称、GitHub 仓库路径等基础信息 | 是 |

**示例：**
```yaml
# project.yaml
name: my-project
github: https://github.com/owner/repo
# 或简写：owner/repo
```

## 环境配置

| 文件 | 用途 | 是否提交 |
|------|------|----------|
| `.env` | 实际环境（生产/预发等）配置，含敏感凭据 | 否，加入 .gitignore |
| `dev.env` | 开发环境配置，可包含示例/占位值 | 是 |

**规则：**
- 应用启动时按环境选择加载 `.env` 或 `dev.env`
- `.env` 不得提交，在 `.gitignore` 中显式忽略
- 可提供 `.env.example` 列出所需变量名（不含实际值），供他人参考

## 目录结构示例

```
项目根目录/
├── project.yaml      # 项目名称、GitHub 路径
├── .env              # 实际环境（不提交）
├── dev.env           # 开发环境
└── .env.example      # 变量清单（可选）
```
