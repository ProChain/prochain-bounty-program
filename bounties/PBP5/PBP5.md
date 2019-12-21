# PBP5

## 1.  Summary 概述

微博解析器:

使用RUST发起HTTP请求，并通过分析请求内返回内容，解析出其中的用户头像URL地址

- 某条微博的转发URL：https://weibo.com/1642591402/IkWAEyqxy?type=repost
- 某条微博的评论URL：https://weibo.com/1642591402/IkWAEyqxy?type=comment

## 2.  Status 状态

- [ ] This PBP is not implemented.

## 3. Requirements 需求

1.发起一个HTTP请求（评论或者转发 类似），获取到返回的HTML文本，并将文本转换为HEX

2.实现函数HTTP_HEX_ANALYZER（HTTP_HEX），该函数负责解析HTTP文档转换成HEX码的结果，通过解析，获取到里面的转发（或评论）下的头像URL、昵称和评论。
（注意：该解析过程（即函数内部）不能使用非 NO_STD的库）

3.HTTP_HEX_ANALYZER输出结果：生成一个vector组，里面包含一些struct，每个struct包含头像URL、昵称、和评论三个key/value数据



## 4. Specifications 细化

1.基于HTTP返回的HTML内容可能会不可读，需要优先测试

2.只需找到对应DIV（评论或者转发）下的头像

3.该HTTP请求是基于公开链接，无需登录无需授权。

