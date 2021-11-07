# 中优商城管理后台接口

[TOC]
## 修订记录
----
日期 | 作者 | 修订类型 | 修订内容 | 版本|
---- | ---- | ---- | ---- | ---- |
2021年11月06日|冷立纲|A|新增设计方案|1.0.1|

> 【修订类型：A-新增  M-修改 D-删除】

## 背景

中优商城管理后台接口

## 产品说明



## 关键流程说明

## 接口说明



### 1. 酿化设置


-------

#### 字段说明

| 字段 | 类型 | 说明 | 备注 |
| --- | --- | --- | --- |
| id | int | 配置ID |  |
| yearFee | double | 每年费用 |  |
| limitYear | int | 最低年限 |  |






#### 1.1.0 获取酿化设置信息

##### 接口说明

商户详情

##### 请求说明

| http 请求方式          | get     |
|:------------- |:---------------:|
| url      | /admin/aging_setting/read |

#####  输入参数

无

#####  错误说明




#####  返回实例

```json
    
{
    "c": 0,
    "m": null,
    "d": {
        "id": 1,
        "yearFee": "每年费用",
        "limitYear": 2,
        "addTime": null
    }
}

```



#### 1.1.2 更新酿化设置信息

##### 接口说明

更新商户

##### 请求说明

| http 请求方式          | post  json   |
|:------------- |:---------------:|
| url      | /admin/aging_setting/update |

#####  输入参数

| 参数          |必选             | 类型       | 参数说明        | 备注          |
|:-------------|:---------------:|:-------------|:-------------|:-------------|
| yearFee | double | 每年费用 |  |
| limitYear | int | 最低年限 |  |


#####  请求实例

```json

{
    "yearFee": "每年费用",
    "limitYear": 2

}

```

#####  错误说明




#####  返回实例
```json
    
{
    "c": 0,
    "m": null,
    "d": {
        "id": null,
        "yearFee": "2.00",
        "limitYear": 2,
        "addTime": "2021-11-07 08:00:35"
    }
}

```







### 2. 酿化管理


-------

#### 字段说明

| 字段 | 类型 | 说明 | 备注 |
| --- | --- | --- | --- |
| id | int | 订单ID |  |
| user | json | 用户信息 |  |
| addTime | string | 添加时间 |  |
| agingFee | double | 酿化费用 |  |
| agingEndtime | string | 酿化截止时间 |  |
| goodsList | json array | 商品信息列表 |  |

#### 2.1.0 酿化管理列表

##### 接口说明



##### 请求说明

| http 请求方式          |get             |
|:------------- |:---------------:|
| url      | /admin/aging/list |

#####  输入参数

| 参数          |必选             | 类型       | 参数说明        | 备注          |
|:-------------|:---------------:|:-------------|:-------------|:-------------|
| page      | 否| int  |  分页 |   |
| limit      | 否| int  |  单页条数 |   |
| userId      | 否| int  | 用户ID | |
| name      | 否| string  |  名字 | |
| mobile      | 否| string  |  手机号 | |
| orderSn      | 否| string  |  订单流水号 | |
| type      | 否| string  |  类型 | 0 全部  -1 欠费 1 付费 |

#####  错误说明





#####  返回实例
```json

{
    "c": 0,
    "m": null,
    "d": {
        "pageSize": 1,
        "currentPage": 1,
        "list": [
            {
                "id": 208,
                "orderSn": "20210831520371",
                "user": {
                    "uid": 10070,
                    "name": "青翼",
                    "mobile": "13810163978"
                }, //用户信息
                "addTime": "2021-08-31 17:11:28", //添加时间
                "agingFee": "0.00", //费用
                "agingEndtime": null, //酿化截止时间
                "goodsList": [ //商品信息
                    {
                        "id": 216,
                        "orderId": null,
                        "goodsId": null,
                        "goodsName": "侨宝 2020年七月果200g深色罐装 新会小青柑",
                        "goodsSn": null,
                        "productId": null,
                        "number": 1,
                        "price": "15.00",
                        "specifications": [
                            "标准"
                        ],
                        "picUrl": "https://zhongyou-mall.oss-cn-beijing.aliyuncs.com/mx6zwyej8b40rejjnord.jpg",
                        "comment": null,
                        "addTime": null,
                        "updateTime": null,
                        "brief": null,
                        "gallery": null,
                        "videos": null,
                        "tags": null,
                        "aftersaleId": null,
                        "handleOption": null
                    }
                ]
            }
        ],
        "end": false,
        "empty": false,
        "startIndex": 0,
        "totalPage": 158
    }
}


```





#### 2.1.2 酿化详情

##### 接口说明

商户详情

##### 请求说明

| http 请求方式          | get     |
|:------------- |:---------------:|
| url      | /admin/aging/read |

#####  输入参数

| 参数          |必选             | 类型       | 参数说明        | 备注          |
|:-------------|:---------------:|:-------------|:-------------|:-------------|
| id      | 是|  int  |  订单ID  |  |

#####  错误说明




#####  返回实例

```json
    
{
    "c": 0,
    "m": null,
    "d": {
        "id": 208,
        "orderSn": "20210831520371",
        "user": {
            "uid": 10070,
            "name": "青翼",
            "mobile": "13810163978"
        },
        "addTime": "2021-08-31 17:11:28",
        "agingFee": "0.00",
        "agingEndtime": null,
        "goodsList": [
            {
                "id": 216,
                "orderId": null,
                "goodsId": null,
                "goodsName": "侨宝 2020年七月果200g深色罐装 新会小青柑",
                "goodsSn": null,
                "productId": null,
                "number": 1,
                "price": "15.00",
                "specifications": [
                    "标准"
                ],
                "picUrl": "https://zhongyou-mall.oss-cn-beijing.aliyuncs.com/mx6zwyej8b40rejjnord.jpg",
                "comment": null,
                "addTime": null,
                "updateTime": null,
                "brief": null,
                "gallery": null,
                "videos": null,
                "tags": null,
                "aftersaleId": null,
                "handleOption": null
            }
        ]
    }
}

```



### 3. 出仓管理


-------

#### 字段说明

| 字段 | 类型 | 说明 | 备注 |
| --- | --- | --- | --- |
| orderId | int | 订单ID |  |
| user | json | 用户信息 |  |
| addTime | string | 添加时间 |  |
| requestTime | string | 申请时间 |  |
| agingEndtime | string | 酿化截止时间 |  |
| orderStatus | int | 订单状态 |  |
| orderStatusText | string | 订单状态描述 |  |

#### 3.1.0 出仓管理列表

##### 接口说明



##### 请求说明

| http 请求方式          |get             |
|:------------- |:---------------:|
| url      | /admin/out_request/list |

#####  输入参数

| 参数          |必选             | 类型       | 参数说明        | 备注          |
|:-------------|:---------------:|:-------------|:-------------|:-------------|
| page      | 否| int  |  分页 |   |
| limit      | 否| int  |  单页条数 |   |
| userId      | 否| int  | 用户ID | |
| name      | 否| string  |  名字 | |
| mobile      | 否| string  |  手机号 | |
| orderSn      | 否| string  |  订单流水号 | |
| type      | 否| string  |  类型 | 0 全部  -1 欠费 1 付费 |
| orderStatusArray      | 否| 订单状态数组  |  订单状态列表 | |

#####  错误说明





#####  返回实例
```json

{
    "c": 0,
    "m": null,
    "d": {
        "pageSize": 10,
        "currentPage": 1,
        "list": [
            {
                "user": { //用户信息
                    "uid": 10070,
                    "name": "青翼",
                    "mobile": "13810163978"
                },
                "orderId": 208, //订单号
                "addTime": "2021-08-31 17:11:28", //添加时间 
                "requestTime": "2021-10-15 10:00:00", //申请时间
                "orderStatus": 103,
                "orderStatusText": "已取消(系统)" //订单状态
            }
        ],
        "end": true,
        "empty": false,
        "startIndex": 0,
        "totalPage": null
    }
}

```





#### 3.1.2 出仓详情

##### 接口说明

商户详情

##### 请求说明

| http 请求方式          | get     |
|:------------- |:---------------:|
| url      | /admin/out_request/read |

#####  输入参数

| 参数          |必选             | 类型       | 参数说明        | 备注          |
|:-------------|:---------------:|:-------------|:-------------|:-------------|
| id      | 是|  int  |  订单ID  |  |

#####  错误说明




#####  返回实例

```json
    
{
    "c": 0,
    "m": null,
    "d": {
        "user": { //用户信息
            "uid": 10070,
            "name": "青翼",
            "mobile": "13810163978"
        },
        "order": { //订单信息
            "id": 208,
            "userId": 10070,
            "orderSn": "20210831520371",
            "orderStatus": 103,
            "aftersaleStatus": 0,
            "consignee": "李青",
            "mobile": "13810163978",
            "address": "北京市市辖区丰台区 请输入地址六里桥",
            "message": "",
            "goodsPrice": "15.00",
            "freightPrice": "0.00",
            "couponPrice": "0.00",
            "integralPrice": "0.00",
            "grouponPrice": "0.00",
            "orderPrice": "15.00",
            "actualPrice": "15.00",
            "payId": null,
            "payTime": null,
            "shipSn": null,
            "shipChannel": null,
            "shipTime": null,
            "refundAmount": null,
            "refundType": null,
            "refundContent": null,
            "refundTime": null,
            "confirmTime": null,
            "comments": 0,
            "endTime": "2021-08-31 17:41:28",
            "addTime": "2021-08-31 17:11:28",
            "updateTime": "2021-08-31 17:41:28",
            "deleted": false,
            "payType": "WX_MP",
            "agingEndtime": null,
            "offlinePayId": null,
            "offlinePayStatus": null
        },
        "goodsList": [ //商品信息
            {
                "id": 216,
                "orderId": null,
                "goodsId": null,
                "goodsName": "侨宝 2020年七月果200g深色罐装 新会小青柑",
                "goodsSn": null,
                "productId": null,
                "number": 1,
                "price": "15.00",
                "specifications": [
                    "标准"
                ],
                "picUrl": "https://zhongyou-mall.oss-cn-beijing.aliyuncs.com/mx6zwyej8b40rejjnord.jpg",
                "comment": null,
                "addTime": null,
                "updateTime": null,
                "brief": null,
                "gallery": null,
                "videos": null,
                "tags": null,
                "aftersaleId": null,
                "handleOption": null
            }
        ],
        "agingFee": "0.00"
    }
}

```









