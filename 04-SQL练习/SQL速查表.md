---
tags: [database, sql, cheatsheet]
aliases: [SQL 速查]
---

# SQL 速查表

## 查行

```sql
SELECT 列 FROM 表 WHERE 条件 ORDER BY 列 LIMIT n;
SELECT DISTINCT 列 FROM 表;              -- 去重
WHERE accuracy IS NULL;                 -- 空判断（不用 =）
WHERE x BETWEEN -6 AND 0;               -- 闭区间
WHERE model LIKE 'Trans%';              -- % 多字，_ 单字
```

## 拼表

```sql
FROM a JOIN b ON a.fk = b.id;           -- 内连接
FROM a LEFT JOIN b ON a.fk = b.id
WHERE b.id IS NULL;                     -- 找孤儿行
```

## 算数

```sql
SELECT COUNT(*) FROM t;                 -- 数行
SELECT g, COUNT(x) FROM t GROUP BY g HAVING COUNT(x) > 2;
SELECT ROUND(AVG(x), 2) FROM t;         -- 修浮点
WITH c AS (SELECT ...) SELECT * FROM c; -- CTE
```

## 改数（Python 里记得 commit）

```sql
INSERT INTO t (a, b) VALUES (?, ?);
UPDATE t SET a = ? WHERE id = ?;
DELETE FROM t WHERE id = ?;
```

## 执行顺序

```
FROM → JOIN → WHERE → GROUP BY → HAVING → SELECT → ORDER BY → LIMIT
```
