---
tags: [database, topic-sql]
aliases: [SQL 专题]
---

# SQL 基础

## 一句话定义

声明式语言：描述**要什么**，不描述怎么做（优化器决定怎么走）。

## 核心机制

```sql
SELECT 列        -- ④ 选什么列
FROM 表          -- ① 从哪张表
WHERE 条件       -- ② 筛选行
ORDER BY 列      -- ③ 排序
LIMIT n;         -- ⑤ 截断
```

- 书写顺序 ≠ 执行顺序：FROM → WHERE → ORDER BY → SELECT → LIMIT。
- NULL 是未知：用 `IS NULL`，不能用 `=`；任何值与 NULL 运算仍是 NULL。
- 常用：`DISTINCT` 去重、`BETWEEN` 闭区间、`LIKE`（`%` 多字、`_` 单字）。

## 代码模板

```sql
SELECT id, model FROM experiments
WHERE status = 'completed' AND accuracy >= 0.85
ORDER BY accuracy DESC, id ASC
LIMIT 3;
```

## 关联

- [[2026-09-16]]（D1 全记录）| [[表设计与JOIN]] | [[聚合统计]]
- 练习：`labs/sql/answers_day01.sql`（12/12）
