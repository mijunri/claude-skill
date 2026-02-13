# 项目说明：claude-skill

本仓库提供可复用的 Claude Skill，用于项目环境与脚本管理。

## Claude Skill 用法

Skill 是 `.claude/skills/<技能名>/SKILL.md` 中的指令文档。当任务涉及下表类型时，请读取对应的 SKILL.md 并遵循其中规则。

## 技能列表

| 用户需求 / 任务类型 | 应读取的 Skill 文件 |
|-------------------|---------------------|
| 环境配置、.env、dev.env、项目结构、脚本目录 | `.claude/skills/environment/SKILL.md` |
| 数据库脚本、SQL、查询、迁移、db_scripts | `.claude/skills/database/SKILL.md` |
| 临时脚本、一次性任务、排查脚本、temp_scripts | `.claude/skills/temp_scripts/SKILL.md` |
| 日志、日志目录、日志格式、HTTP 日志、DB 日志 | `.claude/skills/logging/SKILL.md` |
| 服务器、SSH、远程操作、部署 | `.claude/skills/server_ops/SKILL.md` |

## 引用方式

1. 输入 `@` 后选择技能名或对应 `SKILL.md` 文件
2. 或直接指定路径，如 `@.claude/skills/environment/SKILL.md`
