---
tags: [database, topic-modeling]
aliases: [JOIN 专题, 建模专题]
---

# 表设计与 JOIN

## 一句话定义

一个事实只存一次，其他地方存编号引用；查时用 JOIN 拿编号找详情再拼回去。

## 核心机制

- 一对多：`datasets(1) → runs(N) → metrics(N)`。
- 主键 = 身份证（唯一+非空）；外键 = 指向爹的编号（必须真实存在）。
- `UNIQUE` 防重复事实，`CHECK` 防非法值。
- SQLite 外键默认关闭：每连接 `PRAGMA foreign_keys = ON` 并核验。
- `ON` 管怎么拼（外键 = 主键），`WHERE` 管拼完留哪些。
- INNER 只留两边匹配；LEFT 左全留缺失补 NULL。
- **套路**：`LEFT JOIN + WHERE 右表列 IS NULL` = 找孤儿行。

## 代码模板

```sql
-- 基础拼表
SELECT runs.id, runs.model, datasets.name FROM runs
JOIN datasets ON runs.dataset_id = datasets.id ORDER BY runs.id;
-- 找孤儿
SELECT runs.id FROM runs
LEFT JOIN metrics ON metrics.run_id = runs.id
WHERE metrics.run_id IS NULL ORDER BY runs.id;
```

## 关联

- [[2026-09-17]]（D2 全记录，含三表数据与逐行推演）| [[SQL基础]] | [[事务与ACID]]
- 练习：`labs/sql/answers_day02.sql`（8/8）+ 约束验证 3/3
