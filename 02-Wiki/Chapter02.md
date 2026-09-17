---
tags: [database, chapter-02]
aliases: [第二章笔记]
---

# Chapter 2：B-Tree Basics

> PDF 45–62（书 25–42 页）。

## 核心问题

内存里好好的搜索树，为什么不能直接放磁盘？什么样的树适合磁盘？

## 关键概念

- BST 的病：不平衡退化 O(N)；旋转维护贵；节点散落无局部性。
- 磁盘约束：按块传输；高度 = 寻道次数；fanout 越高高度越矮。
- B 树：N 键 + N+1 指针，键有序，occupancy；B+ 值只放叶。
- 查找：根→叶，读盘数 = 层数；比较是节点内二分（两笔账）。
- 分裂四步 / 合并三步；只根分裂时长高。
- 1971 Bayer & McCreight；1979 Comer 集大成。

## 🤯 最有趣的发现

32 个数顺序插入只长高 3 次——平衡不用人管，结构自己维持。

## ✨ 侧栏学习

- 手写迷你 B 树验证分裂（`labs/sql/learn_day05_btree.py`）。
- 阶段图：`attachments/stage*.png`。

## ❓ 未解问题

- 叶子 sibling 指针的范围扫描具体快多少？（D6/D9 涉及 SSTable 时回看）

## 🔗 关联章节

- [[Chapter01]]（三旋钮的实例化）| [[索引与B树]]
- 待：Chapter03（编码，D6）、Chapter05 深读（D8）
