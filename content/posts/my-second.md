---
title: "Serverless最佳实践"
date: 2023-01-08T00:28:42+08:00
draft: false
---

## Serverless是什么
- CNCF对Serverless的定义：
> Serverless computing refers to a new model of cloud native computing, enabled by architectures that do not require server management to build and run applications. This landscape illustrates a finer-grained deployment model where applications, bundled as one or more functions, are uploaded to a platform and then executed, scaled, and billed in response to the exact demand needed at the moment
- 经典论文《Cloud Programming Simplified: A Berkeley View on Serverless Computing》对Serverless的定义：
> “在云的上下文中，Serverful 的计算就像使用低级的汇编语言编程，而 Serverless 的计算就像使用 Python 这样的高级语言进行编程。例如 c=a+b 这样简单的表达式，如果用汇编描述，就必须先选择几个寄存器，把值加载到寄存器，进行数学计算，再存储结果。这就好比今天在云环境下 Serverful 的计算，开发首先需要分配或找到可用的资源，然后加载代码和数据，再执行计算，将计算的结果存储起来，最后还需要管理资源的释放。Serverful 的计算是当前主流的使用云的方式，但不应该成为未来使用云的方式。Serverless 的愿景应该是代码关心业务逻辑，而由工具和语言去管理资源。

## 优势

- 不用关心服务器
- 自动弹性
- 按实际资源使用付费
- 更少的代码，更快的交付

## 劣势

## 实战
以腾讯云的SCF云函数为例，来做一个小demo