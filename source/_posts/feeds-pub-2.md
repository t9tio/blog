---
title: Feeds Pub 小范围发布半个月, 分享一些数据和感想
date: 2020-04-14
---

## 一些数据

半个月前, 我尝试在几个技术论坛 (v2ex, ruby china, cnodejs) 分享了 [Feeds Pub](https://feeds.pub). 最近这些天我一边根据计划和用户的反馈来做更新, 一边每天忍不住看好几次统计数据, 毕竟闭门造车了快 3 个月, 没人用就尴尬了... 比较幸运的是, 数据看起来似乎还不错, 超过了我的预期. 截止北京时间 4 月 14 日下午 5 点钟

- 有 **2300** 个朋友访问过 Feeds Pub (3300 次打开, 8400 次浏览)
- **550** 个朋友注册了账户
- **37475** 条更新被推送到用户手中
- **1653** 个 follow feed 事件
- **125** 个 star 被给出
- **4** 个付费用户 (patron) 感谢 [@lanzhiheng](https://feeds.pub/lanzhiheng) [@Lenville](https://feeds.pub/Lenville)  [@tankaichuan](https://feeds.pub/tangkaichuan) 和 [@scvoet](https://feeds.pub/scvoet) 

访问变注册的转化率有 20%, 感觉有点过高, 可能是因为用的 google analytics 对访问量有些漏计.

在有很多显而易见的不足之处的前提下, 有四位用户愿意花钱支持让我十分开心. 虽然有几位 patron 不完全是因为 Feeds Pub 才成为 patron 的😅 如果能够保持 0.7% 的用户付费转化, 相信假以时日通过 Feeds Pub 解决我的温饱问题还是有机会的.

总之, 看起来 Feeds Pub 除了我自己之外, 是被人需要的. 接下来我需要做的是不断完善它, 同时通过做周边产品/工具, 写博客等方式吸引更多使用者.

## 一些更新

![](https://timqian-imgs.s3.ap-southeast-1.amazonaws.com/2020-04-Screen%20Shot%202020-04-15%20at%2011.14.23%20AM.png)

- 类似 Hacker News 的排序算法

改变了 [explore](https://feeds.pub/explore) 页面的工作方式, 借鉴了 Hacker News 的排序算法, 根据用户对文章的 star 数据展示最近比较受欢迎的内容.

对每篇文章按照时间发布时间和点赞数按照下面这个公式计算一个得分, 然后按照得分高低排序

```
rank = stars / (hours + 2) ^ 1.4
```

- 支持了通过 OPML 文件批量导入 RSS 源
- 提升了稳定性, 修了许多bug
- 建了一个[公开的看板](https://github.com/feedspub/feedspub-feedback/projects/2), 感兴趣的朋友查看 Feeds Pub 的开发进程或者给予反馈
- 试着在国外一些论坛分享下, 欢迎在 [ProductHunt](https://www.producthunt.com/posts/feeds-pub) 给我投票😊

## 一些想法

一直以来, 我做东西的指导思想是 “创新”, 挖没人做过的事情. 总感觉如果市面上已经有差不多的产品, 再去做一个类似的没太大意思. 在这种 “创新” 精神的指导下, 做了[许多](https://github.com/timqian)自认为有创意的小玩意儿.

其中引起一些关注度的 [chart.xkcd](https://github.com/timqian/chart.xkcd) 让我稍稍改变了自己的态度.

[chart.xkcd](https://github.com/timqian/chart.xkcd) 是我几个月前做了一个手绘风格的图表库, 获得了挺多关注, 简短的[赞助者列表](https://timqian.com)也因此稍微增长了一些.

令我感到惊讶的是, 在 chart.xkcd 发布后的不到一个月时间, 出现了好几个 “手绘风格” 图表库, 这几个图表库在各种论坛, twitter, hackernews 上也一样获得了很多注意力.

这件事情给我的启示是, 不论做什么产品, 只要这个产品有一定的市场或者获得一些的注意力, 必定会有很多人来做类似的事情. 开源软件尚且如此, 更不要说有商业价值的产品了.

**无论做什么产品, 做到一定程度, 总归会有人出现, 和你竞争, 这个点子是谁最先想出来的并不重要**

所以单有“创意”是不够的, 更值钱的能力是”做好“产品的能力.

既然如此, 与其总是要求自己做市面上完全没有的东西, 去验证一些目前没有被满足的需求. 不如磨练自己的技艺, 加入比赛, 到那些已被验证需求的产品池里去尝试做的更好.

Feeds Pub 不能说在这个想法下指导出来的产物, 但也算符合这个想法. ”RSS 订阅“ 这个需求是一个验证存在的, 虽然现在不能算特别大众. 但也是世界上包括我自己在内 1% 左右的人的刚需.

在接下来很长一段时间里, 我将试着在这个战场上作战. 打磨 Feeds Pub, 也是打磨自己的产品力.
