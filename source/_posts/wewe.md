---
title: wewe - Open group chat to the world (中文)
description: About wewe
date: 2019-07-04
---

[![wewe](https://raw.githubusercontent.com/timqian/images/master/20190704122816.png)](https://wewe.t9t.io)

[wewe](https://wewe.t9t.io) 是一个用来记录和公开群聊消息到互联网的开源项目
- url: https://wewe.t9t.io
- github: https://github.com/t9tio/wewe

## wewe 提供的价值

- 在一个地方记录了群聊里的信息, 群外人也可以看到
- 可以被搜索引擎搜到
- 话题抽取,便于浏览和搜索
- 聊天内容的分析(unfinished)
- 支持各种群聊工具(目前支持微信群和 slack 群, 并且计划支持 telegram/gitter 等主流群聊工具)

## 我为什么做这个工具

几周前, 我在几个论坛分享了 [透明创业实验](https://blog.t9t.io/transparent-startup-experiment-2019-05-20/), 并且建了一个微信群方便交流. 

没想到有超过 500 人加入, 在群里了也出现了很多有意思的讨论. 很遗憾的是这些讨论停留在了微信里面, 只有加群的那些人可以看到, 新加入的还看不到旧消息, 对于一些重复的问题, 有时候需要回复多遍. 我就一直在想, 可不可以把这些消息公开出来, 让所有人可见, 这样感兴趣的人可以方便的查看聊天记录, 搜索感兴趣的内容. 如果我做这么一个工具, 对其他希望公开消息的群也是有意义的. 人们在即时聊天工具里谈到的东西更多, 更杂, 因为到论坛发个帖显得比较麻烦, 一些小事去发帖子也显得小题大做. 但是在群里, 有啥说啥, 没有压力. 这里有许多未经发掘的, 有价值的信息. 

说干就干, MVP 整起来!

## 如何加入

最新说明: https://wewe.t9t.io/join

如果你也想将开放你的群聊, 欢迎接入 wewe

要求
1. 告知全体群成员群消息将公开在互联网上
2. 如果是微信群, 需要指定一名愿意收集话题的志愿者(slack 不需要, 自带 threads 功能)

加入方式
- 微信: 加 [timbot](https://raw.githubusercontent.com/timqian/images/master/3811553342733_.pic.jpg) 为好友, 备注 "join wewe", 然后将机器人拉入群聊即可, 如果内容适合公开, 我就会开始收集
- slack: 加入[t9t.io slack 群](https://join.slack.com/t/t9tio/shared_invite/enQtNjgzMzkwMDM0NTE3LTE5ZTUzYjU4Y2I0YzRiZjNkYTkzMzE1ZmM0NDdmYzRlZmMxNGY1MzZlN2EwYjYyNWVlMWY0Nzk2MDBhNWZlY2I)

## wewe 的原理

wewe 是一个基于 GPLv2 license 开源的项目, 具体实现细节可以参考 github 仓库里的代码: https://github.com/t9tio/wewe

### 微信

基于 [wechaty](https://github.com/Chatie/wechaty), 基本原理是启动一个浏览器, 登录网页微信后, 将收到的消息存入数据库

### slack

基于 [slack API](https://api.slack.com/methods), 基本原理是调用 slack API 获取群内消息, 存入数据库


## FAQ
- **隐私问题**: 最大限度保障群友隐私, 所以消息称默认是匿名的. 但是对于愿意公开身份的群友, 也支持公开昵称, 对自己简单介绍, 放上自己的链接等. e.g. t9t 群里的成员 https://wewe.t9t.io/chat/t9t.io%20community/members
- **如何收费**: wewe 仍在开发阶段, 并且因为网站使用 serverless 方式开发(aws lambda & dynamodb & s3), 维护和服务器成本比较低, 对前 30 个加入的群免费提供服务, 之后的收费模式仍在思考当中