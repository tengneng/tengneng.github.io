---
layout:     post   				    # 使用的布局（不需要改）
title:      call,apply,bind				# 标题 
#subtitle:   Hello World, Hello Blog #副标题
date:       2020-01-05				# 时间
author:     Teng 						# 作者
header-img: img/post-bg-2015.jpg 	#这篇文章标题背景图片
catalog: true 						# 是否归档
tags:								#标签
    - javascript
---
## 手写call,apply,bind

### call

```js
Function.prototype.myCall = function(object) {
    let obj = object || windows;
    obj.fn = this;
    let arg = [...arguments].slice(1);
    let result = obj.fn(...arg);
    return result
}
```

### apply

```js
Function.prototype.myApply = function(object) {
    let obj = object || windows;
    obj.fn = this;
    let arg = [...arguments].slice(1);
    let result = obj.fn(arg);
    return result
}
```

### bind

```js
Function.prototype.myBind = function() {
   const args = Array.prototype.slice.call(arguments);
   const t = args.shift()
   const self = this
   return function (){
       return self.apply(t,args)
   }
}
```
