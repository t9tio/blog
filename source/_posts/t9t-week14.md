---
title: 记录一次成功的产品发布现场 - 我的透明创业实验第十四周
description: Build something should exist
date: 2019-08-19
---

Hello world, 我是 [timqian](https://github.com/timqian), 正在进行为期一年的[透明创业实验](https://blog.t9t.io/transparent-startup-experiment-2019-05-20/). 这是关于这个实验第十四周的实验记录.

## 发布了什么

[chart.xkcd](https://github.com/chart.xkcd) - 一个手绘风格的图表库
![](https://raw.githubusercontent.com/timqian/images/master/20190819131226.gif)

## 成功的发布?

- 现在在 show HN 首页第一条: https://news.ycombinator.com/show
<details>
![](https://raw.githubusercontent.com/timqian/images/master/20190819173935.png)
</details>
- reddit programming 首页(第三条): https://www.reddit.com/r/programming/
<details>
![](https://raw.githubusercontent.com/timqian/images/master/20190819173931.png)
</details>
- GitHub 上4 小时涨了 500 star
<details>
![](https://raw.githubusercontent.com/timqian/images/master/20190819174117.png)
</details>

这是我第一次写一个轮子可以同时登上两个全球主要程序员社区首页, 纵向对比, 至少是我所有发布过的轮子中最成功的一次😅

那么, 这个轮子为什么不想我大多数其他轮子一样发布即葬礼呢?

## Build something should exist

虽然有点马后炮, 但是在发布这个轮子之前, 我感觉它受欢迎的可能性是比较大的, 为什么这么说呢

1. 之前在论坛上有多次类似需求/产品的讨论, 都得到了不错的反响:
<details>
  - xkcd styled charts in matplotlib: https://news.ycombinator.com/item?id=19293129
  - simple line graph in d3: https://news.ycombinator.com/item?id=4671676
  - disscussions on stackexchange: https://mathematica.stackexchange.com/questions/11350/xkcd-s...
  - why are xkcd styled graph important: https://news.ycombinator.com/item?id=7511762
</details>
2. 这个东西是新的, 解决了原来没解决的问题或者更好的解决了问题

## 启示

如果这个产品应该要存在, 但是还没有存在, 它大概率会引起人们注意. 少数给我带来收入的 的另一个产品[star-history](https://star-history.t9t.io), 也是符合这个逻辑的. star 的历史是有意义的, 但是 github 没有提供这个功能. 你把它做出来了, 它值得获得关注.

如何确定这个产品/轮子 "should exist"

- previous demand: 之前就存在类似需求, 是一个老需求, 而不是你制造的需求
- 类似需求大家还挺迫切
- 这个解决方案是新的!

如果满足了上述要求, 你的解决方案也过得去, 正常应该可以获得一次成功的发布

## 本周目标

- chart.xkcd 修 bug, 加图表, 加文档.
- 重启 hackermap?

## 数据分享

> 产品详情可以访问 [t9t.io](https://t9t.io) 查看

### 平均每月被动收入($)(本周收入 / 7 * 30)
<canvas id="incomeChart"></canvas>

### 用户量
<canvas id="userChart"></canvas>

### github star 数
<canvas id="starChart"></canvas>

<br/>

> [帮助我改进这篇文章](https://github.com/t9tio/blog/blob/master/source/_posts/t9t-week12.md)

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
        labels: ['week 1', 'week 2', 'week 3', 'week 4', 'week 5', 'week 6', 'week 7', 'week 8', 'week 9', 'week 10', 'week 11', 'week 12', 'week 13', 'week 14'],
        datasets: [{
            label: 'wewe',
            backgroundColor: chartColors.blue,
            borderColor: chartColors.blue,
            fill: false,
            data: [undefined, undefined, undefined, undefined, 0, 60, 80, 91, 95, 95, 103, 103, 103, 103]
        },{
            label: 'open source jobs',
            backgroundColor: chartColors.red,
            borderColor: chartColors.red,
            fill: false,
            data: [39, 60, 62, 80, 101, 105, 109, 111, 113, 114, 119, 121, 122, 123]
        },{
            label: 'tomato-pie',
            backgroundColor: chartColors.orange,
            borderColor: chartColors.orange,
            fill: false,
            data: [653, 673, 722, 634, 647, 705, 681, 714, 712, 733, 774, 779, 801, 821]
        },{
            label: 'star-history 插件',
            backgroundColor: chartColors.green,
            borderColor: chartColors.green,
            fill: false,
            data: [21, 21, 28, 33, 33, 34, 39, 38, 40, 47, 48, 50, 61, 58]
        }]
    },
});

new Chart(starCtx, {
    type: 'line',
    data: {
        labels: ['week 1', 'week 2', 'week 3', 'week 4', 'week 5', 'week 6', 'week 7', 'week 8', 'week 9', 'week 10', 'week 11', 'week 12', 'week 13', 'week 14'],
        datasets: [{
            label: 'wewe',
            backgroundColor: chartColors.blue,
            borderColor: chartColors.blue,
            fill: false,
            data: [undefined, undefined, undefined, undefined, 0, 11, 33, 57, 70, 77, 78, 102, 103, ]
        },{
            label: 'open source jobs',
            backgroundColor: chartColors.red,
            borderColor: chartColors.red,
            fill: false,
            data: [731, 764, 763, 821, 872, 891, 898, 903, 934, 940, 956, 962, 966, 967]
        },{
            label: 'tomato-pie',
            backgroundColor: chartColors.orange,
            borderColor: chartColors.orange,
            fill: false,
            data: [107, 113, 117, 118, 125, 126, 128, 129, 134, 134, 136, 136, 139]
        },{
            label: 'star-history 插件',
            backgroundColor: chartColors.green,
            borderColor: chartColors.green,
            fill: false,
            data: [921, 998, 1110, 1129, 1154, 1178, 1190, 1216, 1238, 1246, 1276, 1291, 1299, 1308]
        }, {
            label: 'chart.xkcd',
            backgroundColor: chartColors.grey,
            borderColor: chartColors.grey,
            fill: false,
            data: [undefined, undefined, undefined, undefined, undefined, undefined, undefined, undefined, undefined, undefined, undefined, undefined, 3, 500,]
        }]
    },
});

new Chart(incomeCtx, {
    type: 'line',
    data: {
        labels: ['week 1', 'week 2', 'week 3', 'week 4', 'week 5', 'week 6', 'week 7', 'week 8', 'week 9', 'week 10', 'week 11', 'week 12', 'week 13', 'week 14'],
        datasets: [{
            label: 'star-history 插件',
            backgroundColor: chartColors.green,
            borderColor: chartColors.green,
            fill: false,
            data: [0.69, 0, 25.7, 12.8, 0, 2/7*30, 1/7*30, 1/7*30, 2/7*30, 2/7*30, 1/7*30, 4/7*30, 2/7*30, 3/7*30]
        }, {
            label: 'patron',
            backgroundColor: chartColors.purple,
            borderColor: chartColors.purple,
            fill: false,
            data: [undefined, undefined, undefined, undefined,undefined, undefined, undefined, undefined,undefined, undefined, undefined, 1, 1, 2]
        }]
    },
});

</script>
