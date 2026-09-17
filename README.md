# Database Internals 学习笔记

基于 Alex Petrov《Database Internals》的 14 天数据库强化学习计划。

## 学习目标

- 掌握基础 SQL 操作
- 理解存储引擎内部机制（B树、LSM树、Bitcask）
- 实现一个持久化键值存储引擎（MiniKV）
- 理解分布式系统核心概念（2PC、Raft）

## 目录结构

```
database-internal-lab/
├── 00-学习技能/            # 方法论、学员档案、进度看板
├── 01-Raw/                 # 原始素材（只增不改）
├── 02-Wiki/                # 结构化知识（专题总结 + 章节笔记）
├── 03-学习笔记/            # 每日学习记录
├── 04-SQL练习/             # SQL 练习题与速查
├── 05-Projects/            # MiniKV 项目（D9 起）
├── 06-Outputs/             # 验收证据（G1–G4）
├── attachments/            # 图片附件
├── templates/              # 笔记模板
└── index.md                # 主页（MOC）
```

## 学习进度

| 天数 | 主题 | 状态 |
|------|------|------|
| D1 | SQL 基础 | ✅ 完成 |
| D2 | 关联查询与多表设计 | ✅ 完成 |
| D3 | 聚合与统计查询 | ✅ 完成 |
| D4 | 事务与 ACID | ✅ 完成 |
| D5 | 索引与 B 树 | ✅ 完成 |
| D6 | 二进制编码与记录格式 | 待开始 |
| D7 | 复盘与补漏 | 待开始 |
| D8 | WAL 与恢复机制 | 待开始 |
| D9 | Bitcask/LSM 树原理 | 待开始 |
| D10 | MiniKV 实现 | 待开始 |
| D11 | 压实与错误处理 | 待开始 |
| D12 | 分布式系统基础 | 待开始 |
| D13 | 2PC 与 Raft | 待开始 |
| D14 | 验收与交付 | 待开始 |

## 使用的工具

- **数据库**: SQLite（通过 Python sqlite3 模块）
- **笔记**: Obsidian
- **版本控制**: Git + GitHub

## 参考资料

- [Database Internals](https://www.databasinternals.com/) - Alex Petrov
- [Python sqlite3 文档](https://docs.python.org/3/library/sqlite3.html)
- [SQLite 官方文档](https://www.sqlite.org/docs.html)

## 许可证

MIT License
