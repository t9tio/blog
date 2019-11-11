---
title: 我的透明创业实验 - 第二十五周
# description:
date: 2019-11-04
---

Hello world, 我是 [timqian](https://github.com/timqian), 正在进行为期一年的[透明创业实验](https://blog.t9t.io/transparent-startup-experiment-2019-05-20/). 这是关于这个实验第二十五周的实验记录.

## 做了什么

在做社会化的 RSS 阅读器之前, 试着收集了一张中文独立博客列表并发布在了 [GitHub](https://github.com/timqian/chinese-independent-blogs). 和预想的一样, 获得了一些关注. 截止目前, 在 github 上获得了 1.1 k star, 有 100 人左右通过邮件订阅了我可能会做的这个 RSS 工具.

### 为什么会受关注?

- 根据博客的大致热度(博客 RSS 在 feedly 上的订阅数)进行了排序, 方便了大家找到热门/有价值的博客
- 列表主要是在 v2ex 收到很多回复, 因为观察到 v 站经常出现晒博客的帖子, 所以收集博客的帖子上热门也很容易理解.

### 关注度与变现

已经做过 5 个在 GitHub 超过 1k star 的项目了. 但是收入并没有起来, “看着 star 两千五, 一看收入二毛五”. 为什么会这样, 其实上周也提到过这个问题, 因为没有的付费入口, 你不试着去向用户收钱, 永远不知道这个产品有没有商业价值.

## 数据分享

> 产品详情可以访问 [t9t.io](https://t9t.io) 查看

### 平均每月被动收入($)(本周收入 / 7 * 30)

<svg id="incomeChart"></svg>

### 用户量
<svg id="userChart"></svg>

<script src="https://cdn.jsdelivr.net/npm/chart.xkcd@1.1.3/dist/chart.xkcd.min.js"></script>

<script>
var incomesvg = document.getElementById('incomeChart');
var usersvg = document.getElementById('userChart');


new chartXkcd.XY(incomesvg, {
  xLabel: 'weeks',
  data: {
    datasets: [{
        label: 'star-history',
        data: [{x:0,y:0.69},{x:1,y:0},{x:2,y:25.7},{x:3,y:12.8},{x:4,y:0},{x:5,y:8.571428571428571},{x:6,y:4.285714285714286},{x:7,y:4.285714285714286},{x:8,y:8.571428571428571},{x:9,y:8.571428571428571},{x:10,y:4.285714285714286},{x:11,y:17.142857142857142},{x:12,y:8.571428571428571},{x:13,y:3/7*30},{x:14,y:1/7*30},{x:15,y:3/7*30},{x:16,y:2/7*30},{x:17,y:0},{x:18,y:3/7*30},{x:21,y:1/7*30},{x:22,y:2/7*30},{x:23,y:3/7*30},{x:24,y:2/7*30}]
    }, {
        label: 'patron',
        data: [{x:10,y:0},{x:11,y:1},{x:12,y:1},{x:13,y:2},{x:14,y:8},{x:15,y:8},{x:16,y:9},{x:17,y:10},{x:18,y:10},{x:21,y:9},{x:22,y:9},{x:23,y:10},{x:24,y:11}]
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
          label: 'repo-analytics',
          data: [{x:21,y:0}, {x:22,y:69},{x:23,y:82},{x:24,y:89}]
      },{
          label: 'wewe',
          data: [{x:3,y:0},{x:4,y:60},{x:5,y:80},{x:6,y:91},{x:7,y:95},{x:8,y:95},{x:9,y:103},{x:10,y:103},{x:11,y:103},{x:12,y:103},{x:13,y:103},{x:14,y:103},{x:15,y:103},{x:16,y:108},{x:16,y:108},{x:17,y:111},{x:18,y:111},{x:21,y:127},{x:22,y:128},{x:23,y:128},{x:24,y:128}]
      },{
          label: 'open source jobs',
          data: [{x:0,y:39},{x:1,y:60},{x:2,y:62},{x:3,y:80},{x:4,y:101},{x:5,y:105},{x:6,y:109},{x:7,y:111},{x:8,y:113},{x:9,y:114},{x:10,y:119},{x:11,y:121},{x:12,y:122},{x:13,y:123},{x:14,y:123},{x:15,y:127},{x:16,y:131},{x:17,y:132},{x:18,y:133},{x:21,y:139},{x:22,y:140},{x:23,y:141},{x:24,y:141}]
      },{
          label: 'tomato-pie',
          data: [{x:0,y:653},{x:1,y:673},{x:2,y:722},{x:3,y:634},{x:4,y:647},{x:5,y:705},{x:6,y:681},{x:7,y:714},{x:8,y:712},{x:9,y:733},{x:10,y:774},{x:11,y:779},{x:12,y:801},{x:13,y:821},{x:14,y:898},{x:15,y:911},{x:16,y:981},{x:17,y:917},{x:18,y:920},{x:21,y:875},{x:22,y:904},{x:23,y:947},{x:24,y:1001}]
      },{
          label: 'star-history',
          data: [{x:0,y:21},{x:1,y:21},{x:2,y:28},{x:3,y:33},{x:4,y:33},{x:5,y:34},{x:6,y:39},{x:7,y:38},{x:8,y:40},{x:9,y:47},{x:10,y:48},{x:11,y:50},{x:12,y:61},{x:13,y:58},{x:14,y:55},{x:15,y:57},{x:16,y:58},{x:17,y:58},{x:18,y:63},{x:21,y:73},{x:22,y:75},{x:23,y:82},{x:24,y:81}]
      },]
  },
  options: {
    showLine: true,
    dotSize: 0.5,
    xTickCount: 5,
  }
});

</script>
