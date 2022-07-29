---
title: 为了老婆的乐队梦, 我做了一个弹钢琴的机器人
# description:
date: 2022-07-29
---

![](https://i.v2ex.co/3SAa692h.jpeg)

事情是这样的：老婆很喜欢唱歌，一直喊我学一个乐器然后和她组乐队。于是我尝试学习了钢琴，吉他，尤克里里… 但是因为资质平平没有节奏感，一直也配不上。

正在老婆马上要放弃我的时候，前段时间无意中刷到一些视频，似乎弹钢琴，弹吉他这活儿可以安排给机器人干。作为一个略懂电子的程序员，这些机器人我也许也能做的出来，成立乐队的希望又出现了。

经过将近一个月的调研，学习，设计，和制作，虽然简陋一些，节奏稍微不准一些，我终于把机器做出来了，先看结果：

<iframe 
  style="width: 640px; height: 430px; max-width: 100%"
  src="https://player.bilibili.com/player.html?aid=428990101&bvid=BV1nG411h7pE&cid=787586760&page=1" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true"> 
</iframe>

<hr/>

> 欢迎大家关注[我的 B 站账号](https://space.bilibili.com/11206127)，**莫得灵魂乐队**后面有可能发新歌/加入新的乐手。


## 记录一下制作过程

## 1. 调研

在b站，youtube，搜索别人做过类似的机器。 发现主要有两种方式。

### 1.1 乐高的方案

乐高除了常规的积木，还卖可编程机器的机器（[SPIKE](https://legoeducation.cn/zh-cn/products/lego-education-spike-prime-/45678#spike-prime%E7%A7%91%E5%88%9B%E5%A5%97%E8%A3%85)，[EV3](https://zh.wikipedia.org/zh-sg/%E6%A8%82%E9%AB%98Mindstorms_EV3)等）这些机器可以连接接传感器，马达以及乐高积木，由此组装出可编程的乐高机器人。

参考 youtube 上[这位博主的视频](https://www.youtube.com/watch?v=cXgB3lIvPHI)，我最终做出了这么一个弹吉他的机器人：

<iframe 
  style="width: 640px; height: 430px; max-width: 100%"
  src="https://player.bilibili.com/player.html?aid=686382957&bvid=BV1AU4y1v7Cz&cid=786446104&page=1" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true"> 
</iframe>

---

不过用乐高做机器有两个问题

1. 第一是不够灵活，因为积木搭建，只有那么一些形状，导致需要不断尝试各种部件组合来达到某些简单的运动。这就导致了要制作更精巧的机器的时候，难度指数型上升。
2. 然后是贵，spike 需要 ¥1000 多一个，一个 spike 只能控制 4 个马达，如果做钢琴机器人，需要好几个 spike 联动，编码也会很复杂。

考虑再三，我放弃了优化这款乐高机器人，转向了另一种方式

### 1.2 单片机 + 舵机 + 亚克力或者板材做结构

乐高 spike 本质上是一个单片机，配套的马达本质是舵机。所以我尝试了自己购买单片机和舵机，然后用亚克力板自己切割出想要的结构组装成想要的样子。

事实证明，这样子做起来方便多了，只花了一周时间，做出了更好的效果。

单片机可选择的范围比较多，主要考察了 [Arduino](https://www.arduino.cc/) 和[树莓派](https://www.raspberrypi.com/)。

最终选择了 arduino，因为它够用，便宜，编程起来方便。

动手前，我希望用 3D 软件先设计结构，通过一番搜索，还找到了一个非常好用的，开源的 3D 设计软件

[Blender](https://github.com/blender/blender)

进行了简单的入门之后，我决定，下次设计更复杂的机械的时候再用它。。原因是这次结构比较简单，而且因为没有太多机械制作经验，设计出来也不知道能不能在现实中实现。

## 2. 原料采购

- 亚克力板两块
- 热熔胶枪一支
- 舵机50个
- Arduino 一块
- 美工刀一只

## 3. 制作过程

1. 用美工刀切割亚克力板得到指定形状
2. 用热熔胶枪把舵机安装在亚克力板上
3. 用热熔胶枪把亚克力板粘起来

## 5. 软件编写

Arduino 配套的编程语言很像 C++，并且提供了很多库方便用户操作，比如控制舵机，只需要使用

## 6. 大功告成

测试一下，弹个两只老虎

<iframe 
  style="width: 640px; height: 430px; max-width: 100%"
  src="https://player.bilibili.com/player.html?aid=428963168&bvid=BV1VG411h7BH&cid=787590517&page=1" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true"> 
</iframe>

<hr/>
照例把相关代码放在了 [GitHub](https://github.com/timqian/modsoul)


