---
title: 我的透明创业实验 - 第二周
description: 探究一个机灵程度中上的普通人, 给他一年时间让他自由创造, 是否有可能获得1000美元每月的被动收入. 
date: 2019-05-27
---
> 去人们在寻找解决方案的地方分享产品

Hello world, 我是 timqian, 正在进行为期一年的透明创业实验. 这是关于这个实验第二周的实验记录.

记录主要分成 4 部分
1. 上周实验内容
2. 本周实验计划
3. 产品数据分享
4. 你的评论

## 上周实验内容

### 产品方面

本周主要是在做 Open Opportunities 的 [help-wanted](https://oo.t9t.io/help-wanted) 板块.

- Open Opportunities
  - 完成了 Open Opportunities 的 [help-wanted](https://oo.t9t.io/help-wanted) 板块: 
    - 选择了一批著名开源项目, 利用 github 的 API 拿到他们 tag 为 `help wanted` 的 issue
    - 一个展示/筛选 issue 的页面
    - 用户推荐开源项目到这个产品
  - 粗糙的搭建了 Open Opportunities 的主页: [oo.t9t.io](https://oo.t9t.io)
  - 为了给注册用户发通知邮件, 在 AWS 上申请启用了新的邮箱地址 [timqian@t9t.io](), 之后准备用这个作为主要邮箱
  - 给 Open Opportunities 加入了 Google Analytics
- 给博客加入了 disqus 评论

### 推广方面

#### Blog

写了 [我的透明创业实验](https://blog.t9t.io/transparent-startup-experiment-2019-05-20/) 这篇博客, 在4个技术论坛分享了博客链接
  - [v2ex](https://www.v2ex.com/t/565771): 3063 次浏览
  - [cnode](https://cnodejs.org/topic/5ce2287e518e0954fc40fc1f): 930 次浏览
  - [rubychina](https://ruby-china.org/topics/38553): 865 次阅读
  - [juejin](https://juejin.im/user/57d99d01bf22ec0058f57262): 看不到统计信息, 也没有评论, 可能没有什么浏览

这篇文章出乎意料的得到了许多共鸣, 也反映在了我的社交账号数据的变化上

- blog 总阅读数(Google Analytics 统计): 2100 左右
- twitter follower: 上周 38 -> 今天 74
- wechat t9tio community: 上周 16 -> 今天 179
- github follower: 上周 207 -> 今天 310

#### help-wanted

试验性得把 [help-wanted](https://oo.t9t.io/help-wanted) 分享到两个地方看看大家有没有需求

- [HN](https://news.ycombinator.com/item?id=19977483): 10 points; 在 Show HN 停留了 2 天;
- [v2ex](https://www.v2ex.com/t/566571): (置顶过一次) 751 views; 1 reply;

大概有不到 5 个人因为这个功能而注册 (目前总注册用户 60 人), 似乎 help-wanted 不是一个很大的需求, 而且和 open-source-jobs 放在一起组成一个产品, 让 open-source-jobs 变得不专注. 我在考虑是否应该删掉这个模块, 专注做 open-soure-jobs. 不知道你怎么看, 欢迎投票和评论: 
[![](https://api.gh-polls.com/poll/01DBVF18HG1JS26Q1EJAQY11TN/%E5%88%A0%E6%8E%89%20help-wanted%20%E6%9D%BF%E5%9D%97%2C%20%E4%B8%93%E6%B3%A8%E5%81%9A%20open-source-jobs)](https://api.gh-polls.com/poll/01DBVF18HG1JS26Q1EJAQY11TN/%E5%88%A0%E6%8E%89%20help-wanted%20%E6%9D%BF%E5%9D%97%2C%20%E4%B8%93%E6%B3%A8%E5%81%9A%20open-source-jobs/vote)

<a href="https://api.gh-polls.com/poll/01DBVEYCFVEBD4XA9EHJ2311E8/%E4%BF%9D%E7%95%99%20help-wanted%20%E6%9D%BF%E5%9D%97%2C%20%E8%99%BD%E7%84%B6%E4%B8%8D%E5%A4%9A%E4%BD%86%E8%BF%98%E6%98%AF%E6%9C%89%E4%B8%80%E5%AE%9A%E5%BC%95%E6%B5%81%E5%8A%9F%E8%83%BD/vote"><img src="https://api.gh-polls.com/poll/01DBVEYCFVEBD4XA9EHJ2311E8/%E4%BF%9D%E7%95%99%20help-wanted%20%E6%9D%BF%E5%9D%97%2C%20%E8%99%BD%E7%84%B6%E4%B8%8D%E5%A4%9A%E4%BD%86%E8%BF%98%E6%98%AF%E6%9C%89%E4%B8%80%E5%AE%9A%E5%BC%95%E6%B5%81%E5%8A%9F%E8%83%BD" alt=""></a></p>

#### Open source jobs

给 16 个有 twitter 账号的 [open company](https://oo.t9t.io/organizations) 发私信询问是否需要到 [open-source-jobs](https://oo.t9t.io/jobs) 发工作链接.
获得了 2 个账号的回应, 一个感谢, 一个说 feel free to post their jobs.
总之, 对于目前这个没有太多访问量和用户量的 open-source-jobs, 可以理解这些组织自己来发招聘帖的动机是很弱的.

#### star-history

[star-history](https://github.com/timqian/star-history) 在群聊时意外得到 [@egoist](https://github.com/egoist) 点赞, 让本来需要一个月左右才能到达 1k star 的 star-history 在一周之内增加到了 998 个 star, 预计这周会破 1k, 找到了对 star-history 的 chrome 插件进行打折促销的机会.


## 本周计划

### 产品方面

本周重心仍然放在 [oo.t9t.io](https://oo.t9t.io)

- [ ] 对 open source jobs 做转型, 从让这些组织自发来分享工作机会, 变成一个收集全网 open source jobs 的工具, 积累用户和知名度为先
- [ ] open-opptunities 删掉 help-wanted 板块, 专注做“找开源工作”这一点
- [ ] 完成付费置顶功能, 即使展示没有用, 也让这个产品形成从使用到付费的闭环.
- [ ] 完成用邮件通知注册用户工作机会的功能

其他一些事情:

- [ ] 博客的 rss
- [ ] tomato-pie 的一些完善

### 推广方面

- [ ] 完善 open-source-jobs 之后, 以收集全网开源工作机会为卖点, 中英文各一篇博客发到所有能发的地方
- [ ] star-history 打折促销活动

## 数据分享

### 用户量
<canvas id="userChart"></canvas>

### github star 数
<canvas id="starChart"></canvas>

### 平均每月被动收入
<canvas id="incomeChart"></canvas>




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
        labels: ['week 1', 'week 2'],
        datasets: [{
            label: 'open opptunities',
            backgroundColor: chartColors.red,
            borderColor: chartColors.red,
            fill: false,
            data: [39, 60]
        },{
            label: 'tomato-pie',
            backgroundColor: chartColors.orange,
            borderColor: chartColors.orange,
            fill: false,
            data: [653, 673]
        },{
            label: 'star-history 插件',
            backgroundColor: chartColors.green, 
            borderColor: chartColors.green,
            fill: false,
            data: [21, 21]
        }]
    },
});

new Chart(starCtx, {
    type: 'line',
    data: {
        labels: ['week 1', 'week 2'],
        datasets: [{
            label: 'open opptunities',
            backgroundColor: chartColors.red,
            borderColor: chartColors.red,
            fill: false,
            data: [731, 764]
        },{
            label: 'tomato-pie',
            backgroundColor: chartColors.orange,
            borderColor: chartColors.orange,
            fill: false,
            data: [107, 113]
        },{
            label: 'star-history 插件',
            backgroundColor: chartColors.green, 
            borderColor: chartColors.green,
            fill: false,
            data: [921, 998]
        }]
    },
});

new Chart(incomeCtx, {
    type: 'line',
    data: {
        labels: ['week 1', 'week 2'],
        datasets: [{
            label: 'open opptunities',
            backgroundColor: chartColors.red,
            borderColor: chartColors.red,
            fill: false,
            data: [0, 0]
        },{
            label: 'tomato-pie',
            backgroundColor: chartColors.orange,
            borderColor: chartColors.orange,
            fill: false,
            data: [0, 0]
        },{
            label: 'star-history 插件',
            backgroundColor: chartColors.green, 
            borderColor: chartColors.green,
            fill: false,
            data: [0.69, 0]
        }]
    },
});

</script>