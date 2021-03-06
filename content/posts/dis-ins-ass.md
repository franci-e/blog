---
title: 【闲得我】如何把一台 2008 年早期 15 寸 MacBook Pro 拆掉、装上三系统、再组装回来
author: Francie Jiang
date: 2022-07-25T00:00:00+08:00
---

> 如果你没有注意到的话，这里来一个小提醒：这篇文章的名字叫做 dis-ins-ass。不知道为什么，这玩意我看一次笑一次，但是这其实是 Disassemble - Install - Assemble 的缩写，很正经的（ 

> 笑死，买了这台 MacBook 研究以后，还拍了一个特别智障的视频发到了 YouTube 上，各位如果对一个听了半天最后发现什么都讲了却又什么都没讲的 Review 视频感兴趣的话（或者你对生草的谷歌翻译机感兴趣的话），可以去 [我的 YouTube 频道](https://www.youtube.com/watch?v=vzGRJqfB9s4) 上看看哦（

## 拆解
2008 年早期 15 寸 MacBook Pro （下简称 「我的 MacBook Pro」或「我的 MBP」） 的螺丝分布如下表：

<center>

|  螺头  | 位置  | 数量  |
|:---:|:---:|:---:|
|  CR-V +2.0 |  侧边  | 10  |
| CR-V +2.0  | 电池仓的侧边  | 2  |
|  CR-V +2.0 |  RAM 插槽的盖盖 | 3  |
| CR-V 1.3 | RAM 插槽的边边 | 2 |
| CR-V T7[^t7] | 硬盘槽固定硬盘的条条 | 2 |

</center>

把这些东西拧掉就可以了（

不过，在拆键盘的时候要注意键盘下面连了根排线到主板上，要先把它拆掉再继续工作哦（

## 装上三系统
作为一个晚上搞了四个小时还是没有装好的大冤种，先介绍一下我的系统安装顺序。

1. 安装 Mac OS X Leopard。
2. 安装 Windows Vista。
3. 安装 Arch Linux[^archLinux]。

其中，因为这台电脑比较老，而且我也没有 Windows Vista 的安装光盘，所以 Boot Camp 的早期版本（需要使用光盘安装）是用不了的。在我苦苦尝试了一个晚上以后，我在电脑上安装了 VMWare Workstation Pro 16 （没有在打广告的意思！），然后用了一个之前因为没有硬盘[^noHDDs]所以没敢用的功能，就是在虚拟机中使用实体硬盘。

<center>

![Alt](/usePhysicalDisks.png)
<small>图 1. 各位看到了吧 就是这个东西（</small>

</center>

在设置好使用整块实体硬盘以后，我们就可以使用 VMWare 来安装系统了，整个过程属于是行云流水（？）因为之前在虚拟机里头安装了蛮多遍老系统的，而且使用 VMWare 的时候不会跳出来奇奇怪怪的提示说找不到 USB 3.0 驱动【完全、一点都、没有、在、影射、Windows Vista、这件事情哦~（气急败坏）】，所以整个安装过程大概只有 30 分钟。

在装完并激活 Windows Vista 后，我又突发奇想：这能不能再装个 Arch Linux 满足我装 X 的需求（没有这种东西啦！）呢？

于是，我就又一次拆开了这台 MacBook Pro，把它的硬盘取了出来...

## Summary


[^t7]: 这个我拧的时候其实有点松，但是看起来正好合适，所以就填的这个了（ ~~（才不是因为我要拧螺丝的时候就找不到对应的螺丝刀头了呢）~~
[^archLinux]: 笑死 这个时候才记起来我自己是 Arch Linux 人哦（
[^noHDDs]: 数了一下 现在我大概有五块随便用不怕数据丢失的硬盘 总计 2 TB 多一点吧（