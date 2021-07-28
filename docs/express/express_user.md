# 物流用户端接口文档

[TOC]
## 修订记录
----
日期 | 作者 | 修订类型 | 修订内容 | 版本|
---- | ---- | ---- | ---- | ---- |
2020年07月03日|冷立纲|A|新增设计方案|1.0|

> 【修订类型：A-新增  M-修改 D-删除】

## 背景

物流用户端接口文档

## 产品说明



## 关键流程说明

## 接口说明

### 登录流程说明


#### 登录头说明

_将accessToken作为请求头 Authorization: 'token'  发送请求即可获取权限_

#### 手机号登录

1. 调用短信发送接口发送短信验证 /user/sendsms 
2. 手机号注册登录获取token /user/joinin 
3. 将accessToken作为请求头 Authorization: 'token'  发送请求

#### 微信登录

1. 微信授权回调接口 /oauth2/weixin/callback 获取登录token
2. 将accessToken作为请求头 Authorization: 'token'  发送请求





#### 1.0 地址列表接口

##### 接口说明



##### 请求说明

| http 请求方式          |get             |
|:------------- |:---------------:|
| url      | /u/address/list |

#####  输入参数

| 参数          |必选             | 类型       | 参数说明        | 备注          |
|:-------------|:---------------:|:-------------|:-------------|:-------------|
| page      | 否| int  |  分页 |   |
| limit      | 否| int  |  单页条数 |   |
#####  错误说明





#####  返回实例
```json
{
    "c": 0,
    "m": null,
    "d": {
        "pageSize": 8,
        "currentPage": 1,
        "list": [
            {
                "user": "zhangsan", //姓名
                "mobile": "15201008961", //手机号
                "province": "beijign", //省份
                "city": "beijing", //城市
                "area": "chaoyang", // 区
                "detail": "测试", //详细地址
                "longitude": null, //经度
                "latitude": null, //纬度
                "addr": "北京市朝阳区测试" //完整地址
            }
        ],
        "end": true,
        "empty": false,
        "startIndex": 0,
        "totalPage": 1
    }
}

```


#### 1.1 智能地址识别

##### 接口说明



##### 请求说明

| http 请求方式          |get             |
|:------------- |:---------------:|
| url      | /u/address/extract |

#####  输入参数

| 参数          |必选             | 类型       | 参数说明        | 备注          |
|:-------------|:---------------:|:-------------|:-------------|:-------------|
| text      | 市 | string  |   地址文本 |   |
#####  错误说明





#####  返回实例
```json
{
    "c": 0,
    "m": null,
    "d": {
        "house": "6栋",  //楼号
        "poi": "规划路罗西住宅区9组团", //poi 信息
        "town": "状元街道", //街道
        "city": "温州市", //城市
        "area": "龙湾区", //区
        "mobile": "18170371112", //手机号
        "detail": "规划路罗西住宅区9组团6栋", //详情
        "user": "吴鸿", //用户名
        "provice": "浙江省" //省份
    }
}

```





#### 1.2 快递费预估

##### 接口说明



##### 请求说明

| http 请求方式          |get             |
|:------------- |:---------------:|
| url      | /u/order/evaluation |

#####  输入参数

| 参数          |必选             | 类型       | 参数说明        | 备注          |
|:-------------|:---------------:|:-------------|:-------------|:-------------|
| fromLongitude      | 是| double  |   来源经度 |   |
| fromLatitude      | 是| double  |   来源纬度 |   |
| toLongitude      | 是| double  |   目的经度 |   |
| toLatitude      | 是| double  |   目的纬度 |   |
| weight      | 是| int  |   重量 |   |
#####  错误说明





#####  返回实例

```json
{
    "c": 0,
    "m": null,
    "d": 48.0 // 估价 元
}

```




#### 1.3 创建订单

##### 接口说明



##### 请求说明

| http 请求方式          |post             |
|:------------- |:---------------:|
| url      | /u/order/create |

#####  输入参数

| 参数          |必选             | 类型       | 参数说明        | 备注          |
|:-------------|:---------------:|:-------------|:-------------|:-------------|
| fromLongitude      | 是| double  |   来源经度 |   |
| fromLatitude      | 是| double  |   来源纬度 |   |
| toLongitude      | 是| double  |   目的经度 |   |
| toLatitude      | 是| double  |   目的纬度 |   |
| fromUser      | 是| string  |   发件人 |   |
| fromMobile      | 是| string  |   发件人手机号 |   |
| toUser      | 是| string  |   收件人 |   |
| toMobile      | 是| string  |   收件人手机号 |   |
| itemComment      | 是| string  |   物品信息 |   |
| fromProvince      | 否 | string  |   来源省份 |   |
| fromCity      | 否 | string  |   来源城市 |   |
| fromArea      | 否 | string  |   来源地区 |   |
| fromDetail      | 否 | string  |   来源详细地址 |   |
| fromAddr      | 否 | string  |   来源完整地址 |   |
| toProvince      | 否 | string  |   目的省份 |   |
| toCity      | 否 | string  |   目的城市 |   |
| toArea      | 否 | string  |   目的地区 |   |
| toDetail      | 否 | string  |   目的详细地址 |   |
| toAddr      | 否 | string  |   目的完整地址 |   |
| num      | 否 | int  |   物品数量  | 最小值1   |
| comments      | 否 | string  |   备注  | |
| expressType      | 否 | int  |    1 取件 0 送件  | 默认 送件 |
| getMinTime      | 否 | long  |     最早取件时间  |  0 立刻 |
| getMaxTime      | 否 | long  |     最晚取件时间  |   |

#####  错误说明





#####  返回实例

```json
{
    "c": 0,
    "m": null,
    "d": {
        "payOrderId": "210728160628475131003",  //订单号
        "outPayOrderId":  "prepay_id=wx28160647996790677d5b39e4077bfa0000",
        "callPayInfo": "{\"appId\":\"wx10becc5288b64881\",\"nonceStr\":\"xhHtKgBx1OXSQQ1g\",\"packageValue\":\"prepay_id=wx28160647996790677d5b39e4077bfa0000\",\"paySign\":\"5CF39FC472949B7E5FF0BF409156D12F\",\"signType\":\"MD5\",\"timeStamp\":\"1627459608\"}",  //支付参数
        "payCallbackInfo": null
    }
}

```



#### 1.4 取消订单

##### 接口说明



##### 请求说明

| http 请求方式          |post             |
|:------------- |:---------------:|
| url      | /u/order/cancel |

#####  输入参数

| 参数          |必选             | 类型       | 参数说明        | 备注          |
|:-------------|:---------------:|:-------------|:-------------|:-------------|
| sn      | 是 |  string  |     物流单号  |   |

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



#### 1.5 重新支付

##### 接口说明



##### 请求说明

| http 请求方式          |post             |
|:------------- |:---------------:|
| url      | /u/order/prepay |

#####  输入参数

| 参数          |必选             | 类型       | 参数说明        | 备注          |
|:-------------|:---------------:|:-------------|:-------------|:-------------|
| sn      | 是 |  string  |     物流单号  |   |
| payType      | 是 |  string  |     支付方式  | 固定值 WX_MP   |
| openId      | 是 |  string  |      微信openId  | |

#####  错误说明





#####  返回实例

```json
{
    "c": 0,
    "m": null,
    "d":  {
        "payOrderId": "210728160628475131003",  //订单号
        "outPayOrderId":  "prepay_id=wx28160647996790677d5b39e4077bfa0000",
        "callPayInfo": "{\"appId\":\"wx10becc5288b64881\",\"nonceStr\":\"xhHtKgBx1OXSQQ1g\",\"packageValue\":\"prepay_id=wx28160647996790677d5b39e4077bfa0000\",\"paySign\":\"5CF39FC472949B7E5FF0BF409156D12F\",\"signType\":\"MD5\",\"timeStamp\":\"1627459608\"}",  //支付参数
        "payCallbackInfo": null
    }
}

```




#### 1.6 订单列表

##### 接口说明



##### 请求说明

| http 请求方式          |get             |
|:------------- |:---------------:|
| url      |/u/order/list |

#####  输入参数

| 参数          |必选             | 类型       | 参数说明        | 备注          |
|:-------------|:---------------:|:-------------|:-------------|:-------------|
| page      | 否| int  |  分页 |   |
| limit      | 否| int  |  单页条数 |   |
| status      | 否| int  |  状态 | //状态 0 初始 100 疑难 102 揽收  207 拒签 205 退签 200 签收 400 派件 401 转发 404 退回   |
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
                "sn": "BBB",
                "fromUser": "zhangsan", //来源用户名
                "fromMobile": "15201008961", //来源用户手机号
                "fromProvince": "beijign", //来源省份
                "fromCity": "beijing",//来源城市
                "fromArea": "chaoyang", //来源地区
                "fromDetail": "测试", //来源详情
                "fromLongitude": null, //来源经度
                "fromLatitude": null, //来源维度
                "fromAddr": "北京市朝阳区测试", //来源详细地址
                "toUser": "laoliu", //目标用户名
                "toMobile": "15201008963" , //目标手机号
                "toProvince": "北京", //目标省份
                "toCity": "北京", //目标城市
                "toArea": "东城", //目标地区
                "toDetail": "姚家园路", //目标详情
                "toLongitude": null, //目标经度
                "toLatitude": null, //目标维度
                "toAddr": "北京市朝阳区东城测试", //目标完整地址
                "itemComment": "我是测试", //包裹说明
                "weight": null, //重量 kg
                "num": 1, //数量 个
                "status": 0, //状态 0 初始 100 疑难 102 揽收  207 拒签 205 退签 200 签收 400 派件 401 转发 404 退回
                "images": null,
                "type": 0, // 0 系统 1 快递员揽收
                "xgetUid": null, // 揽收人
                "deliveryUid": null, //派件人
                "addTime": null, // 下单时间
                "xgetTime": null, // 取件时间
                "arriveTime": null, // 送达时间
                "freightFee": null, // 运费
                "payStatus": 1, // 支付状态 0 未支付 1 已支付
                "comments": "测试", // 备注
                "channel": null, //渠道
                "estimateTime": null  // 预计送达时间
            }
        ],
        "end": true,
        "empty": false,
        "startIndex": 0,
        "totalPage": null
    }
}































