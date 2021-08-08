# 中优，商城接口

[TOC]
## 修订记录
----
日期 | 作者 | 修订类型 | 修订内容 | 版本|
---- | ---- | ---- | ---- | ---- |
2020年07月03日|冷立纲|A|新增设计方案|1.0|

> 【修订类型：A-新增  M-修改 D-删除】

## 背景

中优商城接口文档

## 产品说明



## 关键流程说明

## 接口说明



### 1. 指数


-------



#### 1.1.0 指数首页

##### 接口说明



##### 请求说明

| http 请求方式          |get             |
|:------------- |:---------------:|
| url      |/trading/index |

#####  输入参数

| 参数          |必选             | 类型       | 参数说明        | 备注          |
|:-------------|:---------------:|:-------------|:-------------|:-------------|
| page      | 否| int  |  分页 |   |
| limit      | 否| int  |  单页条数 |   |
| keyword      | 否| string  |  搜索关键字 ||
| feedType      | 否| int  |  圈子类型 | 1 动态 2 求购 3 出货  空则全部|
#####  错误说明





#####  返回实例
```json


{
    "c": 0,
    "m": null,
    "d": {
        "indexData": {  //指数相关
            "value": 66867,  //指数值
            "yesterdayRate": 0.3104091727168805103787008192739449441432952880859375,  //昨日涨幅
            "weekRate": 0.4402313041648742153455486914026550948619842529296875, //周涨幅
            "monthRate": 0.00987847956402188032143385498784482479095458984375, //月涨幅
            "yearRate": 0.671523432892886518175146193243563175201416015625, //年涨幅
            "riseCount": 661,  //上涨数
            "holdCount": 569, // 持平数
            "fallCount": 800, // 下跌数
            "hot": 89522 //热度
        },
        "years": [  //年份
            {
                "code": "2021",
                "name": "2021年"
            },
            {
                "code": "2020",
                "name": "2020年"
            },
            {
                "code": "2019",
                "name": "2019年"
            },
            {
                "code": "2018",
                "name": "2018年"
            }
        ],
        "areas": [  //产地
            {
                "code": "beijing",
                "name": "北京"
            },
            {
                "code": "guangdong",
                "name": "广东"
            },
            {
                "code": "shanxi",
                "name": "陕西"
            }
        ],
        "goodsList": {  //商品列表
            "pageSize": 10,
            "currentPage": 1,
            "list": [
                {
                    "id": 371,
                    "name": "【同城配送】黄冰糖 调料300g",
                    "picUrl": "https://saiwai.oss-cn-huhehaote.aliyuncs.com/gs9mzpl9dii61cp2az3c.jpg",
                    "unit": "g", //单位
                    "unitType": null,  //单位类型 0 箱  1 盒
                    "weight": null, //重量
                    "counterPrice": 3.30,  //专柜价
                    "retailPrice": 3.30,  //零售价
                    "vipPrice": 3.30, //vip 价格
                    "brief": "",  //简介
                    "gallery": null, //图片
                    "videos": null, //视频
                    "tags": null //标签
                    "year":"xxx", //年限
                    "area":"xxxx" //区域
                }
            ],
            "end": false,
            "startIndex": 0,
            "totalPage": 9,
            "empty": false
        }
    }
}
```


#### 1.1.1 分类获取商品信息

##### 接口说明

按商品类别分页拉取商品列表信息

##### 请求说明

| http 请求方式          | get     |
|:------------- |:---------------:|
| url      | /goods/list |

#####  输入参数

| 参数          |必选             | 类型       | 参数说明        | 备注          |
|:-------------|:---------------:|:-------------|:-------------|:-------------|
| year      | 否|  string  |  分类ID  |  年份code |
| area      | 否|  string  |  区域  |  区域code |
| categoryId      | 否|  int  |  分类ID  |  0 为精选 |
| brandId      | 否|  int  |  品牌ID  |   |
| keyword      | 否|  string  |  查询关键词  |   |
| isNew      | 否|  boolean  |  是否新  |   |
| isHot      | 否|  boolean  |  是否热门  |   |
| sort      | 否|  string  |  排序字段  | add_time, retail_price, name|
| order      | 否|  string  |  倒序/正序  | asc  desc|
| page      | 否|  int  |  页码  | 默认值 1 |
| limit      | 否|  int  |  单页条数  | 默认值 10 |


#####  错误说明




#####  返回实例
```json
    
    {
    "c": 0,
    "m": null,
    "d": {
        "pageSize": 10,
        "total": 1,
        "currentPage": 1,
        "list": [
            {
                "id": 1006002,  //产品ID
                "name": "轻奢纯棉刺绣水洗四件套", //名称
                "tags": null,  //标签
                "picUrl": "http://yanxuan.nosdn.127.net/8ab2d3287af0cefa2cc539e40600621d.png",
                "unit": "件", //单位
                "unitType": null,  //单位类型 0 箱  1 盒
                "weight": null, //重量
                "counterPrice": 919.00,  //专柜价
                "retailPrice": 899.00, //零售价
                "vipPrice": 100000.00, //会员价
                "brief": "设计师原款，精致绣花", //简介
                "gallery":["http://yanxuan.nosdn.127.net/8ab2d3287af0cefa2cc539e40600621d.png"], //图片
                "videos":[
                        {
                            "url":"/xxxx",
                            "cover":"cover",
                            "size":"x*y"
                        }
                    ],
                "year":"xxx", //年限
                "area":"xxxx" //区域    
            }
        ],
        "unit": "单位",
        "extInfo": null,
        "endIndex": 10,
        "startIndex": 0,
        "firstPage": true,
        "lastPage": true,
        "nextPage": 1,
        "previousPage": 1,
        "totalPages": 1,
        "empty": false
    }
}

```




#### 1.1.2 大盘指数

##### 接口说明

按商品类别分页拉取商品列表信息

##### 请求说明

| http 请求方式          | get     |
|:------------- |:---------------:|
| url      | /trading/big_index |

#####  输入参数

无


#####  错误说明




#####  返回实例
```json
    
    {
    "c": 0,
    "m": null,
    "d": {
        "indexData": {  
             "value": 66867,  //指数值
            "yesterdayRate": 0.3104091727168805103787008192739449441432952880859375,  //昨日涨幅
            "weekRate": 0.4402313041648742153455486914026550948619842529296875, //周涨幅
            "monthRate": 0.00987847956402188032143385498784482479095458984375, //月涨幅
            "yearRate": 0.671523432892886518175146193243563175201416015625, //年涨幅
            "riseCount": 661,  //上涨数
            "holdCount": 569, // 持平数
            "fallCount": 800, // 下跌数
            "hot": 89522 //热度
        },
        "years": [  //年份
            {
                "code": "2021",
                "name": "2021年"
            },
            {
                "code": "2020",
                "name": "2020年"
            },
            {
                "code": "2019",
                "name": "2019年"
            },
            {
                "code": "2018",
                "name": "2018年"
            }
        ]
    }
}

```



#### 1.1.3 大盘历史指数

##### 接口说明

按商品类别分页拉取商品列表信息

##### 请求说明

| http 请求方式          | get     |
|:------------- |:---------------:|
| url      | /trading/index_history |

#####  输入参数

| 参数          |必选             | 类型       | 参数说明        | 备注          |
|:-------------|:---------------:|:-------------|:-------------|:-------------|
| startTime      | 否|  string  |   | 开始时间  yyyy-MM-dd |
| endTime      | 否|  string  |   | 结束时间  yyyy-MM-dd |
| goodsId      | 否|  int  |   | 商品ID  |
| page      | 否|  int  |  页码  | 默认值 1 |
| limit      | 否|  int  |  单页条数  | 默认值 10 |


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
                "time": "2021-08-07",  //日期
                "price": 10000.000000 //指数
            }
        ],
        "end": true,
        "startIndex": 0,
        "totalPage": null,
        "empty": false
    }
}
```




#### 1.1.4 历史价格数据

##### 接口说明



##### 请求说明

| http 请求方式          | get     |
|:------------- |:---------------:|
| url      | /trading/price_history |

#####  输入参数

| 参数          |必选             | 类型       | 参数说明        | 备注          |
|:-------------|:---------------:|:-------------|:-------------|:-------------|
| startTime      | 否|  string  |   | 开始时间  yyyy-MM-dd |
| endTime      | 否|  string  |   | 结束时间  yyyy-MM-dd |
| goodsId      | 否|  int  |   | 商品ID  |
| page      | 否|  int  |  页码  | 默认值 1 |
| limit      | 否|  int  |  单页条数  | 默认值 10 |


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
                "name": "【同城配送】黄冰糖 调料300g",  // 名称
                "unit": "g",  //单位
                "unitType": null,  //单位类型
                "weight": null, //重量
                "counterPrice": 3.30, //专柜价
                "retailPrice": 3.30, //销售价
                "vipPrice": 3.30, //vip 价格
                "changeVal": 0.00, // 价格变更
                "changePercent": ".00%" //变更百分比
            }
        ],
        "end": true,
        "empty": false,
        "startIndex": 0,
        "totalPage": null
    }
}
```






#### 1.1.4 商品行情

##### 接口说明



##### 请求说明

| http 请求方式          | get     |
|:------------- |:---------------:|
| url      | /trading/goods_index |

#####  输入参数

| 参数          |必选             | 类型       | 参数说明        | 备注          |
|:-------------|:---------------:|:-------------|:-------------|:-------------|
| goodsId      | 是 |  int  |   | 商品ID  |


#####  错误说明




#####  返回实例
```json
    
   {
    "c": 0,
    "m": null,
    "d": {
        "goods": { //商品信息 
            "id": 371,
            "name": "【同城配送】黄冰糖 调料300g",  //名称
            "picUrl": "https://saiwai.oss-cn-huhehaote.aliyuncs.com/ gs9mzpl9dii61cp2az3c.jpg",  //图片
            "unit": "g",  //单位
            "unitType": null,  //单位类型 0 散装 1 盒装
            "weight": null, //重量
            "counterPrice": 3.30,  //专柜价
            "retailPrice": 3.30, //售价
            "vipPrice": 3.30, //vip 价格
            "brief": "", //简介
            "gallery": [
                "https://saiwai.oss-cn-huhehaote.aliyuncs.com/dokso7lipj2kkd864ce6.jpg",
                "https://saiwai.oss-cn-huhehaote.aliyuncs.com/2shb0hrftwp17nivfkuu.jpg",
                "https://saiwai.oss-cn-huhehaote.aliyuncs.com/jb7w8ja1cuueq03gd43c.jpg",
                "https://saiwai.oss-cn-huhehaote.aliyuncs.com/1fih05qeou0tc9144btt.jpg",
                "https://saiwai.oss-cn-huhehaote.aliyuncs.com/z4we6hmtfkqvi86gwglv.jpg"
            ],
            "videos": null,
            "tags": null,
            "area": "beijing",  //地区
            "year": "2019" //年份
        },
        "rates": {  //波动比率
            "addDay": null,
            "yetedayRate": 0, //昨天比率
            "weekRate": 0, //周比率
            "monthRate": 0, //月比率
            "yearRate": 0 //年比率
        },
        "agentProducts": {  //代理商
            "pageSize": 10,
            "currentPage": 1,
            "list": [
                {
                    "goodsId": 371,   //产品ID
                    "agentId": 1, //代理商ID
                    "productId": 476, //商品ID
                    "name": "xiaogang",  //代理商名称
                    "addr": "wangjing", //代理商地址
                    "logoUrl": "/logo", //代理商logo
                    "number": 1000, //库存
                    "saleCount": 0, //已售
                    "price": 3.30 //价格
                }
            ],
            "end": true,
            "startIndex": 0,
            "totalPage": null,
            "empty": false
        }
    }
}
```




#### 1.1.5 商品详情

##### 接口说明



##### 请求说明

| http 请求方式          | get     |
|:------------- |:---------------:|
| url      | /goods/detail |

#####  输入参数

| 参数          |必选             | 类型       | 参数说明        | 备注          |
|:-------------|:---------------:|:-------------|:-------------|:-------------|
| id      | 是 |  int  |   | 商品ID （代理商商品ID productId） |


#####  错误说明




#####  返回实例
```json
  
  {
    "c": 0,
    "m": null,
    "d": {
        "defaultAddress": null,
        "couponList": [],
        "info": {
            "id": 371,
            "goodsSn": "00353",
            "name": "【同城配送】黄冰糖 调料300g",
            "categoryId": 37,
            "brandId": 0,
            "gallery": [
                "https://saiwai.oss-cn-huhehaote.aliyuncs.com/dokso7lipj2kkd864ce6.jpg",
                "https://saiwai.oss-cn-huhehaote.aliyuncs.com/2shb0hrftwp17nivfkuu.jpg",
                "https://saiwai.oss-cn-huhehaote.aliyuncs.com/jb7w8ja1cuueq03gd43c.jpg",
                "https://saiwai.oss-cn-huhehaote.aliyuncs.com/1fih05qeou0tc9144btt.jpg",
                "https://saiwai.oss-cn-huhehaote.aliyuncs.com/z4we6hmtfkqvi86gwglv.jpg"
            ],
            "keywords": "",
            "brief": "",
            "isOnSale": true,
            "sortOrder": 100,
            "picUrl": "https://saiwai.oss-cn-huhehaote.aliyuncs.com/gs9mzpl9dii61cp2az3c.jpg",
            "shareUrl": "",
            "isNew": true,
            "isHot": true,
            "unit": "g",
            "counterPrice": 3.30,
            "retailPrice": 3.30,
            "vipPrice": 3.30,
            "addTime": "2021-07-04 14:31:19",
            "updateTime": "2021-07-05 08:06:50",
            "deleted": false,
            "tags": null,
            "videos": null,
            "testReports": null,
            "goodsType": 0,
            "expressType": 0,
            "area": "2019年",
            "year": "2019",
            "unitType": null,
            "weight": null,
            "detail": [
                {
                    "url": "https://saiwai.oss-cn-huhehaote.aliyuncs.com/tyxjmlhltbjx1vuhczuv.jpg",
                    "size": "2168*5446"
                },
                {
                    "url": "https://saiwai.oss-cn-huhehaote.aliyuncs.com/fdkcytldeidxpfwr7s0h.png",
                    "size": "607*839"
                }
            ]
        },
        "userHasCollect": 0,
        "issue": {
            "total": 0,
            "list": null,
            "pageNum": 0,
            "pageSize": 0,
            "size": 0,
            "startRow": 0,
            "endRow": 0,
            "pages": 0,
            "prePage": 0,
            "nextPage": 0,
            "isFirstPage": false,
            "isLastPage": false,
            "hasPreviousPage": false,
            "hasNextPage": false,
            "navigatePages": 0,
            "navigatepageNums": null,
            "navigateFirstPage": 0,
            "navigateLastPage": 0
        },
        "comment": {
            "count": 0,
            "favorableRating": null,
            "data": []
        },
        "specificationList": [
            {
                "name": "规格",
                "valueList": [
                    {
                        "id": 443,
                        "goodsId": 371,
                        "specification": "规格",
                        "value": "300g",
                        "picUrl": "",
                        "addTime": "2021-07-04 14:31:19",
                        "updateTime": "2021-07-05 08:06:50",
                        "deleted": false
                    }
                ]
            }
        ],
        "productList": [
            {
                "id": 476,
                "goodsId": 371,
                "specifications": [
                    "标准"
                ],
                "price": 3.30,
                "number": 1000,
                "url": "",
                "addTime": "2021-07-04 14:31:19",
                "updateTime": "2021-07-05 08:06:50",
                "vipPrice": 3.30,
                "counterPrice": 0.00,
                "deleted": false,
                "year": "2019",
                "area": "beijing",
                "agentId": 1,
                "sourceType": null,
                "sourceId": null,
                "unitPrice": null,
                "saleCount": 0
            }
        ],
        "attribute": [],
        "keyIndicators": [],
        "brand": {
            "id": null,
            "name": null,
            "desc": null,
            "picUrl": null,
            "sortOrder": null,
            "floorPrice": null,
            "addTime": null,
            "updateTime": null,
            "deleted": null
        },
        "groupon": [],
        "share": false,
        "shareImage": "",
        "agent": {  //代理商信息
            "id": 1,  //代理商ID
            "name": "xiaogang",  //名称
            "addr": "wangjing", //地址
            "logoUrl": "/logo", //logo
            "deleted": false, // 是否已删除
            "addTime": null
        }
    }
}  
  
```



#### 1.1.5 商户报价列表

##### 接口说明



##### 请求说明

| http 请求方式          | get     |
|:------------- |:---------------:|
| url      | /agent/agent_list |

#####  输入参数

| 参数          |必选             | 类型       | 参数说明        | 备注          |
|:-------------|:---------------:|:-------------|:-------------|:-------------|
| goodsId      | 否 |  int  |   | 商品ID  |
| agentId      | 否 |  int  |   | 代理商ID  |
| page      | 否|  int  |  页码  | 默认值 1 |
| limit      | 否|  int  |  单页条数  | 默认值 10 |



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
                "goodsId": 10, //产品Id
                "agentId": 1,  //代理商ID
                "productId": 10,  // 商品ID 
                "name": "xiaogang", //名称
                "addr": "wangjing", //地址
                "logoUrl": "/logo", // logo 地址
                "number": 100, //库存数量
                "saleCount": 0, //销量
                "price": 49.90 //价格
            }
        ],
        "end": false,
        "empty": false,
        "startIndex": 0,
        "totalPage": null
    }
}
  
```







#### 1.1.5 商户售卖商品列表

##### 接口说明

⚠️注意: 只有第一页返回代理商信息

##### 请求说明

| http 请求方式          | get     |
|:------------- |:---------------:|
| url      | /agent/product_list |

#####  输入参数

| 参数          |必选             | 类型       | 参数说明        | 备注          |
|:-------------|:---------------:|:-------------|:-------------|:-------------|
| goodsId      | 否 |  int  |   | 商品ID  |
| agentId      | 否 |  int  |   | 代理商ID  |
| page      | 否|  int  |  页码  | 默认值 1 |
| limit      | 否|  int  |  单页条数  | 默认值 10 |



#####  错误说明




#####  返回实例
```json
  
  {
    "c": 0,
    "m": null,
    "d": {
        "pageSize": 5,
        "currentPage": 50,
        "list": [
           
            {
                "id": 182,
                "name": "【同城配送】澳大利亚原装进口OzCow奶粉1kg",
                "picUrl": "https://saiwai.oss-cn-huhehaote.aliyuncs.com/fpm9kj7b4q2ucoy66x2s.jpg",
                "unit": "袋",
                "unitType": null,
                "weight": null,
                "counterPrice": 198.00,
                "retailPrice": 198.00,
                "vipPrice": 198.00,
                "brief": "奶粉198返券60元（外卖食品不可用）",
                "gallery": null,
                "videos": null,
                "tags": null,
                "area": null,
                "year": null,
                "productId": 270
            }
        ],
        "end": false,
        "agent": {  //第一页返回代理商信息
            "id": 1,
            "name": "xiaogang",
            "addr": "wangjing",
            "logoUrl": "/logo",
            "deleted": false,
            "addTime": null
        },
        "startIndex": 245,
        "totalPage": null,
        "empty": false
    }
}  
```





#### 1.1.6 商城及搜索接口

##### 接口说明

⚠️注意: 只有第一页返回代理商信息

##### 请求说明

| http 请求方式          | get     |
|:------------- |:---------------:|
| url      | /store/index |

#####  输入参数

| 参数          |必选             | 类型       | 参数说明        | 备注          |
|:-------------|:---------------:|:-------------|:-------------|:-------------|
| keyword      | 否 |  string  |   | 关键字  |
| type      | 否 |  int  | 0 散件 1 成品 2 代理商   | 默认 0  |
| page      | 否|  int  |  页码  | 默认值 1 |
| limit      | 否|  int  |  单页条数  | 默认值 10 |



#####  错误说明




#####  返回实例

**type=0/1**

```json
  
  {
    "c": 0,
    "m": null,
    "d": {
        "pageSize": 1,
        "currentPage": 1,
        "list": [
            {
                "id": 371,
                "name": "【同城配送】黄冰糖 调料300g",
                "picUrl": "https://saiwai.oss-cn-huhehaote.aliyuncs.com/gs9mzpl9dii61cp2az3c.jpg",
                "unit": "g",
                "unitType": null,
                "weight": null,
                "counterPrice": 3.30,
                "retailPrice": 3.30,
                "vipPrice": 3.30,
                "brief": "",
                "gallery": null,
                "videos": null,
                "tags": null,
                "area": null,
                "year": null
            }
        ],
        "end": false,
        "totalPage": 84,
        "startIndex": 0,
        "empty": false
    }
}
 
```





**type=2**

```json
  
  {
    "c": 0,
    "m": null,
    "d": {
        "pageSize": 1,
        "currentPage": 1,
        "list": [
            {
                "id": 1,
                "name": "xiaogang",
                "addr": "wangjing",
                "logoUrl": "/logo",
                "totalSale": 0
            }
        ],
        "end": false,
        "totalPage": null,
        "startIndex": 0,
        "empty": false
    }
}
 
```






