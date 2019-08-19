---
title: 我的透明创业实验 - 第十三周
description: 埋头写手绘风格图表库(chart.xkcd)的一周
date: 2019-08-12
---

Hello world, 我是 [timqian](https://github.com/timqian), 正在进行为期一年的[透明创业实验](https://blog.t9t.io/transparent-startup-experiment-2019-05-20/). 这是关于这个实验第十三周的实验记录.

## 做了啥

[![](https://raw.githubusercontent.com/timqian/images/master/20190812085940.png)](https://github.com/timqian/chart.xkcd/)

这周专注于手绘风格图表库 [chart.xkcd](https://github.com/timqian/chart.xkcd/) 的开发, 熟悉 d3, 看了一些图表库的 API 设计和实现, 大概摸清了做一个图表库需要掌握的技术点

|     | plan | 评价 |
| --- | --- | --- |
| 周一 | play with d3  |    |
| 周二 | play with d3; tooltip |     |
| 周三 | play with d3; make line chart work|    |
| 周四 | API design; line chart  |  |
| 周五 | xkcd graph lib |  |
| 周末 |  | 抽取可复用的模块 |

## 本周目标

- 除了 line-chart 完成几种常用图标: bar-chart; pie-chart; dona-chart; 
- 希望可以做到一个可分享的水平

## 数据分享

> 产品详情可以访问 [t9t.io](https://t9t.io) 查看

### 平均每月被动收入($)(本周收入 / 7 * 30)
<canvas id="incomeChart"></canvas>

### 用户量
<canvas id="userChart"></canvas>

### github star 数
<canvas id="starChart"></canvas>

<br/>

> [帮助我改进这篇文章](https://github.com/t9tio/blog/blob/master/source/_posts/t9t-week13.md)

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
        labels: ['week 1', 'week 2', 'week 3', 'week 4', 'week 5', 'week 6', 'week 7', 'week 8', 'week 9', 'week 10', 'week 11', 'week 12', 'week 13'],
        datasets: [{
            label: 'wewe',
            backgroundColor: chartColors.blue,
            borderColor: chartColors.blue,
            fill: false,
            data: [undefined, undefined, undefined, undefined, 0, 60, 80, 91, 95, 95, 103, 103, 103]
        },{
            label: 'open source jobs',
            backgroundColor: chartColors.red,
            borderColor: chartColors.red,
            fill: false,
            data: [39, 60, 62, 80, 101, 105, 109, 111, 113, 114, 119, 121, 122]
        },{
            label: 'tomato-pie',
            backgroundColor: chartColors.orange,
            borderColor: chartColors.orange,
            fill: false,
            data: [653, 673, 722, 634, 647, 705, 681, 714, 712, 733, 774, 779, 801]
        },{
            label: 'star-history 插件',
            backgroundColor: chartColors.green,
            borderColor: chartColors.green,
            fill: false,
            data: [21, 21, 28, 33, 33, 34, 39, 38, 40, 47, 48, 50, 61]
        }]
    },
});

new Chart(starCtx, {
    type: 'line',
    data: {
        labels: ['week 1', 'week 2', 'week 3', 'week 4', 'week 5', 'week 6', 'week 7', 'week 8', 'week 9', 'week 10', 'week 11', 'week 12', 'week 13'],
        datasets: [{
            label: 'wewe',
            backgroundColor: chartColors.blue,
            borderColor: chartColors.blue,
            fill: false,
            data: [undefined, undefined, undefined, undefined, 0, 11, 33, 57, 70, 77, 78, 102, 103]
        },{
            label: 'open source jobs',
            backgroundColor: chartColors.red,
            borderColor: chartColors.red,
            fill: false,
            data: [731, 764, 763, 821, 872, 891, 898, 903, 934, 940, 956, 962, 966]
        },{
            label: 'tomato-pie',
            backgroundColor: chartColors.orange,
            borderColor: chartColors.orange,
            fill: false,
            data: [107, 113, 117, 118, 125, 126, 128, 129, 134, 134, 136, 136, 136]
        },{
            label: 'star-history 插件',
            backgroundColor: chartColors.green, 
            borderColor: chartColors.green,
            fill: false,
            data: [921, 998, 1110, 1129, 1154, 1178, 1190, 1216, 1238, 1246, 1276, 1291, 1299]
        }]
    },
});

new Chart(incomeCtx, {
    type: 'line',
    data: {
        labels: ['week 1', 'week 2', 'week 3', 'week 4', 'week 5', 'week 6', 'week 7', 'week 8', 'week 9', 'week 10', 'week 11', 'week 12', 'week 13'],
        datasets: [{
            label: 'star-history 插件',
            backgroundColor: chartColors.green,
            borderColor: chartColors.green,
            fill: false,
            data: [0.69, 0, 25.7, 12.8, 0, 2/7*30, 1/7*30, 1/7*30, 2/7*30, 2/7*30, 1/7*30, 4/7*30, 2/7*30]
        }, {
            label: 'patron',
            backgroundColor: chartColors.purple,
            borderColor: chartColors.purple,
            fill: false,
            data: [undefined, undefined, undefined, undefined,undefined, undefined, undefined, undefined,undefined, undefined, undefined, 1, 1]
        }]
    },
});

</script>

