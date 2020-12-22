---
title: 通过 GitHub 订阅 Hacker News 每日 top 10
date: 2020-09-03
---

> 代码仓库: https://github.com/headllines/hackernews-daily

## 想要解决的问题

[Hacker News](https://news.ycombinator.com/) 是我最主要的信息源之一, 他独创的[排序算法](https://news.ycombinator.com/item?id=1781417)和严格的[反作弊特性](https://news.ycombinator.com/newsfaq.html)让我每天都能在首页找到有趣的内容. 不过也正是因为这个排序算法, 通常来讲每隔个十几分钟, 首页上的内容就会发生变化.

我没有时间经常去逛. 如果能有一个工具每天帮我挑出最热门的 10 个帖子发给我就好了.

## 解决方案

众所周知, GitHub 的 [Action](https://github.com/features/actions) 支持执行定时任务. 于是我写了一个脚本, 获取每日 upvotes 最多的帖子, 并且记录到了[项目的 issue](https://github.com/headllines/hackernews-daily/issues) 里

[![](https://timqian-imgs.s3.ap-southeast-1.amazonaws.com/2020-09-Screen%20Shot%202020-09-02%20at%203.24.40%20PM.png)](https://github.com/headllines/hackernews-daily)

### 好处

1. 用户 watch 这个项目之后, 每当有新的 issue, 就会在 GitHub 上收到通知(同时收到邮件通知)
2. 感谢 [RSSHub](https://rsshub.app/), 用户也可以通过 [RSS](https://feeds.pub/feed/http%3A%2F%2Frsshub.app%2Fgithub%2Fissue%2Fheadllines%2Fhackernews-daily) 来订阅 issue 的更新
3. 完全 0 成本, 不用担心那一天因为成本问题运行不下去了

## 如何食用

可以通过 watch [GitHub 上的仓库](https://github.com/headllines/hackernews-daily) 或者 [RSS](https://feeds.pub/feed/http%3A%2F%2Frsshub.app%2Fgithub%2Fissue%2Fheadllines%2Fhackernews-daily) 来订阅更新, 除了每天的头条, 我还做了每周和每月的

| GitHub | RSS |
| ---    | --- |
| [headllines/hackernews-daily](https://github.com/headllines/hackernews-daily) | [![RSS](https://img.shields.io/badge/dynamic/json?label=follow&query=%24.data.feed.followerCount&url=https%3A%2F%2Fapi.feeds.pub%2Fgraphql%3Fquery%3Dquery%2520feed%28%2524id%253A%2520String%21%29%257B%2520feed%28id%253A%2520%2524id%29%2520%257B%2520followerCount%2520%257D%2520%257D%26variables%3D%257B%2522id%2522%253A%2520%2522http%3A%2F%2Frsshub.app%2Fgithub%2Fissue%2Fheadllines%2Fhackernews-daily%2522%257D%26operationName%3Dfeed&style=social&logo=data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAEUAAABFCAYAAAAcjSspAAAACXBIWXMAAAInAAACJwG+ElQIAAAAAXNSR0IArs4c6QAAAARnQU1BAACxjwv8YQUAAASkSURBVHgB7Ztdcts2EMf/oDyeNO5MnBOUN4hzAtNvrZ0H8QSimwPEPoHlE9g5gZkTSJ46mU77YPYEVd/6yN5AnWkzrVNxuxAhN3UA0YL46eA3Y30AkDT8c7FY7MKAw+FwlIfAAyAafe2rl/w8m8bhjxOsQedEiUbBNrAVeQLPCBTwJfiaYROiWRiH36ewYAMdIBfiUV+I3oDfBrKN5j3Ge7rDYy/4eQ8WtFoUOS08zxsQiSN+u73ap7EDS1opCosR8J0+4ZcBEWyZwpJWiRKN9tnsxRnUFFkHIjqFJa1wtNJneN7WCVvFEexgqyD+E1MBkWaUXcbhuxiWNC7Ky8sXrzKiIVbzGVO2hDeANwb+mMRhYj1VdDQmytw6xJcXvKz2V/hYwk73NA6vElRII6Io3zHCPNgqhK1CvGaLOC/bIkzU7mij0TccbwgZQxRNl9rFWFCrpby8PBhkhLhoHPsLFuP9sG4xFtQmioo9rguGcXgujqv2GUX0UAMyMmVBpA8xThllHYdx+MOvaJhafIqyEN/Qzb7DY+v4LkZLqFwUFYf4hm4Zb+yxIGtt9cumUp+ipo3RSliQ5xx5tkoQiYdK8QIYBcFxGwWRVCoKxyMnhi4Ozd+eo6VUJopKEfq6PqKbQ7SYCh3txs4iP3aHqRCbZ4fjA16eSS3RIp0/CkyyjH4BssQ2lVgGFYqS7Rj8uBQiyF/e9vvygf0MB3iyrYdvxwdxRrPTJsSpZPrkq47YxRqwjUW8cv0sN4+omdJFkXGJvBiUkD1jtlnc649KGLVQ2vTJ8yOPzzhQi1AuPN08mZGzzcqtTCmWIgURYuuaICJUAFvLADWydkS7EAT3LClwFPsT3wuOUbIU2OTUwI20BOl85WrEuRYM9J/782lnkkwq4XxvZ8h3/auL/tXY0D0+HO/v6qp+vc3HT7BG2WIV1po+vDJEFhl4P6/4mRDaC5/dfHiKmlhLlCVhvIw5ONtOqb73i0DXGo36UiyD1X1IURPWokgrgXn3+5r3NlHuPzQ/anCcPe8fk0NN60xNWouyxEr4At6pKSUS3QBepYK7U0jGIqr+oxmPBDViJYqKMn1dH+dYP9rsbUqHqrvD84rgf993m3fR+xoSb1AjVktyNDo44qXzTNM1uei/ff7/sfvnbFWvdN8jRG4ZBacKEv5OqyMVtlgtyewTdkmzAybKNHc045ikpxWFxRiiAKJZ7WkGq+lDt1v+u/Q+yaTJXW5e1LL4nXl2rjO7ZFMi+m/DCrEx5IcUq/zCvGbcTHbOUhTh61pNB/DicMxZ+5n0CynuQW4hV0M0xMqiqABLx9I4Ip9Gsz1ejsdLhiV5hr/Z/K2Fo/1r21BYLAyulH8Io9GLgB2wLLQ/ExzWZ5T9Js+aNF0uXdDI8S518Qlaio1P8Q3tKR4IFRfDuokTRYONKKmh3ccDwVmKBieKBieKBgtRHpmCtKLTjp1hZVHkPsbQ9fmK8jlgK4rWWpaXLrqDbT5FK4oqWHUeN300OFE0OFE02KYjU13r7Ob973gA2GXziY5xZwXKE83N/NdF2VifT8mPXHlHXAN6knEFry2pRIfD4XA4usm//qauBcoh1b8AAAAASUVORK5CYII=)](https://feeds.pub/feed/http%3A%2F%2Frsshub.app%2Fgithub%2Fissue%2Fheadllines%2Fhackernews-daily) |
| [headllines/hackernews-weekly](https://github.com/headllines/hackernews-weekly) | [![Follow on Feeds Pub](https://img.shields.io/badge/dynamic/json?label=follow&query=%24.data.feed.followerCount&url=https%3A%2F%2Fapi.feeds.pub%2Fgraphql%3Fquery%3Dquery%2520feed%28%2524id%253A%2520String%21%29%257B%2520feed%28id%253A%2520%2524id%29%2520%257B%2520followerCount%2520%257D%2520%257D%26variables%3D%257B%2522id%2522%253A%2520%2522https%3A%2F%2Frsshub.app%2Fgithub%2Fissue%2Fheadllines%2Fhackernews-weekly%2522%257D%26operationName%3Dfeed&style=social&logo=data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAEUAAABFCAYAAAAcjSspAAAACXBIWXMAAAInAAACJwG+ElQIAAAAAXNSR0IArs4c6QAAAARnQU1BAACxjwv8YQUAAASkSURBVHgB7Ztdcts2EMf/oDyeNO5MnBOUN4hzAtNvrZ0H8QSimwPEPoHlE9g5gZkTSJ46mU77YPYEVd/6yN5AnWkzrVNxuxAhN3UA0YL46eA3Y30AkDT8c7FY7MKAw+FwlIfAAyAafe2rl/w8m8bhjxOsQedEiUbBNrAVeQLPCBTwJfiaYROiWRiH36ewYAMdIBfiUV+I3oDfBrKN5j3Ge7rDYy/4eQ8WtFoUOS08zxsQiSN+u73ap7EDS1opCosR8J0+4ZcBEWyZwpJWiRKN9tnsxRnUFFkHIjqFJa1wtNJneN7WCVvFEexgqyD+E1MBkWaUXcbhuxiWNC7Ky8sXrzKiIVbzGVO2hDeANwb+mMRhYj1VdDQmytw6xJcXvKz2V/hYwk73NA6vElRII6Io3zHCPNgqhK1CvGaLOC/bIkzU7mij0TccbwgZQxRNl9rFWFCrpby8PBhkhLhoHPsLFuP9sG4xFtQmioo9rguGcXgujqv2GUX0UAMyMmVBpA8xThllHYdx+MOvaJhafIqyEN/Qzb7DY+v4LkZLqFwUFYf4hm4Zb+yxIGtt9cumUp+ipo3RSliQ5xx5tkoQiYdK8QIYBcFxGwWRVCoKxyMnhi4Ozd+eo6VUJopKEfq6PqKbQ7SYCh3txs4iP3aHqRCbZ4fjA16eSS3RIp0/CkyyjH4BssQ2lVgGFYqS7Rj8uBQiyF/e9vvygf0MB3iyrYdvxwdxRrPTJsSpZPrkq47YxRqwjUW8cv0sN4+omdJFkXGJvBiUkD1jtlnc649KGLVQ2vTJ8yOPzzhQi1AuPN08mZGzzcqtTCmWIgURYuuaICJUAFvLADWydkS7EAT3LClwFPsT3wuOUbIU2OTUwI20BOl85WrEuRYM9J/782lnkkwq4XxvZ8h3/auL/tXY0D0+HO/v6qp+vc3HT7BG2WIV1po+vDJEFhl4P6/4mRDaC5/dfHiKmlhLlCVhvIw5ONtOqb73i0DXGo36UiyD1X1IURPWokgrgXn3+5r3NlHuPzQ/anCcPe8fk0NN60xNWouyxEr4At6pKSUS3QBepYK7U0jGIqr+oxmPBDViJYqKMn1dH+dYP9rsbUqHqrvD84rgf993m3fR+xoSb1AjVktyNDo44qXzTNM1uei/ff7/sfvnbFWvdN8jRG4ZBacKEv5OqyMVtlgtyewTdkmzAybKNHc045ikpxWFxRiiAKJZ7WkGq+lDt1v+u/Q+yaTJXW5e1LL4nXl2rjO7ZFMi+m/DCrEx5IcUq/zCvGbcTHbOUhTh61pNB/DicMxZ+5n0CynuQW4hV0M0xMqiqABLx9I4Ip9Gsz1ejsdLhiV5hr/Z/K2Fo/1r21BYLAyulH8Io9GLgB2wLLQ/ExzWZ5T9Js+aNF0uXdDI8S518Qlaio1P8Q3tKR4IFRfDuokTRYONKKmh3ccDwVmKBieKBieKBgtRHpmCtKLTjp1hZVHkPsbQ9fmK8jlgK4rWWpaXLrqDbT5FK4oqWHUeN300OFE0OFE02KYjU13r7Ob973gA2GXziY5xZwXKE83N/NdF2VifT8mPXHlHXAN6knEFry2pRIfD4XA4usm//qauBcoh1b8AAAAASUVORK5CYII=)](https://feeds.pub/feed/https%3A%2F%2Frsshub.app%2Fgithub%2Fissue%2Fheadllines%2Fhackernews-weekly) |
| [headllines/hackernews-monthly](https://github.com/headllines/hackernews-monthly) | [![Follow on Feeds Pub](https://img.shields.io/badge/dynamic/json?label=follow&query=%24.data.feed.followerCount&url=https%3A%2F%2Fapi.feeds.pub%2Fgraphql%3Fquery%3Dquery%2520feed%28%2524id%253A%2520String%21%29%257B%2520feed%28id%253A%2520%2524id%29%2520%257B%2520followerCount%2520%257D%2520%257D%26variables%3D%257B%2522id%2522%253A%2520%2522https%3A%2F%2Frsshub.app%2Fgithub%2Fissue%2Fheadllines%2Fhackernews-monthly%2522%257D%26operationName%3Dfeed&style=social&logo=data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAEUAAABFCAYAAAAcjSspAAAACXBIWXMAAAInAAACJwG+ElQIAAAAAXNSR0IArs4c6QAAAARnQU1BAACxjwv8YQUAAASkSURBVHgB7Ztdcts2EMf/oDyeNO5MnBOUN4hzAtNvrZ0H8QSimwPEPoHlE9g5gZkTSJ46mU77YPYEVd/6yN5AnWkzrVNxuxAhN3UA0YL46eA3Y30AkDT8c7FY7MKAw+FwlIfAAyAafe2rl/w8m8bhjxOsQedEiUbBNrAVeQLPCBTwJfiaYROiWRiH36ewYAMdIBfiUV+I3oDfBrKN5j3Ge7rDYy/4eQ8WtFoUOS08zxsQiSN+u73ap7EDS1opCosR8J0+4ZcBEWyZwpJWiRKN9tnsxRnUFFkHIjqFJa1wtNJneN7WCVvFEexgqyD+E1MBkWaUXcbhuxiWNC7Ky8sXrzKiIVbzGVO2hDeANwb+mMRhYj1VdDQmytw6xJcXvKz2V/hYwk73NA6vElRII6Io3zHCPNgqhK1CvGaLOC/bIkzU7mij0TccbwgZQxRNl9rFWFCrpby8PBhkhLhoHPsLFuP9sG4xFtQmioo9rguGcXgujqv2GUX0UAMyMmVBpA8xThllHYdx+MOvaJhafIqyEN/Qzb7DY+v4LkZLqFwUFYf4hm4Zb+yxIGtt9cumUp+ipo3RSliQ5xx5tkoQiYdK8QIYBcFxGwWRVCoKxyMnhi4Ozd+eo6VUJopKEfq6PqKbQ7SYCh3txs4iP3aHqRCbZ4fjA16eSS3RIp0/CkyyjH4BssQ2lVgGFYqS7Rj8uBQiyF/e9vvygf0MB3iyrYdvxwdxRrPTJsSpZPrkq47YxRqwjUW8cv0sN4+omdJFkXGJvBiUkD1jtlnc649KGLVQ2vTJ8yOPzzhQi1AuPN08mZGzzcqtTCmWIgURYuuaICJUAFvLADWydkS7EAT3LClwFPsT3wuOUbIU2OTUwI20BOl85WrEuRYM9J/782lnkkwq4XxvZ8h3/auL/tXY0D0+HO/v6qp+vc3HT7BG2WIV1po+vDJEFhl4P6/4mRDaC5/dfHiKmlhLlCVhvIw5ONtOqb73i0DXGo36UiyD1X1IURPWokgrgXn3+5r3NlHuPzQ/anCcPe8fk0NN60xNWouyxEr4At6pKSUS3QBepYK7U0jGIqr+oxmPBDViJYqKMn1dH+dYP9rsbUqHqrvD84rgf993m3fR+xoSb1AjVktyNDo44qXzTNM1uei/ff7/sfvnbFWvdN8jRG4ZBacKEv5OqyMVtlgtyewTdkmzAybKNHc045ikpxWFxRiiAKJZ7WkGq+lDt1v+u/Q+yaTJXW5e1LL4nXl2rjO7ZFMi+m/DCrEx5IcUq/zCvGbcTHbOUhTh61pNB/DicMxZ+5n0CynuQW4hV0M0xMqiqABLx9I4Ip9Gsz1ejsdLhiV5hr/Z/K2Fo/1r21BYLAyulH8Io9GLgB2wLLQ/ExzWZ5T9Js+aNF0uXdDI8S518Qlaio1P8Q3tKR4IFRfDuokTRYONKKmh3ccDwVmKBieKBieKBgtRHpmCtKLTjp1hZVHkPsbQ9fmK8jlgK4rWWpaXLrqDbT5FK4oqWHUeN300OFE0OFE02KYjU13r7Ob973gA2GXziY5xZwXKE83N/NdF2VifT8mPXHlHXAN6knEFry2pRIfD4XA4usm//qauBcoh1b8AAAAASUVORK5CYII=)](https://feeds.pub/feed/https%3A%2F%2Frsshub.app%2Fgithub%2Fissue%2Fheadllines%2Fhackernews-monthly) |

## 后续

定期获取头条的这个需求其实不只是对 Hacker News 存在, 对于 ProductHunt, GitHub, V2EX... 等等网站. 我相信都有制作”头条抓取器“的价值. 我和 [leadream](https://juuun.io/) 决定一起试着做做这个 side project. 我们注册了一个域名

> **[headllines.com](https://headllines.com)**

slogan 是 “Open source headline collectors”.

Hacker News Top 10 只是一个开始, 之后我们会增加更多的 headline collectors, 会有一个方便集中阅读的网站...

如果你也对这件事情感兴趣, 欢迎通过[邮件订阅](https://headllines.com)我们的进展或者加入 [Telegram 群](https://t.me/headllines) 交流.
