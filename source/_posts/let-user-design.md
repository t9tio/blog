---
title: 让用户决定软件长什么样
# description: 
date: 2020-06-18
---



[![](https://timqian-imgs.s3.ap-southeast-1.amazonaws.com/2020-06-Group%204.png)](https://feeds.pub/themes)

> 体验地址: [feeds.pub/themes](https://feeds.pub/themes)

虽然 [Feeds.Pub](https://feeds.pub) 自定义长相的功能已经做了有一会儿了, 但因为最近接了个外包有点忙, 一直没有抽出时间写一篇文章总结下. 今晚终于挤出了几个小时的整块的时间, 简单聊聊.

“自定义长相” 这个需求的起因是时不时有用户过来给我一些 UI 上的建议 -------- “这边字体大点会不会好点, 那边换个颜色怎么样?”

重口难调, 根据反馈改了一些地方和拒绝一些修改之后, 我在想: **要不索性让用户自己决定 APP 该长什么样?**

<!-- 重口难调, 我对自己的设计能力也不是那么自信. 所以经常在一些 UI 细节上花了很多时间纠结却只有很少的进展.

**"为什么不像代码编辑器一样, 让用户可以自己定义颜色和字体呢?"** 一个想法冒了出来.

## 这样做值得吗?

代码编辑器支持自定义样式, 一个重要原因是用户一般花很长时间面对编辑器, 一个使用频率和使用时间较长的应用, 如果用户对一些细节不满意, 支持自定义是一个不错的选项. RSS 阅读器也是一样, 虽然使用时长没有编辑器长, 但频率也是挺高的, 支持自定义是值得的. -->

## 自定义的自由度

自定义有不同的程度, 最低的程度是提供几个设计好的选项给用户, 比如现在很多网站在做的 "dark mode" 就是一个最好的例子.

如果把自由度提得更高一些, 我们可以支持用户选择界面各部分的颜色, 字体, 甚至是布局. 这种细粒度的自由度在代码编辑器里比较常见. 程序员长时间面对一个编辑器, 通常希望界面能最好得满足自己的要求, 所以主流的编辑器一般都会支持自定义配色和字体.

虽然没有编辑器使用频率和时长高, 但对于把 RSS 作为主要信息来源的用户来说, 每天打开两三次 [Feeds.Pub](https://feeds.pub) 也是比较正常的. 对于这种高频应用, 我决定借鉴下编辑器的方式, 给用户提供尽可能高的自由度.

## 那么我应该提供什么样的配置项给用户呢?

这是一个关于平衡的工作: 我希望用尽可能少的配置项, 给予用户尽可能多的灵活性.

> 自定义的配置项应该像物理定律一样, 尽可能简单, 但不是更简单
> -------- Albert Einstein & Tim Qian

现实不像名言, 说说容易做起来难, 断断续续可能做了有一个多月了, 我把 [Feeds.Pub](https://feeds.pub) 的配置项抽象如下:

| 界面的部分 | 支持的配置项 |
| --- | --- |
| Header  (顶部的导航栏) | 背景和文字的颜色 |
| Body (除了 Header) | 背景色, 主要文字颜色, 次要文字颜色, 已访问过的链接的颜色 |
| Side Bar (左侧 feeds 导航栏) | 文字默认颜色, 文字被选中、鼠标悬停时的颜色和背景   |
| Separator (分割线) | 分割线的颜色 (比如分割左右区域, 用户页面的分割等) |
| Button (按钮) | 按钮的边框, 背景, 文字等颜色 |
| Input (输入框) | 输入框的边框, 文字的颜色 |
| Tag | tag 的文字, 背景色等 |
| Dropdown (下拉菜单) | 下拉菜单的背景, 文字等颜色 |

**体验地址: [feeds.pub/themes](https://feeds.pub/themes)**

## 这样做的收获

1. 界面更有逻辑性了, 原来不同地方的按钮, 字号, 颜色等有了一定的规则, 看起来更规整, 也方便我同时调整各个地方的样式.
2. 通过给用户更大的自由度, 有可能发现更好的设计, 加入 feeds.pub

最后, 如果你对 DIY 界面感兴趣, 欢迎在 [telegram 群](https://t.me/feedspub_chat) 或者 [twitter](https://twitter.com/tim_qian) 上分享你的设计❤️
