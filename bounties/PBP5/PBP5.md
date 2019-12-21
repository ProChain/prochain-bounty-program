# PBP5

## 1.  Summary 概述

微博解析器:

使用RUST发起HTTP请求，并通过分析请求内返回内容，解析出其中的用户头像URL地址

- 某条微博的转发URL：https://weibo.com/1642591402/IkWAEyqxy?type=repost
- 某条微博的评论URL：https://weibo.com/1642591402/IkWAEyqxy?type=comment

## 2.  Status 状态

- [ ] This PBP is not implemented.

## 3. Requirements 需求

1. **注意**：因为要集成到substrate wasm运行环境，**要求只能使用rust no_std库（如core::str），以及vec\<u8\>**

2. **注意**：假设已经发起一个HTTP请求（评论或者转发 类似），获取到了返回的HTML文本，**HTTP请求相关代码不需要实现**

3. **注意**：rust no_std对json解析的库，可以借鉴使用 https://github.com/jingleizhang/simple-json，相关解析使用代码在https://github.com/ProChain/prochain-node/blob/master/bin/node/runtime/src/oracle.rs

4. **核心需求**：通过读取步骤3已获得的文本，解析到里面的转发（或评论）下的头像URL、昵称和评论。

## 4. Specifications 细化

1. 基于HTTP返回的HTML内容可能会不可读，需要优先测试

2. 只需找到对应DIV（评论或者转发）下的头像

3. 该HTTP请求是基于公开链接，无需登录无需授权。

4. 需要实现以下输入输出函数代码：
  4.1 输入：假设已经通过https获取到网页，内容以文本形式存储为core::str
  4.2 输出：Vec<struct>， struct含头像URL、昵称和评论
  

