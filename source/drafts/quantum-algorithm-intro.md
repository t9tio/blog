---
title: 量子计算初探 - 从 qubit 到量子算法
description: 量子计算机原理
date: 2019-12-16
---

> TODO: https://github.com/SukkaW/DisqusJS/issues/12

最近对量子计算又产生了一点兴趣, 甚至想做[一个网站和一些相关工具](https://github.com/side-project-club/ideas/issues/8), 经过一番心理斗争终于克制住了自己购买域名的冲动, 决定先稍微研究了下再说. 在此记录下看完一众文章论文之后自己的一些理解.

## 经典计算机的基本构件

> 目前人类鼓捣出来的量子计算机, 很多概念借鉴了经典计算机的原理, 所以首先回顾下经典计算机的底层构件, 对于数字电路比较熟悉的同学可以直接略过这部分.

- `bit`: 用于储存信息, 每个 bit 可以储存的状态只有两个: 0 或 1.
- `gate`: gate 作用于 bit, 改变 bit 的状态.

比如常用的 AND gate

![AND gate](https://upload.wikimedia.org/wikipedia/commons/b/b9/AND_ANSI_Labelled.svg)

当 A 与 B 这两个 `bit` 都为 1 时, AND `gate` 输出为 1. 在其他情况下输出都是 0

这个 `gate` 的用途可以用下面这个表格来描述 (学名叫[真值表/truth table](https://en.wikipedia.org/wiki/Truth_table))

| INPUT A |	INPUT B |OUTPUT |
| --- | --- | --- |
| A	| B | Q |
|0	|0	|0|
|0	|1	|0|
|1	|0	|0|
|1	|1	|1|

下面放一张从维基百科截过来的图, 描述了其他一些常用 `gate` 的性质. 对经典门电路不了解但感兴趣的可以参考这个[维基百科](https://en.wikipedia.org/wiki/Logic_gate)

![常用 logic gates](https://raw.githubusercontent.com/timqian/images/master/20191206110211.png)

现在你用来阅读这篇文章的设备的 CPU, GPU..., 就是一个个 `gate` 做的.

你滑动手指时, 触摸屏把你的操作转换成 `bit`, 这些 `bit` 通过一系列的 `gate`, 输出处理后的 `bit`, 计算机再把这些 `bit` 转化成你能理解的反馈 - 也就是内容滑动了.

为了更具体一些, 我们用上面的 `gate` 来做一个简单的计算器试试, 大概也了解下这些基本的 `gate` 组织在一起的威力.

我们来做一个能想到的, 最简单的二进制计算器, 这个计算器只能做一位数字的加法. 他的表现就是

```
0 + 0 = 00
0 + 1 = 01
1 + 0 = 01
1 + 1 = 10
```

用真值表表示就是

| INPUT A |	INPUT B |OUTPUT A | OUTPUT B |
| --- | --- | --- | --- |
| A	| B | QA | QB |
|0	|0	|0 |0|
|0	|1	|0 |1|
|1	|0	|0 |1|
|1	|1	|1 |0|

这个加法器可以用 `AND gate` 和 `XOR gate` 来实现

![](https://upload.wikimedia.org/wikipedia/commons/d/d9/Half_Adder.svg)
![](https://upload.wikimedia.org/wikipedia/commons/9/92/Halfadder.gif)

关于经典计算机的基本构件就说到这里, 再继续的话要变成数字电路的科普文章了😅 关于 `bit` 和 `gate` 的原理, 如何组装出更复杂的功能甚至是 CPU, 可以参考以下一些资料.

- []()
- []()

## 量子计算机的基本构件

人类的进步大抵都是踩在前人的肩膀上往上爬, 量子计算机也不例外. 如今主流的量子计算机的设计也是参照了经典的 `bit` 和 `gate` 的概念. 只不过 `bit` 换成了 `Qubit`, 操作这些 `Qubit` 的 `gate` 和经典计算机也不太一样.

- `qubit`: 每个 `qubit` 可以处于 |0> 和 |1> 的一个叠加状态(superposition)
- `gates`: gate 作用于 qubit, 改变 qubit 的状态.

处于叠加态的 `qubit` 可以用下面这个式子表示
<p>
$$|X> = a|0> + b|1>$$
</p>
where α and β are probability amplitudes and can in general both be complex numbers.

可以用一个向量表示: 

[1, 2]

经典 `bit` 的状态不是 0 就是 1, 所以 `gate` 是一个简单的符号就表示了, 对于 `qubit`, 作用于它的 `gate` 需要用矩阵来表示. 比如常用的 `H gate`




量子算法

two quantum mechanical effects make qubit outperform classical algorithms
superposition:  before measurement, each qubit is indeed
in both basis states simultaneously with probability proportional to the amplitude of the prefactor
entanglement: Entanglement is a type of correlation that has no classical analog. For example, when two spinning particles are entangled their spins are correlated not only in one direction but in all directions. Because it has no classical analog, entanglement is an effect that is not easily simulated classically and hence is an effect that could create a quantum advantage (i.e., where quantum computers perform better than classical computers).

The main challenge in quantum algorithm design is to
leverage these two quantum effects

operations(gate)
unitary transformation
joint state
tensor product

CNOT

universal gate set: {H, T CNOT}: together can execute all possible quantum computations. or just {Toffoli gate}

What is a quantum algorithm

1. encoding of the data, which could be classical or quantum, into the state of a set of input qubits
2. a sequence of quantum gates applied to this set of input qubits
3. measurements of one or more of the qubits at the end to obtain a classically interpretable result

 quantum Turing machine

## Algorithms

### grover's algorithm

#### Definition

enables one to find (with probability > 1/2) a specific item within a randomly ordered database of N items using O(√N) operations. By contrast, a classical computer would require O(N) operations to achieve this.

#### Algorithm

f([1, 1]) = 1
f([x1, x2]) = 0

传统: 检查 00, 01, 10, 11 检查四个值看是否得到了 1
量子

f: Toffoli gate
the third bit is flipped if the first two bits are 1

search for [1, 1]

