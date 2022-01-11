# 中优商城2.0接口

[TOC]
## 修订记录
----
日期 | 作者 | 修订类型 | 修订内容 | 版本|
---- | ---- | ---- | ---- | ---- |
2021年11月25日|冷立纲|A|新增设计方案|1.0|

> 【修订类型：A-新增  M-修改 D-删除】

## 背景

中优商城接口文档

## 产品说明



## 关键流程说明

## 接口说明



### 1. 商品


-------



#### 1.1.0 商品详情

##### 接口说明



##### 请求说明

| http 请求方式          |get             |
|:------------- |:---------------:|
| url      |/goods/detail |

#####  输入参数

| 参数          |必选             | 类型       | 参数说明        | 备注          |
|:-------------|:---------------:|:-------------|:-------------|:-------------|
| id      | 否| int  |  商品ID |   |

#####  错误说明





#####  返回实例
```json


{
    "c": 0,
    "m": null,
    "d": {
        "productId": null,
        "defaultAddress": null,
        "couponList": null,
        "info": {
            "id": 1,
            "goodsSn": "00001",
            "name": "侨宝2017年酿化陈皮",
            "categoryId": 0,
            "brandId": 0,
            "gallery": [
                "https://zhongyou-mall.oss-cn-beijing.aliyuncs.com/1h3xlxlboyzxzu6wn4yt.png"
            ],
            "keywords": "",
            "brief": "",
            "isOnSale": true,
            "sortOrder": 100,
            "picUrl": "https://zhongyou-mall.oss-cn-beijing.aliyuncs.com/5xa5i9lzwo8fyv62zx3r.png",
            "shareUrl": "",
            "isNew": true,
            "isHot": false,
            "unit": "箱",
            "counterPrice": "2298.00",
            "retailPrice": "2298.00",
            "vipPrice": "2298.00",
            "addTime": "2021-11-24 15:08:40",
            "updateTime": "2021-11-25 13:32:32",
            "deleted": false,
            "tags": null,
            "videos": null,
            "testReports": null,
            "goodsType": 0,
            "expressType": 0,
            "area": "天马",
            "year": "2017年",
            "unitType": 1,
            "weight": null,
            "detail": [
                {
                    "url": "https://zhongyou-mall.oss-cn-beijing.aliyuncs.com/pmrcuwt2z2i8r7luv0er.jpg",
                    "size": "790*682"
                },
                {
                    "url": "https://zhongyou-mall.oss-cn-beijing.aliyuncs.com/qnobzj1h3e0jktmy7ck8.jpg",
                    "size": "790*899"
                },
                {
                    "url": "https://zhongyou-mall.oss-cn-beijing.aliyuncs.com/1zj83hoxhjt1gunwk3je.jpg",
                    "size": "790*899"
                },
                {
                    "url": "https://zhongyou-mall.oss-cn-beijing.aliyuncs.com/6ezps7996rqnmxpfqjvn.jpg",
                    "size": "790*898"
                },
                {
                    "url": "https://zhongyou-mall.oss-cn-beijing.aliyuncs.com/rgzal4xtrlsigth749sq.jpg",
                    "size": "790*899"
                },
                {
                    "url": "https://zhongyou-mall.oss-cn-beijing.aliyuncs.com/z73132dp9vzdft7f8b4l.jpg",
                    "size": "790*899"
                },
                {
                    "url": "https://zhongyou-mall.oss-cn-beijing.aliyuncs.com/z7opj5e64khgzytkr5xn.jpg",
                    "size": "790*898"
                },
                {
                    "url": "https://zhongyou-mall.oss-cn-beijing.aliyuncs.com/s55tevmi69vi9jxsnqjs.jpg",
                    "size": "790*899"
                },
                {
                    "url": "https://zhongyou-mall.oss-cn-beijing.aliyuncs.com/4in6p6ue6xbhgmq3a90i.jpg",
                    "size": "790*899"
                },
                {
                    "url": "https://zhongyou-mall.oss-cn-beijing.aliyuncs.com/2unsmej0hla48pqh55nd.jpg",
                    "size": "790*898"
                },
                {
                    "url": "https://zhongyou-mall.oss-cn-beijing.aliyuncs.com/mim5e5epc5owcwrm060t.jpg",
                    "size": "790*899"
                },
                {
                    "url": "https://zhongyou-mall.oss-cn-beijing.aliyuncs.com/53402o648madbhjfthil.jpg",
                    "size": "790*71"
                },
                {
                    "url": "https://zhongyou-mall.oss-cn-beijing.aliyuncs.com/x346n1bz76oqzf96hob8.jpg",
                    "size": "790*406"
                },
                {
                    "url": "https://zhongyou-mall.oss-cn-beijing.aliyuncs.com/x4fel6n3j9q0xmdv4fv0.jpg",
                    "size": "790*899"
                },
                {
                    "url": "https://zhongyou-mall.oss-cn-beijing.aliyuncs.com/ycnrxhmssf9i1nq66rph.png",
                    "size": "414*414"
                },
                {
                    "url": "https://zhongyou-mall.oss-cn-beijing.aliyuncs.com/5x74ql6jh0txon2okliz.png",
                    "size": "414*349"
                },
                {
                    "url": "https://zhongyou-mall.oss-cn-beijing.aliyuncs.com/ost9oo38jvlgt1spdcmp.png",
                    "size": "414*359"
                },
                {
                    "url": "https://zhongyou-mall.oss-cn-beijing.aliyuncs.com/dyk7zbxmadffek9wfemc.png",
                    "size": "414*359"
                },
                {
                    "url": "https://zhongyou-mall.oss-cn-beijing.aliyuncs.com/p370jcw2dibk1kujnlfs.png",
                    "size": "414*349"
                },
                {
                    "url": "https://zhongyou-mall.oss-cn-beijing.aliyuncs.com/fqr65cxldy56piy3ja61.png",
                    "size": "414*524"
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
        "saleList": { //出售列表
            "pageSize": 10,
            "currentPage": 1,
            "list": [
                {
                    "id": 1,
                    "uid": 10075,
                    "employeeType": null,
                    "avatar": "https://thirdwx.qlogo.cn/mmopen/vi_32/ajNVdqHZLLCR0RRpv80XgfKgjiaunf4KGpPXIubQe63k94icYGayDOKe28xEdQyVwZ63iaAKunbp5Gw5jdsia6iaS5w/132",
                    "name": "gåga💪🏼",
                    "goodsId": 1,
                    "count": 1,
                    "addTime": "2021-09-09 12:33:33",
                    "price": "222.00"
                }
            ],
            "end": true,
            "goods": null,
            "empty": false,
            "startIndex": 0,
            "totalPage": null
        },
        "buyList": { //求购列表
            "pageSize": 10,
            "currentPage": 1,
            "list": [
                {
                    "id": 1,
                    "uid": 10075,
                    "employeeType": null,
                    "avatar": "https://thirdwx.qlogo.cn/mmopen/vi_32/ajNVdqHZLLCR0RRpv80XgfKgjiaunf4KGpPXIubQe63k94icYGayDOKe28xEdQyVwZ63iaAKunbp5Gw5jdsia6iaS5w/132",
                    "name": "gåga💪🏼",
                    "goodsId": 1,
                    "count": 5,
                    "addTime": "2021-09-09 12:33:33",
                    "price": "22.00"
                }
            ],
            "end": true,
            "goods": null,
            "empty": false,
            "startIndex": 0,
            "totalPage": null
        },
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
        "agent": null
    }
}

```



#### 1.1.1 库存预览

##### 接口说明



##### 请求说明

| http 请求方式          |get             |
|:------------- |:---------------:|
| url      |/stock/detail |

#####  输入参数

| 参数          |必选             | 类型       | 参数说明        | 备注          |
|:-------------|:---------------:|:-------------|:-------------|:-------------|
| buyId      | 否| int  |  求购ID |   |
| goodsId      | 否| int  |  商品ID |   |
| agentId      | 否| int  |  代理商ID |  默认平台0  |

#####  错误说明





#####  返回实例

```json


{
    "c": 0,
    "m": null,
    "d": {
        "goods": {
            "id": 1,
            "name": "侨宝2017年酿化陈皮",
            "picUrl": "https://zhongyou-mall.oss-cn-beijing.aliyuncs.com/5xa5i9lzwo8fyv62zx3r.png",
            "unit": "箱",
            "unitType": 1,
            "weight": null,
            "counterPrice": "2298.00",
            "retailPrice": "2298.00",
            "vipPrice": "2298.00",
            "brief": "",
            "gallery": [
                "https://zhongyou-mall.oss-cn-beijing.aliyuncs.com/1h3xlxlboyzxzu6wn4yt.png"
            ],
            "videos": null,
            "tags": null,
            "area": "天马",
            "year": "2017"
        },
        "amount": 0, //库存信息
        "user": null,
        "buyAmount": 5  // 求购数量
    }
}

```


#### 1.1.2 求购

##### 接口说明



##### 请求说明

| http 请求方式          | post    |
|:------------- |:---------------:|
| url      |/buy/add |

#####  输入参数

| 参数          |必选             | 类型       | 参数说明        | 备注          |
|:-------------|:---------------:|:-------------|:-------------|:-------------|
| count      | 是 | int  |  求购数量 |   |
| goodsId      | 是 | int  |  商品ID |   |
| price      | 是 | double  |  商品价格 |   |

#####  错误说明





#####  返回实例

```json


{
    "c": 0,
    "m": null,
    "d": {
        "id": 2
    }
}

```


#### 1.1.3 出售

##### 接口说明



##### 请求说明

| http 请求方式          | post    |
|:------------- |:---------------:|
| url      |/sale/add |

#####  输入参数

| 参数          |必选             | 类型       | 参数说明        | 备注          |
|:-------------|:---------------:|:-------------|:-------------|:-------------|
| count      | 是 | int  |  求购数量 |   |
| goodsId      | 是 | int  |  商品ID |   |
| price      | 是 | double  |  商品价格 |   |

#####  错误说明





#####  返回实例

```json


{
    "c": 0,
    "m": null,
    "d": {
        "id": 2
    }
}

```



#### 1.1.3 立即出售

##### 接口说明



##### 请求说明

| http 请求方式          | post    |
|:------------- |:---------------:|
| url      |/sale/at_once |

#####  输入参数

| 参数          |必选             | 类型       | 参数说明        | 备注          |
|:-------------|:---------------:|:-------------|:-------------|:-------------|
| count      | 是 | int  |  求购数量 |   |
| buyId      | 是 | int  |  求购ID |   |

#####  错误说明





#####  返回实例

```json


{
    "c": 0,
    "m": null,
    "d": {
        "id": 2
    }
}

```



#### 1.1.4 出售列表

##### 接口说明



##### 请求说明

| http 请求方式          | get    |
|:------------- |:---------------:|
| url      |/sale/list |

#####  输入参数

| 参数          |必选             | 类型       | 参数说明        | 备注          |
|:-------------|:---------------:|:-------------|:-------------|:-------------|
| goodsId      | 是 | int  |  商品ID |   |
| page      | 否 | int  |  分页 |   |
| limit      | 否 | int  |  每页条数 |   |

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
                "id": 2,
                "uid": 10075,
                "employeeType": null,
                "avatar": "https://thirdwx.qlogo.cn/mmopen/vi_32/ajNVdqHZLLCR0RRpv80XgfKgjiaunf4KGpPXIubQe63k94icYGayDOKe28xEdQyVwZ63iaAKunbp5Gw5jdsia6iaS5w/132",
                "name": "gåga💪🏼",
                "goodsId": 1,
                "count": 1,
                "addTime": null,
                "price": "2000.00"
            },
            {
                "id": 1,
                "uid": 10075,
                "employeeType": null,
                "avatar": "https://thirdwx.qlogo.cn/mmopen/vi_32/ajNVdqHZLLCR0RRpv80XgfKgjiaunf4KGpPXIubQe63k94icYGayDOKe28xEdQyVwZ63iaAKunbp5Gw5jdsia6iaS5w/132",
                "name": "gåga💪🏼",
                "goodsId": 1,
                "count": 1,
                "addTime": "2021-09-09 12:33:33",
                "price": "222.00"
            }
        ],
        "end": true,
        "goods": {
            "id": 1,
            "name": "侨宝2017年酿化陈皮",
            "picUrl": "https://zhongyou-mall.oss-cn-beijing.aliyuncs.com/5xa5i9lzwo8fyv62zx3r.png",
            "unit": "箱",
            "unitType": 1,
            "weight": null,
            "counterPrice": "2298.00",
            "retailPrice": "2298.00",
            "vipPrice": "2298.00",
            "brief": "",
            "gallery": [
                "https://zhongyou-mall.oss-cn-beijing.aliyuncs.com/1h3xlxlboyzxzu6wn4yt.png"
            ],
            "videos": null,
            "tags": null,
            "area": "天马",
            "year": "2017"
        },
        "empty": false,
        "startIndex": 0,
        "totalPage": null
    }
}

```


#### 1.1.5 求购列表

##### 接口说明



##### 请求说明

| http 请求方式          | get    |
|:------------- |:---------------:|
| url      |/buy/list |

#####  输入参数

| 参数          |必选             | 类型       | 参数说明        | 备注          |
|:-------------|:---------------:|:-------------|:-------------|:-------------|
| goodsId      | 是 | int  |  商品ID |   |
| page      | 否 | int  |  分页 |   |
| limit      | 否 | int  |  每页条数 |   |

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
                "id": 2,
                "uid": 10075,
                "employeeType": null,
                "avatar": "https://thirdwx.qlogo.cn/mmopen/vi_32/ajNVdqHZLLCR0RRpv80XgfKgjiaunf4KGpPXIubQe63k94icYGayDOKe28xEdQyVwZ63iaAKunbp5Gw5jdsia6iaS5w/132",
                "name": "gåga💪🏼",
                "goodsId": 1,
                "count": 1,
                "addTime": "2021-12-25 18:33:03",
                "price": "2000.00"
            },
            {
                "id": 1,
                "uid": 10075,
                "employeeType": null,
                "avatar": "https://thirdwx.qlogo.cn/mmopen/vi_32/ajNVdqHZLLCR0RRpv80XgfKgjiaunf4KGpPXIubQe63k94icYGayDOKe28xEdQyVwZ63iaAKunbp5Gw5jdsia6iaS5w/132",
                "name": "gåga💪🏼",
                "goodsId": 1,
                "count": 5,
                "addTime": "2021-09-09 12:33:33",
                "price": "22.00"
            }
        ],
        "end": true,
        "goods": {
            "id": 1,
            "name": "侨宝2017年酿化陈皮",
            "picUrl": "https://zhongyou-mall.oss-cn-beijing.aliyuncs.com/5xa5i9lzwo8fyv62zx3r.png",
            "unit": "箱",
            "unitType": 1,
            "weight": null,
            "counterPrice": "2298.00",
            "retailPrice": "2298.00",
            "vipPrice": "2298.00",
            "brief": "",
            "gallery": [
                "https://zhongyou-mall.oss-cn-beijing.aliyuncs.com/1h3xlxlboyzxzu6wn4yt.png"
            ],
            "videos": null,
            "tags": null,
            "area": "天马",
            "year": "2017"
        },
        "empty": false,
        "startIndex": 0,
        "totalPage": null
    }
}

```


#### 1.1.6 我的出售(库存管理)

##### 接口说明



##### 请求说明

| http 请求方式          | get    |
|:------------- |:---------------:|
| url      |/stock/list |

#####  输入参数

| 参数          |必选             | 类型       | 参数说明        | 备注          |
|:-------------|:---------------:|:-------------|:-------------|:-------------|
| page      | 否 | int  |  分页 |   |
| limit      | 否 | int  |  每页条数 |   |

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
                "goods": {
                    "id": 1,
                    "name": "侨宝2017年酿化陈皮",
                    "picUrl": "https://zhongyou-mall.oss-cn-beijing.aliyuncs.com/5xa5i9lzwo8fyv62zx3r.png",
                    "unit": "箱",
                    "unitType": 1,
                    "weight": null,
                    "counterPrice": "2298.00",
                    "retailPrice": "2298.00",
                    "vipPrice": "2298.00",
                    "brief": "",
                    "gallery": null,
                    "videos": null,
                    "tags": null,
                    "area": "天马",
                    "year": "2017年"
                },
                "buyPrice": "0.00",
                "amount": 9,
                "freezeAmount": null
            }
        ],
        "end": true,
        "empty": false,
        "startIndex": 0,
        "totalPage": null
    }
}

```


#### 1.1.7 我的求购

##### 接口说明



##### 请求说明

| http 请求方式          | get    |
|:------------- |:---------------:|
| url      |/buy/my_list |

#####  输入参数

| 参数          |必选             | 类型       | 参数说明        | 备注          |
|:-------------|:---------------:|:-------------|:-------------|:-------------|
| page      | 否 | int  |  分页 |   |
| limit      | 否 | int  |  每页条数 |   |

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
                "goods": {
                    "id": 1,
                    "name": "侨宝2017年酿化陈皮",
                    "picUrl": "https://zhongyou-mall.oss-cn-beijing.aliyuncs.com/5xa5i9lzwo8fyv62zx3r.png",
                    "unit": "箱",
                    "unitType": 1,
                    "weight": null,
                    "counterPrice": "2298.00",
                    "retailPrice": "2298.00",
                    "vipPrice": "2298.00",
                    "brief": "",
                    "gallery": null,
                    "videos": null,
                    "tags": null,
                    "area": "天马",
                    "year": "2017年"
                },
                "buyList": [
                    {
                        "id": 1,
                        "uid": 10075,
                        "goodsId": 1,
                        "count": 5,
                        "addTime": "2021-09-09 12:33:33",
                        "price": "22.00",
                        "saleList": null
                    },
                    {
                        "id": 2,
                        "uid": 10075,
                        "goodsId": 1,
                        "count": 1,
                        "addTime": "2021-12-25 18:33:03",
                        "price": "2000.00",
                        "saleList": null
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



#### 1.1.8 下架求购

##### 接口说明



##### 请求说明

| http 请求方式          | post    |
|:------------- |:---------------:|
| url      |/buy/cancel |

#####  输入参数

| 参数          |必选             | 类型       | 参数说明        | 备注          |
|:-------------|:---------------:|:-------------|:-------------|:-------------|
| buyId      | 是 | int  |  求购ID |   |

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


#### 1.1.9 下架出售

##### 接口说明



##### 请求说明

| http 请求方式          | post    |
|:------------- |:---------------:|
| url      |/sale/cancel |

#####  输入参数

| 参数          |必选             | 类型       | 参数说明        | 备注          |
|:-------------|:---------------:|:-------------|:-------------|:-------------|
| saleId      | 是 | int  |  求购ID |   |

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



### 2. 圈子


-------


#### 2.0.1 圈子-求购

##### 接口说明



##### 请求说明

| http 请求方式          | get    |
|:------------- |:---------------:|
| url      |/buy/list_all |

#####  输入参数

| 参数          |必选             | 类型       | 参数说明        | 备注          |
|:-------------|:---------------:|:-------------|:-------------|:-------------|
| uid      | 否 | int  |  用户ID |   |
| page      | 否 | int  |  分页 |   |
| limit      | 否 | int  |  每页条数 |   |

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
                "pageSize": 20,
                "currentPage": 1,
                "list": [
                    {
                        "id": 1,
                        "uid": 10075,
                        "employeeType": 1,
                        "avatar": null,
                        "name": "gåga💪🏼",
                        "goodsId": 1,
                        "count": 5,
                        "addTime": "2021-09-09 12:33:33",
                        "price": "22.00"
                    },
                    {
                        "id": 2,
                        "uid": 10075,
                        "employeeType": null,
                        "avatar": null,
                        "name": "gåga💪🏼",
                        "goodsId": 1,
                        "count": 1,
                        "addTime": "2021-12-25 18:33:03",
                        "price": "2000.00"
                    }
                ],
                "end": true,
                "goods": {
                    "id": 1,
                    "name": "侨宝2017年酿化陈皮",
                    "picUrl": "https://zhongyou-mall.oss-cn-beijing.aliyuncs.com/5xa5i9lzwo8fyv62zx3r.png",
                    "unit": "箱",
                    "unitType": 1,
                    "weight": null,
                    "counterPrice": "2298.00",
                    "retailPrice": "2298.00",
                    "vipPrice": "2298.00",
                    "brief": "",
                    "gallery": null,
                    "videos": null,
                    "tags": null,
                    "area": "天马",
                    "year": "2017年"
                },
                "empty": false,
                "startIndex": 0,
                "totalPage": null
            }
        ],
        "end": true,
        "empty": false,
        "startIndex": 0,
        "totalPage": null
    }
}

```


#### 2.0.2 圈子-出售

##### 接口说明



##### 请求说明

| http 请求方式          | get    |
|:------------- |:---------------:|
| url      |/sale/list_all |

#####  输入参数

| 参数          |必选             | 类型       | 参数说明        | 备注          |
|:-------------|:---------------:|:-------------|:-------------|:-------------|
| page      | 否 | int  |  分页 |   |
| limit      | 否 | int  |  每页条数 |   |

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
                "pageSize": 20,
                "currentPage": 1,
                "list": [
                    {
                        "id": 1,
                        "uid": 10075,
                        "employeeType": 1,
                        "avatar": null,
                        "name": "gåga💪🏼",
                        "goodsId": 1,
                        "count": 1,
                        "addTime": "2021-09-09 12:33:33",
                        "price": "222.00"
                    },
                    {
                        "id": 2,
                        "uid": 10075,
                        "employeeType": null,
                        "avatar": null,
                        "name": "gåga💪🏼",
                        "goodsId": 1,
                        "count": 1,
                        "addTime": null,
                        "price": "2000.00"
                    }
                ],
                "end": true,
                "goods": {
                    "id": 1,
                    "name": "侨宝2017年酿化陈皮",
                    "picUrl": "https://zhongyou-mall.oss-cn-beijing.aliyuncs.com/5xa5i9lzwo8fyv62zx3r.png",
                    "unit": "箱",
                    "unitType": 1,
                    "weight": null,
                    "counterPrice": "2298.00",
                    "retailPrice": "2298.00",
                    "vipPrice": "2298.00",
                    "brief": "",
                    "gallery": null,
                    "videos": null,
                    "tags": null,
                    "area": "天马",
                    "year": "2017年"
                },
                "empty": false,
                "startIndex": 0,
                "totalPage": null
            }
        ],
        "end": true,
        "empty": false,
        "startIndex": 0,
        "totalPage": null
    }
}

```


### 3. 酿化


-------


#### 3.0.1 酿化管理

##### 接口说明



##### 请求说明

| http 请求方式          | get    |
|:------------- |:---------------:|
| url      |/aging/list |

#####  输入参数

| 参数          |必选             | 类型       | 参数说明        | 备注          |
|:-------------|:---------------:|:-------------|:-------------|:-------------|
| page      | 否 | int  |  分页 |   |
| limit      | 否 | int  |  每页条数 |   |

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
                "goods": {  //商品信息
                    "id": 1,
                    "name": "侨宝2017年酿化陈皮",
                    "picUrl": "https://zhongyou-mall.oss-cn-beijing.aliyuncs.com/5xa5i9lzwo8fyv62zx3r.png",
                    "unit": "箱",
                    "unitType": 1,
                    "weight": null,
                    "counterPrice": "2298.00",
                    "retailPrice": "2298.00",
                    "vipPrice": "2298.00",
                    "brief": "",
                    "gallery": null,
                    "videos": null,
                    "tags": null,
                    "area": "天马",
                    "year": "2017年"
                },
                "id": 2,  //库存ID
                "orderId": null,  //订单ID
                "goodsId": 1 // 商品ID
            }
        ],
        "end": true,
        "empty": false,
        "startIndex": 0,
        "totalPage": null
    }
}

```


#### 3.0.2 酿化详情

##### 接口说明



##### 请求说明

| http 请求方式          | get    |
|:------------- |:---------------:|
| url      |/aging/detail |

#####  输入参数

| 参数          |必选             | 类型       | 参数说明        | 备注          |
|:-------------|:---------------:|:-------------|:-------------|:-------------|
| id      | 是 | int  |  库存ID |   |
| page      | 否 | int  |  分页 |   |
| limit      | 否 | int  |  单页条数 |   |
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
                "id": 2,
                "stockId": 2,
                "serviceId": 1,
                "addTime": "2022-01-05 23:08:44",
                "serviceName": "阳光杀虫"
            }
        ],
        "end": true,
        "empty": false,
        "startIndex": 0,
        "totalPage": 1
    }
}
```



### 4. 发票


-------


#### 4.0.1 查看发票信息

##### 接口说明



##### 请求说明

| http 请求方式          | get    |
|:------------- |:---------------:|
| url      |/bill/read |

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
        "uid": 12345,
        "companyName": "北京测试",
        "taxNum": "xxxxxx",
        "type": "转票",
        "address": "地址",
        "name": "姓名",
        "mobile": "12345",
        "addTime": null
    }
}
```


#### 4.0.2 保存发票信息

##### 接口说明

缇娜家

##### 请求说明

| http 请求方式          | post   |
|:------------- |:---------------:|
| url      | /bill/save |

#####  输入参数

| 参数          |必选             | 类型       | 参数说明        | 备注          |
|:-------------|:---------------:|:-------------|:-------------|:-------------|
| uid      | 是| int  |  用户ID |  0 则为平台发票配置  |
| companyName      | 是| string  |  公司名|   |
| taxNum      | 是| string  |  税号 |   |
| type      | 是| string  |  发票类型|  转票/普票  |
| address      | 是| string  |  发票地址 |  |
| name      | 是| string  |  姓名 |  |
| mobile      | 是| string  |  手机号 |  |


    


#####  返回实例

```json
    
{
    "c": 0,
    "m": null,
    "d": {
      
    }
}

```




### 5. 提仓


-------


#### 5.0.1 提仓预览 

##### 接口说明



##### 请求说明

| http 请求方式          | post    |
|:------------- |:---------------:|
| url      |/stock/checkout |

#####  输入参数

 | 参数          |必选             | 类型       | 参数说明        | 备注          |
|:-------------|:---------------:|:-------------|:-------------|:-------------|
| goodsId      | 是| int  |  商品ID | |
| number      | 是| int  |  提仓数量 |   |
| addressId      | 否 | int  |  提货地址 |   |
| payType      | 否 | string  |  支付方式 |  |
| packType      | 否 | int  |  打包方式 | 0: 整箱  1: 大包 2:小包  |


#####  错误说明

#####  返回实例



```json

{
    "c": 0,
    "m": null,
    "d": {
        "payTypes": [ //支付方式列表
            {
                "typeName": "balance",
                "comment": "余额支付",
                "thumbnail": null
            },
            {
                "typeName": "ALIPAYCASH",
                "comment": "支付宝支付",
                "thumbnail": null
            },
            {
                "typeName": "WX_APP",
                "comment": "微信支付",
                "thumbnail": null
            }
        ],
        "address": { //地址
            "id": 2,
            "name": "孟宪德",
            "userId": 10066,
            "province": "河北省",
            "city": "秦皇岛市",
            "county": "北戴河区",
            "addressDetail": "朝阳公园南路甲2号23号",
            "areaCode": "1",
            "postalCode": "2",
            "tel": "13241109876",
            "isDefault": false,
            "addTime": "2021-12-18 19:38:11",
            "updateTime": "2021-12-18 19:38:58",
            "deleted": false,
            "location": "116.475068,39.933085",
            "locationId": "B000A7C61H"
        },
        "goods": { //商品信息
            "id": 1,
            "goodsSn": "00001",
            "name": "侨宝2017年酿化陈皮",
            "categoryId": 0,
            "brandId": 0,
            "gallery": [
                "https://zhongyou-mall.oss-cn-beijing.aliyuncs.com/1h3xlxlboyzxzu6wn4yt.png"
            ],
            "keywords": "",
            "brief": "",
            "isOnSale": true,
            "sortOrder": 100,
            "picUrl": "https://zhongyou-mall.oss-cn-beijing.aliyuncs.com/5xa5i9lzwo8fyv62zx3r.png",
            "shareUrl": "",
            "isNew": true,
            "isHot": false,
            "unit": "箱",
            "counterPrice": "2298.00",
            "retailPrice": "2298.00",
            "vipPrice": "2298.00",
            "addTime": "2021-11-24 15:08:40",
            "updateTime": "2022-01-11 01:35:46",
            "deleted": false,
            "tags": null,
            "videos": null,
            "testReports": null,
            "goodsType": 0,
            "expressType": 0,
            "area": "天马",
            "year": "2017",
            "unitType": 1,
            "weight": 18000,
            "detail": [
                {
                    "url": "https://zhongyou-mall.oss-cn-beijing.aliyuncs.com/pmrcuwt2z2i8r7luv0er.jpg",
                    "size": "790*682"
                },
                {
                    "url": "https://zhongyou-mall.oss-cn-beijing.aliyuncs.com/qnobzj1h3e0jktmy7ck8.jpg",
                    "size": "790*899"
                },
                {
                    "url": "https://zhongyou-mall.oss-cn-beijing.aliyuncs.com/1zj83hoxhjt1gunwk3je.jpg",
                    "size": "790*899"
                },
                {
                    "url": "https://zhongyou-mall.oss-cn-beijing.aliyuncs.com/6ezps7996rqnmxpfqjvn.jpg",
                    "size": "790*898"
                },
                {
                    "url": "https://zhongyou-mall.oss-cn-beijing.aliyuncs.com/rgzal4xtrlsigth749sq.jpg",
                    "size": "790*899"
                },
                {
                    "url": "https://zhongyou-mall.oss-cn-beijing.aliyuncs.com/z73132dp9vzdft7f8b4l.jpg",
                    "size": "790*899"
                },
                {
                    "url": "https://zhongyou-mall.oss-cn-beijing.aliyuncs.com/z7opj5e64khgzytkr5xn.jpg",
                    "size": "790*898"
                },
                {
                    "url": "https://zhongyou-mall.oss-cn-beijing.aliyuncs.com/s55tevmi69vi9jxsnqjs.jpg",
                    "size": "790*899"
                },
                {
                    "url": "https://zhongyou-mall.oss-cn-beijing.aliyuncs.com/4in6p6ue6xbhgmq3a90i.jpg",
                    "size": "790*899"
                },
                {
                    "url": "https://zhongyou-mall.oss-cn-beijing.aliyuncs.com/2unsmej0hla48pqh55nd.jpg",
                    "size": "790*898"
                },
                {
                    "url": "https://zhongyou-mall.oss-cn-beijing.aliyuncs.com/mim5e5epc5owcwrm060t.jpg",
                    "size": "790*899"
                },
                {
                    "url": "https://zhongyou-mall.oss-cn-beijing.aliyuncs.com/53402o648madbhjfthil.jpg",
                    "size": "790*71"
                },
                {
                    "url": "https://zhongyou-mall.oss-cn-beijing.aliyuncs.com/x346n1bz76oqzf96hob8.jpg",
                    "size": "790*406"
                },
                {
                    "url": "https://zhongyou-mall.oss-cn-beijing.aliyuncs.com/x4fel6n3j9q0xmdv4fv0.jpg",
                    "size": "790*899"
                },
                {
                    "url": "https://zhongyou-mall.oss-cn-beijing.aliyuncs.com/ycnrxhmssf9i1nq66rph.png",
                    "size": "414*414"
                },
                {
                    "url": "https://zhongyou-mall.oss-cn-beijing.aliyuncs.com/5x74ql6jh0txon2okliz.png",
                    "size": "414*349"
                },
                {
                    "url": "https://zhongyou-mall.oss-cn-beijing.aliyuncs.com/ost9oo38jvlgt1spdcmp.png",
                    "size": "414*359"
                },
                {
                    "url": "https://zhongyou-mall.oss-cn-beijing.aliyuncs.com/dyk7zbxmadffek9wfemc.png",
                    "size": "414*359"
                },
                {
                    "url": "https://zhongyou-mall.oss-cn-beijing.aliyuncs.com/p370jcw2dibk1kujnlfs.png",
                    "size": "414*349"
                },
                {
                    "url": "https://zhongyou-mall.oss-cn-beijing.aliyuncs.com/fqr65cxldy56piy3ja61.png",
                    "size": "414*524"
                }
            ],
            "agingImages": [
                {
                    "url": "https://zhongyou-mall.oss-cn-beijing.aliyuncs.com/wycvrsvg20tzj018sbmb.png",
                    "size": "750*3326"
                }
            ]
        },
        "actualPrice": "760.00",  //实付金额
        "packingFee": "760.00", //打包费用
        "userStock": { //库存信息
            "id": 3,
            "uid": 10066,
            "goodsId": 1,
            "amount": 998,
            "freezeAmount": 62,
            "addTime": null,
            "updateTime": "2022-01-11 18:12:19"
        }
    }
}

```


#### 5.0.2 发起提仓订单

##### 接口说明

缇娜家

##### 请求说明

| http 请求方式          | post   |
|:------------- |:---------------:|
| url      | /stock/submit |

#####  输入参数

 | 参数          |必选             | 类型       | 参数说明        | 备注          |
|:-------------|:---------------:|:-------------|:-------------|:-------------|
| goodsId      | 是| int  |  商品ID | |
| number      | 是| int  |  提仓数量 |   |
| addressId      | 是 | int  |  提货地址 |   |
| payType      | 是 | string  |  支付方式 |  |
| packType      | 否 | int  |  打包方式 | 0: 整箱  1: 大包 2:小包  |


    


#####  返回实例

```json
    
{
    "c": 0,
    "m": null,
    "d": {
        "payOrderId": "79",
        "outPayOrderId": "prepay_id=wx11182107984767bd2ec008623bbdff0000",
        "callPayInfo": "{\"appId\":\"wxb0a09ff275fac5ad\",\"nonceStr\":\"1641896468076\",\"packageValue\":\"prepay_id=wx11182107984767bd2ec008623bbdff0000\",\"paySign\":\"CEA33A1552F0C991A6A7769F9E3C3B71\",\"signType\":\"MD5\",\"timeStamp\":\"1641896468\"}",
        "payCallbackInfo": null
    }
}

```