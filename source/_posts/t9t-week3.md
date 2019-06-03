---
title: 我的透明创业实验 - 第三周
description: 探究一个机灵程度中上的普通人, 给他一年时间让他自由创造, 是否有可能获得1000美元每月的被动收入. 
date: 2019-06-03
---

> The way to succeed in a startup is not to be an expert on startups, but to be an expert on your users and the problem you're solving for them. -- [Paul Graham](http://www.paulgraham.com/before.html)

Hello world, 我是 timqian, 正在进行为期一年的透明创业实验. 这是关于这个实验第三周的实验记录.

记录主要分成 4 部分
1. 上周实验内容
2. 本周实验计划
3. 产品数据分享
4. 你的评论

## 上周实验内容

### 产品方面

#### 关于 open source jobs

[open source jobs](https://github.com/t9tio/open-source-jobs) 稍微整理了下准备让它进入稳定期了, 目前看来想要从这个细分招聘领域挣到钱还是比较困难, 但留着这个项目埋下伏笔, 期待开源蒸蒸日上, 未来有越来越多的软件公司以开源方式运作, 越来越多人想要从事这方面工作. 

<details>
<summary>比较凌乱的思考细节</summary>
open-source-jobs 是开始实验的这几周所花时间最多的项目, 它的起源是大概一两个月之前收集了一张 *在招聘工程师的开源项目列表*. 意外在 [Reddit]() 得到了很多认同, 然后又看到一些小众招聘网站做的不错, 什么[瑞士码农招聘(链接找不到了)]() 之类, 做的还可以. 
我就在想, open-source-jobs 这个细分找工作市场, 总归比*瑞士码农招聘* 稍微更大众一些, 于是就想着做一个类似网站, 希望有许多人注册, 比较大的访问量. 然后那些开源组织就会想要来投放招聘广告.
于是投入了应该有 3 周时间, 做了网站. 然后还做一个 [help-wanted](https://oo.t9t.io/help-wanted) 板块, 收集 github 上 "help-wanted" tagged issue. 想着可以引流. 但是其实这个需求不是那么足, 起不到引流的作用, 反而让我不能再把这个项目称做 open-source-jobs, 换成了一个拗口, 并且不太容易通过搜索引擎搜到的名字: "open-opptunities".
所以最后我决定, 把 open-source-jobs 又改回了这个名字, 一会儿准备把 readme 也变回最初的模样: 直接列出提供工作机会的开源项目. 以最直接的方式提供用户价值. 

最后, 也发现了有人在[做类似的工作](https://www.fossjobs.net/) 已经做了有段时间, 一直只是一个未能盈利的 side project, 间接表明这个市场目前想挣到钱还是比较困难.

- 访问量不是一蹴而就的, 要有耐心
- brand 是很重要的, 从 open-source-jobs 改名为 open-opptunities, 就少了一个很重要的流量渠道: 搜索引擎, 原来 open source jobs 一下子就可以搜到, 现在搜 open opptunities, 这个词太大众了, 翻几页也找不到你的项目

</details>

### 新项目 [wewe](https://github.com/t9tio/wewe)

这周开始了一个新的项目 wewe, 主要功能是把微信(之后还可以是其他的)群消息同步到互联网, 现在还在制作当中, 具体思考可见这篇[还是草稿的博客](/drafts/wewe.html)

### 推广方面

[star-history](https://star-history.t9t.io) 庆祝 1k star, 打折促销

![](https://raw.githubusercontent.com/timqian/images/master/Screen%20Shot%202019-06-03%20at%203.01.25%20PM.png)

在以下潜在用户所在的地方进行了分享

[Hackernews](https://news.ycombinator.com/item?id=20020249); [Reddit](https://www.reddit.com/r/programming/comments/btjag9/starhistory_the_missing_star_history_graph_of/); [Product Hunt](https://www.producthunt.com/posts/star-history); [v2ex](https://www.v2ex.com/t/568062); [cnode](https://cnodejs.org/topic/5ceb95f54036f24194cf6e8e); [rubychina](https://ruby-china.org/topics/38574); [ruanyf weekly](https://github.com/ruanyf/weekly/issues/589)

大多数平台上都没有太多反应, 除了 Product Hunt 得到了 36 个 upvotes, 在[我提交过的产品](https://www.producthunt.com/@tim_qian/submitted)里还算可以.

网站流量相较于平时有一定提升:
![](https://raw.githubusercontent.com/timqian/images/master/Screen%20Shot%202019-06-03%20at%202.30.52%20PM.png)

新卖出去 6 份:
![](https://raw.githubusercontent.com/timqian/images/master/Screen%20Shot%202019-06-03%20at%2010.23.55%20AM.png)

看 github 和 google analytics 上的流量来源, 主要还是老用户的访问和谷歌搜索. 

一个结论是不要把产品的发布看得太重, 产品想要成功最重要的还是用户需要它. 发这些帖子功能不是那么强. 不过在这些排名较高的网站上发这些链接还是必要的, 毕竟要让搜索引擎多多找到你的网站, 搜索引擎的权重会参考这些. 

## 本周计划

完成 wewe 的 MVP

## 数据分享

### 用户量
<canvas id="userChart"></canvas>

### github star 数
<canvas id="starChart"></canvas>

### 平均每月被动收入(本周收入 / 7 * 30)
<canvas id="incomeChart"></canvas>

<br/>

> [帮助我改进这篇文章](https://github.com/t9tio/blog/blob/master/source/_posts/t9t-week3.md)

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
        labels: ['week 1', 'week 2', 'week 3'],
        datasets: [{
            label: 'open source jobs',
            backgroundColor: chartColors.red,
            borderColor: chartColors.red,
            fill: false,
            data: [39, 60, 62]
        },{
            label: 'tomato-pie',
            backgroundColor: chartColors.orange,
            borderColor: chartColors.orange,
            fill: false,
            data: [653, 673, 722]
        },{
            label: 'star-history 插件',
            backgroundColor: chartColors.green, 
            borderColor: chartColors.green,
            fill: false,
            data: [21, 21, 28]
        }]
    },
});

new Chart(starCtx, {
    type: 'line',
    data: {
        labels: ['week 1', 'week 2', 'week 3'],
        datasets: [{
            label: 'open source jobs',
            backgroundColor: chartColors.red,
            borderColor: chartColors.red,
            fill: false,
            data: [731, 764, 763]
        },{
            label: 'tomato-pie',
            backgroundColor: chartColors.orange,
            borderColor: chartColors.orange,
            fill: false,
            data: [107, 113, 117]
        },{
            label: 'star-history 插件',
            backgroundColor: chartColors.green, 
            borderColor: chartColors.green,
            fill: false,
            data: [921, 998, 1110]
        }]
    },
});

new Chart(incomeCtx, {
    type: 'line',
    data: {
        labels: ['week 1', 'week 2', 'week 3'],
        datasets: [{
            label: 'open opptunities',
            backgroundColor: chartColors.red,
            borderColor: chartColors.red,
            fill: false,
            data: [0, 0, 0]
        },{
            label: 'tomato-pie',
            backgroundColor: chartColors.orange,
            borderColor: chartColors.orange,
            fill: false,
            data: [0, 0, 0]
        },{
            label: 'star-history 插件',
            backgroundColor: chartColors.green, 
            borderColor: chartColors.green,
            fill: false,
            data: [0.69, 0, 5.88]
        }]
    },
});

</script>