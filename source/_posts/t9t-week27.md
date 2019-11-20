---
title: 为了用 markdown 写简历, 我做了这个工具 - 我的透明创业实验第二十七周
# description:
date: 2019-11-20
---

前段时间看到一家很[有趣的公司](https://www.v2ex.com/t/617200), 可以自己定工作时间, 可以远程, [他们的产品](https://xinxiao.tech/)做的也很精美. 我想, 把自己的一部分时间分配到为这家公司工作是一个不错的选择, 有许多我可以学习的地方(当然, 还可以挣钱😅).

于是我打开了尘封已久的简历.

这个简历是 LaTeX 写的, 信息有点老了, 样式我也不再喜欢. 要是用 markdown 写的简历可以方便得定制样式并导出 PDF 就好了....

我搜了一圈, 发现了一些[提供这些功能的工具](https://github.com/timqian/resumd#privious-art), 但是没有可以完全满足我要求的. 最接近我需求的是一个国人做的 [冷熊简历](http://cv.ftqq.com/#), 提供了 PDF 下载. 但是他提供的样式我不太喜欢, 又不能自定义.

于是, 我自己做了一个 [web app](https://github.com/timqian/resumd) 来满足这个小小的需求:

<p align="center">
  <a href="https://resumd.t9t.io"><img width="300" src="https://i.v2ex.co/e0W134z7.png"></a>
</p>

[Resumd](https://github.com/timqian/resumd) 特点是

- 可以导出为 HTML/PDF ([example PDF](https://github.com/timqian/resumd/blob/master/samplePDFs/TUI.pdf))
- [是一个网页应用](https://resumd.t9t.io)
- 可以自定义样式([GitHub theme](https://github.com/timqian/resumd/blob/master/samplePDFs/GitHub.pdf), [timqian.com theme](https://github.com/timqian/resumd/blob/master/samplePDFs/timqian.pdf), [TUI theme](https://github.com/timqian/resumd/blob/master/samplePDFs/TUI.pdf))
- 方便得分享给别人一个可编辑的简历
- 一个纯前端应用, 不用担心数据泄漏

如果你也想用 markdown 写简历的话, 欢迎试用~

## 我成为了一个 half day indie hacker

简历投出去, 经过几轮面试, 我成为了[新小科技](https://xinxiao.tech/)的一员. 从这周开始, 我每天下午的时间会和新小科技一起探索/制作/维护产品. 每天上午时间做我自己的事情. 现在是一个 half day indie hacker 了😅

## 透明创业实验会继续吗?

side project 还会继续做, 博客还会继续写, 但是可能不再以每周记录的格式, 而是在有想法或者新产品时, 记录下 side project 的背后的一些想法和过程.

## 有一份不完全占据精力的工作的好处

在做自己的产品时, 因为更少的资金上的压力, 我可以更少的关心盈利, 更多的关注做的东西是不是新的, 是不是有用的, 而不是短期能否给我带来收入. 以赚钱为主要目的做产品, 你要为你的产品设置使用障碍, 比如一些功能只有付钱才能用(pay wall). 花很多时间去设置这个 pay wall 是一件必须但是没那么有趣的事情.

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
        data: [{x:0,y:0.69},{x:1,y:0},{x:2,y:25.7},{x:3,y:12.8},{x:4,y:0},{x:5,y:8.571428571428571},{x:6,y:4.285714285714286},{x:7,y:4.285714285714286},{x:8,y:8.571428571428571},{x:9,y:8.571428571428571},{x:10,y:4.285714285714286},{x:11,y:17.142857142857142},{x:12,y:8.571428571428571},{x:13,y:3/7*30},{x:14,y:1/7*30},{x:15,y:3/7*30},{x:16,y:2/7*30},{x:17,y:0},{x:18,y:3/7*30},{x:21,y:1/7*30},{x:22,y:2/7*30},{x:23,y:3/7*30},{x:24,y:2/7*30},{x:25,y:3/7*30},{x:26,y:4/7*30}]
    }, {
        label: 'patron',
        data: [{x:10,y:0},{x:11,y:1},{x:12,y:1},{x:13,y:2},{x:14,y:8},{x:15,y:8},{x:16,y:9},{x:17,y:10},{x:18,y:10},{x:21,y:9},{x:22,y:9},{x:23,y:10},{x:24,y:11},{x:25,y:11},{x:26,y:11}]
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
          data: [{x:21,y:0}, {x:22,y:69},{x:23,y:82},{x:24,y:89},{x:25,y:103},{x:26,y:125}]
      },{
          label: 'wewe',
          data: [{x:3,y:0},{x:4,y:60},{x:5,y:80},{x:6,y:91},{x:7,y:95},{x:8,y:95},{x:9,y:103},{x:10,y:103},{x:11,y:103},{x:12,y:103},{x:13,y:103},{x:14,y:103},{x:15,y:103},{x:16,y:108},{x:16,y:108},{x:17,y:111},{x:18,y:111},{x:21,y:127},{x:22,y:128},{x:23,y:128},{x:24,y:128},{x:25,y:130},{x:26,y:130}]
      },{
          label: 'open source jobs',
          data: [{x:0,y:39},{x:1,y:60},{x:2,y:62},{x:3,y:80},{x:4,y:101},{x:5,y:105},{x:6,y:109},{x:7,y:111},{x:8,y:113},{x:9,y:114},{x:10,y:119},{x:11,y:121},{x:12,y:122},{x:13,y:123},{x:14,y:123},{x:15,y:127},{x:16,y:131},{x:17,y:132},{x:18,y:133},{x:21,y:139},{x:22,y:140},{x:23,y:141},{x:24,y:141},{x:25,y:144},{x:26,y:144}]
      },{
          label: 'tomato-pie',
          data: [{x:0,y:653},{x:1,y:673},{x:2,y:722},{x:3,y:634},{x:4,y:647},{x:5,y:705},{x:6,y:681},{x:7,y:714},{x:8,y:712},{x:9,y:733},{x:10,y:774},{x:11,y:779},{x:12,y:801},{x:13,y:821},{x:14,y:898},{x:15,y:911},{x:16,y:981},{x:17,y:917},{x:18,y:920},{x:21,y:875},{x:22,y:904},{x:23,y:947},{x:24,y:1001},{x:25,y:960},{x:26,y:1004}]
      },{
          label: 'star-history',
          data: [{x:0,y:21},{x:1,y:21},{x:2,y:28},{x:3,y:33},{x:4,y:33},{x:5,y:34},{x:6,y:39},{x:7,y:38},{x:8,y:40},{x:9,y:47},{x:10,y:48},{x:11,y:50},{x:12,y:61},{x:13,y:58},{x:14,y:55},{x:15,y:57},{x:16,y:58},{x:17,y:58},{x:18,y:63},{x:21,y:73},{x:22,y:75},{x:23,y:82},{x:24,y:81},{x:25,y:79},{x:26,y:89}]
      },]
  },
  options: {
    showLine: true,
    dotSize: 0.5,
    xTickCount: 5,
  }
});

</script>
