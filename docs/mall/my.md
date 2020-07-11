# 个人中心相关接口

[TOC]
## 修订记录
----
日期 | 作者 | 修订类型 | 修订内容 | 版本|
---- | ---- | ---- | ---- | ---- |
2020年07月03日|冷立纲|A|新增设计方案|1.0|

> 【修订类型：A-新增  M-修改 D-删除】

## 背景

个人中心相关接口

## 产品说明



## 关键流程说明

## 接口说明


#### 1.0 我的个人中心

##### 接口说明

我的个人中心页

##### 请求说明

| http 请求方式          | get     |
|:------------- |:---------------:|
| url      | /home/u/index |

#####  输入参数

无


#####  错误说明




#####  返回实例
```json
    
    {
    "c": 0,
    "m": null,
    "d": {
        "user": {
            "nickname": null,  //昵称
            "avatar": "/c/d/e", //头像
            "vip": false, //是否VIP
            "level": null, //vip 等级
            "startTime": null, //开始时间
            "endTime": null //截止时间
        },
        "order": {  //订单信息
            "unpaid": 0,  //待支付
            "unship": 0, // 待发货
            "unrecv": 0, // 待收货
            "uncomment": 0 //待评论
        },
        "banner": [  //广告
            {
                "id": 8,
                "url": "http://yanxuan.nosdn.127.net/8e50c65fda145e6dd1bf4fb7ee0fcecc.jpg",
                "link": "",
                "content": "活动 母亲节5"
            }
        ],
        "wallet": {
            "couponCount": 0,  //优惠券数量
            "redEnvelopCount": 0, //红包数量
            "giftCardCount": 0 //礼品卡数量
        }
    }
}
    
```






