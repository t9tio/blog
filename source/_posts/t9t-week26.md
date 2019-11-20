---
title: 产品从 0 到 1 的法则 - 我的透明创业实验第二十六周
# description:
date: 2019-11-11
---

上周, 久未更新的 [wewe](https://wewe.t9t.io) 迎来了第一个除捐赠以外的客户(虽然收费渠道都还没建好). 截止目前, 我已经做了 5 个有人愿意为之付费的 [MVP](https://en.wikipedia.org/wiki/Minimum_viable_product) 了, 在这篇博客里, 冒昧得谈一谈从 0 到 1 的法则, 作为自己的记录.

> 产品收入情况
- [Repo Analytics](http://repo-analytics.github.io) - 一个每月 1 美金的 [patron](https://www.patreon.com/timqian)
- [chart.xkcd](https://github.com/timqian/chart.xkcd) - 一个每月 5 美金的 [patron](https://www.patreon.com/timqian)
- [Tomato Pie](https://github.com/t9tio/tomato-pie) - 一个每月 1 美金的 [patron](https://www.patreon.com/timqian)
- [Star history Extension](https://chrome.google.com/webstore/detail/star-history/iijibbcdddbhokfepbblglfgdglnccfn) - 总共卖出 65 份, 总收入 100 美金左右
- [wewe](https://github.com/t9tio/wewe) - 一个每月 1.5 美金的 [patron](https://www.patreon.com/timqian), 一个还未付费的每月 5 人民币的用户

## 产品从 0 到 1 的法则

经过这 5 个小工具的经验, 我可以自信的说, 从 0 开始做一个有人愿意为之付费的产品并不是一件遥不可及的事情

下面通过 [Repo Analytics](http://repo-analytics.github.io) 作为例子来看看从 0 到 1 的大概过程

1. 发现问题
> 一个托管于 GitHub 上面的项目, GitHub 只帮你记录了 15 天的访问量, 15 天之前的记录就这样丢了. 可以一直保存着就好了
2. 搜索现有方案, 没有? 做的不够好? 你的机会来了
> 找到两个方案, e.g. [Repo Traffic](https://repotraffic.com). 试用了下发现用不了了.
3. 做出来看看呗, 尽可能简单, 最好一周之内就可以搞定
> 于是做了一个新的网页应用 [Repo Analytics](http://repo-analytics.github.io)
4. 建立用户付费的渠道
> 不一定要做什么付费才能用的功能, 即使是一个捐赠按钮或链接也是可以的, 让喜欢这个工具的人可以付费来支持它. 否则你永远不知道是否有人会付费
5. 分享到有可能有人需要的地方
> 在 `2. 搜索现有方案` 时找到的[有人在问的地方](https://github.com/isaacs/github/issues/399#issuecomment-541497364)
> 一些程序员论坛比如 [HackerNews](https://news.ycombinator.com/item?id=21278767), [v2ex](https://v2ex.com/t/610231#reply6) 等
6. 喝杯咖啡, 散散步, 收集收集反馈. 让用户和时间告诉你这个工具有没有价值

如果你会一点代码, 你可以不断尝试这个过程, 在这个过程中不断提高编码和产品方面的能力. 
每一次尝试的成功率取决于 “问题”, “实现质量”, “运气” 等等因素. 但只要你关注生活, 多次尝试, 相信从 0 到 1 不是难事.

祝你早日找到自己的付费产品.

## 从 1 到 1000 ?

从 1 到 1000, 我自己还没有做到所以也没有什么发言权. 不过在没有做到之前, 我也想谈谈我觉得应该怎么做, 也是一个记录, 多年之后回头看看自己幼稚的观点也挺有意思.

我个人认为从 1 到 1000 最重要的一点是找到你最想做好/最值得做好的那件事. 为什么呢, 因为排除特殊情况, 从 1 到 1000, 你需要持久得专注, 持续得投入精力.

从 0 到 1 做出来的东西，不一定是大多数用户需要的状态，用户会给你反馈，告诉你怎么做可能更好，收集到大量反馈的你，大概率会了解到，这个产品如何改进会更好.

你的重心转变成了如何让产品更好, 如何通过各种方式吸引更多用户.

另一方面，用户的需求不是不变的.

看到你的产品有一定的影响力，也会有人出来和你竞争. 从1到n，这个n越大，你将面临的竞争越大，你收到的反馈越多, 如果你真的想把产品做好, 可能会需要注入越来越多的精力.

- 注重产品的优化
- 注重重复性工作的自动化
- 注重增长

你是否找到了自己愿意为之持续投入精力的产品了呢? 我常常这样问自己, 答案似乎是还没有, 所以我还会继续寻找.

也祝你早日找到自己愿意持续投入的方向.

## 数据分享

> 产品详情可以访问 [t9t.io](https://t9t.io) 查看

### 平均每月被动收入($)(本周收入 / 7 * 30)

<svg id="incomeChart"></svg>

### 用户量
<svg id="userChart"></svg>

<script src="https://cdn.jsdelivr.net/npm/chart.xkcd@1.1.3/dist/chart.xkcd.min.js"></script>

<script>
var incomesvg = document.getElementById('incomeChart');
var usersvg = document.getElementById('userChart');


new chartXkcd.XY(incomesvg, {
  xLabel: 'weeks',
  data: {
    datasets: [{
        label: 'star-history',
        data: [{x:0,y:0.69},{x:1,y:0},{x:2,y:25.7},{x:3,y:12.8},{x:4,y:0},{x:5,y:8.571428571428571},{x:6,y:4.285714285714286},{x:7,y:4.285714285714286},{x:8,y:8.571428571428571},{x:9,y:8.571428571428571},{x:10,y:4.285714285714286},{x:11,y:17.142857142857142},{x:12,y:8.571428571428571},{x:13,y:3/7*30},{x:14,y:1/7*30},{x:15,y:3/7*30},{x:16,y:2/7*30},{x:17,y:0},{x:18,y:3/7*30},{x:21,y:1/7*30},{x:22,y:2/7*30},{x:23,y:3/7*30},{x:24,y:2/7*30},{x:25,y:3/7*30}]
    }, {
        label: 'patron',
        data: [{x:10,y:0},{x:11,y:1},{x:12,y:1},{x:13,y:2},{x:14,y:8},{x:15,y:8},{x:16,y:9},{x:17,y:10},{x:18,y:10},{x:21,y:9},{x:22,y:9},{x:23,y:10},{x:24,y:11},{x:25,y:11}]
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
          data: [{x:21,y:0}, {x:22,y:69},{x:23,y:82},{x:24,y:89},{x:25,y:103}]
      },{
          label: 'wewe',
          data: [{x:3,y:0},{x:4,y:60},{x:5,y:80},{x:6,y:91},{x:7,y:95},{x:8,y:95},{x:9,y:103},{x:10,y:103},{x:11,y:103},{x:12,y:103},{x:13,y:103},{x:14,y:103},{x:15,y:103},{x:16,y:108},{x:16,y:108},{x:17,y:111},{x:18,y:111},{x:21,y:127},{x:22,y:128},{x:23,y:128},{x:24,y:128},{x:25,y:130}]
      },{
          label: 'open source jobs',
          data: [{x:0,y:39},{x:1,y:60},{x:2,y:62},{x:3,y:80},{x:4,y:101},{x:5,y:105},{x:6,y:109},{x:7,y:111},{x:8,y:113},{x:9,y:114},{x:10,y:119},{x:11,y:121},{x:12,y:122},{x:13,y:123},{x:14,y:123},{x:15,y:127},{x:16,y:131},{x:17,y:132},{x:18,y:133},{x:21,y:139},{x:22,y:140},{x:23,y:141},{x:24,y:141},{x:25,y:144}]
      },{
          label: 'tomato-pie',
          data: [{x:0,y:653},{x:1,y:673},{x:2,y:722},{x:3,y:634},{x:4,y:647},{x:5,y:705},{x:6,y:681},{x:7,y:714},{x:8,y:712},{x:9,y:733},{x:10,y:774},{x:11,y:779},{x:12,y:801},{x:13,y:821},{x:14,y:898},{x:15,y:911},{x:16,y:981},{x:17,y:917},{x:18,y:920},{x:21,y:875},{x:22,y:904},{x:23,y:947},{x:24,y:1001},{x:25,y:960}]
      },{
          label: 'star-history',
          data: [{x:0,y:21},{x:1,y:21},{x:2,y:28},{x:3,y:33},{x:4,y:33},{x:5,y:34},{x:6,y:39},{x:7,y:38},{x:8,y:40},{x:9,y:47},{x:10,y:48},{x:11,y:50},{x:12,y:61},{x:13,y:58},{x:14,y:55},{x:15,y:57},{x:16,y:58},{x:17,y:58},{x:18,y:63},{x:21,y:73},{x:22,y:75},{x:23,y:82},{x:24,y:81},{x:25,y:79}]
      },]
  },
  options: {
    showLine: true,
    dotSize: 0.5,
    xTickCount: 5,
  }
});

</script>
