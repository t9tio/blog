---
title: keep on shipping, 你可能会发现用户可能喜欢什么 - 我的透明创业实验第二十二周
# description: 
date: 2019-10-14
---

Hello world, 我是 [timqian](https://github.com/timqian), 正在进行为期一年的[透明创业实验](https://blog.t9t.io/transparent-startup-experiment-2019-05-20/). 这是关于这个实验第二十二周的实验记录. 

## 做一个通用的 Analytics 工具?

在第 18 和 19 周, 我的大部分时间都投入在了 18 周开始的一个项目 - [AnaHub](https://github.com/timqian/anahub) (一个无服务,可自行部署的 Google Analytics 替代品). 但是遇到了麻烦:

纯做一个自部署的 analytics 工具比较简单, 但是要同时兼顾下面几个需求不那么容易

- 允许用户自行部署
- 允许用户用我部署的 anahub
- 付费限制 (不同流量的网站不同的价格)
- 开源

兼容这四个需求的产品, 从设计和实现上来讲都比较难以在短时间做出来. 但是纯做一个可自行部署的 analytics 工具, 收入渠道就只能是捐助了. 又是一个用爱发电的纯粹开源项目. 对于目前没多少收入, 渴求温饱的我, 急需用户可能有付费意愿的产品. 所以一直在犹豫该怎么办...

### 另一个与 Analytics 相关的小需求

我经常看自己 github 项目的 traffic. 你可能已经知道, github 支持用户看到项目的访问数据 (包括 clone / visits / referral / top pages 等). 我常通过浏览这些数据判断我在某些论坛上分享自己的项目之后效果如何. 不过官方 traffic 有一个缺点, 只能看到最近 14 天的数据. 要是有完整的 traffic 记录就好了.

#### 这个问题有其他人碰到吗?

在 Google 搜索了 "github traffic more than 14 days", 可以发现至少有几百人有这个需求的

- https://github.com/isaacs/github/issues/399
- https://webapps.stackexchange.com/questions/60915/track-traffic-to-github-repo-longer-than-14-days

在做一个通用的 analytics 工具之前, 我先做 github 项目的 analytics 怎么样呢?

做开源项目的人, 必定关心自己项目的 traffic / clone / star / fork 等 analytics 数据. 我手上少数几个给我带来微薄收入的产品之一的 [star-history](https://github.com/timqian/star-history) 其实就是帮助用户了解项目 analytics 数据的一个小小部分. 如果有一个对项目 analytics 做更完善和多方位分析的工具. 至少对我来说是需要的.

从收费模式角度讲. 这种需要长期保存数据的产品, 周期性收费是合理的, 有可能为我带来每个月比较稳定的一些收入.

于是, 我暂时放下写了一半的 anahub, 动手开始先解决这个问题.

经过三周的工作, [Repo Analytics](https://repo-analytics.github.io) 的骨架终于搭好了, 并且大致完成了第一个功能: 保存 github repo 的 traffic 记录. 欢迎试用

<a href="https://repo-analytics.github.io">
  <img src="https://raw.githubusercontent.com/timqian/images/master/20191002233726.png" style="display: block; margin-left: auto; margin-right: auto;width: 30%;">
</a>

## 失败的公众号的尝试

忘了什么动机开了一个公众号, 想要记录下每天所见所思. 还立下了日更的 flag. 更了三天之后发现这活不轻松. 写出有价值的内容, 还是每天更新, 需要的精力太过巨大, 影响了我做产品的节奏. 而且我还有一周一篇的周报要写😂

那么这个公众号可以用来干啥呢? 我决定把它作为订阅本博客除了 RSS 之外的另一个渠道

<img src="https://raw.githubusercontent.com/timqian/images/master/20190926202015.jpg" style="display: block; margin-left: auto; margin-right: auto;width: 30%;">

当 t9t.io 有博文更新, 我会在公众号里发一条消息过去.

## 数据分享

> 产品详情可以访问 [t9t.io](https://t9t.io) 查看

### 平均每月被动收入($)(本周收入 / 7 * 30)

<svg id="incomeChart"></svg>

### 用户量
<svg id="userChart"></svg>

### github star 数
<svg id="starChart"></svg>

<br/>

> [帮助我改进这篇文章](https://github.com/t9tio/blog/blob/master/source/_posts/t9t-week22.md)

<script src="https://cdn.jsdelivr.net/npm/chart.xkcd@1.1.3/dist/chart.xkcd.min.js"></script>

<script>
var incomesvg = document.getElementById('incomeChart');
var usersvg = document.getElementById('userChart');
var starsvg = document.getElementById('starChart');


new chartXkcd.XY(incomesvg, {
  xLabel: 'weeks',
  data: {
    datasets: [{
        label: 'star-history',
        data: [{x:0,y:0.69},{x:1,y:0},{x:2,y:25.7},{x:3,y:12.8},{x:4,y:0},{x:5,y:8.571428571428571},{x:6,y:4.285714285714286},{x:7,y:4.285714285714286},{x:8,y:8.571428571428571},{x:9,y:8.571428571428571},{x:10,y:4.285714285714286},{x:11,y:17.142857142857142},{x:12,y:8.571428571428571},{x:13,y:3/7*30},{x:14,y:1/7*30},{x:15,y:3/7*30},{x:16,y:2/7*30},{x:17,y:0},{x:18,y:3/7*30},{x:21,y:1/7*30}]
    }, {
        label: 'patron',
        data: [{x:10,y:0},{x:11,y:1},{x:12,y:1},{x:13,y:2},{x:14,y:8},{x:15,y:8},{x:16,y:9},{x:17,y:10},{x:18,y:10},{x:21,y:9}]
    }]
  },
  options: {
    showLine: true,
    dotSize: 0.5,
    xTickCount: 5,
  },
});

new chartXkcd.XY(usersvg, {
  xLabel: 'weeks',
  data: {
      datasets: [{
          label: 'wewe',
          data: [{x:3,y:0},{x:4,y:60},{x:5,y:80},{x:6,y:91},{x:7,y:95},{x:8,y:95},{x:9,y:103},{x:10,y:103},{x:11,y:103},{x:12,y:103},{x:13,y:103},{x:14,y:103},{x:15,y:103},{x:16,y:108},{x:16,y:108},{x:17,y:111},{x:18,y:111},{x:21,y:127}]
      },{
          label: 'open source jobs',
          data: [{x:0,y:39},{x:1,y:60},{x:2,y:62},{x:3,y:80},{x:4,y:101},{x:5,y:105},{x:6,y:109},{x:7,y:111},{x:8,y:113},{x:9,y:114},{x:10,y:119},{x:11,y:121},{x:12,y:122},{x:13,y:123},{x:14,y:123},{x:15,y:127},{x:16,y:131},{x:17,y:132},{x:18,y:133},{x:21,y:139}]
      },{
          label: 'tomato-pie',
          data: [{x:0,y:653},{x:1,y:673},{x:2,y:722},{x:3,y:634},{x:4,y:647},{x:5,y:705},{x:6,y:681},{x:7,y:714},{x:8,y:712},{x:9,y:733},{x:10,y:774},{x:11,y:779},{x:12,y:801},{x:13,y:821},{x:14,y:898},{x:15,y:911},{x:16,y:981},{x:17,y:917},{x:18,y:920},{x:21,y:875}]
      },{
          label: 'star-history',
          data: [{x:0,y:21},{x:1,y:21},{x:2,y:28},{x:3,y:33},{x:4,y:33},{x:5,y:34},{x:6,y:39},{x:7,y:38},{x:8,y:40},{x:9,y:47},{x:10,y:48},{x:11,y:50},{x:12,y:61},{x:13,y:58},{x:14,y:55},{x:15,y:57},{x:16,y:58},{x:17,y:58},{x:18,y:63},{x:21,y:73}]
      }]
  },
  options: {
    showLine: true,
    dotSize: 0.5,
    xTickCount: 5,
  }
});

new chartXkcd.XY(starsvg, {
  xLabel: 'weeks',
  data: {
    datasets: [{
        label: 'wewe',
        data: [{x:4,y:0},{x:5,y:11},{x:6,y:33},{x:7,y:57},{x:8,y:70},{x:9,y:77},{x:10,y:78},{x:11,y:102},{x:12,y:103},{x:13,y:108},{x:14,y:111},{x:15,y:114},{x:16,y:211},{x:17,y:242},{x:18,y:250},{x:21,y:269}]
    },{
        label: 'open source jobs',
        data: [{x:0,y:731},{x:1,y:764},{x:2,y:763},{x:3,y:821},{x:4,y:872},{x:5,y:891},{x:6,y:898},{x:7,y:903},{x:8,y:934},{x:9,y:940},{x:10,y:956},{x:11,y:962},{x:12,y:966},{x:13,y:967},{x:14,y:976},{x:15,y:980},{x:16,y:994},{x:17,y:1002},{x:18,y:1005},{x:21,y:1020}]
    },{
        label: 'tomato-pie',
        data: [{x:0,y:107},{x:1,y:113},{x:2,y:117},{x:3,y:118},{x:4,y:125},{x:5,y:126},{x:6,y:128},{x:7,y:129},{x:8,y:134},{x:9,y:134},{x:10,y:136},{x:11,y:136},{x:12,y:139},{x:13,y:139},{x:14,y:141},{x:15,y:148},{x:16,y:155},{x:17,y:156},{x:18,y:158},{x:21,y:164}]
    },{
        label: 'star-history',
        data: [{x:0,y:921},{x:1,y:998},{x:2,y:1110},{x:3,y:1129},{x:4,y:1154},{x:5,y:1178},{x:6,y:1190},{x:7,y:1216},{x:8,y:1238},{x:9,y:1246},{x:10,y:1276},{x:11,y:1291},{x:12,y:1299},{x:13,y:1308},{x:14,y:1328},{x:15,y:1343},{x:16,y:1361},{x:17,y:1367},{x:18,y:1382},{x:21,y:1422}]
    }, {
        label: 'chart.xkcd',
        data: [{x:12,y:3},{x:13,y:500},{x:14,y:3069},{x:15,y:3764},{x:16,y:4308},{x:17,y:4508},{x:18,y:4651},{x:21,y:5166}]
    }]
  },
  options: {
    showLine: true,
    dotSize: 0.5,
    xTickCount: 5,
  }
});


</script>

