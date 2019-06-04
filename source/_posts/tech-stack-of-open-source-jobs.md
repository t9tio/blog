---
title: 我最近一个网站的技术选择和源码分享
description: serverless + react server side rendering
---

> 关键词: serverless + react server side rendering

## 产品简介

[open-source-jobs](https://github.com/t9tio/open-source-jobs) 是一个收集主要项目为开源, 并且提供工作机会的公司的网站. 一开始只是一个 github 上的 markdown 项目. 因为发表到 [reddit](https://www.reddit.com/r/programming/comments/b44hm5/a_list_of_jobs_whose_major_responsibility_is/?utm_source=share&utm_medium=web2x) 上受到一些关注, 并且开源在近些年的蓬勃发展. 我觉得这个细分的找工作工具可能有一定价值, 于是把这个 markdown 做成了一个网站形式方便使用. 主要的两部分功能是用户通过 github 注册我可以拿到邮箱, 以及工作/组织的展示和筛选.

## 用到的工具, 技术以及我为什么这么选择

### Serverless

技术选择里面最重要的可能就是选择了以 serverless 的方式开发. 

Serverless 这个名字其实取得不是那么好, 容易让人以为开发网站不再需要服务器, 其实它真正的意思不是没有 server, 而是 server 由云平台帮你管理了, 根据需求自动伸缩服务器资源. 

Serverless 目前可能还有各种问题, 比如代码包尺寸限制, 语言限制等. 但它的好处也是显而易见的, 你不用管理服务器了!! 

做过几个失败的网站的同学应该有所经验. 一个纯前端的项目, 基本不会死, 因为你不用维护它, 还有各种免费稳定的托管静态网站的服务, 它总能正常工作. 

但对于带服务器的网站就不一样了, 很多时候网站失败的原因都是因为有一天服务器挂了, 你觉得这个东西反正没什么人用, 我还要花时间去管理服务器, 为这个服务器付钱. 挂了就挂了吧. 但我们也知道, 一些网站/应用想要成功, 时间也是一个关键因素. 尤其对于小众网站. 刚做出来, 分享到各个地方, 因为需求比较小众, 一开始收到的关注可能不是那么多, 很难通过一个很成功发布获得很多用户. 主要还是靠有这种需求的人通过搜索引擎找到你这个工具. 所以用户量需要时间慢慢增加. 网站需要你在用户量比较少的情况下长期维护. 如果没有 serverless, 在这漫长而没有太多回报的维护生涯中, 你很有可能就放弃了. 

Serverless 让写后端变得更像前端了一些, 你只负责写为用户提供价值的逻辑, 维护服务器这种脏活就不用管了. 增加了这种应用的成活时长, 使之更有可能成功.

[open-source-jobs](https://github.com/t9tio/open-source-jobs) 在我看来就是属于这一类的应用. 比较小众, 现在可能没有那么大需求, 但需求在慢慢增长. 是一个需要慢慢成长的小众产品.

#### Serverless 开发用到的工具

- Server: [AWS lambda](https://aws.amazon.com/lambda/)
- Serverless Database: [AWS dynamodb](https://aws.amazon.com/dynamodb/)
- Easy Deployment: [apex up](https://github.com/apex/up)
  - 这里的部署包括: 子域名自动注册; HTTPS; 以及部署服务端最新代码

### 前端模块化开发: React

React 可能不用多做介绍了, 是现在前端圈子里最火的框架. 让你可以模块化开发前端页面. 

- Frontend Components: [React.js](https://reactjs.org/)

### Server Side Rendering(SSR)

open-source-jobs 是一个内容站, 所以对搜索引擎友好是很重要的一点, 目前 React 圈这一点做的最好的应该就是 next.js 了

- Server Side Rendering for SEO: [next.js](https://github.com/zeit/next.js/)

## 最后附上项目链接和源码地址

- [网站地址](https://oo.t9t.io)
- [Github 源码](https://github.com/t9tio/open-source-jobs)
- [代码结构](https://github.com/t9tio/open-source-jobs#folder-structure)

<br/>

> [帮助我改进这篇文章](https://github.com/t9tio/blog/blob/master/source/_posts/tech-stack-of-open-source-jobs.md)
