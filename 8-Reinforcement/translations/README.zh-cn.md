# 强化学习简介

强化学习（Reinforcement learning, RL）被视为除监督学习和无监督学习以外的一种基本学习范式。强化学习关心的是决策：做出正确的决策，或至少从做出的决策中进行学习。

想象一下你有一个虚拟的环境，比如说股票市场。如果你做出了一个决策，会发生什么事呢？它会带来正面影响还是负面影响？如果发生了一些负面的事情，你会得到_负反馈_，从中吸取经验并改变你的做法。如果有正面收益，你会得到_正反馈_。



![peter and the wolf](../images/peter.png)

> 彼得（Peter）和他的朋友们需要从狼的口中逃脱！图片由 [Jen Looper](https://twitter.com/jenlooper)提供

## 地区专题：彼得与狼（俄罗斯）

[彼得与狼](https://en.wikipedia.org/wiki/Peter_and_the_Wolf)是由俄罗斯作曲家[Sergei Prokofiev](https://en.wikipedia.org/wiki/Sergei_Prokofiev)创作的音乐童话故事。它描述了一个少先队员彼得勇敢地走出他的房屋，去森林里驱逐狼的故事。在这一节中，我们将训练机器学习算法来帮助彼得：

- **探索** 周边的区域，建立最佳的导航地图。
- **学习** 如何使用滑雪板以及如何控制平衡以更快地移动。

[![Peter and the Wolf](https://img.youtube.com/vi/Fmi5zHg4QSM/0.jpg)](https://www.youtube.com/watch?v=Fmi5zHg4QSM)

> 🎥 点击图片播放Prokofiev作品《彼得与狼》

## 强化学习

在之前的章节中，你已经见过了两类机器学习问题：

- **有监督学习**， 我们有数据集，可以为我们想解决的问题提供参考答案。 [分类](../../4-Classification/README.md)和 [回归](../../2-Regression/README.md) 都是监督学习任务。
- **无监督学习**，我们没有标注好的训练数据。无监督学习的主要例子是[聚类](../../5-Clustering/README.md).

在这一节中，我们将为你介绍一类新的学习问题，它同样不需要标注好的训练数据。有几类这样的问题：

- **[半监督学习](https://wikipedia.org/wiki/Semi-supervised_learning)**，我们有大量的无标注数据，可以用来预训练模型。
- **[强化学习](https://wikipedia.org/wiki/Reinforcement_learning)**，智能体在一个模拟的环境中进行实验来学习如何进行决策。

### 例 - 计算机游戏

假设你想要教计算机玩一个游戏，比如下棋或[超级马里奥](https://wikipedia.org/wiki/Super_Mario)。为了让计算机学会玩这个游戏，我们需要它能够在每个游戏状态下预测下一步该怎么操作。虽然这看起来像是一个分类问题，但它并不是——因为我们没有一个数据集记录游戏状态和对应的动作。虽然我们有一些下棋或者玩家玩超级马里奥的数据，这些数据不足以覆盖所有足够多的可能的游戏状态。

**强化学习** (RL)的基本思想是*让计算机玩*许多次并观察结果，而不是在现有的游戏数据上做文章。因此，为了应用强化学习，我们需要两样东西：

- **一个环境**及**一个模拟器**，可以让我们多次玩游戏。模拟器定义了所有的游戏规则、可能的状态和动作。

- **一个奖励函数**，它能告诉我们在每一步或者整盘游戏中做得是好是坏。

其他类型的机器学习和强化学习的主要区别是，在强化学习中我们在游戏结束之前并不知道我们会赢还是会输。因此，我们不能判断某一步是好还是坏——我们只有在游戏结束后才能得到一个奖励。我们的目标是设计算法来在不确定的条件下训练模型。我们将学习一个叫做**Q-学习**的强化学习算法。

## 课程

1. [Introduction to reinforcement learning and Q-Learning](1-QLearning/README.md)
2. [Using a gym simulation environment](2-Gym/README.md)

## 致谢

"Introduction to Reinforcement Learning" 由 [Dmitry Soshnikov](http://soshnikov.com)倾心撰写
