---
title: "GraphQL入门教程"
date: 2023-01-08T22:22:48+08:00
draft: true
---

## 入门教程

[传送门](https://www.graphql-java.com/tutorials/getting-started-with-spring-boot/)

## 个人理解

不由得让我想起了SQL（structured query language），结尾都是QL，是一种查询语言。实际使用来说的话，也有几点相似之处：
- 都有schema和数据类型的概念。
- 都是按需查询，客户端需要什么就查询什么，但不能超出schema的范围。

不同：
- SQL用于关系型数据库，GraphQL和关系型数据库没关系，是用解析器和数据源建立连接。

## 实战

有多种语言的实现，这里就以Java语言为例，来说一下如何实现GraphQL的hello world。



## 实现原理


## 最佳实践

- 安全性

接口鉴权在业务逻辑实现还是在GraphQL实现？

- 客户端有哪些

GraphQL是一种标准规范，有各种[不同语言的实现](https://graphql.cn/code/)，包括服务器端和客户端。