---
title: 我的透明创业实验 - 第六周
description: 探究一个机灵程度中上的普通人, 给他一年时间让他自由创造, 是否有可能获得1000美元每月的被动收入.
date: 2019-06-23
---

Hello world, 我是 [timqian](https://github.com/timqian), 正在进行为期一年的[透明创业实验](https://blog.t9t.io/transparent-startup-experiment-2019-05-20/). 这是关于这个实验第六周的实验记录.

## 实验内容

本周继续专注于 [wewe](https://wewe.t9t.io), 完成的功能有:
- 注册功能(认领群聊身份)
- 基于一些群友的反馈, 从默认显示昵称变成了默认匿名, 注册用户才显示昵称
- members page: 显示注册群友的信息, 方便大家相互了解
- 聊天记录中的图片/emoj 支持
- bot 消息过滤, 把一些加群等无关消息剔除
- 关于如何摘取 topic 的思考

在完成了最基本的聊天记录收集&注册功能之后在我自己的四个群开始试用 [wewe](https://wewe.t9t.io), 有60几位群友认领了自己在群内的身份, 收到了不少反馈和建议, 是一个不错的开始

关于听取用户的需求, 从用户那里得到一些原本没有预想到的应用和顾虑, 例如
- 用微信快闪群直播分享的需求
- 有群友对[wewe](https://wewe.t9t.io)隐私的顾虑
- 群消息通过语音接口读出来等附加功能
- 关于激励机制提高群聊话题质量
- 等等

<details>
<summary>*从 tomato-pie 截取的每日工作细节*</summary>
![](https://raw.githubusercontent.com/timqian/images/master/Screen%20Shot%202019-06-23%20at%2010.44.10%20PM.png)
![](https://raw.githubusercontent.com/timqian/images/master/Screen%20Shot%202019-06-23%20at%2010.44.20%20PM.png)
![](https://raw.githubusercontent.com/timqian/images/master/Screen%20Shot%202019-06-23%20at%2010.44.35%20PM.png)
![](https://raw.githubusercontent.com/timqian/images/master/Screen%20Shot%202019-06-23%20at%2010.46.20%20PM.png)
![](https://raw.githubusercontent.com/timqian/images/master/Screen%20Shot%202019-06-23%20at%2010.44.53%20PM.png)
![](https://raw.githubusercontent.com/timqian/images/master/Screen%20Shot%202019-06-23%20at%2010.45.02%20PM.png)
![](https://raw.githubusercontent.com/timqian/images/master/Screen%20Shot%202019-06-23%20at%2010.45.08%20PM.png)
</details>

## 一些思考

[wewe](https://wewe.t9t.io) 为这个世界提供的核心价值
- 让散落在封闭群聊里有价值的信息变得公开 & 可被搜索

[wewe](https://wewe.t9t.io) 的主要盈利方式
- 作为一个信息类网站, 主要收入来自广告

聊天话题的提取是 wewe 很重要的一部分, 单纯的聊天记录意义不是那么大, 因为
- 过长的聊天记录很难阅读, 找到重点.
- 当用户在搜索引擎搜索某个关键词时, 引擎对页面的排序与关键词所在位置有关, 在 url 匹配到的话优先级最高, title 中其次, 无主题的某一页聊天记录优先级是比较低的, 难以被搜索到. 摘成话题的聊天记录, 不仅易读, 还对搜索引擎比较友好, 预计搜索引擎是 wewe 最大的流量来源

周三和周四陷入对某些前端效果细节来回修改, 拖慢了整体的进度, 应该先把产品最核心的价值做好

## 本周计划

本周继续专注 [wewe](https://wewe.t9t.io), 完成 topic 模块之后准备再加入一些其他的技术群, 并且发布到几个技术社区收取更多的反馈意见. 如果有时间, 增强一下 [tomato-pie](https://github.com/t9tio/tomato-pie) 的统计功能, 希望之后每周的工作日志可以自动导出, 而不是像现在这样一天天截屏😅

## 数据分享 (本周开始记录和分享 [wewe](https://wewe.t9t.io) 的数据)

目前维护和开发的四个主要产品是 [wewe](https://github.com/t9tio/wewe), [open-source-jobs](https://github.com/t9tio/open-source-jobs) , [tomato-pie](https://github.com/t9tio/tomato-pie) , [star-history](https://github.com/timqian/star-history)

### 用户量
<canvas id="userChart"></canvas>

### github star 数
<canvas id="starChart"></canvas>

### 平均每月被动收入($)(本周收入 / 7 * 30)
<canvas id="incomeChart"></canvas>

<br/>

> [帮助我改进这篇文章](https://github.com/t9tio/blog/blob/master/source/_posts/t9t-week6.md)

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
        labels: ['week 1', 'week 2', 'week 3', 'week 4', 'week 5', 'week 6'],
        datasets: [{
            label: 'wewe',
            backgroundColor: chartColors.blue,
            borderColor: chartColors.blue,
            fill: false,
            data: [undefined, undefined, undefined, undefined, 0, 60]
        },{
            label: 'open source jobs',
            backgroundColor: chartColors.red,
            borderColor: chartColors.red,
            fill: false,
            data: [39, 60, 62, 80, 101, 105]
        },{
            label: 'tomato-pie',
            backgroundColor: chartColors.orange,
            borderColor: chartColors.orange,
            fill: false,
            data: [653, 673, 722, 634, 647, 705]
        },{
            label: 'star-history 插件',
            backgroundColor: chartColors.green, 
            borderColor: chartColors.green,
            fill: false,
            data: [21, 21, 28, 33, 33, 34]
        }]
    },
});

new Chart(starCtx, {
    type: 'line',
    data: {
        labels: ['week 1', 'week 2', 'week 3', 'week 4', 'week 5', 'week 6'],
        datasets: [{
            label: 'wewe',
            backgroundColor: chartColors.blue,
            borderColor: chartColors.blue,
            fill: false,
            data: [undefined, undefined, undefined, undefined, 0, 11]
        },{
            label: 'open source jobs',
            backgroundColor: chartColors.red,
            borderColor: chartColors.red,
            fill: false,
            data: [731, 764, 763, 821, 872, 891]
        },{
            label: 'tomato-pie',
            backgroundColor: chartColors.orange,
            borderColor: chartColors.orange,
            fill: false,
            data: [107, 113, 117, 118, 125, 126]
        },{
            label: 'star-history 插件',
            backgroundColor: chartColors.green, 
            borderColor: chartColors.green,
            fill: false,
            data: [921, 998, 1110, 1129, 1154, 1178]
        }]
    },
});

new Chart(incomeCtx, {
    type: 'line',
    data: {
        labels: ['week 1', 'week 2', 'week 3', 'week 4', 'week 5', 'week 6'],
        datasets: [{
            label: 'wewe',
            backgroundColor: chartColors.blue,
            borderColor: chartColors.blue,
            fill: false,
            data: [undefined, undefined, undefined, undefined, 0, 0]
        },{
            label: 'open opptunities',
            backgroundColor: chartColors.red,
            borderColor: chartColors.red,
            fill: false,
            data: [0, 0, 0, 0, 0, 0]
        },{
            label: 'tomato-pie',
            backgroundColor: chartColors.orange,
            borderColor: chartColors.orange,
            fill: false,
            data: [0, 0, 0, 0, 0, 0]
        },{
            label: 'star-history 插件',
            backgroundColor: chartColors.green, 
            borderColor: chartColors.green,
            fill: false,
            data: [0.69, 0, 25.7, 12.8, 0, 2/7*30]
        }]
    },
});

</script>