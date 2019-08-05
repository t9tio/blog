---
title: 惨淡的发布现场, 网络讨饭和接外包, 我的透明创业实验 - 第十二周
# description: what's your problem? what can I do for you
date: 2019-08-05
---

Hello world, 我是 [timqian](https://github.com/timqian), 正在进行为期一年的[透明创业实验](https://blog.t9t.io/transparent-startup-experiment-2019-05-20/). 这是关于这个实验第十二周的实验记录.

## 做了啥

- 在不同平台发布了 [wewe](https://wewe.t9t.io), 效果比较惨淡, 只有零星几个点赞, 没有增加新的用户. 不过之后会持续在新增大功能时做持续的发布. (自勉: 无意中看到 [TJ](https://github.com/tj) 的 [HN submissions](https://news.ycombinator.com/submitted?id=tjholowaychuk). 就连 [mocha](https://news.ycombinator.com/item?id=3271903) 现在这么出名的项目, 当初他发在 HN 都没有收到关注. Keep moving)
- 借鉴 evanyou.me 更新了 timqian.com
- 在 timqian.com & github & hackernews 实验性得放出了接活的报价: https://news.ycombinator.com/item?id=20585097, 一年之后如果产品不能养活自己, 接外包也是除了找工作之外的一个选择
- 前段时间注册的 patreon.com/timqian 获得了第一笔每月一美元捐助🎉
- 继续在做从 json 生成网页的工具, 暂时为自己所用, 用来生成自己产品的一些 landing page.
- 更新了 t9t.io 主页(由 json2site 生成)
- 看到这个[项目](https://github.com/imkevinxu/xkcdgraphs) 想做一个手绘风格的 chart 库, 找了一圈没发现有人做, 感觉挺有意义的, 先做起来了

|     | plan | 评价 |
| --- | --- | --- |
| 周一 | share wewe on different places; json2site;   |    |
| 周二 | json2site |  完成   |
| 周三 | json2site generate t9t.io page  |    |
| 周四 | xkcd graph lib |  |
| 周五 | xkcd graph lib |  |


> 附: 发布 wewe 的车祸的现场
  - https://news.ycombinator.com/item?id=20551336
  - https://www.reddit.com/r/programming/comments/cj5th1/wewe_open_slackwechat_group_to_the_internet/
  - https://juejin.im/post/5d3e71cee51d45775f516b72
  - https://ruby-china.org/topics/38882
  - https://cnodejs.org/topic/5d3e7286b4725a628e26953d

## 本周目标

- 大致完成手绘风格图表库 [chart.xkcd](https://github.com/timqian/chart.xkcd)

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
        labels: ['week 1', 'week 2', 'week 3', 'week 4', 'week 5', 'week 6', 'week 7', 'week 8', 'week 9', 'week 10', 'week 11', 'week 12'],
        datasets: [{
            label: 'wewe',
            backgroundColor: chartColors.blue,
            borderColor: chartColors.blue,
            fill: false,
            data: [undefined, undefined, undefined, undefined, 0, 60, 80, 91, 95, 95, 103, 103]
        },{
            label: 'open source jobs',
            backgroundColor: chartColors.red,
            borderColor: chartColors.red,
            fill: false,
            data: [39, 60, 62, 80, 101, 105, 109, 111, 113, 114, 119, 121]
        },{
            label: 'tomato-pie',
            backgroundColor: chartColors.orange,
            borderColor: chartColors.orange,
            fill: false,
            data: [653, 673, 722, 634, 647, 705, 681, 714, 712, 733, 774, 779]
        },{
            label: 'star-history 插件',
            backgroundColor: chartColors.green,
            borderColor: chartColors.green,
            fill: false,
            data: [21, 21, 28, 33, 33, 34, 39, 38, 40, 47, 48, 50]
        }]
    },
});

new Chart(starCtx, {
    type: 'line',
    data: {
        labels: ['week 1', 'week 2', 'week 3', 'week 4', 'week 5', 'week 6', 'week 7', 'week 8', 'week 9', 'week 10', 'week 11', 'week 12'],
        datasets: [{
            label: 'wewe',
            backgroundColor: chartColors.blue,
            borderColor: chartColors.blue,
            fill: false,
            data: [undefined, undefined, undefined, undefined, 0, 11, 33, 57, 70, 77, 78, 102]
        },{
            label: 'open source jobs',
            backgroundColor: chartColors.red,
            borderColor: chartColors.red,
            fill: false,
            data: [731, 764, 763, 821, 872, 891, 898, 903, 934, 940, 956, 962]
        },{
            label: 'tomato-pie',
            backgroundColor: chartColors.orange,
            borderColor: chartColors.orange,
            fill: false,
            data: [107, 113, 117, 118, 125, 126, 128, 129, 134, 134, 136, 136]
        },{
            label: 'star-history 插件',
            backgroundColor: chartColors.green, 
            borderColor: chartColors.green,
            fill: false,
            data: [921, 998, 1110, 1129, 1154, 1178, 1190, 1216, 1238, 1246, 1276, 1291]
        }]
    },
});

new Chart(incomeCtx, {
    type: 'line',
    data: {
        labels: ['week 1', 'week 2', 'week 3', 'week 4', 'week 5', 'week 6', 'week 7', 'week 8', 'week 9', 'week 10', 'week 11', 'week 12'],
        datasets: [{
            label: 'star-history 插件',
            backgroundColor: chartColors.green,
            borderColor: chartColors.green,
            fill: false,
            data: [0.69, 0, 25.7, 12.8, 0, 2/7*30, 1/7*30, 1/7*30, 2/7*30, 2/7*30, 1/7*30, 4/7*30]
        }, {
            label: 'patron',
            backgroundColor: chartColors.purple,
            borderColor: chartColors.purple,
            fill: false,
            data: [undefined, undefined, undefined, undefined,undefined, undefined, undefined, undefined,undefined, undefined, undefined, 1]
        }]
    },
});

</script>

