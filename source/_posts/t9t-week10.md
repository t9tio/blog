---
title: 我的透明创业实验 - 第十周 
# description: what's your problem? what can I do for you
date: 2019-07-22
---

Hello world, 我是 [timqian](https://github.com/timqian), 正在进行为期一年的[透明创业实验](https://blog.t9t.io/transparent-startup-experiment-2019-05-20/). 这是关于这个实验第十周的实验记录.

## 一些思考

- 平时的每周总结不再到群里分享, 一是这是个人的一个记录, 不是博眼球, 赚阅读量的工具. 二是这个记录没那么有意思到让我想要到群里分享, 感兴趣的知道博客地址的自己偶尔自己访问比较让我舒服. 第三是我不需要那么多意见告诉我应该怎么做, 应该做什么, 我要做的是找到自己的工作节奏, 做自己感兴趣的产品.

- 放平心态, 一年时间, 不求一定要获得多少收入, 做出一些有用, 精致并且有一定用户量的产品, 就是成功.

- 尝试给自己的工作时间定个价: $100 每小时, 并且做一个接外包的页面. 希望努力让自己的时间至少值得这个价.

- 开始了新的工作习惯, 每天制定计划, 并考察完成情况. 计划定的不用很难实现, 可以在 4 小时内完成为佳.

- side project of side project: 发现自己专注做一个产品容易懈怠, 但同时做两个产品就要好些, 一个主要产品每天制定适当的计划逼迫自己前进. 另一个side project 全凭兴趣. 是我效率最高的工作方式.

## 每日计划和实施情况

|     | plan | 评价 |
| --- | --- | --- |
| 周一 |     |     |
| 周二 |  - [ ] slack oauth 1/2; - [x] submit blog to wechaty   |  - [ ] tried slack outgoing webhook;(但发现还是用 oauth 好些)  |
| 周三 |  - [x] finish slack oauth of [wewe](https://wewe.t9t.io)   |     |
| 周四 |  - [ ] landing page of [wewe](https://wewe.t9t.io)  |  没有完成landing page, 决定做一个 json to landing page 的工具, 方便之后做landing page 同时作为一个 side project   |
| 周五 |  忘记做 plan   |  在做 json to landing page, 估计还要一段时间才能完成   |
| 周六 |     |  抽空更新 json to landing page   |
| 周日 |     |  抽空推进 json to landing page   |

## 数据分享

> 产品详情可以访问 t9t.io 查看

### 用户量
<canvas id="userChart"></canvas>

### github star 数
<canvas id="starChart"></canvas>

### 平均每月被动收入($)(本周收入 / 7 * 30)
<canvas id="incomeChart"></canvas>

<br/>

> [帮助我改进这篇文章](https://github.com/t9tio/blog/blob/master/source/_posts/t9t-week10.md)

<script src="https://cdn.jsdelivr.net/npm/chart.js@2.8.0"></script>

<script>
var chartColors = {
	red: 'rgb(255, 99, 132)',
	orange: 'rgb(255, 159, 64)',
	yellow: 'rgb(255, 205, 86)',
	green: 'rgb(75, 192, 192)',
	blue: 'rgb(54, 162, 235)',
	purple: 'rgb(153, 102, 255)',
	grey: 'rgb(201, 203, 207)'
};
var userCtx = document.getElementById('userChart').getContext('2d');
var starCtx = document.getElementById('starChart').getContext('2d');
var incomeCtx = document.getElementById('incomeChart').getContext('2d');

new Chart(userCtx, {
    type: 'line',
    data: {
        labels: ['week 1', 'week 2', 'week 3', 'week 4', 'week 5', 'week 6', 'week 7', 'week 8', 'week 9',  'week 10'],
        datasets: [{
            label: 'wewe',
            backgroundColor: chartColors.blue,
            borderColor: chartColors.blue,
            fill: false,
            data: [undefined, undefined, undefined, undefined, 0, 60, 80, 91, 95, 95]
        },{
            label: 'open source jobs',
            backgroundColor: chartColors.red,
            borderColor: chartColors.red,
            fill: false,
            data: [39, 60, 62, 80, 101, 105, 109, 111, 113, 114]
        },{
            label: 'tomato-pie',
            backgroundColor: chartColors.orange,
            borderColor: chartColors.orange,
            fill: false,
            data: [653, 673, 722, 634, 647, 705, 681, 714, 712, 733]
        },{
            label: 'star-history 插件',
            backgroundColor: chartColors.green,
            borderColor: chartColors.green,
            fill: false,
            data: [21, 21, 28, 33, 33, 34, 39, 38, 40, 47]
        }]
    },
});

new Chart(starCtx, {
    type: 'line',
    data: {
        labels: ['week 1', 'week 2', 'week 3', 'week 4', 'week 5', 'week 6', 'week 7', 'week 8', 'week 9', 'week 10'],
        datasets: [{
            label: 'wewe',
            backgroundColor: chartColors.blue,
            borderColor: chartColors.blue,
            fill: false,
            data: [undefined, undefined, undefined, undefined, 0, 11, 33, 57, 70, 77]
        },{
            label: 'open source jobs',
            backgroundColor: chartColors.red,
            borderColor: chartColors.red,
            fill: false,
            data: [731, 764, 763, 821, 872, 891, 898, 903, 934, 940]
        },{
            label: 'tomato-pie',
            backgroundColor: chartColors.orange,
            borderColor: chartColors.orange,
            fill: false,
            data: [107, 113, 117, 118, 125, 126, 128, 129, 134, 134]
        },{
            label: 'star-history 插件',
            backgroundColor: chartColors.green, 
            borderColor: chartColors.green,
            fill: false,
            data: [921, 998, 1110, 1129, 1154, 1178, 1190, 1216, 1238, 1246]
        }]
    },
});

new Chart(incomeCtx, {
    type: 'line',
    data: {
        labels: ['week 1', 'week 2', 'week 3', 'week 4', 'week 5', 'week 6', 'week 7', 'week 8', 'week 9', 'week 10'],
        datasets: [{
            label: 'wewe',
            backgroundColor: chartColors.blue,
            borderColor: chartColors.blue,
            fill: false,
            data: [undefined, undefined, undefined, undefined, 0, 0, 0, 0, 0, 0]
        },{
            label: 'open opptunities',
            backgroundColor: chartColors.red,
            borderColor: chartColors.red,
            fill: false,
            data: [0, 0, 0, 0, 0, 0, 0, 0, 0, 0]
        },{
            label: 'tomato-pie',
            backgroundColor: chartColors.orange,
            borderColor: chartColors.orange,
            fill: false,
            data: [0, 0, 0, 0, 0, 0, 0, 0, 0, 0]
        },{
            label: 'star-history 插件',
            backgroundColor: chartColors.green, 
            borderColor: chartColors.green,
            fill: false,
            data: [0.69, 0, 25.7, 12.8, 0, 2/7*30, 1/7*30, 1/7*30, 2/7*30, 2/7*30]
        }]
    },
});

</script>
