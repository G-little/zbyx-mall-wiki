# 优惠券相关接口

[TOC]
## 修订记录
----
日期 | 作者 | 修订类型 | 修订内容 | 版本|
---- | ---- | ---- | ---- | ---- |
2020年07月03日|冷立纲|A|新增设计方案|1.0|

> 【修订类型：A-新增  M-修改 D-删除】

## 背景

优惠券相关接口

## 产品说明



## 关键流程说明

## 接口说明






#### 1.1 领取优惠券

##### 接口说明

根据优惠券ID领取优惠券

##### 请求说明

| http 请求方式          | get     |
|:------------- |:---------------:|
| url      | /coupon/receive |

#####  输入参数

| 参数          |必选             | 类型       | 参数说明        | 备注          |
|:-------------|:---------------:|:-------------|:-------------|:-------------|
|  couponId      | 是|  int  |  优惠券ID | |


#####  错误说明

1. 优惠券已经领取过
2. 优惠券已领完


#####  返回实例
```json
    
    {
    "c": 0,
    "m": null,
    "d": {

    }
}

```


#### 1.2 分页查询优惠券商品

##### 接口说明

根据优惠券ID获取可使用优惠券商品

##### 请求说明

| http 请求方式          | get     |
|:------------- |:---------------:|
| url      | /coupon/goods/list |

#####  输入参数

| 参数          |必选             | 类型       | 参数说明        | 备注          |
|:-------------|:---------------:|:-------------|:-------------|:-------------|
|  couponId      | 是|  int  |  优惠券ID | |


#####  错误说明

1. 优惠券已经领取过
2. 优惠券已领完


#####  返回实例
```json
    
    {
    "c": 0,
    "m": null,
    "d": {

    }
}

```


