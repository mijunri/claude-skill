---
name: logging
description: 日志规范。时间戳、HTTP 出入参、数据库 SQL、第三方接口参数与返回值，统一 JSON 格式，输出到指定日志目录。
---

# 日志 Skill

处理项目日志时遵循以下规范。

## 日志目录与滚动

- 日志存放于**项目根目录下**的 `logs/` 目录
- 按类型分流到不同文件，**按日期滚动**（如 `app.2025-02-13.log`，或使用 `app.log` 搭配按日切割）

| 文件 | 内容 |
|------|------|
| `logs/app.log` | 应用通用日志 |
| `logs/error.log` | 错误、异常日志 |
| `logs/sql.log` | 数据库 SQL 执行日志 |
| `logs/http.log` | HTTP 请求/响应日志（入站、出站） |
| `logs/third_party.log` | 第三方接口调用日志 |

**滚动规则：**
- 按日期滚动，如 `app.2025-02-13.log`、`sql.2025-02-13.log`
- 或保留当前文件 `app.log`，由日志框架按日切割并归档历史文件

## 格式要求

- **统一 JSON 格式**，便于解析与检索
- **必须有时间戳**，格式如 `ISO 8601`：`2025-02-13T10:30:00.123Z` 或 `YYYY-MM-DD HH:mm:ss.SSS`

## 记录范围

### 1. 外部 HTTP 请求（入站/出站）

- **入站**：请求的 URL、Method、Headers、Body（入参）
- **出站**：请求的 URL、Method、Headers、Body（入参）、响应的 Status、Body（出参）

示例：
```json
{
  "timestamp": "2025-02-13T10:30:00.123Z",
  "type": "http_request",
  "direction": "outbound",
  "url": "https://api.example.com/v1/orders",
  "method": "POST",
  "request": { "orderId": "123", "amount": 100 },
  "response": { "code": 0, "data": { "id": "xxx" } },
  "status": 200
}
```

### 2. 数据库请求

- 打印 **SQL 语句**（含占位符替换后的完整 SQL，或参数与 SQL 分开记录）
- 可选：影响行数、执行耗时

示例：
```json
{
  "timestamp": "2025-02-13T10:30:00.124Z",
  "type": "db_query",
  "sql": "SELECT id, name FROM users WHERE id = ?",
  "params": ["123"],
  "rows_affected": 1,
  "duration_ms": 5
}
```

### 3. 第三方接口调用

- 调用参数（入参）
- 返回值（出参）
- 异常信息（若有）

示例：
```json
{
  "timestamp": "2025-02-13T10:30:00.125Z",
  "type": "third_party",
  "service": "payment-gateway",
  "action": "createPayment",
  "request": { "amount": 100, "currency": "CNY" },
  "response": { "transactionId": "tx_xxx", "status": "success" }
}
```

## 敏感信息

- 密码、token、密钥等敏感字段需脱敏（如 `***` 或部分掩码）
- 可配置脱敏字段列表
