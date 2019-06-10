---
title: 我的透明创业实验 - 第四周
description: 探究一个机灵程度中上的普通人, 给他一年时间让他自由创造, 是否有可能获得1000美元每月的被动收入.
---

<blockquote class="twitter-tweet" data-lang="en"><p lang="en" dir="ltr">Before getting your hands dirty with code. Find people who might be future customers and get their feedback on your idea first.</p>&mdash; timqian (@Tim_Qian) <a href="https://twitter.com/Tim_Qian/status/1137879896296812544?ref_src=twsrc%5Etfw">June 10, 2019</a></blockquote>
<script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

Hello world, 我是 timqian, 正在进行为期一年的透明创业实验. 这是关于这个实验第三周的实验记录.

记录主要分成 4 部分
1. 上周实验内容
2. 本周实验计划
3. 产品数据分享
4. 你的评论

## 上周实验内容

### Product related

#### [open-source-jobs](https://github.com/t9tio/open-source-jobs)

- 拿掉了 help-wanted 入口, 专心做开源相关招聘站.
- 写了一篇[关于网站技术选择的博客](./tech-stack-of-open-source-jobs.md), 谈谈为什么选择 serverless, react 以及 serverside rendering
- 产品暂时进入稳定阶段, 停止更新时间, 看看项目自己会不会成长. 因为是 serverless 方式开发, 没有维护成本, 对于这种有可能需要长时间积累用户量的应用十分合适

#### [wewe](https://github.com/t9tio/wewe)

wewe 的主要功能是把微信(之后还可以是其他的)群消息同步到互联网, 现在还在制作当中.
值得说两句的是, wewe 做到一半时纠结在了要不要继续做的考虑之中, 效率很低, 以至于上周懈怠了将近3天时间. 一开始感觉这事儿肯定有价值, 把互联网上原本没有的信息带了过去, 于是没有经过太多考虑就动手了, 到中途开始怀疑起来, 虽然肯定有价值, 但这玩意儿最终有可能盈利吗? 除了我之外是否有其他人需要呢? 这问题在一开始没考虑清楚, 在产品制作过程中一但遇到一点麻烦, 就容易动摇, 后悔一开始没有对这个想法做足够的验证和市场调查. 现在回想一下, 之前做的一些产品, 都没有系统得经过想法验证和市场调查, 自己感觉有可能有用就动手了, 产品成功与否大概率是运气成分决定的. 之后在这方面需要一点改进.

#### 于是关于 wewe 做了以下一些事 (还不够)

#### 调查是否有人需要
- 和[题叶](http://tiye.me/)聊了下这个想法,  (题叶有挺多技术社区的创建, 维护经验, 创建了 react china, 前 cnodejs 社区管理员等, 并且是很多技术微信群的群主) 
  - 他觉得有价值, 但只是记录消息历史可能不是那么有用, 如果话题抽取做的比较好会比较有价值
  - 从他那儿得知 clojure 社区[也在做类似的事情(slack 消息公开到互联网)](https://clojureverse.org/t/replacing-the-clojurians-slack-log/1614)

#### 总结可以提供的价值
- 更仔细的思考了 wewe 可以提供的价值
  - 在一个地方记录了群聊里的信息, 群外人也可以看到
  - 聊天历史的查询
  - 可以被搜索引擎搜到
  - 聊天内容的分析(词频, 趋势等)
  - 话题抽取,便于搜索
  - 可以在 wewe 上进行群直播, 类似 知乎 live; 各种群/论坛的 AMA;

#### 现在是否有类似工具
- 一个用的人比较多的微信聊天记录到处工具: https://zhuanlan.zhihu.com/p/32511173
- [clojure 社区 slack 群消息公开工具)](https://clojureverse.org/t/replacing-the-clojurians-slack-log/1614)

#### 盈利模式
- 其他地方没有的信息 => 访问量 => 广告
- 赞助
- 高级功能收费(群消息导出等)
- 如果可能, 可以以这个项目为起点, 做自己的群聊应用, 想象力就比较大了

### Marketing related

[写了一篇博客关于 open-source-jobs 的技术选择和源码分享](./tech-stack-of-open-source-jobs.md), 发到了 v2ex, cnodejs, ruby-china, juejin, 为 open-source-jobs 人为的带来了一些流量

![](https://raw.githubusercontent.com/timqian/images/master/Screen%20Shot%202019-06-10%20at%209.24.49%20AM.png)
(traffic on github repo)


## 本周计划

- 完成 wewe 的 MVP 并发布
- 完成一篇透明创业实验第一个月的总结博客并发布
  - 在那篇博客里**调研读者最喜欢的订阅博客的方式**
[![](https://api.gh-polls.com/poll/01DCZDSAQW3S4HS0K0S5WQSRKK/email)](https://api.gh-polls.com/poll/01DCZDSAQW3S4HS0K0S5WQSRKK/email/vote)
[![](https://api.gh-polls.com/poll/01DCZDSAQW3S4HS0K0S5WQSRKK/RSS)](https://api.gh-polls.com/poll/01DCZDSAQW3S4HS0K0S5WQSRKK/RSS/vote)
[![](https://api.gh-polls.com/poll/01DCZDSAQW3S4HS0K0S5WQSRKK/twitter)](https://api.gh-polls.com/poll/01DCZDSAQW3S4HS0K0S5WQSRKK/twitter/vote)
[![](https://api.gh-polls.com/poll/01DCZDSAQW3S4HS0K0S5WQSRKK/wechat)](https://api.gh-polls.com/poll/01DCZDSAQW3S4HS0K0S5WQSRKK/wechat/vote)

## 数据分享

### 用户量
<canvas id="userChart"></canvas>

### github star 数
<canvas id="starChart"></canvas>

### 平均每月被动收入(本周收入 / 7 * 30)
<canvas id="incomeChart"></canvas>

<br/>

> [帮助我改进这篇文章](https://github.com/t9tio/blog/blob/master/source/_posts/t9t-week4.md)

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
        labels: ['week 1', 'week 2', 'week 3', 'week 4'],
        datasets: [{
            label: 'open source jobs',
            backgroundColor: chartColors.red,
            borderColor: chartColors.red,
            fill: false,
            data: [39, 60, 62, 80]
        },{
            label: 'tomato-pie',
            backgroundColor: chartColors.orange,
            borderColor: chartColors.orange,
            fill: false,
            data: [653, 673, 722, 634]
        },{
            label: 'star-history 插件',
            backgroundColor: chartColors.green, 
            borderColor: chartColors.green,
            fill: false,
            data: [21, 21, 28, 33]
        }]
    },
});

new Chart(starCtx, {
    type: 'line',
    data: {
        labels: ['week 1', 'week 2', 'week 3', 'week 4'],
        datasets: [{
            label: 'open source jobs',
            backgroundColor: chartColors.red,
            borderColor: chartColors.red,
            fill: false,
            data: [731, 764, 763, 821]
        },{
            label: 'tomato-pie',
            backgroundColor: chartColors.orange,
            borderColor: chartColors.orange,
            fill: false,
            data: [107, 113, 117, 118]
        },{
            label: 'star-history 插件',
            backgroundColor: chartColors.green, 
            borderColor: chartColors.green,
            fill: false,
            data: [921, 998, 1110, 1129]
        }]
    },
});

new Chart(incomeCtx, {
    type: 'line',
    data: {
        labels: ['week 1', 'week 2', 'week 3', 'week 4'],
        datasets: [{
            label: 'open opptunities',
            backgroundColor: chartColors.red,
            borderColor: chartColors.red,
            fill: false,
            data: [0, 0, 0, 0]
        },{
            label: 'tomato-pie',
            backgroundColor: chartColors.orange,
            borderColor: chartColors.orange,
            fill: false,
            data: [0, 0, 0, 0]
        },{
            label: 'star-history 插件',
            backgroundColor: chartColors.green, 
            borderColor: chartColors.green,
            fill: false,
            data: [0.69, 0, 25.7, 12.8]
        }]
    },
});

</script>