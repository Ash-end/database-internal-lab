---
tags: [database, topic-transaction]
aliases: [ACID 专题, 事务专题]
---

# 事务与 ACID

## 一句话定义

多步操作打包成一步：要么全生效，要么全撤销（书 79–80 页）。

## 核心机制

- 三件套：自动开始（首条写操作）→ `commit()` 生效 / `rollback()` 撤销。
- Python 三规则：自动开始；commit 前仅本连接可见；忘 commit 就关 = 白干。
- ACID：A 不可分；C 合法到合法（唯一用户也要负责）；I 未提交不可见；
  D 提交落盘（靠日志，D8 展开）。
- 图 1-1 定位：A=事务管理器，I=锁管理器，D=恢复管理器+日志，C=到处都是。

## 代码模板

```python
try:
    conn.execute("INSERT INTO runs ...")
    conn.execute("INSERT INTO metrics ...")
    conn.commit()
except Exception:
    conn.rollback()
```

## 关联

- [[2026-09-17-D4]]（D4 全记录，5 个实测例子）| [[表设计与JOIN]]（约束即 C 的一部分）
- 演示：`labs/sql/learn_day04.py`
- 待：D8（隔离级别、WAL、锁、MVCC）、D7 变式验收（G1）
