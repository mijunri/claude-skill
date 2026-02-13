---
name: automation_test
description: 前端自动化测试规范。前端部署后运行 Playwright 测试，测试结果按日期命名保存到指定目录。
---

# 自动化测试 Skill

前端项目部署完成后进行 Playwright 自动化测试时遵循以下规范。

## 时机

- 在**部署完成**后运行 Playwright 自动化测试，验证页面与关键流程

## 测试结果存放

- 目录：`test_results/e2e/` 或 `test_results/playwright/`（位于项目根目录下）
- 命名规范：`YYYYMMDD_描述`，Playwright 默认会生成报告、截图、录像等
- 示例目录结构：
  ```
  test_results/playwright/
  ├── 20250213_regression/
  │   ├── report.html
  │   ├── results.json
  │   ├── screenshots/
  │   └── videos/
  └── ...
  ```

## 记录内容

- 用例执行结果（通过/失败）
- 失败截图、录屏
- 测试报告（HTML/JSON）
- 执行时间、总耗时

## 工具

- **Playwright**：推荐，支持多浏览器、自动等待、截图、录屏
- 测试脚本可放在项目内，如 `tests/e2e/` 或 `e2e/`
