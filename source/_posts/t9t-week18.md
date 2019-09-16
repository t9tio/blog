---
title: 我的透明创业实验 - 第十八周
# description: 
date: 2019-09-16
---

Hello world, 我是 [timqian](https://github.com/timqian), 正在进行为期一年的[透明创业实验](https://blog.t9t.io/transparent-startup-experiment-2019-05-20/). 这是关于这个实验第十八周的实验记录.

## 做了啥

本周又开始了一个新项目 - 一个[自用的 Google Analytics](https://github.com/timqian/anahub), 暂时取名叫 [anahub](https://github.com/timqian/anahub) (analytics hub)

想要的功能
- 可 本地服务器部署 / serverless 方式部署
- 统计
  - 网站每日访问量(page view)
  - 流量来源(referral)
  - 浏览器类型统计
  - 国家统计
  - 最常访问页面
- 手绘风格图表
- 支持用户自己部署, 或者付费接入

同时逐渐意识到这个博客的一个的问题, 虽然做的产品都是面向世界上所有用户的, 博客却只是用中文写. 作为 “marketing asset” 其实不是很合适.

之后每个产品无论大小, 都至少中英各写一篇背后的故事

## 为什么想要做这么一个工具

相信每一个创作者都很关心自己做的东西大家是否受到别人的欢迎, 想知道每天有多少人使用了自己的产品/网站，他们是从哪里看到我的产品的，回头客多吗? 这个时候我们都会给自己接一个比如 Google analytics 之类的工具来统计这些信息. 作为一个做了超过10个大大小小网站的人，每个网站我都会接上 Google analytics, 但其实我只用了其中很少的功能, 关心它几百个指标里的4-5个. 它复杂的UI反而让我难以找到那几个我关心的数据. 当然，像所有类似的需求巨大的领域, 市面上不缺开源/简化版的 Google analytics，我将要实现的这个版本有它自己一些如上面提到的独特的地方. 希望这个产品可以获得小部分有这个需求的用户的喜欢

> 另, 早上多了一位来自 [tomato-pie](https://github.com/t9tio/tomato-pie) 的 [patron](https://patreon.com/timqian), 多了一份更新 [tomato-pie](https://github.com/t9tio/tomato-pie) 的动力

## 数据分享

> 产品详情可以访问 [t9t.io](https://t9t.io) 查看

### 平均每月被动收入($)(本周收入 / 7 * 30)
<svg id="incomeChart"></svg>

### 用户量
<svg id="userChart"></svg>

### github star 数
<svg id="starChart"></svg>

<br/>

> [帮助我改进这篇文章](https://github.com/t9tio/blog/blob/master/source/_posts/t9t-week18.md)

<script src="https://cdn.jsdelivr.net/npm/chart.xkcd@1.1.3/dist/chart.xkcd.min.js"></script>

<script>
var usersvg = document.getElementById('userChart');
var starsvg = document.getElementById('starChart');
var incomesvg = document.getElementById('incomeChart');

new chartXkcd.XY(usersvg, {
  xLabel: 'weeks',
  data: {
      datasets: [{
          label: 'wewe',
          data: [{x:3,y:0},{x:4,y:60},{x:5,y:80},{x:6,y:91},{x:7,y:95},{x:8,y:95},{x:9,y:103},{x:10,y:103},{x:11,y:103},{x:12,y:103},{x:13,y:103},{x:14,y:103},{x:15,y:103},{x:16,y:108},{x:16,y:108},{x:17,y:111}]
      },{
          label: 'open source jobs',
          data: [{x:0,y:39},{x:1,y:60},{x:2,y:62},{x:3,y:80},{x:4,y:101},{x:5,y:105},{x:6,y:109},{x:7,y:111},{x:8,y:113},{x:9,y:114},{x:10,y:119},{x:11,y:121},{x:12,y:122},{x:13,y:123},{x:14,y:123},{x:15,y:127},{x:16,y:131},{x:17,y:132}]
      },{
          label: 'tomato-pie',
          data: [{x:0,y:653},{x:1,y:673},{x:2,y:722},{x:3,y:634},{x:4,y:647},{x:5,y:705},{x:6,y:681},{x:7,y:714},{x:8,y:712},{x:9,y:733},{x:10,y:774},{x:11,y:779},{x:12,y:801},{x:13,y:821},{x:14,y:898},{x:15,y:911},{x:16,y:981},{x:17,y:917}]
      },{
          label: 'star-history',
          data: [{x:0,y:21},{x:1,y:21},{x:2,y:28},{x:3,y:33},{x:4,y:33},{x:5,y:34},{x:6,y:39},{x:7,y:38},{x:8,y:40},{x:9,y:47},{x:10,y:48},{x:11,y:50},{x:12,y:61},{x:13,y:58},{x:14,y:55},{x:15,y:57},{x:16,y:58},{x:17,y:58}]
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
        data: [{x:4,y:0},{x:5,y:11},{x:6,y:33},{x:7,y:57},{x:8,y:70},{x:9,y:77},{x:10,y:78},{x:11,y:102},{x:12,y:103},{x:13,y:108},{x:14,y:111},{x:15,y:114},{x:16,y:211},{x:17,y:242}]
    },{
        label: 'open source jobs',
        data: [{x:0,y:731},{x:1,y:764},{x:2,y:763},{x:3,y:821},{x:4,y:872},{x:5,y:891},{x:6,y:898},{x:7,y:903},{x:8,y:934},{x:9,y:940},{x:10,y:956},{x:11,y:962},{x:12,y:966},{x:13,y:967},{x:14,y:976},{x:15,y:980},{x:16,y:994},{x:17,y:1002}]
    },{
        label: 'tomato-pie',
        data: [{x:0,y:107},{x:1,y:113},{x:2,y:117},{x:3,y:118},{x:4,y:125},{x:5,y:126},{x:6,y:128},{x:7,y:129},{x:8,y:134},{x:9,y:134},{x:10,y:136},{x:11,y:136},{x:12,y:139},{x:13,y:139},{x:14,y:141},{x:15,y:148},{x:16,y:155},{x:17,y:156}]
    },{
        label: 'star-history',
        data: [{x:0,y:921},{x:1,y:998},{x:2,y:1110},{x:3,y:1129},{x:4,y:1154},{x:5,y:1178},{x:6,y:1190},{x:7,y:1216},{x:8,y:1238},{x:9,y:1246},{x:10,y:1276},{x:11,y:1291},{x:12,y:1299},{x:13,y:1308},{x:14,y:1328},{x:15,y:1343},{x:16,y:1361},{x:17,y:1367}]
    }, {
        label: 'chart.xkcd',
        data: [{x:12,y:3},{x:13,y:500},{x:14,y:3069},{x:15,y:3764},{x:16,y:4308},{x:17,y:4508}]
    }]
  },
  options: {
    showLine: true,
    dotSize: 0.5,
    xTickCount: 5,
  }
});

new chartXkcd.XY(incomesvg, {
  xLabel: 'weeks',
  data: {
    datasets: [{
        label: 'star-history',
        data: [{x:0,y:0.69},{x:1,y:0},{x:2,y:25.7},{x:3,y:12.8},{x:4,y:0},{x:5,y:8.571428571428571},{x:6,y:4.285714285714286},{x:7,y:4.285714285714286},{x:8,y:8.571428571428571},{x:9,y:8.571428571428571},{x:10,y:4.285714285714286},{x:11,y:17.142857142857142},{x:12,y:8.571428571428571},{x:13,y:3/7*30},{x:14,y:1/7*30},{x:15,y:3/7*30},{x:16,y:2/7*30},{x:17,y:0}]
    }, {
        label: 'patron',
        data: [{x:10,y:0},{x:11,y:1},{x:12,y:1},{x:13,y:2},{x:14,y:8},{x:15,y:8},{x:16,y:9},{x:17,y:10}]
    }]
  },
  options: {
    showLine: true,
    dotSize: 0.5,
    xTickCount: 5,
  },
});

</script>

