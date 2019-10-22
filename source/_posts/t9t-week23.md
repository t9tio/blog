---
title: 年中总结? - 我的透明创业实验第二十三周
# description:
date: 2019-10-21
---

Hello world, 我是 [timqian](https://github.com/timqian), 正在进行为期一年的[透明创业实验](https://blog.t9t.io/transparent-startup-experiment-2019-05-20/). 这是关于这个实验第二十三周的实验记录.

透明创业实验的第一篇博客写于 5 月 20 日, 仿佛昨天才开始独立开发, 但事实上一转眼已经快半年了... time flies...


## 我做了些什么?

在上周做完 [Repo Analytics](http://repo-analytics.github.io) 的第一版之后, 现在手头有 5 个项目我都想要维护和改进. 同时又想做很多新东西. 坦白讲开始觉得摊子铺太大了😅 原来觉得用 serverless 方式开发, 省去了维护服务器的麻烦. 但真正有很多产品要维护的时候才发现, 想要做出符合用户期待并愿意为之付费的产品, 维护服务器的成本相对于产品改进所需要的成本来讲不值一提.

- [Repo Analytics](http://repo-analytics.github.io) - analytics for your GitHub repos
- [chart.xkcd](https://github.com/timqian/chart.xkcd) - xkcd styled chart lib
- [Tomato Pie](https://github.com/t9tio/tomato-pie) - A new UI for Pomodoro Technique.
- [Open source jobs](https://github.com/t9tio/open-source-jobs) - A list of Open Source projects offering jobs.
- [wewe](https://github.com/t9tio/wewe) - Open group chat to the world

## 收入怎么样?

可以从看到文尾的收入情况图看出来, 除了因为以上项目获得的一些捐助和开始这个实验之前做的 [star-history](https://github.com/timqian/star-history) 少量的销售量, 每月收入很少且不稳定. 主要原因是上面这些项目不够 polished, 我还没有自信对他们收费. 接下来需要做的是花时间完善他们和加入收费渠道.

## 我学到了什么?

- 独立开发一个广受欢迎并且可以养活自己的产品真的很难, 在 producthunt, HN, v2ex, 你每天都可以看到上百个雄心勃勃的新产品发布. 我真的可以吗? 每天问自己最多的就是这个问题.
- 对“工作”的新的认识
  就像我在透明创业实验的第一篇博客里所说, 在开始这段经历之前, 我把工作看是一个用劳动力和时间换取生存资本的活动. 经过这段时间的独立开发, 让我认识到加入一家优秀的组织的意义 - 一个抱大腿的机会. 一个优秀的公司, 如果因为自己的产品已经足够有价值以至于养活这个公司和里面的员工. 说明这个产品的价值, 完成度, 受众都远远好过目前我做的任何一个. 加入一个自己认可的公司, 在它身上有很多可以学习的地方.
- 对自己的认识
  我的缺点是改进老项目的动力没有做新东西足. 但是改进一个产品和做新东西一样重要. 二者其实基于同一个目的, 给别人带去一些价值/便利/愉悦. 对目前的我而言, 做产品最大的意义在于是否真正帮助了用户. 做新项目像是探索新的帮助他们的可能, 而优化老项目是切切实实的更好的帮助了用户.

## 接下来的 7 个月, 我应当如何度过?

- 放平心态和期待, 享受这段旅程
- 每天抽时间优化老项目, 完善功能, 增加收费渠道
- 多关注和别人合作的机会 - 市面上最成功的产品大多不是独立开发出来的, 不能忽视合作开发的能力
- 锻炼自己的能力
  - 写作能力
  - 学习增长黑客的一些手段
  - 提升开发速度和质量
  - 基础知识
- 开始逐渐留意自己欣赏的团队和产品. 如果实验失败, 找一个靠谱团队加入

## 数据分享

> 产品详情可以访问 [t9t.io](https://t9t.io) 查看

### 平均每月被动收入($)(本周收入 / 7 * 30)

<svg id="incomeChart"></svg>

### 用户量
<svg id="userChart"></svg>

<br/>

> [帮助我改进这篇文章](https://github.com/t9tio/blog/blob/master/source/_posts/t9t-week23.md)

<script src="https://cdn.jsdelivr.net/npm/chart.xkcd@1.1.3/dist/chart.xkcd.min.js"></script>

<script>
var incomesvg = document.getElementById('incomeChart');
var usersvg = document.getElementById('userChart');


new chartXkcd.XY(incomesvg, {
  xLabel: 'weeks',
  data: {
    datasets: [{
        label: 'star-history',
        data: [{x:0,y:0.69},{x:1,y:0},{x:2,y:25.7},{x:3,y:12.8},{x:4,y:0},{x:5,y:8.571428571428571},{x:6,y:4.285714285714286},{x:7,y:4.285714285714286},{x:8,y:8.571428571428571},{x:9,y:8.571428571428571},{x:10,y:4.285714285714286},{x:11,y:17.142857142857142},{x:12,y:8.571428571428571},{x:13,y:3/7*30},{x:14,y:1/7*30},{x:15,y:3/7*30},{x:16,y:2/7*30},{x:17,y:0},{x:18,y:3/7*30},{x:21,y:1/7*30},{x:22,y:2/7*30}]
    }, {
        label: 'patron',
        data: [{x:10,y:0},{x:11,y:1},{x:12,y:1},{x:13,y:2},{x:14,y:8},{x:15,y:8},{x:16,y:9},{x:17,y:10},{x:18,y:10},{x:21,y:9},{x:22,y:9}]
    }]
  },
  options: {
    showLine: true,
    dotSize: 0.5,
    xTickCount: 5,
  },
});

new chartXkcd.XY(usersvg, {
  xLabel: 'weeks',
  data: {
      datasets: [{
          label: 'repo-analytics',
          data: [{x:21,y:0}, {x:22,y:69}]
      },{
          label: 'wewe',
          data: [{x:3,y:0},{x:4,y:60},{x:5,y:80},{x:6,y:91},{x:7,y:95},{x:8,y:95},{x:9,y:103},{x:10,y:103},{x:11,y:103},{x:12,y:103},{x:13,y:103},{x:14,y:103},{x:15,y:103},{x:16,y:108},{x:16,y:108},{x:17,y:111},{x:18,y:111},{x:21,y:127},{x:22,y:128}]
      },{
          label: 'open source jobs',
          data: [{x:0,y:39},{x:1,y:60},{x:2,y:62},{x:3,y:80},{x:4,y:101},{x:5,y:105},{x:6,y:109},{x:7,y:111},{x:8,y:113},{x:9,y:114},{x:10,y:119},{x:11,y:121},{x:12,y:122},{x:13,y:123},{x:14,y:123},{x:15,y:127},{x:16,y:131},{x:17,y:132},{x:18,y:133},{x:21,y:139},{x:22,y:140}]
      },{
          label: 'tomato-pie',
          data: [{x:0,y:653},{x:1,y:673},{x:2,y:722},{x:3,y:634},{x:4,y:647},{x:5,y:705},{x:6,y:681},{x:7,y:714},{x:8,y:712},{x:9,y:733},{x:10,y:774},{x:11,y:779},{x:12,y:801},{x:13,y:821},{x:14,y:898},{x:15,y:911},{x:16,y:981},{x:17,y:917},{x:18,y:920},{x:21,y:875},{x:22,y:904}]
      },{
          label: 'star-history',
          data: [{x:0,y:21},{x:1,y:21},{x:2,y:28},{x:3,y:33},{x:4,y:33},{x:5,y:34},{x:6,y:39},{x:7,y:38},{x:8,y:40},{x:9,y:47},{x:10,y:48},{x:11,y:50},{x:12,y:61},{x:13,y:58},{x:14,y:55},{x:15,y:57},{x:16,y:58},{x:17,y:58},{x:18,y:63},{x:21,y:73},{x:22,y:75}]
      },]
  },
  options: {
    showLine: true,
    dotSize: 0.5,
    xTickCount: 5,
  }
});

</script>
