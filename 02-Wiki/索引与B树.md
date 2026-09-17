---
tags: [database, topic-index]
aliases: [B 树专题, 索引专题]
---

# 索引与 B 树

## 一句话定义

索引是数据的目录（有序键 + 行位置）；B 树是目录在磁盘上的形状：又矮又宽。

## 核心机制

- 索引：为不每次全表扫描而设的辅助结构；代价 = 空间 + 写变慢。
- `SCAN` 翻全表 vs `SEARCH USING INDEX` 走目录（万行实测快 4.6 倍）。
- 磁盘按块传输、寻道贵 → 节点即页、高 fanout、低高度。
- N 键 + N+1 指针；根/中间/叶；B+ 值只放叶。
- 读盘次数 = 层数；节点内二分。
- 分裂四步：申请新节点 → 搬一半 → 放新元素 → 父记路牌；只根分裂时长高。
- 哲学：数据结构是硬件的形状；用宽度换高度；有序是免费导航；接受一半空。
- 三旋钮：Buffering / Mutability / Ordering（B 树选原地改+有序）。

## 代码模板

```sql
CREATE INDEX idx_items_grp ON items(grp);
EXPLAIN QUERY PLAN SELECT id FROM items WHERE grp = 42;
-- SEARCH items USING INDEX idx_items_grp (grp=?)
```

```python
# 迷你 B 树：labs/sql/learn_day05_btree.py
# 万行实验：labs/sql/learn_day05.py
```

## 关联

- [[2026-09-17-D5]]（D5 全记录，4 张阶段图）| [[事务与ACID]]（D8 恢复即日志这一面）
- 待：D6 编码（页内长什么样）、D9 LSM（另一套哲学）
