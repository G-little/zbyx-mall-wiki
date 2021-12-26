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

