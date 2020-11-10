---
title: blender封闭空间外部光照
date: 2020-04-14 10:10:00
tags: [blender, 学习]
categories: 
	- [教程]
index_img: https://pic.imgdb.cn/item/5e9527f9c2a9a83be57d8fee.png
banner_img: https://pic.imgdb.cn/item/5e9527f9c2a9a83be57d8fee.png
---

### ？无光源的封闭场景中，室外光线穿透玻璃

增加玻璃后内部光线严重不足，阴影锐度降低，噪点增加

1. 玻璃内部增加光源。
2. 使用进口光，类似max中的天光？？（这个我尝试后效果并不理想，不知道是我哪弄错了还是怎么回是）
3. 给玻璃添加光程节点。

### 看图-光程

只添加了一个玻璃节点

![玻璃](https://pic.imgdb.cn/item/5e9527eac2a9a83be57d820a.png)

删除玻璃，窗户镂空

![无玻璃](https://pic.imgdb.cn/item/5e9527dac2a9a83be57d732e.png)

添加光程节点

![光程](https://pic.imgdb.cn/item/5e9527f9c2a9a83be57d8fee.png)

> 以上不难看出，想保证室外光照，又想保留玻璃的质感。
>
> 使用光程节点是不错的选择。

### 看图-进口光

进口光，理论上应该和vray的天光入口类似，但是不知道为何，并没有什么效果。。还是我使用方式不对？

![进口光](https://pic.imgdb.cn/item/5e952c32c2a9a83be58153c7.png)

添加进口光

![进口光-光程](https://pic.imgdb.cn/item/5e952b4cc2a9a83be580b055.png)

添加进口光

![进口光-玻璃](https://pic.imgdb.cn/item/5e952b43c2a9a83be580a791.png)

> 还是不太懂进口光的作用，也没感觉到采样的变化。

### 最平常的做法，还是增加内部光照~~~

在窗口增加内部光照，噪点降下去了，亮度提起来了，但是不符合自然光照规律了~~

![窗口增加光照](https://pic.imgdb.cn/item/5e952e8cc2a9a83be582cdb3.png)

----

### 小结

建议以上几种方法结合使用，根据不同的情况采用不同的方法，以求最佳效果。

光程节点能够在保证玻璃质感的同时实现最大光照。是挺不错的方法。

以下是光程节点的参考。

![节点示意](https://pic.imgdb.cn/item/5e952f6ac2a9a83be58357b2.png)

