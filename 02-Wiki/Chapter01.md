---
tags: [database, chapter-01]
aliases: [第一章笔记]
---

# Chapter 1：Introduction and Overview

> PDF 28–30（8–10 页，架构）、37–42（17–22 页，文件与索引）。

## 核心问题

数据库和"一堆文件"的区别在哪？数据在磁盘上怎么摆才找得快？

## 关键概念

- 请求五层：transport → query processor → optimizer → execution engine → storage engine
  （事务/锁/存取/缓冲/恢复）。
- 索引 = 辅助结构，为不每次全表扫描；索引文件通常比数据文件小。
- 堆文件（无序+索引找）/ 哈希文件（分桶）/ 索引组织表（数据存索引里）。
- 主索引 vs 辅索引；clustered（顺序跟键走）vs nonclustered。
- 三旋钮：Buffering、Mutability、Ordering。

## 🤯 最有趣的发现

查询计划（optimizer 的选择）是可以亲眼看到的：`EXPLAIN QUERY PLAN`。

## ❓ 未解问题

- IOT 和堆+主索引，什么 workload 选哪个？（先记下，D9 对比 LSM 时回看）

## 🔗 关联章节

- [[Chapter02]]（存取结构的具体实现）| [[索引与B树]]
