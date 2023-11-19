---
title: 我如何帮助 GPT-4 在 1 小时内自主解决 LeetCode 上 100 个编程问题
description: 
date: 2023-11-20
---

> Talk is cheap, 先上 code: **[github.com/timqian/letcode.ai](https://github.com/timqian/letcode.ai)** 以及运行视频：

<iframe 
  style="width: 640px; height: 430px; max-width: 100%"
  src="https://player.bilibili.com/player.html?bvid=BV1L94y1H78U" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true"> 
</iframe>


## 前因

前段时间，公司的一个重要客户有一个紧急的需求，我需要为此写一个逻辑比较复杂的函数并且最好是在1天内写完。即使作为一个拥有 [GPT-4](https://openai.com/gpt-4) 和 [GitHub copilot](https://github.com/features/copilot) 辅助的选手，我也感受到了一丝压力。通常来讲，我现在写代码的方式是这样的：

1. 写 comment, 让 copilot/GPT-4 实现这个函数/补全逻辑。
2. 如果不行，我会使用 GPT-4，问答的形式更具体和完善的描述我的问题。并且可以来回得让他优化答案

但是对于当时这个函数逻辑比较复杂的时候，这一套有点行不通了，总是写不出满意的效果，当时有些着急，我自己写又没这么快写出来。

突然想到一个办法。想让 GPT-4 获取更多关于我这个函数的信息，一个好办法是把一些输入/输出的例子也给到他。会不会帮助他写得更好呢？在我提供了测试用例之后，果不其然，GPT-4 就写出了满足我要求的代码。只不过对于有一个测试用例没通过。我把错误消息再提供给他，他修复之后，这个函数完全满足了我的需求。我阅读了他的代码，优美简洁。

## 发展

于是我就联想到，leetcode 上的题目，似乎都是这样组织的。包含问题的详细描述，例子，还有测试环境。如果用 GPT-4 ，加上我的一点辅助（帮助它获取题目，点击测试，获取测试反馈）。他是不是可以高效，优美得解决这些问题呢？说干就干

## 实践

### 第一阶段

我知道 [pupeeter](https://github.com/puppeteer/puppeteer) 可以帮助操纵浏览器，但我对它的 API 没有那么熟悉，不过没关系在 GPT-4 的帮助下，我很快写出了第一版的代码，逻辑比较简单：

1. Get problem set(Thanks https://github.com/haoel/leetcode)
2. For each problem
    1. get description
    2. get function format
    3. Provide the above info to GPT-4
    4. GPT-4 generate an answer
    5. Input into the answer box
    6. Press submit

中间遇到一些细节上的困难，但在 GPT-4 的协助下一一被我解决（比如可能是为了防止类似的机器刷题， leetcode 输入代码的编辑器不能直接设置内容，而是需要模拟人，手工输入）

就是这么一个简单的方式，GPT-4 的成功率到了 68% 左右（100/145）。大家可以在 https://leetcode.com/letcodeai/ 看到它提交的答案。


### 升级，Agent?

接下来，针对一次没有解决的问题，我帮助 GPT-4 获取失败的原因，让他修改。他顺利得修复了之前给出的代码，并且在第二次提交的时候成功解决了这个问题。我没有用代码实现这部分，不过你可以在这里看到这种处理的聊天记录：https://openprompt.co/conversations/3744 对应的 leetcode 链接：https://leetcode.com/problems/valid-number/

这一部分如果要用代码实现，也不难的。如果用这个方式，成功率估计可以超过 80%。有兴趣的小伙伴可以在我现在代码的基础上试一试：[github.com/timqian/letcode.ai](https://github.com/timqian/letcode.ai)

## 感想

如果是我来做 leetcode 上的题目，估计我一个月也做不了 100 题，但是在 LLM 的帮助下，这个时间缩短到了小时级别。效率提升达到了惊人的 1000 倍级别（2*30*24）。

我想，我从这个小小的窗口偶然瞥见了 AI 的潜力，它有机会百倍千倍的提升人类智力劳动的效率。