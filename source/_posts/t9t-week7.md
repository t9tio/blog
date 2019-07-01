---
title: 独立开发的心情起伏 - 我的透明创业实验第七周 
description: 心情起起伏伏伏伏伏伏伏伏
date: 2019-07-01
---

Hello world, 我是 [timqian](https://github.com/timqian), 正在进行为期一年的[透明创业实验](https://blog.t9t.io/transparent-startup-experiment-2019-05-20/). 这是关于这个实验第六周的实验记录.

## 实验内容

本周还是专注于 [wewe](https://wewe.t9t.io)
- 完成了 topic 手动摘取的功能 e.g. [https://wewe.t9t.io/chat/t9t.io%20community/topics](https://wewe.t9t.io/chat/t9t.io%20community/topics)
- 增加了 [about 页](https://wewe.t9t.io/about)
- 调研了并且尝试了 slack bot, 开始为 wewe 增加 slack 群支持
- 前同事组织了许多技术群, 这周邀请了他在维护的一些群加入了 wewe.<!-- 得到了更多反馈.最多的还是对隐私的顾虑. 可以想象之后发布的时候, 最多的问题还是这个, 所以打算先做好 slack 的支持再做发布-->

<details>
<summary>*从 tomato-pie 截取的每日工作细节*</summary>
![](https://raw.githubusercontent.com/timqian/images/master/20190701095125.png)
![](https://raw.githubusercontent.com/timqian/images/master/20190701095128.png)
![](https://raw.githubusercontent.com/timqian/images/master/20190701095131.png)
![](https://raw.githubusercontent.com/timqian/images/master/20190701095135.png)
![](https://raw.githubusercontent.com/timqian/images/master/20190701095138.png)
</details>

## 心情的起起伏伏伏伏伏伏伏伏

两个月没有上班了, 最近却感觉比上班还要累. 焦虑慌张, 腰酸背痛却不愿意离开座位休息一下想要再多输出点什么, 最后更累了效率极低在网上充起浪来. 微信群也是 distraction, 做事做到一半打开群看看, 思路被群里的讨论吸引向别处...
对未知的焦虑, 缺乏自律让我寸步难行

好在意识到了问题之后, 应该怎么做的答案也自然而然出现了

1. 感觉了累了就放空自己, 不要怕休息时间太长, 没有状态死磕一上午还不如出去散个长步回来换一下午的高效,  但放松的方式不能是屏幕相关否则更累
2. 微信定时打开, 工作时段坚决不看消息
3. 学习 startup 元知识, 看过挺多成功经验, 失败 tip, 有许多值得借鉴的地方。我相信产品的成功是存在很多套路的, 比如通过发对用户有意义的邮件这种保持活跃度的方式, 是任何产品都可以套用的。停下来, 花点时间收集总结一下这些前人总结的套路, 让自己心里更有谱一些
4. 心情起伏还是太大, 一下觉得自己做的事很有意义, 下一秒又觉得毫无意义, 上一秒精力充沛想要大干一场, 下一秒灰心丧气不想干了, 不成熟的表现, 所以需要一些框架来判断点子的好坏, 而不是凭心情来判断点子的好坏

## 本周计划

- 本周准备停下来, 学习几天. 最近看到 [YC startup school 2019](https://blog.ycombinator.com/announcing-startup-school-2019/) 快开始了, 报了个名. 这份大纲描述的主题很多都很有意思很重要. 准备花几天时间自己对其中几个主题做一下调研, 总结. 作为学习和课程预习, 最后写一篇 "startup 套路" / "startup checklist" 的博客作为总结.

![](https://raw.githubusercontent.com/timqian/images/master/20190701105912.png)

- wewe 的 slack 支持要在本周完成

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
        labels: ['week 1', 'week 2', 'week 3', 'week 4', 'week 5', 'week 6', 'week 7'],
        datasets: [{
            label: 'wewe',
            backgroundColor: chartColors.blue,
            borderColor: chartColors.blue,
            fill: false,
            data: [undefined, undefined, undefined, undefined, 0, 60, 80]
        },{
            label: 'open source jobs',
            backgroundColor: chartColors.red,
            borderColor: chartColors.red,
            fill: false,
            data: [39, 60, 62, 80, 101, 105, 109]
        },{
            label: 'tomato-pie',
            backgroundColor: chartColors.orange,
            borderColor: chartColors.orange,
            fill: false,
            data: [653, 673, 722, 634, 647, 705, 681]
        },{
            label: 'star-history 插件',
            backgroundColor: chartColors.green, 
            borderColor: chartColors.green,
            fill: false,
            data: [21, 21, 28, 33, 33, 34, 39]
        }]
    },
});

new Chart(starCtx, {
    type: 'line',
    data: {
        labels: ['week 1', 'week 2', 'week 3', 'week 4', 'week 5', 'week 6', 'week 7'],
        datasets: [{
            label: 'wewe',
            backgroundColor: chartColors.blue,
            borderColor: chartColors.blue,
            fill: false,
            data: [undefined, undefined, undefined, undefined, 0, 11, 33]
        },{
            label: 'open source jobs',
            backgroundColor: chartColors.red,
            borderColor: chartColors.red,
            fill: false,
            data: [731, 764, 763, 821, 872, 891, 898]
        },{
            label: 'tomato-pie',
            backgroundColor: chartColors.orange,
            borderColor: chartColors.orange,
            fill: false,
            data: [107, 113, 117, 118, 125, 126, 128]
        },{
            label: 'star-history 插件',
            backgroundColor: chartColors.green, 
            borderColor: chartColors.green,
            fill: false,
            data: [921, 998, 1110, 1129, 1154, 1178, 1190]
        }]
    },
});

new Chart(incomeCtx, {
    type: 'line',
    data: {
        labels: ['week 1', 'week 2', 'week 3', 'week 4', 'week 5', 'week 6', 'week 7'],
        datasets: [{
            label: 'wewe',
            backgroundColor: chartColors.blue,
            borderColor: chartColors.blue,
            fill: false,
            data: [undefined, undefined, undefined, undefined, 0, 0, 0]
        },{
            label: 'open opptunities',
            backgroundColor: chartColors.red,
            borderColor: chartColors.red,
            fill: false,
            data: [0, 0, 0, 0, 0, 0, 0]
        },{
            label: 'tomato-pie',
            backgroundColor: chartColors.orange,
            borderColor: chartColors.orange,
            fill: false,
            data: [0, 0, 0, 0, 0, 0, 0]
        },{
            label: 'star-history 插件',
            backgroundColor: chartColors.green, 
            borderColor: chartColors.green,
            fill: false,
            data: [0.69, 0, 25.7, 12.8, 0, 2/7*30, 1/7*30]
        }]
    },
});

</script>