# PBP1

## 1.  Summary 概述

开发一个支付宝抽奖小程序，当用户使用区块身份头像登录时，即可开始抽奖

## 2.  Status 状态

- [x] This PBP is implemented.

## 3. Requirements 需求
1. 使用支付宝小程序的用户信息接口 https://opendocs.alipay.com/mini/api/ch8chh 获取到用户头像
2. 使用区块身份解析接口，获取到用户DID
3. 参照 https://github.com/landluck/lucky_wheel 实现小程序前端的界面展示，并在合适的地方展示出获取到的用户DID
4. 将奖品修改为不同数量的PRA

## 4. Specifications 细化
1. 需要按照支付宝小程序的要求来进行用户头像的获取
2. 解析使用的图片需要为原尺寸大小的图
3. 为了避免重复造轮子，抽奖页面可以使用开源的，并通过类似vue转支付宝小程序等工具完成转换。
4. 未中奖概率改成0

## 5. Contributer

- [yokosogithub](https://github.com/yokosogithub) [alipay-lottery](https://github.com/ProChain/alipay-lottery)
