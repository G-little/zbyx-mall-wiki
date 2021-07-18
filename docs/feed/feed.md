# 圈子接口文档

[TOC]
## 修订记录
----
日期 | 作者 | 修订类型 | 修订内容 | 版本|
---- | ---- | ---- | ---- | ---- |
2020年07月03日|冷立纲|A|新增设计方案|1.0|

> 【修订类型：A-新增  M-修改 D-删除】

## 背景

圈子接口文档

## 产品说明



## 关键流程说明

## 接口说明


#### 1.0 圈子分页列表

##### 接口说明



##### 请求说明

| http 请求方式          |get             |
|:------------- |:---------------:|
| url      |/feed/list |

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
        "pageSize": 10,
        "currentPage": 1,
        "list": [
            {
                "id": 1,  //id
                "uid": 10060, // 用户id
                "name": "微信用户", //用户昵称
                "avatar": "https://thirdwx.qlogo.cn/mmopen/vi_32/ POgEwh4mIHO4nibH0KlMECNjjGxQUq24ZEaGT4poC6icRiccVGKSyXwibcPq4BWmiaIGuG1icwxaQX6grC9VemZoJ8rg/132", //用户头像
                "feedType": 1, //圈子类型 1 动态 2 求购 3 出货
                "addr": "test", //地址
                "content": "test", //内容
                "phoneNum": null, //手机号
                "bid": null, //价格
                "images": [ //图片列表
                    "xxxxx"
                ],
                "addTime": "2021-07-18 16:01:38", //添加时间
                "deleted": false, //是否删除
                "thumbCount": 0, //点赞数
                "commentCount": 0, //评论数
                "readCount": 0 //阅读数
            }
        ],
        "end": true,
        "totalPage": null,
        "startIndex": 0,
        "empty": false
    }
}

```


#### 1.1 添加圈子动态

##### 接口说明



##### 请求说明

| http 请求方式          |post             |
|:------------- |:---------------:|
| url      |/feed/add |

#####  输入参数

| 参数          |必选             | 类型       | 参数说明        | 备注          |
|:-------------|:---------------:|:-------------|:-------------|:-------------|
| feedType      | 是| int  |  圈子类型  |   1 动态 2 求购 3 出货 |
| addr      | 是| string  |  地址 |   |
| content      | 是 | string  |  内容 ||
| phoneNum      | 否| string  |  手机号 |  求购/出货必填 |
| bid      | 否| string  |  价格 |  求购/出货必填 |
| images      | 否| string  |  图片数组字符串 |  例如 ['a','b'] |

#####  错误说明





#####  返回实例
```json


{
    "c": 0,
    "m": null,
    "d": {
        "id":1  //ID
    }
}

```



#### 1.2 点赞接口

##### 接口说明



##### 请求说明

| http 请求方式          |post             |
|:------------- |:---------------:|
| url      | /feed/interact/thumb |

#####  输入参数

| 参数          |必选             | 类型       | 参数说明        | 备注          |
|:-------------|:---------------:|:-------------|:-------------|:-------------|
| id      | 是 | int  |  圈子ID |  |
| value      |  是 | boolean  |  点赞值 |   true 点赞 false 取消|

#####  错误说明





#####  返回实例
```json


{
    "c": 0,
    "m": null,
    "d": {
        "status": true  //点赞状态 true 点赞  false 取消
    }
}
```



#### 1.3 评论接口

##### 接口说明



##### 请求说明

| http 请求方式          |post             |
|:------------- |:---------------:|
| url      | /feed/interact/comment |

#####  输入参数

| 参数          |必选             | 类型       | 参数说明        | 备注          |
|:-------------|:---------------:|:-------------|:-------------|:-------------|
| id      | 是 | int  |  圈子ID |  |
| content      |  是 | string  |   评论内容 |   |

#####  错误说明





#####  返回实例
```json


{
    "c": 0,
    "m": null,
    "d": {
        "id": 1  //评论id
    }
}
```


#### 1.4 详情接口

##### 接口说明



##### 请求说明

| http 请求方式          |get             |
|:------------- |:---------------:|
| url      | /feed/detail|

#####  输入参数

| 参数          |必选             | 类型       | 参数说明        | 备注          |
|:-------------|:---------------:|:-------------|:-------------|:-------------|
| id      | 是 | int  |  圈子ID |  |

#####  错误说明





#####  返回实例
```json


{
    "c": 0,
    "m": null,
    "d": {
        "id": 1,  //id
        "uid": 10060, // 用户id
        "name": "微信用户", //用户昵称
        "avatar": "https://thirdwx.qlogo.cn/mmopen/vi_32/ POgEwh4mIHO4nibH0KlMECNjjGxQUq24ZEaGT4poC6icRiccVGKSyXwibcPq4BWmiaIGuG1icwxaQX6grC9VemZoJ8rg/132", //用户头像
        "feedType": 1, //圈子类型 1 动态 2 求购 3 出货
        "addr": "test", //地址
        "content": "test", //内容
        "phoneNum": null, //手机号
        "bid": null, //价格
        "images": [ //图片列表
            "xxxxx"
        ],
        "addTime": "2021-07-18 16:01:38", //添加时间
        "deleted": false, //是否删除
        "thumbCount": 0, //点赞数
        "commentCount": 0, //评论数
        "readCount": 0 //阅读数
        "commentList": {
            "pageSize": 10,
            "currentPage": 1,
            "list": [
                {
                    "id": 2,
                    "feedId": 1,
                    "uid": 10060,
                    "type": 2,
                    "addTime": "2021-07-18 16:23:43",
                    "content": "test"  // 评论内容
                }
            ],
            "end": true,
            "totalPage": 1,
            "startIndex": 0,
            "empty": false
        }
    }
}

```


#### 1.5 分页拉取评论列表

##### 接口说明



##### 请求说明

| http 请求方式          |get             |
|:------------- |:---------------:|
| url      | /feed/comment/list |

#####  输入参数

| 参数          |必选             | 类型       | 参数说明        | 备注          |
|:-------------|:---------------:|:-------------|:-------------|:-------------|
| id      | 是 | int  |  圈子ID |  |

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
                "feedId": 1,  //圈子ID
                "uid": 10060, //用户ID
                "type": 2, //类型  0 点赞 1 浏览 2评论
                "addTime": "2021-07-18 16:23:43", //发表时间
                "content": "test" //评论内容
            }
        ],
        "end": true,
        "totalPage": 1,
        "startIndex": 0,
        "empty": false
    }
}
```





















