---
title: UML类图关系
date: 2019-03-14 21:20:13
tags: UML
---

<span id="top"></span>
[TOC]

[End](#end)

# 类图关系
<!--More-->
![UML类图][]

## 泛化(generalization)
![generalization][]
- 继承非抽象类 

## 实现(realize)
![realize][]
- 继承抽象类，实现接口

## 聚合(aggregation)
![aggregation]
- 构造函数中包含另一个**类的实例作为参数**
- 客户端**同时了解两个类**，因为他们是独立的

## 组合(composition)
![composition]
- 构造函数包含另一个**类的实例化**，两者紧密耦合在一起
- 客户端中**只认识类B**,因为类A被严密地封装在类B中

## 关联(association)
![association]
- 成员变量，类B是类A的属性

## 依赖(dependency)
![dependency][]
- 类B是Public的, 类A可以调用它
- 类B是类A中某个方法的局部变量（持有类B的是类A的一个方法，而不是类A自身）
- 类B是类A某个方法的参数或返回值


[UML类图]: http://ww1.sinaimg.cn/large/006Q2Ktwgy1g0ztrhovk1j30ns0bj0t8.jpg "UML类图"
[generalization]: http://ww1.sinaimg.cn/large/006Q2Ktwgy1g0ztwk4zhbj308a036t8k.jpg "泛化"
[realize]: http://ww1.sinaimg.cn/large/006Q2Ktwgy1g0ztwqshhhj309407hmx6.jpg "实现"
[aggregation]: http://ww1.sinaimg.cn/large/006Q2Ktwgy1g0ztwxhebwj307o02vq2s.jpg "聚合"
[composition]: http://ww1.sinaimg.cn/large/006Q2Ktwgy1g0ztx11obkj307t02tmx0.jpg "组合"
[association]: http://ww1.sinaimg.cn/large/006Q2Ktwgy1g0ztx5q1lhj308903aq2s.jpg "关联"
[dependency]: http://ww1.sinaimg.cn/large/006Q2Ktwgy1g0ztx8yn3rj3086035t8k.jpg "依赖"

<span id = "end"></span>
[Top](#top)