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
├── daily/                  # 每日学习笔记
├── sql-exercises/          # SQL 练习题
├── templates/              # 笔记模板
├── src/                    # 源代码（D9 起）
│   └── minikv/             # MiniKV 存储引擎
├── tests/                  # 测试文件
├── docs/                   # 设计文档
└── index.md                # 主页（MOC）
```

## 学习进度

| 天数 | 主题 | 状态 |
|------|------|------|
| D1 | SQL 基础 | 进行中 |
| D2 | 关联查询与多表设计 | 待开始 |
| D3 | 聚合与统计查询 | 待开始 |
| D4 | 事务与 ACID | 待开始 |
| D5 | 索引与 B 树 | 待开始 |
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
