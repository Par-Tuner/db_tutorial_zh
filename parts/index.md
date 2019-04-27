# 概览

## 数据库是如何工作的？

- 数据是以什么格式存储的？（在内存与硬盘中）
- 数据在何时从内存被存入硬盘？
- 为什么每个表（table）中只能有一个主码（primary key）？
- 事务回滚（roll back a transaction）是如何工作的？
- 索引是怎样的格式？
- Full table scan 在何时怎样发生？
- 预编译指令(a prepared statement)是以什么格式存储的？

简单来说，数据库如何**工作**？

为了了解以上问题，我在用 C 语言从零开始写一份 [sqlite](https://www.sqlite.org/arch.html) 的克隆，并在工作中记录我的进度。

## 目录
Part 1 - 介绍，与建立交互式解释器（REPL）
Part 2 - 世界上最简单的 SQL 编译器与虚拟机
Part 3 - 一个只存在于内存中、只能添加的单表数据库
Part 4 - 我们的第一个测试（与 bug）
Part 5 - 存入硬盘
Part 6 - 光标抽象
Part 7 - 介绍 B 树
Part 8 - B 树叶结点的格式
Part 9 - 二分查找与重复的键
Part 10 - 分裂一个叶结点
Part 11 - 递归查找 B 树
Part 12 - 扫描一个多层级的 B 树
Part 13 - 分裂之后更新父节点

> “我不能创造的东西，我就不了解。” ——[理查德·菲利普·费曼](https://zh.wikiquote.org/wiki/費曼)

![sqlite architecture](https://www.sqlite.org/images/arch2.gif)