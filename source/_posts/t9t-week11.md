---
title: 吉他与产品开发 - 我的透明创业实验第十一周
# description: what's your problem? what can I do for you
date: 2019-07-22
---

Hello world, 我是 [timqian](https://github.com/timqian), 正在进行为期一年的[透明创业实验](https://blog.t9t.io/transparent-startup-experiment-2019-05-20/). 这是关于这个实验第十一周的实验记录.

## 一些思考

我使用[番茄工作法](https://github.com/t9tio/tomato-pie)来管理自己的时间. 番茄工作法的标准流程是工作25分钟, 休息5分钟为一个番茄; 在经过一些番茄之后(比如4个)进行较长时间的休息(比如半小时). 

一直以来在, 在番茄的间隙没有找到很好的放松方式，最近第三次开始练起了吉他😅，尝试作为工作间隙的休息.

没想到效果出奇的好. 仅次于疲劳时的睡一觉的效果.

为什么会这样呢? 可能是因为弹吉他时大脑使劲的部分大部改变，让负责写代码部分的神经＆肌肉获得了充分休息(我随便说说, 你随便听听)

练习吉他是一个纯粹针以提升能力为目标的活动, 设计产品, 写代码则是以产出东西为目标. 在这种完全不同目标的活动中, 让我注意到能力的重要性.

我的目标是 "make something many people want", 这是很难的，可能要失败99次才有一个产品成功。所以又快又好得完成产品能力是很重要的. 极端情况下，如果我的产品能力很强，一天就可以完成一个淘宝复杂度的产品。我就可以每天尝试一个点子，这种情况下成功概率是很大的.

在之后的产品制作过程中，除了产品本身，我也应该像练习吉他一样，一部分注意力放在如何提升产品的能力上.

关注哪些方面可以提升这方面能力呢？

1. 关注每次做产品会重复做的一些事情，寻找有没有办法减少重复劳动. 比如最近在做的生成 landing page 的工具算作这一类
2. 提高工作效率，利用番茄工作法，"计划，实施，反思"等方法, 寻找自己效率最高, 最舒服的工作方式, 让自己在同样时间有更多的产出
3. 算法，设计模式等可复用的知识，但花在这些东西上的时间要适量，毕竟解决现实问题是第一要务

关于提升产品力, 你有什么建议呢？
·
## 工作计划和实施情况

|     | plan | 评价 |
| --- | --- | --- |
| 周一 | - [ ] json to landing page: finish necessary components for wewe  |  没有完成, 工作时间太短   |
| 周二 | - [ ] 补上昨天没做完的 + - [ ] update wewe to include landing page |  完成   |
| 周三 | - [ ] wewe: 抽取话题 UI  |  粗略完成了从一条消息生成 topic 的工作, 还有一些其他工作: topic 分页, topic msg 分页   |
| 周四 | - [ ]  wewe: topic 分页, - [ ] topic msg 分页 其他一些优化 |  优化了 landing page, make wewe being ready to share  |
| 周五 | - [ ] json2landing 展示组建的模块 | 完成   |
| 周末 |     | 抽空推进 json2landing  |

## 数据分享

> 产品详情可以访问 [t9t.io](https://t9t.io) 查看

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
        labels: ['week 1', 'week 2', 'week 3', 'week 4', 'week 5', 'week 6', 'week 7', 'week 8', 'week 9', 'week 10', 'week 11'],
        datasets: [{
            label: 'wewe',
            backgroundColor: chartColors.blue,
            borderColor: chartColors.blue,
            fill: false,
            data: [undefined, undefined, undefined, undefined, 0, 60, 80, 91, 95, 95, 103]
        },{
            label: 'open source jobs',
            backgroundColor: chartColors.red,
            borderColor: chartColors.red,
            fill: false,
            data: [39, 60, 62, 80, 101, 105, 109, 111, 113, 114, 119]
        },{
            label: 'tomato-pie',
            backgroundColor: chartColors.orange,
            borderColor: chartColors.orange,
            fill: false,
            data: [653, 673, 722, 634, 647, 705, 681, 714, 712, 733, 774]
        },{
            label: 'star-history 插件',
            backgroundColor: chartColors.green,
            borderColor: chartColors.green,
            fill: false,
            data: [21, 21, 28, 33, 33, 34, 39, 38, 40, 47, 48]
        }]
    },
});

new Chart(starCtx, {
    type: 'line',
    data: {
        labels: ['week 1', 'week 2', 'week 3', 'week 4', 'week 5', 'week 6', 'week 7', 'week 8', 'week 9', 'week 10', 'week 11'],
        datasets: [{
            label: 'wewe',
            backgroundColor: chartColors.blue,
            borderColor: chartColors.blue,
            fill: false,
            data: [undefined, undefined, undefined, undefined, 0, 11, 33, 57, 70, 77, 78]
        },{
            label: 'open source jobs',
            backgroundColor: chartColors.red,
            borderColor: chartColors.red,
            fill: false,
            data: [731, 764, 763, 821, 872, 891, 898, 903, 934, 940, 956]
        },{
            label: 'tomato-pie',
            backgroundColor: chartColors.orange,
            borderColor: chartColors.orange,
            fill: false,
            data: [107, 113, 117, 118, 125, 126, 128, 129, 134, 134, 136]
        },{
            label: 'star-history 插件',
            backgroundColor: chartColors.green, 
            borderColor: chartColors.green,
            fill: false,
            data: [921, 998, 1110, 1129, 1154, 1178, 1190, 1216, 1238, 1246, 1276]
        }]
    },
});

new Chart(incomeCtx, {
    type: 'line',
    data: {
        labels: ['week 1', 'week 2', 'week 3', 'week 4', 'week 5', 'week 6', 'week 7', 'week 8', 'week 9', 'week 10', 'week 11'],
        datasets: [{
            label: 'wewe',
            backgroundColor: chartColors.blue,
            borderColor: chartColors.blue,
            fill: false,
            data: [undefined, undefined, undefined, undefined, 0, 0, 0, 0, 0, 0, 0]
        },{
            label: 'open opptunities',
            backgroundColor: chartColors.red,
            borderColor: chartColors.red,
            fill: false,
            data: [0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0]
        },{
            label: 'tomato-pie',
            backgroundColor: chartColors.orange,
            borderColor: chartColors.orange,
            fill: false,
            data: [0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0]
        },{
            label: 'star-history 插件',
            backgroundColor: chartColors.green,
            borderColor: chartColors.green,
            fill: false,
            data: [0.69, 0, 25.7, 12.8, 0, 2/7*30, 1/7*30, 1/7*30, 2/7*30, 2/7*30, 1/7*30]
        }]
    },
});

</script>
