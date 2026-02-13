---
name: temp_scripts
description: 临时脚本规范。一次性任务、排查用脚本放在 temp_scripts 目录。
---

# 临时脚本 Skill

处理临时脚本时，统一放在 `temp_scripts/` 目录。

## 目录

- 所有临时脚本置于 `temp_scripts/`
- 一次性任务、排查用脚本、实验性代码等均归此类

## 命名规范

- 格式：`YYYYMMDD_功能描述.扩展名`，日期开头，下划线后接功能
- 示例：`20250213_export_orders.py`、`20250213_debug_payment.sh`

## 何时使用

- 一次性数据修复或导入
- 问题排查、调试用脚本
- 临时实验或 POC
- 用毕可删除的辅助脚本

## 规范

- 脚本头部注明用途与日期，例如：`# 用于 XXX，2025-02 创建`
- 用毕或废弃后及时删除或标注 `# deprecated`
- 避免将临时脚本放到 `db_scripts/` 或 `scripts/` 等持久化目录
