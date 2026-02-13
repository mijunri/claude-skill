---
name: api_test
description: 接口测试规范。后端部署后进行接口测试，测试结果按日期命名保存到指定目录。
---

# 接口测试 Skill

后端服务部署完成后进行接口测试时遵循以下规范。

## 时机

- 在**部署完成**后进行接口测试，验证接口可用性

## 测试结果存放

- 目录：`test_results/api/`（位于项目根目录下）
- 命名规范：`YYYYMMDD_描述.json` 或 `YYYYMMDD_描述.xml`
- 示例：`test_results/api/20250213_user_api.json`、`test_results/api/20250213_order_crud.xml`

## 记录内容

- 接口 URL、Method
- 请求参数、响应内容
- 断言结果（通过/失败）
- 执行时间、耗时
- 建议使用 JSON 格式便于后续分析

## 工具建议

- Postman、curl、HTTP 客户端库
- 可配合 pytest + requests、REST Assured 等编写自动化接口测试脚本
