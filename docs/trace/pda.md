# PDA相关接口

[TOC]
## 修订记录
----
日期 | 作者 | 修订类型 | 修订内容 | 版本|
---- | ---- | ---- | ---- | ---- |
2020年07月03日|冷立纲|A|新增设计方案|1.0|

> 【修订类型：A-新增  M-修改 D-删除】

## 背景

PDA 出入库管理接口

## 产品说明



## 关键流程说明

## 接口说明


#### 登录头说明

_将accessToken作为请求头 Authorization: 'token'  发送请求即可获取权限_

#### 手机号登录

1. 手机号密码登陆 /trace/employee/login
2. 将accessToken作为请求头 Authorization: 'token'  发送请求


#### 1.0 手机号密码登陆

##### 接口说明

后台添加企业员工，根据手机号和密码可以登陆

##### 请求说明

| http 请求方式          | post     |
|:------------- |:---------------:|
| url      | /trace/employee/login |

#####  输入参数

| 参数          |必选             | 类型       | 参数说明        | 备注          |
|:-------------|:---------------:|:-------------|:-------------|:-------------|
| mobile      | 是|  string  |  手机号 |   |
| deviceId      | 是|  设备号  |  手机imei|   |
| password      | 是|  密码  |  密码 |   |




#####  错误说明




#####  返回实例
```json  
    
    {
    "c": 0,
    "m": null,
    "d": {
        "id": 2,  //员工ID
        "enterpriseId": "8a2a41fa75d42fc50176643762630025", //所属企业ID
        "name": "张三", //员工名称
        "employeeRole": 1, //员工角色  1 出库 2 入库  3 全部
        "accessToken": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJhdWQiOlsiMiIsIkExNTIwMTAwODk2MSJdLCJleHAiOjE2MTQ1MjUzNzN9.ye4Hz3aDGuSr4OGYe3uR-oe5YLaypQ9YUfNC4boIjBo",
        "accessExpiresIn": 1614525373964, //过期时间
        "refreshToken": "jRXTmvWiToGbjkb", //刷新token
        "refreshExpiresIn": 1619622973964 // 刷新token 过期时间
    }
}
        
```



#### 1.1.1 刷新token

##### 接口说明

刷新token

##### 请求说明

| http 请求方式          | post     |
|:------------- |:---------------:|
| url      | /trace/employee/token/refresh |

#####  输入参数

| 参数          |必选             | 类型       | 参数说明        | 备注          |
|:-------------|:---------------:|:-------------|:-------------|:-------------|
| refreshToken      | 是|  string  |  刷新token |   |




#####  错误说明




#####  返回实例
```json  
    
    {
    "c": 0,
    "m": null,
    "d": {
        "accessToken": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJhdWQiOlsiMiIsIkExNTIwMTAwODk2MSJdLCJleHAiOjE2MTQ1MjUzNzN9.ye4Hz3aDGuSr4OGYe3uR-oe5YLaypQ9YUfNC4boIjBo",
        "accessExpiresIn": 1614525373964, //过期时间
        "refreshToken": "jRXTmvWiToGbjkb", //刷新token
        "refreshExpiresIn": 1619622973964 // 刷新token 过期时间
    }
}
        
```


#### 1.1 查询接口

##### 接口说明

根据扫码信息回显产品信息

##### 请求说明

| http 请求方式          | get     |
|:------------- |:---------------:|
| url      | /trace/barcode/get |

#####  输入参数

| 参数          |必选             | 类型       | 参数说明        | 备注          |
|:-------------|:---------------:|:-------------|:-------------|:-------------|
| code      | 是|  string  |  扫码信息 |   |
| from      | 否|  string  |  来源仓库 | 获取指定仓库信息   |




#####  错误说明




#####  返回实例
```json  
    
    {
    "c": 0,
    "m": null,
    "d": {
        "productName": "老才臣腐乳",
        "productionBatch": null,
        "picUrl": "",
        "enterpriseName": null,  //企业名称
        "beginDate": "2020-12-15 00:00:00",
        "bundleId": "6266170d-88ed-482e-ac5c-28b045bbc151", //盘符
        "houseName":"所在仓库名",
        "status":0 ,//0 已入库 -1 已出库
        "total": 2, //总数
        "list": [ //列表
            "001H0V247S82Y70100P7",
            "001K07HV0M90AZ01KCQ8"
        ]
    }
}
        
```



#### 1.2 获取产品列表信息

##### 接口说明

产品列表信息

##### 请求说明

| http 请求方式          | get     |
|:------------- |:---------------:|
| url      | /trace/product/list |

#####  输入参数

| 参数          |必选             | 类型       | 参数说明        | 备注          |
|:-------------|:---------------:|:-------------|:-------------|:-------------|
| limit      | 否|  int  |  分页条数 | 默认10   |
| page      | 否|  int  |  分页 | 默认1   |




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
                "name": "老才臣腐乳", //产品名称
                "productId": "8a2a41fa75d4301e0176643db4ab004c", //产品ID
                "defaultPanSize": 50, //默认盘大小
                "batchList": [
                    {
                        "batchId": "xxxxxxxx",  //生产批次ID
                        "batchCode": "20210101" //批次码
                    }
                ]
            }
        ],
        "end": true,
        "empty": false,
        "startIndex": 0,
        "totalPage": null
    }
}
         
```


#### 1.3 添加批次信息

##### 接口说明

手工添加批次信息

##### 请求说明

| http 请求方式          | post     |
|:------------- |:---------------:|
| url      | /trace/batch/add |

#####  输入参数

| 参数          |必选             | 类型       | 参数说明        | 备注          |
|:-------------|:---------------:|:-------------|:-------------|:-------------|
| productId      | 是|  string  |  产品ID |    |
| batchCode      | 是|  string  |  生产批次 |    |




#####  错误说明




#####  返回实例
```json  
    
    {
    "c": 0,
    "m": null,
    "d": {
        "id": "803a1b88-2515-4516-b1f5-d9e80d8f057c" //批次ID
    }
}
         
```



#### 1.4  仓库/经销商 列表

##### 接口说明

手工添加批次信息

##### 请求说明

| http 请求方式          | get     |
|:------------- |:---------------:|
| url      | /trace/house/list |

#####  输入参数

| 参数          |必选             | 类型       | 参数说明        | 备注          |
|:-------------|:---------------:|:-------------|:-------------|:-------------|
| type      | 否 |  int  |  类别 |  1仓库  2 经销商   |
| cityId      | 否 |  int  |  类别 |  城市ID  |
| keywords      | 否 |  string  |  关键字 |  关键字搜索  |




#####  错误说明




#####  返回实例
```json  
    
    {
    "c": 0,
    "m": null,
    "d": [
        {
            "houseId": "2c984b814cb180b5014cb1a19dcf0006", //仓库ID
            "houseCode": "0002", //仓库编码
            "houseName": "测试仓库", //仓库名
            "enterpriseId": "8a2a41fa75d42fc50176643762630025", //所属企业
            "provincesId": 10, //省份信息
            "cityId": 1 //城市信息
        }
    ]
}
         
```


#### 1.4.1  城市列表

##### 接口说明

城市列表

##### 请求说明

| http 请求方式          | get     |
|:------------- |:---------------:|
| url      | /trace/house/area_list |

#####  输入参数

| 参数          |必选             | 类型       | 参数说明        | 备注          |
|:-------------|:---------------:|:-------------|:-------------|:-------------|
| type      | 否 |  int  |  类别 |  1仓库  2 经销商   |




#####  错误说明




#####  返回实例
```json  
    
    {
    "c": 0,
    "m": null,
    "d": [
        {
            "areaid":123, //城市ID
            "name":"北京", //城市ID
            "parentid": 3, //父节点
        }
    ]
}
         
```



#### 1.5  入库接口

##### 接口说明

入库接口

##### 请求说明

| http 请求方式          | post     |
|:------------- |:---------------:|
| url      | /trace/input |

#####  输入参数

__post json协议说明__


```json 

{
	"actionType": 101, // 101:普通入库  102:调拨入库 103:退换货入库
	"batchId": "803a1b88-2515-4516-b1f5-d9e80d8f057c", //批次
	"id": "eae1c1e0-c17f-411f-b118-dd8cbb23c1a4", //请求ID 防止重复提交,建议uuid
	"target":"xxxxx",//仓库ID
	"list": [{ //盘列表,可多个
		"codes": ["001H0V247S82Y70100P7"],
		"size": 1
	}],
	"productId": "8a2a41fa75d4301e0176643db4ab004c", //产品ID
	"total": 1 //总数
}


```




##### 案例

__1.普通入库__


```json 

{
    "actionType": 101,
    "batchId": "803a1b88-2515-4516-b1f5-d9e80d8f057c",
    "target":"xxxxx",//仓库ID
    "list": [
        {
            "codes": [
                "001H0V247S82Y70100P7",
                "001K07HV0M90AZ01KCQ8"
            ],
            "size": 2
        }
    ],
    "productId": "8a2a41fa75d4301e0176643db4ab004c",
    "total": 2
}


```


__2.退盘__


```json 

{
    "actionType": 101,
    "list": [
        {
            "bundleId":"035e150e-81f1-4128-84e9-bcfa069ee9ed",
            "action":"REMOVE",
            "codes": [
                "001H0V247S82Y70100P7",
            ],
            "size": 1
        }
    ],
    "productId": "8a2a41fa75d4301e0176643db4ab004c",
    "total": 1
}


```

__3.补盘__


```json 

{
    "actionType": 101,
    "list": [
        {
            "bundleId":"035e150e-81f1-4128-84e9-bcfa069ee9ed",
            "action":"ADD",
            "codes": [
                "001H0V247S82Y70100P7",
            ],
            "size": 1
        }
    ],
    "productId": "8a2a41fa75d4301e0176643db4ab004c",
    "total": 1
}


```


__4.调拨入库__


```json 

{
    "actionType": 102,
    "batchId": "803a1b88-2515-4516-b1f5-d9e80d8f057c",
    "from":"2c984b814cb180b5014cb1a19dcf0006",
    "list": [
        {
            "bundleId":"035e150e-81f1-4128-84e9-bcfa069ee9ed",
            "size": 2
        }
    ],
    "productId": "8a2a41fa75d4301e0176643db4ab004c",
    "total": 2
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


#### 1.6  出库接口

##### 接口说明

出库接口

##### 请求说明

| http 请求方式          | post     |
|:------------- |:---------------:|
| url      | /trace/output |

#####  输入参数

__post json协议说明__


```json 

{
    "actionType": 201,
    "batchId": "803a1b88-2515-4516-b1f5-d9e80d8f057c",
    "target":"2c984b814cb180b5014cb1a19dcf0006",
    "carNo":"xxxx", //车牌号
    "list": [
        {
            "bundleId":"2709daaf-aa3f-4dac-a3ae-ad23637fe52d", //盘符
            "size": 1
        },
        {
            "action":"REMOVE",  // 退盘
            "bundleId":"2709daaf-aa3f-4dac-a3ae-ad23637fe52d",
            "codes":[
                "001H0V247S82Y70100P7"
            ],
            "size": 1
        }
    ],
    "productId": "8a2a41fa75d4301e0176643db4ab004c",
    "total": 2
}


```




##### 案例

__1.普通出库__


```json 

{
    "actionType": 201,
    "batchId": "803a1b88-2515-4516-b1f5-d9e80d8f057c",
    "target":"2c984b814cb180b5014cb1a19dcf0006",
    "carNo":"xxxx", //车牌号
    "list": [
        {
            "bundleId":"2709daaf-aa3f-4dac-a3ae-ad23637fe52d", //盘符
            "size": 1
        }
    ],
    "productId": "8a2a41fa75d4301e0176643db4ab004c",
    "total": 2
}


```


__2.退盘出库__


```json 

{
    "actionType": 201,
    "batchId": "803a1b88-2515-4516-b1f5-d9e80d8f057c",
    "target":"2c984b814cb180b5014cb1a19dcf0006", //仓库
    "list": [
        {
            "bundleId":"2709daaf-aa3f-4dac-a3ae-ad23637fe52d", //盘符
            "size": 1
        },
        {
            "action":"REMOVE",  // 退盘
            "bundleId":"2709daaf-aa3f-4dac-a3ae-ad23637fe52d",
            "codes":[
                "001H0V247S82Y70100P7"
            ],
            "size": 1
        }
    ],
    "productId": "8a2a41fa75d4301e0176643db4ab004c",
    "total": 2
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






