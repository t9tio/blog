---
title: wewe - Open group chat messages to the world
---

> wewe 现在还是一个想法, 第0版产品正在制作当中, 欢迎对这个项目感兴趣的朋友告诉 [timbot](https://raw.githubusercontent.com/timqian/images/master/3811553342733_.pic.jpg), 加入 wewe 的微信群讨论

repo:  https://github.com/t9tio/wewe

### Introducting wewe

上上周, 我在几个论坛分享了 [透明创业实验](https://blog.t9t.io/transparent-startup-experiment-2019-05-20/), 放出了 微信, spectrum, twitter, github 的链接. 用微信的人还是最多, 有近200人加了 timbot 为好友. 在群里了也出现了很多有意思的讨论. 很遗憾的是这些讨论停留在了微信里面, 自由加群的那些人可以看到, 新加入的还看不到旧消息, 对于一些重复的问题, 有时候需要回复多遍. 我就一直在想, 可不可以把这些消息公开出来, 让所有人可见, 这样感兴趣的人可以方便的查看聊天记录, 搜索感兴趣的内容. 如果我做这么一个工具, 对其他希望公开消息的群也是有意义的. 微信号称十亿日活, 有很多有价值的消息只存在于 500 人可见的群里, 确实是浪费了. 继续思考, 这个概念还可以衍生到其他即时聊天工具比如 slack, telegram 等. 人们在即时聊天工具里谈到的东西更多, 更杂, 因为到论坛发个帖显得比较麻烦, 一些小事去发帖子也显得小题大做. 但是在即使聊天群里, 有啥说啥, 没有压力. 这里有许多未经发掘的, 有价值的信息. 

说干就干, MVP 整起来!

### 提供的价值

- 在一个地方记录了群聊里的信息, 群外人也可以看到
- 聊天内容的查询
- 可以被搜索引擎搜到
- 聊天内容的分析
- 话题抽取,便于搜索
- 用户注册(分享微信)与群成员绑定

###
| Tool | group history | open on the web | search engine accessible | topic extraction | 
| --- | --- | --- | --- | --- |
| wechat | x | x | x | x |
|slack/tg | y | x | x | x |
| gitter | y | y | x | x|
