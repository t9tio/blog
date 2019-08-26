---
title: 享受被需求推着走的感觉 - 我的透明创业实验第十五周
description: Build something should exist
date: 2019-08-26
---

Hello world, 我是 [timqian](https://github.com/timqian), 正在进行为期一年的[透明创业实验](https://blog.t9t.io/transparent-startup-experiment-2019-05-20/). 这是关于这个实验第十五周的实验记录.

## 状态的改变

之前的状态主要是做自己想做的东西. 上周一发布的新产品 [chart.xkcd](https://github.com/timqian/chart.xkcd) 反响不错, 得到了挺多人的关注和喜爱(保守估计有多于5万人看到了这个产品, 其中3000多人在 github上点赞收藏). 最近的状态是, 因为发布的MVP做的很糙, 人们会出来提很多改进的建议. 是一个被需求推着走的状态

这些建议是很宝贵的, 分为三种

1. 自己原来就觉得要做, 只是因为作为 MVP, 认为这个功能/bug 不重要所以暂时没做
2. ✨给你一些原来都没有想到, 让产品更好的建议
3. ✨有些自己原来很纠结的点, 发现压根就没人来提建议, 那么其实是为你节省了时间, 可以去做那些人们更关心的功能

可以被需求推着走, 是幸福的烦恼

## 本周目标

这一周还是继续专注于chart.xkcd

- 尽可能把代码变得更易于阅读和贡献
- 在博客, star-history; tomato-pie 等产品中开始用上这个图表库, 在使用中找到更多bug和进步的方向
  - 例如在这篇博客里用到 chart.xkcd 之后发现的问题: 
    - legend 太多时, 在手机端占据图表空间过大, 需要一个选项, 把 legend 挪到图表之外
    - 小数点后面位数太多, 需要一个选项让用户可以控制

## 数据分享

> 产品详情可以访问 [t9t.io](https://t9t.io) 查看

### 平均每月被动收入($)(本周收入 / 7 * 30)
<svg id="incomeChart"></svg>

### 用户量
<svg id="userChart"></svg>

### github star 数
<svg id="starChart"></svg>

<br/>

> [帮助我改进这篇文章](https://github.com/t9tio/blog/blob/master/source/_posts/t9t-week15.md)

<script src="https://cdn.jsdelivr.net/npm/chart.xkcd@1.0.7/dist/chart.xkcd.min.js"></script>

<script>
var usersvg = document.getElementById('userChart');
var starsvg = document.getElementById('starChart');
var incomesvg = document.getElementById('incomeChart');

new chartXkcd.XY(usersvg, {
  xLabel: 'weeks',
  data: {
      datasets: [{
          label: 'wewe',
          data: [{x:0, y:0}, {x:1, y:0}, {x:2, y:0}, {x:3, y:0}, {x:4,y:60},{x:5,y:80},{x:6,y:91},{x:7,y:95},{x:8,y:95},{x:9,y:103},{x:10,y:103},{x:11,y:103},{x:12,y:103},{x:13,y:103},{x:14,y:103}]
      },{
          label: 'open source jobs',
          data: [{x:0,y:39},{x:1,y:60},{x:2,y:62},{x:3,y:80},{x:4,y:101},{x:5,y:105},{x:6,y:109},{x:7,y:111},{x:8,y:113},{x:9,y:114},{x:10,y:119},{x:11,y:121},{x:12,y:122},{x:13,y:123},{x:14,y:123},]
      },{
          label: 'tomato-pie',
          data: [{x:0,y:653},{x:1,y:673},{x:2,y:722},{x:3,y:634},{x:4,y:647},{x:5,y:705},{x:6,y:681},{x:7,y:714},{x:8,y:712},{x:9,y:733},{x:10,y:774},{x:11,y:779},{x:12,y:801},{x:13,y:821},{x:14,y:898}]
      },{
          label: 'star-history',
          data: [{x:0,y:21},{x:1,y:21},{x:2,y:28},{x:3,y:33},{x:4,y:33},{x:5,y:34},{x:6,y:39},{x:7,y:38},{x:8,y:40},{x:9,y:47},{x:10,y:48},{x:11,y:50},{x:12,y:61},{x:13,y:58},{x:14,y:55}]
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
        data: [{x:0,y:0},{x:1,y:0},{x:2,y:0},{x:3,y:0},{x:4,y:0},{x:5,y:11},{x:6,y:33},{x:7,y:57},{x:8,y:70},{x:9,y:77},{x:10,y:78},{x:11,y:102},{x:12,y:103},{x:13,y:108},{x:14,y:111}]
    },{
        label: 'open source jobs',
        data: [{x:0,y:731},{x:1,y:764},{x:2,y:763},{x:3,y:821},{x:4,y:872},{x:5,y:891},{x:6,y:898},{x:7,y:903},{x:8,y:934},{x:9,y:940},{x:10,y:956},{x:11,y:962},{x:12,y:966},{x:13,y:967},{x:14,y:976}]
    },{
        label: 'tomato-pie',
        data: [{x:0,y:107},{x:1,y:113},{x:2,y:117},{x:3,y:118},{x:4,y:125},{x:5,y:126},{x:6,y:128},{x:7,y:129},{x:8,y:134},{x:9,y:134},{x:10,y:136},{x:11,y:136},{x:12,y:139},{x:13,y:139},{x:14,y:141}]
    },{
        label: 'star-history',
        data: [{x:0,y:921},{x:1,y:998},{x:2,y:1110},{x:3,y:1129},{x:4,y:1154},{x:5,y:1178},{x:6,y:1190},{x:7,y:1216},{x:8,y:1238},{x:9,y:1246},{x:10,y:1276},{x:11,y:1291},{x:12,y:1299},{x:13,y:1308},{x:14,y:1328}]
    }, {
        label: 'chart.xkcd',
        data: [{x:0,y:0},{x:1,y:0},{x:2,y:0},{x:3,y:0},{x:4,y:0},{x:5,y:0},{x:6,y:0},{x:7,y:0},{x:8,y:0},{x:9,y:0},{x:10,y:0},{x:11,y:0},{x:12,y:3},{x:13,y:500},{x:14,y:3069}]
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
        label: 'star-history 插件',
        data: [{x:0,y:0.69},{x:1,y:0},{x:2,y:25.7},{x:3,y:12.8},{x:4,y:0},{x:5,y:8.571428571428571},{x:6,y:4.285714285714286},{x:7,y:4.285714285714286},{x:8,y:8.571428571428571},{x:9,y:8.571428571428571},{x:10,y:4.285714285714286},{x:11,y:17.142857142857142},{x:12,y:8.571428571428571},{x:13,y:3/7*30},{x:14,y:1/7*30}]
    }, {
        label: 'patron',
        data: [{x:0,y:0},{x:1,y:0},{x:2,y:0},{x:3,y:0},{x:4,y:0},{x:5,y:0},{x:6,y:0},{x:7,y:0},{x:8,y:0},{x:9,y:0},{x:10,y:0},{x:11,y:1},{x:12,y:1},{x:13,y:2},{x:14,y:8}]
    }]
  },
  options: {
    showLine: true,
    dotSize: 0.5,
    xTickCount: 5,
  },
});

</script>
