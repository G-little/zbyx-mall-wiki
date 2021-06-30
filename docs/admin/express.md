# 物流管理后台接口

[TOC]
## 修订记录
----
日期 | 作者 | 修订类型 | 修订内容 | 版本|
---- | ---- | ---- | ---- | ---- |
2020年07月03日|冷立纲|A|新增设计方案|1.0|

> 【修订类型：A-新增  M-修改 D-删除】

## 背景

物流接口文档

## 产品说明



## 关键流程说明

## 接口说明

## 渠道管理

-------



#### 1.0 渠道列表

##### 接口说明

扫码取件

##### 请求说明

| http 请求方式          | get  |
|:------------- |:---------------:|
| url      |/admin/channel/list |

#####  输入参数

| 参数          |必选             | 类型       | 参数说明        | 备注          |
|:-------------|:---------------:|:-------------|:-------------|:-------------|
| code      | 否 | string  |    |   |
| page     | 否 | int  |  分页   |   |
| limit     | 否 | int  |  分页条数   |   |


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
                "id": 1, // id
                "code": "nongchuangke", //农创客
                "name": "农创客", //农创客 
                "addTime": null,  //添加时间
                "deleted": false  // 删除状态
            }
        ],
        "end": true,
        "totalPage": 1,
        "startIndex": 0,
        "empty": false
    }
}

```


#### 1.1 渠道详情

##### 接口说明

扫码取件

##### 请求说明

| http 请求方式          | get  |
|:------------- |:---------------:|
| url      |/admin/channel/read |

#####  输入参数

| 参数          |必选             | 类型       | 参数说明        | 备注          |
|:-------------|:---------------:|:-------------|:-------------|:-------------|
| id      | 是 | int  |    |   |

#####  错误说明





#####  返回实例
```json
{
    "c": 0,
    "m": null,
    "d": {
        "id": 1,
        "code": "nongchuangke", 
        "name": "农创客",
        "addTime": null,
        "deleted": false
    }
}

```



#### 1.2 创建渠道

##### 接口说明

创建渠道

##### 请求说明

| http 请求方式          | post json |
|:------------- |:---------------:|
| url      |/admin/channel/create |

#####  输入参数

| 参数          |必选             | 类型       | 参数说明        | 备注          |
|:-------------|:---------------:|:-------------|:-------------|:-------------|
| name      | 是 | string  | 名称    |   |
| code      | 是 | string  | 代号    |   |


#####  请求实例

```json
{
    "name":"test",
    "code":"xxxxx"
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


#### 1.3 删除渠道

##### 接口说明

创建渠道

##### 请求说明

| http 请求方式          | post json |
|:------------- |:---------------:|
| url      |/admin/channel/delete |

#####  输入参数

| 参数          |必选             | 类型       | 参数说明        | 备注          |
|:-------------|:---------------:|:-------------|:-------------|:-------------|
| id      | 是 | string  | 渠道ID    |   |


#####  请求实例

```json
{
    "id":"2"
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



#### 1.4 更新渠道

##### 接口说明

更新渠道

##### 请求说明

| http 请求方式          | post json |
|:------------- |:---------------:|
| url      |/admin/channel/update |

#####  输入参数

| 参数          |必选             | 类型       | 参数说明        | 备注          |
|:-------------|:---------------:|:-------------|:-------------|:-------------|
| id      | 是 | int  | 渠道ID    |   |
| name      | 否 | string  | 名称    |   |
| code      | 否 | string  | 代号    |   |


#####  请求实例

```json
{
    "id":2,
    "name":"test",
    "code":"xxxxx"
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





## 订单管理

-------



#### 2.0 订单列表

##### 接口说明

2.1 订单列表

##### 请求说明

| http 请求方式          | get  |
|:------------- |:---------------:|
| url      |/admin/logistics_order/list |

#####  输入参数

| 参数          |必选             | 类型       | 参数说明        | 备注          |
|:-------------|:---------------:|:-------------|:-------------|:-------------|
| sn      | 否 | string  |  快递单号  |   |
| channel      | 否 | int  |  渠道号  |   |
| page     | 否 | int  |  分页   |   |
| limit     | 否 | int  |  分页条数   |   |


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
        "totalPage": 1,
        "startIndex": 0,
        "empty": false
    }
}

```


#### 2.1 订单详情

##### 接口说明

扫码取件

##### 请求说明

| http 请求方式          | get  |
|:------------- |:---------------:|
| url      |/admin/logistics_order/read |

#####  输入参数

| 参数          |必选             | 类型       | 参数说明        | 备注          |
|:-------------|:---------------:|:-------------|:-------------|:-------------|
| id      | 是 | string  |   物流单号  |   |

#####  错误说明





#####  返回实例
```json
{
    "c": 0,
    "m": null,
    "d": {
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
}

```



#### 2.2 创建订单

##### 接口说明

创建渠道

##### 请求说明

| http 请求方式          | post json |
|:------------- |:---------------:|
| url      |/admin/logistics_order/create |

#####  输入参数


#####  请求实例

```json
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


#### 2.3 删除订单

##### 接口说明

创建渠道

##### 请求说明

| http 请求方式          | post json |
|:------------- |:---------------:|
| url      |/admin/logistics_order/delete |

#####  输入参数

| 参数          |必选             | 类型       | 参数说明        | 备注          |
|:-------------|:---------------:|:-------------|:-------------|:-------------|
| sn      | 是 | string  | 名称    |  快递单号  |



#####  请求实例

```json
{
    "sn":"2"
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



#### 2.4 更新订单

##### 接口说明

更新订单

##### 请求说明

| http 请求方式          | post json |
|:------------- |:---------------:|
| url      |/admin/logistics_order/update |

#####  输入参数


#####  请求实例

```json
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


#### 2.5 分配快递员

##### 接口说明

分配快递员

##### 请求说明

| http 请求方式          | post json |
|:------------- |:---------------:|
| url      |/admin/logistics_order/assign_expressman |

#####  输入参数


#####  请求实例

```json
{
        "sn": "BBB",
        "xgetUid": null, // 揽收人
        "estimateTime": null  // 预计送达时间 yyyy-MM-dd HH:mm:ss

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

### 3 快递员管理


-------


#### 3.0 快递员列表

##### 接口说明

快递员列表

##### 请求说明

| http 请求方式          | get  |
|:------------- |:---------------:|
| url      |/admin/expressman/list |

#####  输入参数

| 参数          |必选             | 类型       | 参数说明        | 备注          |
|:-------------|:---------------:|:-------------|:-------------|:-------------|
| code      | 否 | string  |    |   |
| page     | 否 | int  |  分页   |   |
| limit     | 否 | int  |  分页条数   |   |


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
                "uid": 10053, // 用户ID
                "avatar": "https://thirdwx.qlogo.cn/mmopen/vi_32/Q0j4TwGTfTIKFlBJWNvX2ibN3heYPbXou5uJBZWNoJfnOicVc958XhhjnB2YDOX1E4msicbJy92Ve5Ubd0PML2pWg/132",
                "name": "郭明山", // 用户名
                "gender": 1, 
                "birthday": null,
                "status": 0,
                "mobile": "18731355555", // 手机号
                "createTime": 1616144378080, //创建时间
                "updateTime": null,
                "vipStartTime": null,
                "vipEndTime": null,
                "userSource": "MINI",
                "level": null,
                "vipTotalMillis": null,
                "buyTimes": null,
                "employeeType": null,
                "settleMethod": null,
                "inviteCode": null,
                "inviteUid": null,
                "groupAdmin": false,
                "employeeCode": null, // 员工码
                "vip": false,
                "vipTotalDays": 0,
                "remainDays": 0
            }
        ],
        "end": false,
        "totalPage": 45,
        "startIndex": 0,
        "empty": false
    }
}

```


#### 3.1 快递员详情

##### 接口说明

扫码取件

##### 请求说明

| http 请求方式          | get  |
|:------------- |:---------------:|
| url      |/admin/expressman/read |

#####  输入参数

| 参数          |必选             | 类型       | 参数说明        | 备注          |
|:-------------|:---------------:|:-------------|:-------------|:-------------|
| id      | 是 | int  |    |   |

#####  错误说明





#####  返回实例
```json
{
    "c": 0,
    "m": null,
    "d": {
        "uid": 10053, // 用户ID
        "avatar": "https://thirdwx.qlogo.cn/mmopen/vi_32/Q0j4TwGTfTIKFlBJWNvX2ibN3heYPbXou5uJBZWNoJfnOicVc958XhhjnB2YDOX1E4msicbJy92Ve5Ubd0PML2pWg/132",
        "name": "郭明山", // 用户名
        "gender": 1, 
        "birthday": null,
        "status": 0,
        "mobile": "18731355555", // 手机号
        "createTime": 1616144378080, //创建时间
        "updateTime": null,
        "vipStartTime": null,
        "vipEndTime": null,
        "userSource": "MINI",
        "level": null,
        "vipTotalMillis": null,
        "buyTimes": null,
        "employeeType": null,
        "settleMethod": null,
        "inviteCode": null,
        "inviteUid": null,
        "groupAdmin": false,
        "employeeCode": null, // 员工码
        "vip": false,
        "vipTotalDays": 0,
        "remainDays": 0
    }
}

```



#### 3.2 创建快递员

##### 接口说明

创建渠道

##### 请求说明

| http 请求方式          | post json |
|:------------- |:---------------:|
| url      |/admin/expressman/create |

#####  输入参数


#####  请求实例

```json
{
    "uid": 10053, // 用户ID
    "avatar": "https://thirdwx.qlogo.cn/mmopen/vi_32/Q0j4TwGTfTIKFlBJWNvX2ibN3heYPbXou5uJBZWNoJfnOicVc958XhhjnB2YDOX1E4msicbJy92Ve5Ubd0PML2pWg/132",
    "name": "郭明山", // 用户名
    "gender": 1, 
    "birthday": null,
    "status": 0,
    "mobile": "18731355555", // 手机号
    "createTime": 1616144378080, //创建时间
    "updateTime": null,
    "vipStartTime": null,
    "vipEndTime": null,
    "userSource": "MINI",
    "level": null,
    "vipTotalMillis": null,
    "buyTimes": null,
    "employeeType": null,
    "settleMethod": null,
    "inviteCode": null,
    "inviteUid": null,
    "groupAdmin": false,
    "employeeCode": null, // 员工码
    "vip": false,
    "vipTotalDays": 0,
    "remainDays": 0
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


#### 3.3 删除快递员

##### 接口说明

创建渠道

##### 请求说明

| http 请求方式          | post json |
|:------------- |:---------------:|
| url      |/admin/expressman/delete |

#####  输入参数

| 参数          |必选             | 类型       | 参数说明        | 备注          |
|:-------------|:---------------:|:-------------|:-------------|:-------------|
| uid      | 是 | string  | 渠道ID    |   |


#####  请求实例

```json
{
    "uid":"2"
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



#### 3.4 更新快递员

##### 接口说明

更新渠道

##### 请求说明

| http 请求方式          | post json |
|:------------- |:---------------:|
| url      |/admin/expressman/update |

#####  输入参数



#####  请求实例

```json
{
    "uid": 10053, // 用户ID
    "avatar": "https://thirdwx.qlogo.cn/mmopen/vi_32/Q0j4TwGTfTIKFlBJWNvX2ibN3heYPbXou5uJBZWNoJfnOicVc958XhhjnB2YDOX1E4msicbJy92Ve5Ubd0PML2pWg/132",
    "name": "郭明山", // 用户名
    "gender": 1, 
    "birthday": null,
    "status": 0,
    "mobile": "18731355555", // 手机号
    "createTime": 1616144378080, //创建时间
    "updateTime": null,
    "vipStartTime": null,
    "vipEndTime": null,
    "userSource": "MINI",
    "level": null,
    "vipTotalMillis": null,
    "buyTimes": null,
    "employeeType": null,
    "settleMethod": null,
    "inviteCode": null,
    "inviteUid": null,
    "groupAdmin": false,
    "employeeCode": null, // 员工码
    "vip": false,
    "vipTotalDays": 0,
    "remainDays": 0
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






















