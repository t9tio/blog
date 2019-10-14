---
title: dynamodb 简介
description: 最简洁的方式概括 dynamodb 原理, 使用和例子
---

## dynamodb 如何存数据

- Primary key
  - Partition key 
  - Sort key (可选)
- 剩下的数据

![](https://raw.githubusercontent.com/timqian/images/master/20190610170154.png)


## 增删改查

### 查
https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/Query.html
https://docs.aws.amazon.com/zh_cn/amazondynamodb/latest/developerguide/Query.html

可以对 sort key 或者 secondary index 做查询, 没有办法对 partition key 做查询(只支持 EQ 操作): https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/LegacyConditionalParameters.KeyConditions.html

得到某 partition 里最大 range key 的: https://stackoverflow.com/questions/25457799/querying-for-greatest-value-of-range-key-on-aws-dynamodb

pagenation

create a unique and 有顺序的 id for your table
有顺序有什么用: msg 有顺序, reply 有顺序, 很多数据是有先后顺序的

简单 pagination: https://stackoverflow.com/a/9107030

想查看 Nth page: https://stackoverflow.com/a/42163206/4674834

## 不便之处
pagination offset: 
Item count of a table
range key 不支持 IN 查询 https://stackoverflow.com/a/32751240/4674834
local Secondary index 建表后不支持修改

## 最佳实践

https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/best-practices.html

partition key 要平均, why?
https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/bp-partition-key-uniform-load.html

## 免费套餐

https://aws.amazon.com/cn/dynamodb/pricing/provisioned/

25 个 WCU 和 25 个 RCU 的预置容量
25 GB 的数据存储
部署在两个 WAS 区域的全局表需要 25 个 rWCU
250 万个来自 DynamoDB Streams 的流读取请求
适用于所有 AWS 服务的共计 1GB 的数据传出量（前 12 个月为 15GB）


## Ref

https://aws.amazon.com/cn/blogs/database/choosing-the-right-dynamodb-partition-key/
https://docs.aws.amazon.com/zh_cn/amazondynamodb/latest/developerguide/bp-sort-keys.html