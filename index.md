---
tags: [database, moc]
aliases: [数据库学习主页]
---

# Database Internals 学习笔记

## 学习进度

| 天数 | 主题 | 笔记 | 状态 |
|------|------|------|------|
| D1 | SQL 基础 | [[2026-09-16]] | 进行中 |
| D2 | 关联查询与多表设计 | | 待开始 |
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

## 项目文件位置

- 练习代码：`F:\mywork\Project\database\database_internals_day01_starter\database-internals-lab\`
- 笔记位置：本 vault

## 核心概念索引

### SQL 基础
- [[#SELECT 查询结构]]
- [[#NULL 的特殊性]]
- [[#聚合函数]]

### 存储引擎
- Bitcask 模型
- LSM 树
- B 树

### 分布式系统
- 2PC (两阶段提交)
- Raft 共识算法

