---
tags: [database, moc]
aliases: [数据库学习主页]
---

# Database Internals 学习笔记

> [!quote] 核心理念
> **费曼技巧**：教别人是最好的学习方式
> **结构化笔记**：原始素材 → 知识图谱，层层递进
> **AI 辅助**：用 Claude 驱动自适应学习闭环

---

## 快速导航

### 学习配置
- [[database-learning-skill|学习技能]] - 方法论与流程
- [[学员档案]] - 个人状态
- [[进度看板]] - 学习进度

### 学习内容
- [[2026-09-17|今日笔记]] - D2 关联查询与多表设计
- [[2026-09-16|D1 笔记]] - SQL 基础
- [[2026-09-17#二、JOIN：把拆开的表拼回去|JOIN 知识点]] - 关联查询

### 参考资源
- [Database Internals](https://www.databasinternals.com/) - 教材
- [database-internals-notes](https://github.com/Akshat-Jain/database-internals-notes) - 前人笔记
- [力扣百题通](https://github.com/mo-lx/LeetCode-BaiTiTong) - 学习方法论

---

## 学习进度

| 天数 | 主题 | 笔记 | 状态 |
|------|------|------|------|
| D1 | SQL 基础 | [[2026-09-16]] | ✅ 完成 |
| D2 | 关联查询与多表设计 | [[2026-09-17]] | 进行中 |
| D3 | 聚合与统计查询 | | 待开始 |
| D4 | 事务与 ACID | | 待开始 |
| D5 | 索引与 B 树 | | 待开始 |
| D6 | 二进制编码与记录格式 | | 待开始 |
| D7 | 复盘与补漏 | | 待开始 |
| D8 | WAL 与恢复机制 | | 待开始 |
| D9 | Bitcask/LSM 树原理 | | 待开始 |
| D10 | MiniKV 实现 | | 待开始 |
| D11 | 压实与错误处理 | | 待开始 |
| D12 | 分布式系统基础 | | 待开始 |
| D13 | 2PC 与 Raft | | 待开始 |
| D14 | 验收与交付 | | 待开始 |

---

## 核心概念索引

### SQL 基础
- [[2026-09-16#SELECT 查询结构]]
- [[2026-09-16#NULL 的特殊性]]
- [[2026-09-16#聚合函数]]

### 存储引擎
- Bitcask 模型
- LSM 树
- B 树

### 分布式系统
- 2PC (两阶段提交)
- Raft 共识算法

