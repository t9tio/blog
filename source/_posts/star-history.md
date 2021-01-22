---
title: 一个付费 chrome 插件的一生
description: star history 的故事
date: 2021-01-21
---

## 链接

- [Chrome 插件](https://chrome.google.com/webstore/detail/iijibbcdddbhokfepbblglfgdglnccfn)
- [GitHub](https://github.com/timqian/star-history)
- [网站](https://star-history.t9t.io/)

## 故事

![](https://i.v2ex.co/J5pyh6aH.png)

最近收到 Google 的一封邮件，告诉我 Chrome Web Store Payments 2月1日就要停止运营了。[接入新的付费方式](https://developer.chrome.com/docs/webstore/cws-payments-deprecation/)看起来还挺麻烦的。我没有美国的税收编号，要把原来的收入的几百美金提出来也不是特别容易。于是我决定把这个小插件设为免费安装，可以让更多人使用自己做的小产品也是很好的。


[star-history](https://github.com/timqian/star-history) 诞生于 5 年前，我想看看 GitHub 上那些玲琅满目的开源项目的 star 的历史，于是花了一个周末做了一个网站，调用 GitHub API 可以画出项目 star 的历史曲线。为了方便自己使用，后来做了一个 chrome 插件版本。这样我每次想看一个项目的 star history，就不用总是需要打开网站输入链接，而是直接点击一个按钮就行。

![](https://i.v2ex.co/345TEcCd.png)

插件本身是开源的，用户可以 clone 代码添加到浏览器。我自己操作起来感觉不是特别麻烦，不过时不时的有用户给我提 issue, 发邮件说希望可以直接从 chrome web store 下载。

于是我花了点时间注册了谷歌开发者，准备必要的素材，根据谷歌的要求改代码和素材着实花了我好几个小时，于是在看到有“设为付费插件”这个选项，我毫不犹豫的点击了它。。定价 $2.99 一个吧，管他有没有人买。。

没有想到几天之后还真有人付费购买了，当时很兴奋，获得了自己售卖软件获得的第一笔收入😂。之后这个插件每一两周可以卖出去一个。大概半年之前，star-history 自己[在 GitHub 上](https://github.com/timqian/star-history)获得了 1k star，而且自己的 star  曲线看着很健康。

![](https://i.v2ex.co/14WUkb4t.png)

于是我做了两个小小的操作，一是把他降价为 $0.99，二是把降价消息放在了网站很显眼的地方，销量一下子就上去了。。。大概每一两天会有一个人购买，到目前为止总共帮我赚了400多美金。

![](https://i.v2ex.co/Qi0a9r07.png)

![](https://i.v2ex.co/N4JSU5co.png)

在这个插件的鼓舞下，我后来又做了很多开源项目，不过遗憾的是到目前为止那些花费我大量时间的其他 side project 没有一个的收入超过这个“周末产品”😅 

### 两点感想

- 用户是愿意付费的，如果产品真正帮助他们解决了问题
- 产品的成败与你付出的工作量没有关系
