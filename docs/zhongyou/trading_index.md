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

























