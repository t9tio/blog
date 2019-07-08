---
title: 你这玩意儿对我有啥好处? - 我的透明创业实验第八周 
description: what's your problem? what can I do for you
date: 2019-07-08
---

Hello world, 我是 [timqian](https://github.com/timqian), 正在进行为期一年的[透明创业实验](https://blog.t9t.io/transparent-startup-experiment-2019-05-20/). 这是关于这个实验第八周的实验记录.

## 一些想法

### 关于如何判断某一个产品的点子是否值得做

这周着重研究了一下这个问题, 看了一些文章, 其中最值得推荐的是一个 [startup idea checklist](https://smallbiztrends.com/2013/04/startup-checklist.html). idea 是无限的, 精力却是有限的, 在动手之前系统 check 一下这个 idea 是否值得投入精力十分必要. 当然, 如果只是为了娱乐而做的 project, 就没有太大必要了, 毕竟人活着, 最重要的是开心嘛😄

这篇文章在 hackernews 上也引起了巨大关注 https://news.ycombinator.com/item?id=20254057

最上面的一个评论令我反思良多

![](https://raw.githubusercontent.com/timqian/images/master/20190708143730.png)

做产品, 如果不是仅仅为了自娱自乐, 最重要的, 首要考虑的问题应该是 "who are the users", 这些用户对什么东西感到不满意, 我应该为他们做点什么.

而不是说我做了一个什么东西, 你快看, 这个东西多么炫酷多么高科技快来用吧, 你的朋友们可能关心你做了什么, 但大多数用户不是这样, 他们关心的是: **这玩意儿能为我带来什么**.

我之前做东西, 这个角度考虑的比较少, 所以做了许多没人用的东西(最后发现对别人没用的东西, 常常对自己也没有什么用, 最后就废弃了), 现在回过头去看看, 如果每次我动手之前都过一遍这个 checklist, 很多弯路就不必走了.

### 关于群聊消息打扰工作的问题

这周因为 wewe 新加入一些群聊的关系, 大量时间花费在和潜在用户沟通.
与用户交流是好事, 但是查看消息是会打断思路的, 这段时间与网友的交流越来越多, 对工作效率影响很大

**怎么办呢?**
一方面是想着设立一个聊微信/刷社区比较规律的节奏, 比如每隔一小时看一眼消息/邮件等, 杜绝一收到消息就前去查看的毛病
另一方面是下决心打压了 t9t.io 微信群里与产品无关的聊天, 移除了一些我觉得经常聊与产品无关的群友

关于微信群里太多闲聊, 也是为难了一阵, 因为一开始感觉禁止无关话题和移除群友不是很好意思, 但仔细想了想其实也还好.
对于进群闲聊的群友, 这个群并不重要, 无聊的时候进来翻翻聊天记录随意聊两句, 有没有这个群影响不大.
但当大多数话题都是这种闲聊的时候, 这个群变成了消磨无聊时间的无聊的群, 群友不会关心聊天记录, 但置顶了这个群聊的我却会食用所有的消息, 无疑会浪费我很多时间.
如果硬要从“水群”和“死群”二者选一个, 我选择后者😅

## 上周实验内容

本周一方面继续完善 [wewe](https://wewe.t9t.io)
- 在[v2ex 社区尝试发布了 wewe](https://www.v2ex.com/t/579952), 大概获得了 1000 次点击, 新加入了6个群. 得到不少反馈
- 发布前常常是最有效率的, 改善了不少问题比如支持撤回, 支持消息里的链接, 支持视频, 更新加群脚本让加新群更容易等等
- 基于原有计划和反馈, 在 github 上建了一个 [kanban 来组织 TODO](https://github.com/orgs/t9tio/projects/2), 也萌生了对 tomato-pie 做一个大改动的想法(kanban + todolist + pomodoro + share kanban)
- 初步加入了 slack 的支持, 建了 t9t 的 slack 群并且同步了消息, 但要让其他群可用, 还需要一点时间

## 本周计划

- wewe 加入 slack 支持, 与一些 slack 群主沟通看看
- 做 wewe 已经一个月了, 我好动的性格已经开始感到长时间做一件事情的疲倦. 可以做一些一两天能完成的小玩具调剂一下

## 数据分享

### 用户量
<canvas id="userChart"></canvas>

### github star 数
<canvas id="starChart"></canvas>

### 平均每月被动收入($)(本周收入 / 7 * 30)
<canvas id="incomeChart"></canvas>

<br/>

> [帮助我改进这篇文章](https://github.com/t9tio/blog/blob/master/source/_posts/t9t-week7.md)

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
        labels: ['week 1', 'week 2', 'week 3', 'week 4', 'week 5', 'week 6', 'week 7', 'week 8'],
        datasets: [{
            label: 'wewe',
            backgroundColor: chartColors.blue,
            borderColor: chartColors.blue,
            fill: false,
            data: [undefined, undefined, undefined, undefined, 0, 60, 80, 91]
        },{
            label: 'open source jobs',
            backgroundColor: chartColors.red,
            borderColor: chartColors.red,
            fill: false,
            data: [39, 60, 62, 80, 101, 105, 109, 111]
        },{
            label: 'tomato-pie',
            backgroundColor: chartColors.orange,
            borderColor: chartColors.orange,
            fill: false,
            data: [653, 673, 722, 634, 647, 705, 681, 714]
        },{
            label: 'star-history 插件',
            backgroundColor: chartColors.green, 
            borderColor: chartColors.green,
            fill: false,
            data: [21, 21, 28, 33, 33, 34, 39, 38]
        }]
    },
});

new Chart(starCtx, {
    type: 'line',
    data: {
        labels: ['week 1', 'week 2', 'week 3', 'week 4', 'week 5', 'week 6', 'week 7', 'week 8'],
        datasets: [{
            label: 'wewe',
            backgroundColor: chartColors.blue,
            borderColor: chartColors.blue,
            fill: false,
            data: [undefined, undefined, undefined, undefined, 0, 11, 33, 57]
        },{
            label: 'open source jobs',
            backgroundColor: chartColors.red,
            borderColor: chartColors.red,
            fill: false,
            data: [731, 764, 763, 821, 872, 891, 898, 903]
        },{
            label: 'tomato-pie',
            backgroundColor: chartColors.orange,
            borderColor: chartColors.orange,
            fill: false,
            data: [107, 113, 117, 118, 125, 126, 128, 129]
        },{
            label: 'star-history 插件',
            backgroundColor: chartColors.green, 
            borderColor: chartColors.green,
            fill: false,
            data: [921, 998, 1110, 1129, 1154, 1178, 1190, 1216]
        }]
    },
});

new Chart(incomeCtx, {
    type: 'line',
    data: {
        labels: ['week 1', 'week 2', 'week 3', 'week 4', 'week 5', 'week 6', 'week 7', 'week 8'],
        datasets: [{
            label: 'wewe',
            backgroundColor: chartColors.blue,
            borderColor: chartColors.blue,
            fill: false,
            data: [undefined, undefined, undefined, undefined, 0, 0, 0, 0]
        },{
            label: 'open opptunities',
            backgroundColor: chartColors.red,
            borderColor: chartColors.red,
            fill: false,
            data: [0, 0, 0, 0, 0, 0, 0, 0]
        },{
            label: 'tomato-pie',
            backgroundColor: chartColors.orange,
            borderColor: chartColors.orange,
            fill: false,
            data: [0, 0, 0, 0, 0, 0, 0, 0]
        },{
            label: 'star-history 插件',
            backgroundColor: chartColors.green, 
            borderColor: chartColors.green,
            fill: false,
            data: [0.69, 0, 25.7, 12.8, 0, 2/7*30, 1/7*30, 1/7*30]
        }]
    },
});

</script>
