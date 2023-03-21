---
title: A "GitHub" for ChatGPT prompts
description: Create, use and share ChatGPT prompts
date: 2023-03-21
---


[![open prompt](https://user-images.githubusercontent.com/5512552/226391224-1f634578-1479-4c2f-ae52-3e57de6a3390.png)](https://openprompt.co)

ChatGPT 极大的改变了我的工作习惯。最近几个月来，不论是写 SQL, 调优代码，润色英文，写软件 changelog 等等，几乎每天都要向他求助。

对于这些工作，一般都要预设一个 “prompt"， 这样 ChatGPT 就能更好的弄明白我的意图，回复的内容也能更直接为我所用。而且，这些 Prompts 是可以复用的。

比如，如果希望他帮我他翻译或者润色我写的 Chinglish，一般需要在输入内容前给 ChatGPT 下面提示：

- 我希望你能够扮演一个英语翻译，拼写纠正和改进的角色。
- 我会用任何语言和你交流，你会检测语言，翻译它，并用英语以我文本的更正和改进版本回答。
- 我希望你用更美丽和优雅的，高级别的英语单词和句子来替换我的简化的 A0 级单词和句子。
- 保持意思相同，但使它们更有文学性。
- 我希望你只回复更正，改进，不要写解释。

但是如果每次都要输入这么一段，还是比较累人的。因此，有人收集了常用的 Prompt，放在了一个 Github 仓库里面([ChatGPT-Prompt](https://github.com/f/awesome-chatgpt-prompts))，这个仓库受欢迎程度惊人:

![star-history](https://user-images.githubusercontent.com/5512552/226507783-32ff01c5-3f30-43e1-8316-d0bb3f7f0f73.png)

在未来，我们会创造越来越多的 Prompts, 每个人常用的 Prompts 也不同。

也许，对于 Prompts, 我们需要一个类似 GitHub 的平台。大家在创建自己需要的 Prompts, 在平台上发现别人创建的 Prompts。于是，我做了这个尝试：[Open Prompt](https://openprompt.co)

## [Open Prompt](https://openprompt.co) 是什么

### 1. 发现：看看别人做了有用/有趣的 prompts: [openprompt.co](https://openprompt.co)

![](https://user-images.githubusercontent.com/5512552/226404226-b8a6bbe8-eb7a-49d0-8394-05a71b4d7f90.png)

### 2. 创建：你可以创建自己的 Prompt 方便复用: [openprompt.co/create](https://openprompt.co/create)

![](https://user-images.githubusercontent.com/5512552/226507585-8179d7b8-2b4f-4263-bf34-6fbc4f4f5753.png)

### 3. 使用：Star 了一个 prompt 之后，他会被记录在侧边栏方便使用: [openprompt.co/refactor-code](https://openprompt.co/refactor-code)

![](https://user-images.githubusercontent.com/5512552/226388684-9c06558e-92e7-4b02-882f-b587bc64400a.png)


### 4. 当然，你也可以直接和不预设 Prompt 的 ChatGPT 对话: [openprompt.co/ChatGPT](https://openprompt.co/ChatGPT)
![](https://user-images.githubusercontent.com/5512552/226508887-43472a52-b372-4dfe-a230-0e8244037074.png)

## 未来

1. 除了 gpt-3.5 支持更多模型
2. 除了 ChatGPT, 也支持 DALL·E/Midjourney 的 prompts
3. 保存聊天记录
4. ...
