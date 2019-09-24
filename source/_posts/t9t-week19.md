---
title: 我的透明创业实验 - 第十九周
# description: 
date: 2019-09-23
---

Hello world, 我是 [timqian](https://github.com/timqian), 正在进行为期一年的[透明创业实验](https://blog.t9t.io/transparent-startup-experiment-2019-05-20/). 这是关于这个实验第十九周的实验记录.

## 做了啥

继续 [AnaHub](https://github.com/timqian/anahub) (一个无服务,可自行部署的 Google Analytics 替代品), 算是把前端和数据库的格式确定下来了, 希望可以在这周完成 MVP 💪

在使用 [chart.xkcd](https://github.com/timqian/chart.xkcd) 画图过程中发现许多问题待修.

## 手头上同时维护的项目太多怎么办? 更不要说 TODO list 里那些闪闪发亮, 迫不及待, 想要破土而出的想法💡

新注册了一个域名 [sideproject.club](https://jinshuju.net/f/fJvCBJ). 希望做一个 invite only 的非盈利组织, 把喜欢做 sideproject 的朋友连接起来. 朋友们可以把自己想要做的新 side project 贴到上面, 和其他头脑做碰撞, 寻找合作者.

这件事完全处于一个想法阶段, 如果你也喜欢这个想法, 欢迎[加入讨论](https://jinshuju.net/f/fJvCBJ).

## 数据分享

> 产品详情可以访问 [t9t.io](https://t9t.io) 查看

### 平均每月被动收入($)(本周收入 / 7 * 30)

<svg id="incomeChart"></svg>

### 用户量
<svg id="userChart"></svg>

### github star 数
<svg id="starChart"></svg>

<br/>

> [帮助我改进这篇文章](https://github.com/t9tio/blog/blob/master/source/_posts/t9t-week18.md)

<script src="https://cdn.jsdelivr.net/npm/chart.xkcd@1.1.3/dist/chart.xkcd.min.js"></script>

<script>
var incomesvg = document.getElementById('incomeChart');
var usersvg = document.getElementById('userChart');
var starsvg = document.getElementById('starChart');


new chartXkcd.XY(incomesvg, {
  xLabel: 'weeks',
  data: {
    datasets: [{
        label: 'star-history',
        data: [{x:0,y:0.69},{x:1,y:0},{x:2,y:25.7},{x:3,y:12.8},{x:4,y:0},{x:5,y:8.571428571428571},{x:6,y:4.285714285714286},{x:7,y:4.285714285714286},{x:8,y:8.571428571428571},{x:9,y:8.571428571428571},{x:10,y:4.285714285714286},{x:11,y:17.142857142857142},{x:12,y:8.571428571428571},{x:13,y:3/7*30},{x:14,y:1/7*30},{x:15,y:3/7*30},{x:16,y:2/7*30},{x:17,y:0},{x:18,y:3/7*30}]
    }, {
        label: 'patron',
        data: [{x:10,y:0},{x:11,y:1},{x:12,y:1},{x:13,y:2},{x:14,y:8},{x:15,y:8},{x:16,y:9},{x:17,y:10},{x:18,y:10}]
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
          label: 'wewe',
          data: [{x:3,y:0},{x:4,y:60},{x:5,y:80},{x:6,y:91},{x:7,y:95},{x:8,y:95},{x:9,y:103},{x:10,y:103},{x:11,y:103},{x:12,y:103},{x:13,y:103},{x:14,y:103},{x:15,y:103},{x:16,y:108},{x:16,y:108},{x:17,y:111},{x:18,y:111}]
      },{
          label: 'open source jobs',
          data: [{x:0,y:39},{x:1,y:60},{x:2,y:62},{x:3,y:80},{x:4,y:101},{x:5,y:105},{x:6,y:109},{x:7,y:111},{x:8,y:113},{x:9,y:114},{x:10,y:119},{x:11,y:121},{x:12,y:122},{x:13,y:123},{x:14,y:123},{x:15,y:127},{x:16,y:131},{x:17,y:132},{x:18,y:133}]
      },{
          label: 'tomato-pie',
          data: [{x:0,y:653},{x:1,y:673},{x:2,y:722},{x:3,y:634},{x:4,y:647},{x:5,y:705},{x:6,y:681},{x:7,y:714},{x:8,y:712},{x:9,y:733},{x:10,y:774},{x:11,y:779},{x:12,y:801},{x:13,y:821},{x:14,y:898},{x:15,y:911},{x:16,y:981},{x:17,y:917},{x:18,y:920}]
      },{
          label: 'star-history',
          data: [{x:0,y:21},{x:1,y:21},{x:2,y:28},{x:3,y:33},{x:4,y:33},{x:5,y:34},{x:6,y:39},{x:7,y:38},{x:8,y:40},{x:9,y:47},{x:10,y:48},{x:11,y:50},{x:12,y:61},{x:13,y:58},{x:14,y:55},{x:15,y:57},{x:16,y:58},{x:17,y:58},{x:18,y:63}]
      }]
  },
  options: {
    showLine: true,
    dotSize: 0.5,
    xTickCount: 5,
  }
});

new chartXkcd.XY(starsvg, {
  xLabel: 'weeks',
  data: {
    datasets: [{
        label: 'wewe',
        data: [{x:4,y:0},{x:5,y:11},{x:6,y:33},{x:7,y:57},{x:8,y:70},{x:9,y:77},{x:10,y:78},{x:11,y:102},{x:12,y:103},{x:13,y:108},{x:14,y:111},{x:15,y:114},{x:16,y:211},{x:17,y:242},{x:18,y:250}]
    },{
        label: 'open source jobs',
        data: [{x:0,y:731},{x:1,y:764},{x:2,y:763},{x:3,y:821},{x:4,y:872},{x:5,y:891},{x:6,y:898},{x:7,y:903},{x:8,y:934},{x:9,y:940},{x:10,y:956},{x:11,y:962},{x:12,y:966},{x:13,y:967},{x:14,y:976},{x:15,y:980},{x:16,y:994},{x:17,y:1002},{x:18,y:1005}]
    },{
        label: 'tomato-pie',
        data: [{x:0,y:107},{x:1,y:113},{x:2,y:117},{x:3,y:118},{x:4,y:125},{x:5,y:126},{x:6,y:128},{x:7,y:129},{x:8,y:134},{x:9,y:134},{x:10,y:136},{x:11,y:136},{x:12,y:139},{x:13,y:139},{x:14,y:141},{x:15,y:148},{x:16,y:155},{x:17,y:156},{x:18,y:158}]
    },{
        label: 'star-history',
        data: [{x:0,y:921},{x:1,y:998},{x:2,y:1110},{x:3,y:1129},{x:4,y:1154},{x:5,y:1178},{x:6,y:1190},{x:7,y:1216},{x:8,y:1238},{x:9,y:1246},{x:10,y:1276},{x:11,y:1291},{x:12,y:1299},{x:13,y:1308},{x:14,y:1328},{x:15,y:1343},{x:16,y:1361},{x:17,y:1367},{x:18,y:1382}]
    }, {
        label: 'chart.xkcd',
        data: [{x:12,y:3},{x:13,y:500},{x:14,y:3069},{x:15,y:3764},{x:16,y:4308},{x:17,y:4508},{x:18,y:4651}]
    }]
  },
  options: {
    showLine: true,
    dotSize: 0.5,
    xTickCount: 5,
  }
});


</script>

