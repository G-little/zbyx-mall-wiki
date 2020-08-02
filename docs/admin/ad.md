# 推广管理

[TOC]
## 修订记录
----
日期 | 作者 | 修订类型 | 修订内容 | 版本|
---- | ---- | ---- | ---- | ---- |
2020年07月03日|冷立纲|A|新增设计方案|1.0|

> 【修订类型：A-新增  M-修改 D-删除】

## 背景

推广管理相关接口

## 产品说明

推广管理相关接口

## 关键流程说明



## 接口说明


#### 1.0 添加广告

##### 接口说明

添加广告

##### 请求说明

| http 请求方式          | post     |
|:------------- |:---------------:|
| url      | /admin/ad/create |

#####  输入参数


```json  

{
  "content": "string",  //描述
  "deleted": true, //是否删除
  "enabled": true, //是否开启
  "extParams": {},  //附加参数
  "idValue": 0, //跳转ID
  "link": "string", //跳转链接（H5）
  "name": "string", //标题
  "position": 0,  // 1 首页 2 活动 3 用户 
  "type": 0, //跳转类型  0:H5 1:产品详情 2:活动
  "url": "string" //图片地址 //图片地址
}

```

#####  错误说明




#####  返回实例
```json
    {
    "c": 0,
    "m": null,
    "d": {
    }
}  
```


#### 1.1 修改广告

##### 接口说明

修改广告

##### 请求说明

| http 请求方式          | post     |
|:------------- |:---------------:|
| url      | /admin/ad/update |

#####  输入参数


```json  

{
  "id":1,  //广告ID , //必填
  "content": "string",  //描述
  "deleted": true, //是否删除
  "enabled": true, //是否开启
  "extParams": {},  //附加参数
  "idValue": 0, //跳转ID
  "link": "string", //跳转链接（H5）
  "name": "string", //标题
  "position": 0,  // 1 首页 2 活动 3 用户 
  "type": 0, //跳转类型  0:H5 1:产品详情 2:活动
  "url": "string" //图片地址 //图片地址
}

```

#####  错误说明




#####  返回实例
```json
    {
    "c": 0,
    "m": null,
    "d": {
    }
}  
```




#### 1.2 添加优惠券

##### 接口说明

添加优惠券

##### 请求说明

| http 请求方式          | post     |
|:------------- |:---------------:|
| url      | /admin/coupon/create |

#####  输入参数


```json  

{
  "ccrossGoods": true,  //是否允许跨商品使用
  "days": 0,  // 有效天数
  "desc": "string",  //优惠描述
  "discount": 0, //优惠金额 
  "discountType": 0,  //优惠类型  0 默认:取 discount 优惠金额  1:满减  2:满折扣 
  "endTime": "2020-07-19T12:59:59.267Z",  //优惠券结束时间
  "goodsType": 0,  // 商品限制类型，如果0则全商品，如果是1则是类目限制，如果是2则是商品限制。
  "goodsValue": [  
    0
  ],  商品限制值，goods_type如果是0则空集合，如果是1则是类目集合，如果是2则是商品集合。
  "imageUrl": "string",  //优惠券图片
  "limit": 0,  //用户领券限制数量，如果是0，则是不限制；默认是1，限领一张.
  "min": 0,  //最少消费金额才能使用优惠券。
  "name": "string", //优惠券名称
  "rules": [
    {
      "comment": "string",   //使用规则描述
      "countType": 0,  //0:根据钱   1:根据数量
      "countValue": 0, //计数值 
      "discountType": 0, //满减类型   1:满减  2:满折扣 
      "discountValue": 0  //根据discountType 取值 钱或者折扣
    }
  ],
  "startTime": "2020-07-19T12:59:59.267Z", //优惠券开始时间
  "tag": "string",  //优惠券tag
  "timeType": 0, //有效时间限制，如果是0，则基于领取时间的有效天数days；如果是1，则start_time和end_time是优惠券有效期；
  "total": 0,   //优惠券数量，如果是0，则是无限量
  "type": 0  优惠券赠送类型，如果是0则通用券，用户领取；如果是1，则是注册赠券；如果是2，则是优惠券码兑换; 如果是3，则是无需领取直接使用 ；
}
```

#####  错误说明




#####  返回实例
```json
    {
    "c": 0,
    "m": null,
    "d": {
    }
}  
```




#### 1.2 更新优惠券

##### 接口说明

添加优惠券

##### 请求说明

| http 请求方式          | post     |
|:------------- |:---------------:|
| url      | /admin/coupon/update |

#####  输入参数


```json  

{
  "id":12,//优惠券ID
  "ccrossGoods": true,  //是否允许跨商品使用
  "days": 0,  // 有效天数
  "desc": "string",  //优惠描述
  "discount": 0, //优惠金额 
  "discountType": 0,  //优惠类型  0 默认:取 discount 优惠金额  1:满减  2:满折扣 
  "endTime": "2020-07-19T12:59:59.267Z",  //优惠券结束时间
  "goodsType": 0,  // 商品限制类型，如果0则全商品，如果是1则是类目限制，如果是2则是商品限制。
  "goodsValue": [  
    0
  ],  商品限制值，goods_type如果是0则空集合，如果是1则是类目集合，如果是2则是商品集合。
  "imageUrl": "string",  //优惠券图片
  "limit": 0,  //用户领券限制数量，如果是0，则是不限制；默认是1，限领一张.
  "min": 0,  //最少消费金额才能使用优惠券。
  "name": "string", //优惠券名称
  "rules": [
    {
      "id":12, //优惠券ID
      "comment": "string",   //使用规则描述
      "countType": 0,  //0:根据钱   1:根据数量
      "countValue": 0, //计数值 
      "discountType": 0, //满减类型   1:满减  2:满折扣 
      "discountValue": 0  //根据discountType 取值 钱或者折扣
    }
  ],
  "startTime": "2020-07-19T12:59:59.267Z", //优惠券开始时间
  "tag": "string",  //优惠券tag
  "timeType": 0, //有效时间限制，如果是0，则基于领取时间的有效天数days；如果是1，则start_time和end_time是优惠券有效期；
  "total": 0,   //优惠券数量，如果是0，则是无限量
  "type": 0  优惠券赠送类型，如果是0则通用券，用户领取；如果是1，则是注册赠券；如果是2，则是优惠券码兑换; 如果是3，则是无需领取直接使用 ；
}
```

#####  错误说明




#####  返回实例
```json
    {
    "c": 0,
    "m": null,
    "d": {
    }
}  
```



#### 1.3 优惠券详情

##### 接口说明

添加优惠券

##### 请求说明

| http 请求方式          | get     |
|:------------- |:---------------:|
| url      | /admin/coupon/read |

#####  输入参数


| 参数          |必选             | 类型       | 参数说明        | 备注          |
|:-------------|:---------------:|:-------------|:-------------|:-------------|
|  id      | 是|  int  |  优惠券ID | |



#####  错误说明




#####  返回实例

```json  

{
  "id":12,//优惠券ID
  "ccrossGoods": true,  //是否允许跨商品使用
  "days": 0,  // 有效天数
  "desc": "string",  //优惠描述
  "discount": 0, //优惠金额 
  "discountType": 0,  //优惠类型  0 默认:取 discount 优惠金额  1:满减  2:满折扣 
  "endTime": "2020-07-19T12:59:59.267Z",  //优惠券结束时间
  "goodsType": 0,  // 商品限制类型，如果0则全商品，如果是1则是类目限制，如果是2则是商品限制。
  "goodsValue": [  
    0
  ],  商品限制值，goods_type如果是0则空集合，如果是1则是类目集合，如果是2则是商品集合。
  "imageUrl": "string",  //优惠券图片
  "limit": 0,  //用户领券限制数量，如果是0，则是不限制；默认是1，限领一张.
  "min": 0,  //最少消费金额才能使用优惠券。
  "name": "string", //优惠券名称
  "rules": [
    {
      "id":12, //优惠券ID
      "comment": "string",   //使用规则描述
      "countType": 0,  //0:根据钱   1:根据数量
      "countValue": 0, //计数值 
      "discountType": 0, //满减类型   1:满减  2:满折扣 
      "discountValue": 0  //根据discountType 取值 钱或者折扣
    }
  ],
  "startTime": "2020-07-19T12:59:59.267Z", //优惠券开始时间
  "tag": "string",  //优惠券tag
  "timeType": 0, //有效时间限制，如果是0，则基于领取时间的有效天数days；如果是1，则start_time和end_time是优惠券有效期；
  "total": 0,   //优惠券数量，如果是0，则是无限量
  "type": 0  优惠券赠送类型，如果是0则通用券，用户领取；如果是1，则是注册赠券；如果是2，则是优惠券码兑换; 如果是3，则是无需领取直接使用 ；
}
```



#### 1.4 绑定商品列表

##### 接口说明

添加优惠券

##### 请求说明

| http 请求方式          | get     |
|:------------- |:---------------:|
| url      | /admin/coupon/goods_list |

#####  输入参数


| 参数          |必选             | 类型       | 参数说明        | 备注          |
|:-------------|:---------------:|:-------------|:-------------|:-------------|
|  id      | 是|  int  |  优惠券ID | |



#####  错误说明




#####  返回实例

```json  


{
    "c": 0,
    "m": null,
    "d": [
        {
            "id": 1110016,
            "name": "天然硅胶宠物除毛按摩刷",
            "picUrl": "http://yanxuan.nosdn.127.net/3bd73b7279a83d1cbb50c0e45778e6d6.png"
        }
    ]
}

```










