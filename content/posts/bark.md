---
title: "Bark"
date: 2023-01-08T22:24:24+08:00
draft: false
---

## 带有标题的消息
通过在 URL 路径上增加一个 title 来实现，形如：
/:key/:title/:body 

## 自动复制推送内容
自动复制功能适用于验证码推送的场景，参数如下：
automaticallyCopy：自动复制的开关，默认关闭。1：开启，其它值：关闭。
copy：指定自动复制的内容，不指定则复制所有 body 的内容。
比如发送以下请求会自动复制 9527，无需手动复制：
https://api.day.app/yourkey/验证码是9527?automaticallyCopy=1&copy=9527 

## URL跳转
通过指定参数 url，点击推送将跳转到相应的网址，比如：
发送时，URL参数需要编码
https://api.day.app/yourkey/百度网址?url=https://www.baidu.com 

## 保存历史记录
一些推送，我们可以阅后即焚，另一些则可以选择保存。保存与否通过 isArchive 来控制：
isArchive：1：保存，其他值：不保存。
要说明的是，如果不指定参数，是否保存则取决于 App 内的设置。相较于 App，参数具有更高的优先级，所以对于确认需要保存记录的消息，可以这样发送请求：
https://api.day.app/yourkey/需要保存的推送?isArchive=1 