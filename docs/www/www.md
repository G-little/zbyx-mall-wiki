# 官网接口文档

[TOC]
## 修订记录
----
日期 | 作者 | 修订类型 | 修订内容 | 版本|
---- | ---- | ---- | ---- | ---- |
2020年07月03日|冷立纲|A|新增设计方案|1.0|

> 【修订类型：A-新增  M-修改 D-删除】

## 背景

商城用户注册登录相关接口

## 产品说明



## 关键流程说明

## 接口说明

### 1 新闻

-------


#### 1.1 新闻列表

##### 接口说明

分页拉取新闻列表

##### 请求说明

| http 请求方式          |get            |
|:------------- |:---------------:|
| url      | {{host}}/www/news/list |
| token说明      | 无 |

#####  输入参数



| 参数          |必选             | 类型       | 参数说明        | 备注          |
|:-------------|:---------------:|:-------------|:-------------|:-------------|
| page      | 否| int  |  分页 | 默认值1   |
| limit      | 否 | int  |  分页条数 | 默认值10   |

#####  错误说明




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
                "id": 1,
                "title": "test",
                "brief": "test",
                "addTime": null,
                "deleted": false,
                "enabled": false,
                "content": null
            }
        ],
        "end": true,
        "empty": false,
        "startIndex": 0,
        "totalPage": 1
    }
}
```


#### 1.2 新闻详情

##### 接口说明



##### 请求说明

| http 请求方式          |get            |
|:------------- |:---------------:|
| url      | {{host}}/www/news/detail |
| token说明      |如果是更换手机号，校验手机身份需要登陆状态|

#####  输入参数



| 参数          |必选             | 类型       | 参数说明        | 备注          |
|:-------------|:---------------:|:-------------|:-------------|:-------------|
| id      | 是 | int  |  新闻ID | |

#####  错误说明




#####  返回实例

```json
{
    "c": 0,
    "m": null,
    "d": {
        "id": 1,
        "title": "test",
        "brief": "test",
        "addTime": null,
        "deleted": false,
        "enabled": false,
        "content": "content"
    }
}

```


### 2 产品


-------


#### 2.1 产品列表

##### 接口说明

分页拉取新闻列表

##### 请求说明

| http 请求方式          |get            |
|:------------- |:---------------:|
| url      | {{host}}/www/product/list |
| token说明      | 无 |

#####  输入参数



| 参数          |必选             | 类型       | 参数说明        | 备注          |
|:-------------|:---------------:|:-------------|:-------------|:-------------|
| page      | 否| int  |  分页 | 默认值1   |
| limit      | 否 | int  |  分页条数 | 默认值10   |

#####  错误说明




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
                "id": 1,
                "name": "test",
                "brief": "xxx",
                "addTime": null,
                "deleted": false,
                "images": [
                    "/a"
                ],
                "enabled": false
            }
        ],
        "end": true,
        "empty": false,
        "startIndex": 0,
        "totalPage": 1
    }
}
```

#### 2.2 产品详情

##### 接口说明



##### 请求说明

| http 请求方式          |get            |
|:------------- |:---------------:|
| url      | {{host}}/www/product/detail |
| token说明      | |

#####  输入参数


| 参数          |必选             | 类型       | 参数说明        | 备注          |
|:-------------|:---------------:|:-------------|:-------------|:-------------|
| id      | 是 | int  |  产品ID | |

#####  错误说明




#####  返回实例

```json
{
    "c": 0,
    "m": null,
    "d": {
        "id": 1,
        "name": "test",
        "brief": "xxx",
        "addTime": null,
        "deleted": false,
        "images": [
            "/a"
        ],
        "enabled": false
    }
}

```

### 3 活动


-------



#### 3.1 活动列表

##### 接口说明

分页拉取新闻列表

##### 请求说明

| http 请求方式          |get            |
|:------------- |:---------------:|
| url      | {{host}}/www/promotion/list |
| token说明      | |

#####  输入参数



| 参数          |必选             | 类型       | 参数说明        | 备注          |
|:-------------|:---------------:|:-------------|:-------------|:-------------|
| page      | 否| int  |  分页 | 默认值1   |
| limit      | 否 | int  |  分页条数 | 默认值10   |

#####  错误说明




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
                "id": 1,
                "name": "test",
                "brief": "xxx",
                "addTime": null,
                "deleted": false,
                "images": [
                    "/a"
                ],
                "enabled": false
            }
        ],
        "end": true,
        "empty": false,
        "startIndex": 0,
        "totalPage": 1
    }
}
```


#### 3.2 活动详情

##### 接口说明



##### 请求说明

| http 请求方式          |get            |
|:------------- |:---------------:|
| url      | {{host}}/www/promotion/detail |
| token说明      ||

#####  输入参数



| 参数          |必选             | 类型       | 参数说明        | 备注          |
|:-------------|:---------------:|:-------------|:-------------|:-------------|
| id      | 是 | int  |  产品ID | |

#####  错误说明




#####  返回实例

```json
{
    "c": 0,
    "m": null,
    "d": {
        "id": 1,
        "name": "test",
        "brief": "xxx",
        "addTime": null,
        "deleted": false,
        "images": [
            "/a"
        ],
        "enabled": false
    }
}

```


### 4 首页

-------


#### 3.2 活动详情

##### 接口说明



##### 请求说明

| http 请求方式          |get            |
|:------------- |:---------------:|
| url      | {{host}}/www/index |
| token说明      ||

#####  输入参数



无

#####  错误说明




#####  返回实例

{
    "c": 0,
    "m": null,
    "d": {
        "c": 0,
        "m": null,
        "d": {
            "newsList": {
                "pageSize": 10,
                "currentPage": 1,
                "list": [
                    {
                        "id": 1,
                        "title": "test2",
                        "brief": "test",
                        "addTime": null,
                        "deleted": false,
                        "enabled": true,
                        "content": null
                    }
                ],
                "end": true,
                "empty": false,
                "startIndex": 0,
                "totalPage": 1
            },
            "promotionList": {
                "pageSize": 10,
                "currentPage": 1,
                "list": [
                    {
                        "id": 1,
                        "name": "huodong",
                        "images": [
                            "/c"
                        ],
                        "addTime": null,
                        "brief": "test",
                        "enabled": true,
                        "deleted": false
                    }
                ],
                "end": true,
                "empty": false,
                "startIndex": 0,
                "totalPage": 1
            },
            "productList": {
                "pageSize": 10,
                "currentPage": 1,
                "list": [
                    {
                        "id": 1,
                        "name": "test",
                        "brief": "xxx",
                        "addTime": null,
                        "deleted": false,
                        "images": [
                            "/a"
                        ],
                        "enabled": true
                    }
                ],
                "end": true,
                "empty": false,
                "startIndex": 0,
                "totalPage": 1
            }
        }
    }
}
























