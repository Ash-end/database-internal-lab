---
tags: [database, skill, methodology]
aliases: [数据库学习方法论, Database Learning Skill]
---

# Database Internals 学习技能

> [!quote] 核心理念
> **费曼技巧**：教别人是最好的学习方式。
> **结构化笔记**：从原始素材到知识图谱，层层递进。
> **AI 辅助**：用 Claude 驱动自适应学习闭环。

---

## 一、方法论来源

| 体系 | 核心方法 | 本项目应用 |
|------|----------|------------|
| **力扣百题通** | 14 天速成 + AI 教练 + 知识图谱 | 14 天学习计划 + Obsidian 互链 |
| **Akshat-Jain** | 章节笔记 + 侧栏学习 + 费曼技巧 | 每章笔记 + 未解问题 + 讨论记录 |
| **labuladong** | 框架思维 + 模板套题型 | 核心概念模板化 |
| **代码随想录** | 五步拆解法 | 知识点结构化分析 |

---

## 二、笔记结构（四层模型）

```
database-internal-lab/
├── 00-学习技能/           # 方法论与配置
│   ├── database-learning-skill.md  ← 你在这里
│   ├── 学员档案.md
│   └── 进度看板.md
│
├── 01-Raw/                # 原始素材（只增不改）
│   ├── 教材核心概念.md
│   └── 参考资料汇总.md
│
├── 02-Wiki/               # 核心知识区（结构化）
│   ├── 专题总结/
│   │   ├── SQL基础.md
│   │   ├── 存储引擎.md
│   │   ├── B树与索引.md
│   │   ├── 事务与恢复.md
│   │   ├── LSM树.md
│   │   └── 分布式系统.md
│   └── 章节笔记/
│       ├── Chapter01-架构概览.md
│       ├── Chapter02-B树基础.md
│       └── ...
│
├── 03-学习笔记/           # 每日学习记录
│   ├── 2026-09-16.md
│   ├── 2026-09-17.md
│   └── ...
│
├── 04-SQL练习/            # SQL 练习题与答案
│
├── 05-Projects/           # MiniKV 项目代码
│
└── 06-Outputs/            # 输出区（知识图谱、总结）
```

---

## 三、每日学习流程

### 3.1 学习前准备

```markdown
1. 打开 进度看板.md，确认今日任务
2. 打开 学员档案.md，回顾学习目标
3. 创建当日笔记：daily/YYYY-MM-DD.md
```

### 3.2 学习中（四步法）

| 步骤 | 动作 | 产出 |
|------|------|------|
| **读** | 阅读教材/文档，标记重点 | 原始笔记 |
| **记** | 用自己的话重写，添加标签 | 结构化笔记 |
| **练** | 做练习题，写代码验证 | 代码 + 测试 |
| **教** | 向 AI 或他人解释概念 | 费曼笔记 |

### 3.3 学习后

```markdown
1. 更新当日笔记
2. 更新 进度看板.md
3. Git commit + push
```

---

## 四、笔记模板

### 4.1 章节笔记模板

```markdown
---
chapter: X
book: Database Internals
tags: [database, chapter-XX]
---

# Chapter X: 章节标题

## 核心问题
> 这章解决什么问题？

## 关键概念

### 概念1: XXX
- **是什么**：
- **为什么需要**：
- **代价/权衡**：
- **验证方式**：

### 概念2: XXX


## 🤯 最有趣的发现


## ✨ 侧栏学习（书外补充）


## ❓ 未解问题


## 🔗 关联章节


```

### 4.2 每日笔记模板

```markdown
---
date: YYYY-MM-DD
tags: [database, day-XX]
---

# YYYY-MM-DD DXX：今日主题

## 今日目标


## 学习内容

### 上午


### 下午


## 核心收获


## 错误记录


## 明日计划

```

### 4.3 专题总结模板

```markdown
---
topic: XXX
tags: [database, topic-XXX]
---

# XXX 专题总结

## 一句话定义


## 核心机制


## 应用场景

| 场景 | 方案 | 代价 |
|------|------|------|
| | | |

## 代码模板

```python
# 模板代码
```

## 关联知识

- [[B树]]
- [[LSM树]]

## 常见问题

1. Q: 
   A: 

```

---

## 五、Obsidian 技巧

### 5.1 标签系统

| 标签 | 用途 |
|------|------|
| `#database` | 所有数据库笔记 |
| `#day-XX` | 第几天的学习 |
| `#topic-XXX` | 专题分类 |
| `#chapter-XX` | 教材章节 |
| `#sql` | SQL 相关 |
| `#minikv` | MiniKV 项目 |

### 5.2 Wikilink 互链

```markdown
- 详见 [[B树基础]]
- 参考 [[Chapter02-B树基础#核心机制]]
- 关联 [[LSM树]] 的 [[LSM树#压缩策略]]
```

### 5.3 Callout 语法

```markdown
> [!note] 笔记
> 普通笔记

> [!tip] 提示
> 有用技巧

> [!warning] 警告
> 容易出错的地方

> [!question] 问题
> 未解问题

> [!example] 示例
> 具体例子
```

---

## 六、Git 工作流

```bash
# 每日学习后
git add .
git commit -m "study: DXX 完成 XXX"
git push

# 专题总结后
git commit -m "docs: 添加 XXX 专题总结"

# 项目里程碑
git commit -m "feat: MiniKV 实现 XXX 功能"
```

---

## 七、验收标准

| 阶段 | 标准 |
|------|------|
| SQL 基础 | 20 道题独立完成 ≥16 道 |
| 存储引擎 | 能解释 B树/LSM/Bitcask 区别 |
| MiniKV | 通过 12 项必做测试 |
| 分布式 | 能推演 Raft 选举流程 |

---

## 参考资料

- [力扣百题通](https://github.com/mo-lx/LeetCode-BaiTiTong) - 学习方法论
- [database-internals-notes](https://github.com/Akshat-Jain/database-internals-notes) - 章节笔记范例
- [Database Internals](https://www.databasinternals.com/) - 教材

