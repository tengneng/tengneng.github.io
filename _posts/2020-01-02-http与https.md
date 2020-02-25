---
layout:     post   				    # 使用的布局（不需要改）
title:      http与https				# 标题 
#subtitle:   Hello World, Hello Blog #副标题
date:       2020-01-01				# 时间
author:     Teng 						# 作者
header-img: img/post-bg-2015.jpg 	#这篇文章标题背景图片
catalog: true 						# 是否归档
tags:								#标签
    - 网络
---
## http与https

### 基本概念

HTTP（HyperText Transfer Protocol：超文本传输协议）是一种用于分布式、协作式和超媒体信息系统的应用层协议。 简单来说就是一种发布和接收 HTML 页面的方法，被用于在 Web 浏览器和网站服务器之间传递信息。HTTP 默认工作在 TCP 协议 80 端口，用户访问网站 http:// 打头的都是标准 HTTP 服务。HTTP 协议以明文方式发送内容，不提供任何方式的数据加密，如果攻击者截取了Web浏览器和网站服务器之间的传输报文，就可以直接读懂其中的信息，因此，HTTP协议不适合传输一些敏感信息，比如：信用卡号、密码等支付信息。

HTTPS（Hypertext Transfer Protocol Secure：超文本传输安全协议）是一种透过计算机网络进行安全通信的传输协议。HTTPS 经由 HTTP 进行通信，但利用 SSL/TLS 来加密数据包。HTTPS 开发的主要目的，是提供对网站服务器的身份认证，保护交换数据的隐私与完整性。
HTTPS 默认工作在 TCP 协议443端口，它的工作流程一般如以下方式：

    1、TCP 三次同步握手
    2、客户端验证服务器数字证书
    3、DH 算法协商对称加密算法的密钥、hash 算法的密钥
    4、SSL 安全加密隧道协商完成
    5、网页以加密的方式传输，用协商的对称加密算法和密钥加密，保证数据机密性；用协商的hash算法进行数据完整性保护，保证数据不被篡改。

### HTTP与HTTPS区别

    1、HTTP 明文传输，数据都是未加密的，安全性较差，HTTPS(SSL+HTTP) 数据传输过程是加密的，安全性较好。
    2、使用 HTTPS 协议需要到 CA 申请证书，一般免费证书较少，因而需要一定费用。
    3、HTTP 页面响应速度比 HTTPS 快，主要是应为 HTTP 使用 TCP 三次握手建立连接，客户端与服务端需要交换3个包，而 HTTPS 除了 TCP 的三个包，还要加上 SSL 握手需要的9个包，一共是12个包。
    4、HTTP 和 HTTPS 使用的是完全不同的连接方式，用的端口也不一样，前者是80，后者是443。
    5、HTTPS 其实就是建构在 SSL/TLS 之上的 HTTP 协议，所以，要比较 HTTPS 比 HTTP 要更耗费服务器资源。