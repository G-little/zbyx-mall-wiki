# 分类接口

[TOC]
## 修订记录
----
日期 | 作者 | 修订类型 | 修订内容 | 版本|
---- | ---- | ---- | ---- | ---- |
2020年07月03日|冷立纲|A|新增设计方案|1.0|

> 【修订类型：A-新增  M-修改 D-删除】

## 背景

分类相关接口

## 产品说明



## 关键流程说明

## 接口说明




#### 1.1 分类首页接口

##### 接口说明

首页数据

##### 请求说明

| http 请求方式          | get     |
|:------------- |:---------------:|
| url      | /catalog/index |

#####  输入参数
| 参数          |必选             | 类型       | 参数说明        | 备注          |
|:-------------|:---------------:|:-------------|:-------------|:-------------|
| id      | 否|  int  | 分类ID  |  默认 取第一个分类 |


#####  错误说明


#####  返回实例
```json
    
{
    "c":0,
    "m":null,
    "d":{
        "categoryList":[ //分类列表
            {
                "id":34,
                "name":"♥“吃了吗？”",
                "keywords":"",
                "desc":"外卖店铺",
                "pid":0,
                "iconUrl":"",
                "picUrl":"",
                "level":"L1",
                "sortOrder":50,
                "addTime":"2021-03-21 11:48:40",
                "updateTime":"2021-04-26 10:46:11",
                "deleted":false
            },
            {
                "id":35,
                "name":"新鲜果蔬",
                "keywords":"",
                "desc":"新鲜果蔬",
                "pid":0,
                "iconUrl":"",
                "picUrl":"",
                "level":"L1",
                "sortOrder":50,
                "addTime":"2021-03-22 10:57:13",
                "updateTime":"2021-04-29 10:07:07",
                "deleted":false
            },
            {
                "id":36,
                "name":"肉蛋水产豆制品",
                "keywords":"",
                "desc":"肉蛋水产",
                "pid":0,
                "iconUrl":"",
                "picUrl":"",
                "level":"L1",
                "sortOrder":50,
                "addTime":"2021-03-22 10:57:42",
                "updateTime":"2021-04-29 10:07:31",
                "deleted":false
            },
            {
                "id":37,
                "name":"粮油调味",
                "keywords":"",
                "desc":"粮油调味",
                "pid":0,
                "iconUrl":"",
                "picUrl":"",
                "level":"L1",
                "sortOrder":50,
                "addTime":"2021-03-22 10:58:16",
                "updateTime":"2021-03-22 16:12:23",
                "deleted":false
            },
            {
                "id":38,
                "name":"零食酒水",
                "keywords":"",
                "desc":"零食酒水",
                "pid":0,
                "iconUrl":"",
                "picUrl":"",
                "level":"L1",
                "sortOrder":50,
                "addTime":"2021-03-22 10:58:37",
                "updateTime":"2021-03-22 16:12:30",
                "deleted":false
            },
            {
                "id":39,
                "name":"家居百货",
                "keywords":"",
                "desc":"家居百货",
                "pid":0,
                "iconUrl":"",
                "picUrl":"",
                "level":"L1",
                "sortOrder":50,
                "addTime":"2021-03-22 10:58:56",
                "updateTime":"2021-03-22 16:12:48",
                "deleted":false
            }
        ],
        "currentCategory":{  //当前分类
            "id":35,
            "name":"新鲜果蔬",
            "keywords":"",
            "desc":"新鲜果蔬",
            "pid":0,
            "iconUrl":"",
            "picUrl":"",
            "level":"L1",
            "sortOrder":50,
            "addTime":"2021-03-22 10:57:13",
            "updateTime":"2021-04-29 10:07:07",
            "deleted":false
        },
        "currentSubCategory":[ //子分类列表
            {
                "id":41,
                "name":"水果",
                "keywords":"",
                "desc":"",
                "pid":35,
                "iconUrl":"",
                "picUrl":"",
                "level":"L2",
                "sortOrder":50,
                "addTime":"2021-04-29 10:07:55",
                "updateTime":"2021-04-29 10:07:55",
                "deleted":false
            },
            {
                "id":42,
                "name":"蔬菜",
                "keywords":"",
                "desc":"",
                "pid":35,
                "iconUrl":"",
                "picUrl":"",
                "level":"L2",
                "sortOrder":50,
                "addTime":"2021-04-29 10:08:04",
                "updateTime":"2021-04-29 10:08:04",
                "deleted":false
            }
        ],
        "categoryGoodsMap":{ //子分类对应商品数据
            "42":{
                "pageSize":10,
                "currentPage":1,
                "list":null,
                "end":true,
                "totalPage":null,
                "startIndex":0,
                "empty":true
            },
            "41":{
                "pageSize":10,
                "currentPage":1,
                "list":[
                    {
                        "id":313,
                        "name":"【同城配送】☺新西兰加力果1斤3颗",
                        "picUrl":"https://saiwai.oss-cn-huhehaote.aliyuncs.com/kewclilvgoy6d6e4vzhr.jpg",
                        "unit":"组",
                        "counterPrice":10,
                        "retailPrice":10,
                        "vipPrice":10,
                        "brief":"姬娜果，又称“加力果”、“皇家加力果”，原产于新西兰。",
                        "gallery":[
                            "https://saiwai.oss-cn-huhehaote.aliyuncs.com/454mm22b8a8cifb32qsh.jpg",
                            "https://saiwai.oss-cn-huhehaote.aliyuncs.com/bsam8hbd1wsfin3wq1ih.jpg",
                            "https://saiwai.oss-cn-huhehaote.aliyuncs.com/gsjjg7m63tyja23g5hdf.jpg",
                            "https://saiwai.oss-cn-huhehaote.aliyuncs.com/nrryvvgxxdjnbw7s34ut.jpg"
                        ],
                        "videos":null,
                        "tags":null
                    },
                    {
                        "id":319,
                        "name":"【同城配送】☺冰淇淋西瓜（黄壤）一颗",
                        "picUrl":"https://saiwai.oss-cn-huhehaote.aliyuncs.com/gfzt15yb5u92iha4tb1y.jpg",
                        "unit":"颗",
                        "counterPrice":20,
                        "retailPrice":20,
                        "vipPrice":20,
                        "brief":"",
                        "gallery":[
                            "https://saiwai.oss-cn-huhehaote.aliyuncs.com/ojvnn4vio8rm022cpzce.jpg",
                            "https://saiwai.oss-cn-huhehaote.aliyuncs.com/95z0umdeygswdwl4r2k9.jpg",
                            "https://saiwai.oss-cn-huhehaote.aliyuncs.com/vpaia5o1ks91ujr8itvi.jpg",
                            "https://saiwai.oss-cn-huhehaote.aliyuncs.com/fuyxaub2kgu0mxmkn3jj.jpg",
                            "https://saiwai.oss-cn-huhehaote.aliyuncs.com/i7tgbbn0jssl4bhcnoss.jpg"
                        ],
                        "videos":null,
                        "tags":null
                    },
                    {
                        "id":321,
                        "name":"【同城配送】☺月萝哈密瓜一颗",
                        "picUrl":"https://saiwai.oss-cn-huhehaote.aliyuncs.com/zzgl4vpytzcwk5xu4xpc.jpg",
                        "unit":"颗",
                        "counterPrice":29.9,
                        "retailPrice":29.9,
                        "vipPrice":29.9,
                        "brief":"",
                        "gallery":[
                            "https://saiwai.oss-cn-huhehaote.aliyuncs.com/c646376tkaaz33w6qz3t.jpg",
                            "https://saiwai.oss-cn-huhehaote.aliyuncs.com/hfacgsx2njzkd8tf0r4j.jpg",
                            "https://saiwai.oss-cn-huhehaote.aliyuncs.com/0fmnsqk1wkuxn3kxg2k5.jpg",
                            "https://saiwai.oss-cn-huhehaote.aliyuncs.com/m5bf735p2u281hsturq1.jpg"
                        ],
                        "videos":null,
                        "tags":null
                    }
                ],
                "end":true,
                "totalPage":null,
                "startIndex":0,
                "empty":false
            }
        }
    }
}
```




#### 1.2 分类分页获取商品接口

##### 接口说明

分页获取分类商品数据接口

##### 请求说明

| http 请求方式          | get     |
|:------------- |:---------------:|
| url      | /catalog/goods_list |

#####  输入参数
| 参数          |必选             | 类型       | 参数说明        | 备注          |
|:-------------|:---------------:|:-------------|:-------------|:-------------|
| id      | 否|  int  | 分类ID  |  默认 取第一个分类 |
| page      | 否|  int  | 分页  |  |
| limit      | 否|  int  | 单页条数  |  |


#####  错误说明


#####  返回实例
```json
    
{
    "c":0,
    "m":null,
    "d":{
        "pageSize":10,
        "currentPage":1,
        "list":[
            {
                "id":4,
                "name":"【同城配送】塞外明珠张家口甜糯玉米 200g*10",
                "picUrl":"https://saiwai.oss-cn-huhehaote.aliyuncs.com/0xawx5lqsrpxo88knpgm.jpg",
                "unit":"箱",
                "counterPrice":49.9,
                "retailPrice":39.9,
                "vipPrice":39.9,
                "brief":"颗粒饱满 软糯鲜香",
                "gallery":[
                    "https://saiwai.oss-cn-huhehaote.aliyuncs.com/ku5qf8mx89a0m5bz7ng8.jpg",
                    "https://saiwai.oss-cn-huhehaote.aliyuncs.com/e2kwyi7ymtl7h9yreqfj.jpg",
                    "https://saiwai.oss-cn-huhehaote.aliyuncs.com/49s8xdaipmvqkaq4rcwu.jpg",
                    "https://saiwai.oss-cn-huhehaote.aliyuncs.com/olbkouv5gfx3bebz9dqp.jpg"
                ],
                "videos":null,
                "tags":null
            },
            {
                "id":193,
                "name":"【同城配送】混合沙拉蔬菜组合装",
                "picUrl":"https://saiwai.oss-cn-huhehaote.aliyuncs.com/1u4lfujghx35ripjcnim.jpg",
                "unit":"套",
                "counterPrice":29.9,
                "retailPrice":29.9,
                "vipPrice":29.9,
                "brief":"每种蔬菜450g±50g，送柠檬2颗",
                "gallery":[
                    "https://saiwai.oss-cn-huhehaote.aliyuncs.com/yqaar9cgnpaf6x3cazst.jpg",
                    "https://saiwai.oss-cn-huhehaote.aliyuncs.com/xxp5llk3ht5hq5drkbyk.jpg",
                    "https://saiwai.oss-cn-huhehaote.aliyuncs.com/lbp0xhx7fo3wa29p6mpx.jpg",
                    "https://saiwai.oss-cn-huhehaote.aliyuncs.com/dfreq99ce09cnekxb1xe.jpg",
                    "https://saiwai.oss-cn-huhehaote.aliyuncs.com/puuskx3umlf0kqwmnk66.jpg"
                ],
                "videos":null,
                "tags":null
            },
            {
                "id":194,
                "name":"【同城配送】混合火锅蔬菜组合装",
                "picUrl":"https://saiwai.oss-cn-huhehaote.aliyuncs.com/cr4qq94nl4uon2el51h2.jpg",
                "unit":"套",
                "counterPrice":49.9,
                "retailPrice":49.9,
                "vipPrice":49.9,
                "brief":"精选15种菜品，火锅必备",
                "gallery":[
                    "https://saiwai.oss-cn-huhehaote.aliyuncs.com/t2arprcbcrk2v4spbk1p.jpg",
                    "https://saiwai.oss-cn-huhehaote.aliyuncs.com/16rcnlt5uy99tbvaz3k4.jpg",
                    "https://saiwai.oss-cn-huhehaote.aliyuncs.com/rfpxhafefih29e1uiwjd.jpg",
                    "https://saiwai.oss-cn-huhehaote.aliyuncs.com/2ev783sjr9ea63lpqos6.jpg"
                ],
                "videos":null,
                "tags":null
            },
            {
                "id":213,
                "name":"【同城配送】农创客优选冬瓜约800g",
                "picUrl":"https://saiwai.oss-cn-huhehaote.aliyuncs.com/2o0slbeou88vo2m6fbeb.jpg",
                "unit":"克",
                "counterPrice":8.9,
                "retailPrice":8.9,
                "vipPrice":8.9,
                "brief":"",
                "gallery":[
                    "https://saiwai.oss-cn-huhehaote.aliyuncs.com/xivwz5k94sjzkpjr6nhs.jpg",
                    "https://saiwai.oss-cn-huhehaote.aliyuncs.com/i07va4srk4jo6j8ad0q4.jpg",
                    "https://saiwai.oss-cn-huhehaote.aliyuncs.com/4ndhi5ur5xev8kjipx0x.jpg"
                ],
                "videos":null,
                "tags":null
            },
            {
                "id":214,
                "name":"【同城配送】农创客优选大葱450±50g",
                "picUrl":"https://saiwai.oss-cn-huhehaote.aliyuncs.com/8p972dlp5w03t0i7bpgo.jpg",
                "unit":"g",
                "counterPrice":7.9,
                "retailPrice":7.9,
                "vipPrice":7.9,
                "brief":"",
                "gallery":[
                    "https://saiwai.oss-cn-huhehaote.aliyuncs.com/14yb1s1viwbd3alav6fb.jpg",
                    "https://saiwai.oss-cn-huhehaote.aliyuncs.com/1idtto7hl0wguu86urql.jpg",
                    "https://saiwai.oss-cn-huhehaote.aliyuncs.com/z20kutsqu5bf0hl5hari.jpg",
                    "https://saiwai.oss-cn-huhehaote.aliyuncs.com/zgu3sglvcdlzc27pn826.jpg",
                    "https://saiwai.oss-cn-huhehaote.aliyuncs.com/i1ruz7ex0e3xupf73mln.jpg"
                ],
                "videos":null,
                "tags":null
            },
            {
                "id":215,
                "name":"【同城配送】农创客优选土豆450±50g",
                "picUrl":"https://saiwai.oss-cn-huhehaote.aliyuncs.com/j5m18kw869qdmnoxv7la.jpg",
                "unit":"克",
                "counterPrice":3.9,
                "retailPrice":3.9,
                "vipPrice":3.9,
                "brief":"",
                "gallery":[
                    "https://saiwai.oss-cn-huhehaote.aliyuncs.com/a5ttedshqnxx9vp1t1j1.jpg",
                    "https://saiwai.oss-cn-huhehaote.aliyuncs.com/3b213lf6169v9f23ukey.jpg",
                    "https://saiwai.oss-cn-huhehaote.aliyuncs.com/ngjeauqzpdjmxrnf90my.png"
                ],
                "videos":null,
                "tags":null
            },
            {
                "id":216,
                "name":"【同城配送】农创客优选白葱头800±50g",
                "picUrl":"https://saiwai.oss-cn-huhehaote.aliyuncs.com/xwh5paydkzmu57p1rg6h.jpg",
                "unit":"g",
                "counterPrice":3.5,
                "retailPrice":3.5,
                "vipPrice":3.5,
                "brief":"",
                "gallery":[
                    "https://saiwai.oss-cn-huhehaote.aliyuncs.com/bcjvh4ow9gyoqul0xe3i.jpg",
                    "https://saiwai.oss-cn-huhehaote.aliyuncs.com/x9mj2dyytw8ec7ds3hrg.jpg",
                    "https://saiwai.oss-cn-huhehaote.aliyuncs.com/4ws8kaz45h6dgf1t01rm.jpg",
                    "https://saiwai.oss-cn-huhehaote.aliyuncs.com/kxrldjwcqanrzcrwc294.jpg",
                    "https://saiwai.oss-cn-huhehaote.aliyuncs.com/wm0skdfd6twrpqocykjr.jpg"
                ],
                "videos":null,
                "tags":null
            },
            {
                "id":217,
                "name":"【同城配送】农创客优选紫葱头900±50g",
                "picUrl":"https://saiwai.oss-cn-huhehaote.aliyuncs.com/fd4qe6jlrd0purrlei24.jpg",
                "unit":"克",
                "counterPrice":6.9,
                "retailPrice":6.9,
                "vipPrice":6.9,
                "brief":"",
                "gallery":[
                    "https://saiwai.oss-cn-huhehaote.aliyuncs.com/1wci6dbdu16grc2wwon4.jpg",
                    "https://saiwai.oss-cn-huhehaote.aliyuncs.com/fyvbszk479jshmvhgfhd.jpg",
                    "https://saiwai.oss-cn-huhehaote.aliyuncs.com/cp238g3riwgbv3srnu6e.jpg"
                ],
                "videos":null,
                "tags":null
            },
            {
                "id":218,
                "name":"【同城配送】农创客优选铁棍山药450±50g",
                "picUrl":"https://saiwai.oss-cn-huhehaote.aliyuncs.com/u0ur3zf1x3jtvwly7n0g.jpg",
                "unit":"g",
                "counterPrice":7.9,
                "retailPrice":7.9,
                "vipPrice":7.9,
                "brief":"",
                "gallery":[
                    "https://saiwai.oss-cn-huhehaote.aliyuncs.com/k388uzxizhtjy77p98th.jpg",
                    "https://saiwai.oss-cn-huhehaote.aliyuncs.com/yf4xbuley1f8i8n528d5.jpg",
                    "https://saiwai.oss-cn-huhehaote.aliyuncs.com/k9nycr9cyd7jsi9dyrba.jpg"
                ],
                "videos":null,
                "tags":null
            },
            {
                "id":219,
                "name":"【同城配送】农创客优选鲜藕400±50g",
                "picUrl":"https://saiwai.oss-cn-huhehaote.aliyuncs.com/cefuy71r80s7dnl1j0uy.jpg",
                "unit":"克",
                "counterPrice":6.9,
                "retailPrice":6.9,
                "vipPrice":6.9,
                "brief":"",
                "gallery":[
                    "https://saiwai.oss-cn-huhehaote.aliyuncs.com/v2cms3drlk7xc018xxtl.jpg",
                    "https://saiwai.oss-cn-huhehaote.aliyuncs.com/w6c4c98wt88zf7ln74jj.jpg",
                    "https://saiwai.oss-cn-huhehaote.aliyuncs.com/29r632mw0rk7vuqm323h.jpg"
                ],
                "videos":null,
                "tags":null
            }
        ],
        "end":false,
        "totalPage":null,
        "startIndex":0,
        "empty":false
    }
}

```







