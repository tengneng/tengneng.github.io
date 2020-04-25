---
layout:     post   				    # 使用的布局（不需要改）
title:      CSS3 transform属性				# 标题 
#subtitle:   Hello World, Hello Blog #副标题
date:       2020-04-17				# 时间
author:     Teng 						# 作者
header-img: img/post-bg-2015.jpg 	#这篇文章标题背景图片
catalog: true 						# 是否归档
tags:								#标签
    - CSS
---
## CSS3 transform属性
在CSS3中，可以利用transform功能来实现文字或图像的旋转、缩放、倾斜、移动这四种类型的变形处理。

### 一、旋转 rotate
用法：```transform:rotate(45deg);```

deg为度的意思，正数为顺时针旋转，负数为逆时针旋转，上述代码的作用是顺时针旋转45度。

### 二、缩放 scale
用法：```transfrom:scale(0.5)``` 或者 ```transfrom:scale(0.5,2)```

参数表示缩放倍数；一个参数时，表示水平和垂直同时缩放该倍率；两个参数时，第一个参数指定水平方向的缩放倍率，第二个参数指定垂直方向的缩放倍率。

### 三、倾斜 skew
用法：```transfrom:skew(30deg)```或者```transfrom:skew(30deg,30deg)```

参数表示倾斜角度，单位deg；一个参数时：表示水平方向的倾斜角度，第二个参数表示垂直方向的倾斜角度。

首先需要说明的是skew的默认原点transform-origin是这个物件的中心点。

![img](../img/tr1.png)

### 四、移动 translate
用法：```transform:translate(45px)```或者```transform:skew(45px,150px)```

参数表示移动距离，单位px；一个参数时，表示水平方向的移动距离；两个参数时，表示垂直方向的移动距离。

### 五、注意
transform虽然是关于坐标系统，但变换改变的只是元素的视觉渲染，那是在元素的布局计算后起作用的，因此在布局层面没有影响。

一般我们所看到的网页布局，遵循的是坐标系统的概念，这就是说，浏览器在实地渲染和显示一个网页之前，都会先进行布局计算，得到网页中所有元素对应的坐标位置，一旦元素的坐标位置或尺寸信息发生改变，浏览器就会重新进行布局计算，这个重新计算的过程叫做回流（reflow），一般情况下，transform不会引发回流。
