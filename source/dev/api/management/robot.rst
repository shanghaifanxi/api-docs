机器人
======================

说明
-----------------------------------------------------------------------------------------------------------------------
- 机器人管理


1、机器人列表
-----------------------------------------------------------------------------------------------------------------------


**请求方式：**   GET

**请求地址：**   /api/robot/robot


**Content-Type：**
::

    application/x-www-form-urlencoded —— 表示通过表单方式提交


**查询参数：**

+------------------------+------------+------------+------------------------------------------------+
|**参数**                |**数据类型**|**是否必须**|**说明**                                        |
+------------------------+------------+------------+------------------------------------------------+
| id                     | string     | 否         | pk(无需输入)                                   |
+------------------------+------------+------------+------------------------------------------------+
| name                   | string     | 否         | 应用名称，String                               |
+------------------------+------------+------------+------------------------------------------------+
| state                  | string     | 否         | 状态：online-在线；offline-离线；busy-忙碌     |
+------------------------+------------+------------+------------------------------------------------+
| resource               | string     | 否         | 资源组ID，String                               |
+------------------------+------------+------------+------------------------------------------------+
| activate_state         | String     | 否         | 激活状态，String                               |
+------------------------+------------+------------+------------------------------------------------+
| atime_from             | long       | 否         | 激活时间(from)，long                           |
+------------------------+------------+------------+------------------------------------------------+
| atime_to               | long       | 否         | 激活时间(to)，long                             |
+------------------------+------------+------------+------------------------------------------------+
| last_time_from         | long       | 否         | 最后通讯时间(from)，long                       |
+------------------------+------------+------------+------------------------------------------------+
| last_time_to           | long       | 否         | 最后通讯时间(to)，long                         |
+------------------------+------------+------------+------------------------------------------------+



**输入参数：**

+------------------------+------------+------------+------------------------------------------------------------------------+
|**参数**                |**数据类型**|**是否必须**|**说明**                                                                |
+------------------------+------------+------------+------------------------------------------------------------------------+
| id                     | string     | 否         | pk(无需输入)                                                           |
+------------------------+------------+------------+------------------------------------------------------------------------+
| name                   | string     | 否         | 应用名称，String                                                       |
+------------------------+------------+------------+------------------------------------------------------------------------+
| state                  | string     | 否         | 状态：unactivated-未激活；free-空闲；busy-忙碌；unreachable-无响应     |
+------------------------+------------+------------+------------------------------------------------------------------------+
| resource               | string     | 否         | 资源组ID，String                                                       |
+------------------------+------------+------------+------------------------------------------------------------------------+
| atime                  | int        | 否         | 激活时间                                                               |
+------------------------+------------+------------+------------------------------------------------------------------------+
| remark                 | string     | 否         | 备注，Text                                                             |
+------------------------+------------+------------+------------------------------------------------------------------------+
| last_time              | int        | 否         | 最后通讯时间，int                                                      |
+------------------------+------------+------------+------------------------------------------------------------------------+
| ctime                  | int        | 否         | 创建时间，int                                                          |
+------------------------+------------+------------+------------------------------------------------------------------------+
| version                | String     | 否         | 版本，String                                                           |
+------------------------+------------+------------+------------------------------------------------------------------------+
| ip                     | String     | 否         | IP，String                                                             |
+------------------------+------------+------------+------------------------------------------------------------------------+
| credential             | String     | 否         | 凭证ID，String                                                         |
+------------------------+------------+------------+------------------------------------------------------------------------+
| computer_name          | String     | 否         | 计算机名称，string                                                     |
+------------------------+------------+------------+------------------------------------------------------------------------+


**输出参数：**


+------------------------+------------+------------+------------------------------------------------------------------------+
|**参数**                |**数据类型**|**是否必须**|**说明**                                                                |
+------------------------+------------+------------+------------------------------------------------------------------------+
| id                     | string     | 否         | pk(无需输入)                                                           |
+------------------------+------------+------------+------------------------------------------------------------------------+
| name                   | string     | 否         | 应用名称，String                                                       |
+------------------------+------------+------------+------------------------------------------------------------------------+
| state                  | string     | 否         | 状态：unactivated-未激活；free-空闲；busy-忙碌；unreachable-无响应     |
+------------------------+------------+------------+------------------------------------------------------------------------+
| resource               | string     | 否         | 资源组ID，String                                                       |
+------------------------+------------+------------+------------------------------------------------------------------------+
| atime                  | int        | 否         | 激活时间                                                               |
+------------------------+------------+------------+------------------------------------------------------------------------+
| remark                 | string     | 否         | 备注，Text                                                             |
+------------------------+------------+------------+------------------------------------------------------------------------+
| last_time              | int        | 否         | 最后通讯时间，int                                                      |
+------------------------+------------+------------+------------------------------------------------------------------------+
| ctime                  | int        | 否         | 创建时间，int                                                          |
+------------------------+------------+------------+------------------------------------------------------------------------+
| version                | String     | 否         | 版本，String                                                           |
+------------------------+------------+------------+------------------------------------------------------------------------+
| ip                     | String     | 否         | IP，String                                                             |
+------------------------+------------+------------+------------------------------------------------------------------------+
| credential             | String     | 否         | 凭证ID，String                                                         |
+------------------------+------------+------------+------------------------------------------------------------------------+
| computer_name          | String     | 否         | 计算机名称，string                                                     |
+------------------------+------------+------------+------------------------------------------------------------------------+

**机器人列表请求示例：**

- Content-Type: 'application/json'

::

    {
        "id":"",
        "name":"",
        "state":"",
        "resource":"",
        "remark":"",
        "atime":"",
        "last_time":"",
        "ctime":"",
        "version":"",
        "ip":"",
        "credential":"",
        "computer_name":"",
    }

- Content-Type: 'application/x-www-form-urlencoded'

::

    curl http://ip:port/api/robot/robot?id=&name=&state=&resource=&remark=&atime=&last_time=&ctime=&version=&ip=&credential=&computer_name=


**机器人列表返回数据示例：**

-  Content-Type: 'application/json'

::

    {
        "count": 14,
        "next": null,
        "previous": null,
        "results": [
            {
                "id": "d206cb06-1db2-11eb-bab5-0001228265cb",
                "resource": 1,
                "name": "robotx",
                "version": "1.0",
                "activate_state": "unactivated",
                "state": "offline",
                "ip": "192.168.10.28",
                "credential": 45,
                "last_time": 1606288894,
                "ctime": 1604393942,
                "atime": 1606288837,
                "remark": null,
                "state_name": "离线",
                "activate_state_name": "未激活",
                "credential_name": "jackson_windows",
                "connection_id": null,
                "template_ids": [
                    145,
                    148
                ],
                "template_list": [
                    {
                        "id": 145,
                        "name": "查询机票",
                        "project": 87
                    },
                    {
                        "id": 148,
                        "name": "点击测试",
                        "project": 89
                    }
                ],
                "computer_name": ""
            },
            {
                "id": "ce8699dc-2271-11eb-9d93-0000442dcdf9",
                "resource": 1,
                "name": "大主机",
                "version": "1.0",
                "activate_state": "activated",
                "state": "offline",
                "ip": "192.168.10.97",
                "credential": 27,
                "last_time": 1605268199,
                "ctime": 1604915775,
                "atime": 1604915801,
                "remark": null,
                "state_name": "离线",
                "activate_state_name": "已激活",
                "credential_name": "windows机器",
                "connection_id": 23,
                "template_ids": [
                    148
                ],
                "template_list": [
                    {
                        "id": 148,
                        "name": "点击测试",
                        "project": 89
                    }
                ],
                "computer_name": ""
            },
            {
                "id": "c439f0c8-2582-11eb-9ddd-0001eb7e19ed",
                "resource": 1,
                "name": "飞力达RPA",
                "version": "1.0",
                "activate_state": "activated",
                "state": "offline",
                "ip": "192.168.10.227",
                "credential": 27,
                "last_time": 1606293889,
                "ctime": 1605252913,
                "atime": 1605252922,
                "remark": null,
                "state_name": "离线",
                "activate_state_name": "已激活",
                "credential_name": "windows机器",
                "connection_id": 25,
                "template_ids": [
                    155,
                    160,
                    162,
                    163,
                    165,
                    179,
                    186
                ],
                "template_list": [
                    {
                        "id": 155,
                        "name": "宁波港",
                        "project": 83
                    },
                    {
                        "id": 160,
                        "name": "太仓港1",
                        "project": 83
                    },
                    {
                        "id": 162,
                        "name": "太仓港2",
                        "project": 83
                    },
                    {
                        "id": 163,
                        "name": "上海港",
                        "project": 83
                    },
                    {
                        "id": 165,
                        "name": "太仓港3",
                        "project": 83
                    },
                    {
                        "id": 179,
                        "name": "飞力达excel操作",
                        "project": 83
                    },
                    {
                        "id": 186,
                        "name": "51job简历上传",
                        "project": 94
                    }
                ],
                "computer_name": ""
            },
            {
                "id": "b4d5cbb8-0d24-11eb-81e6-0000b0adc4d1",
                "resource": 1,
                "name": "JAVIS",
                "version": "1.0",
                "activate_state": "activated",
                "state": "offline",
                "ip": "172.16.200.164",
                "credential": 33,
                "last_time": 1602583224,
                "ctime": 1602573686,
                "atime": 1602574462,
                "remark": null,
                "state_name": "离线",
                "activate_state_name": "已激活",
                "credential_name": "Jackson 机器登录凭据",
                "connection_id": null,
                "template_ids": [],
                "template_list": [],
                "computer_name": ""
            },
            {
                "id": "b413da38-2e2f-11eb-af83-000027b6bfd1",
                "resource": 1,
                "name": "tinkpad",
                "version": "1.0",
                "activate_state": "activated",
                "state": "online",
                "ip": "192.168.10.132",
                "credential": 50,
                "last_time": 1606906669,
                "ctime": 1606206798,
                "atime": 1606206857,
                "remark": null,
                "state_name": "在线",
                "activate_state_name": "已激活",
                "credential_name": "tinkpad登录",
                "connection_id": 26,
                "template_ids": [
                    163,
                    188
                ],
                "template_list": [
                    {
                        "id": 163,
                        "name": "上海港",
                        "project": 83
                    },
                    {
                        "id": 188,
                        "name": "舒尔rpa整合流程",
                        "project": 96
                    }
                ],
                "computer_name": ""
            },
            {
                "id": "a7f154a8-2eee-11eb-bba1-0001f11db06e",
                "resource": 1,
                "name": "win7",
                "version": "1.0",
                "activate_state": "activated",
                "state": "offline",
                "ip": "192.168.10.28",
                "credential": 50,
                "last_time": 1606289224,
                "ctime": 1606288811,
                "atime": 1606288903,
                "remark": null,
                "state_name": "离线",
                "activate_state_name": "已激活",
                "credential_name": "tinkpad登录",
                "connection_id": 28,
                "template_ids": [
                    188
                ],
                "template_list": [
                    {
                        "id": 188,
                        "name": "舒尔rpa整合流程",
                        "project": 96
                    }
                ],
                "computer_name": ""
            },
            {
                "id": "a0194f86-2319-11eb-8bce-00010daea7a4",
                "resource": 1,
                "name": "泛汐机器人",
                "version": "1.0",
                "activate_state": "activated",
                "state": "offline",
                "ip": "172.16.0.181",
                "credential": 27,
                "last_time": 1605233217,
                "ctime": 1604987853,
                "atime": 1604987868,
                "remark": null,
                "state_name": "离线",
                "activate_state_name": "已激活",
                "credential_name": "windows机器",
                "connection_id": null,
                "template_ids": [
                    148
                ],
                "template_list": [
                    {
                        "id": 148,
                        "name": "点击测试",
                        "project": 89
                    }
                ],
                "computer_name": ""
            },
            {
                "id": "8e62dde6-2d3c-11eb-be1d-0001ea721897",
                "resource": 1,
                "name": "test1",
                "version": "",
                "activate_state": "unactivated",
                "state": "",
                "ip": "",
                "credential": 42,
                "last_time": null,
                "ctime": 1606102367,
                "atime": null,
                "remark": null,
                "state_name": "",
                "activate_state_name": "未激活",
                "credential_name": "测试凭据",
                "connection_id": null,
                "template_ids": [
                    164
                ],
                "template_list": [
                    {
                        "id": 164,
                        "name": "ceshiliucheng",
                        "project": 89
                    }
                ],
                "computer_name": ""
            },
            {
                "id": "88a7af70-1cd1-11eb-abf4-0001bd1fe9d6",
                "resource": 1,
                "name": "jackson",
                "version": "1.0",
                "activate_state": "activated",
                "state": "offline",
                "ip": "192.168.10.143",
                "credential": 45,
                "last_time": 1605859354,
                "ctime": 1604297183,
                "atime": 1604297219,
                "remark": null,
                "state_name": "离线",
                "activate_state_name": "已激活",
                "credential_name": "jackson_windows",
                "connection_id": 15,
                "template_ids": [
                    144
                ],
                "template_list": [
                    {
                        "id": 144,
                        "name": "网银转账",
                        "project": 86
                    }
                ],
                "computer_name": ""
            },
            {
                "id": "766d357a-1fd1-11eb-80ea-0001e1938a54",
                "resource": 1,
                "name": "David_测试",
                "version": "1.1",
                "activate_state": "activated",
                "state": "offline",
                "ip": "192.168.10.130",
                "credential": 42,
                "last_time": 1606362116,
                "ctime": 1604627006,
                "atime": 1606806717,
                "remark": null,
                "state_name": "离线",
                "activate_state_name": "已激活",
                "credential_name": "测试凭据",
                "connection_id": 30,
                "template_ids": [
                    139,
                    187
                ],
                "template_list": [
                    {
                        "id": 139,
                        "name": "测试网站点击",
                        "project": 82
                    },
                    {
                        "id": 187,
                        "name": "david测试jipr_text",
                        "project": 95
                    }
                ],
                "computer_name": ""
            },
            {
                "id": "6a8962de-2556-11eb-94a5-000048fdab24",
                "resource": 1,
                "name": "泛汐机器人RPA",
                "version": "1.0",
                "activate_state": "activated",
                "state": "online",
                "ip": "172.16.0.181",
                "credential": 27,
                "last_time": 1606906670,
                "ctime": 1605233864,
                "atime": 1605233912,
                "remark": null,
                "state_name": "在线",
                "activate_state_name": "已激活",
                "credential_name": "windows机器",
                "connection_id": null,
                "template_ids": [
                    155,
                    160,
                    162,
                    163,
                    165,
                    179
                ],
                "template_list": [
                    {
                        "id": 155,
                        "name": "宁波港",
                        "project": 83
                    },
                    {
                        "id": 160,
                        "name": "太仓港1",
                        "project": 83
                    },
                    {
                        "id": 162,
                        "name": "太仓港2",
                        "project": 83
                    },
                    {
                        "id": 163,
                        "name": "上海港",
                        "project": 83
                    },
                    {
                        "id": 165,
                        "name": "太仓港3",
                        "project": 83
                    },
                    {
                        "id": 179,
                        "name": "飞力达excel操作",
                        "project": 83
                    }
                ],
                "computer_name": ""
            },
            {
                "id": "60ad6ea8-1fe1-11eb-b50d-00010a56bc23",
                "resource": 1,
                "name": "robot-test",
                "version": "1.0",
                "activate_state": "activated",
                "state": "offline",
                "ip": "192.168.10.17",
                "credential": 27,
                "last_time": 1604644949,
                "ctime": 1604633841,
                "atime": 1604644893,
                "remark": null,
                "state_name": "离线",
                "activate_state_name": "已激活",
                "credential_name": "windows机器",
                "connection_id": 19,
                "template_ids": [
                    150
                ],
                "template_list": [
                    {
                        "id": 150,
                        "name": "测试无分支流程-复制",
                        "project": null
                    }
                ],
                "computer_name": ""
            },
            {
                "id": "4da91052-2f99-11eb-9faf-0001f3cf97e9",
                "resource": 1,
                "name": "飞力达POC机器人",
                "version": "1.0",
                "activate_state": "activated",
                "state": "offline",
                "ip": "192.168.253.1",
                "credential": 50,
                "last_time": 1606437906,
                "ctime": 1606362104,
                "atime": 1606362164,
                "remark": null,
                "state_name": "离线",
                "activate_state_name": "已激活",
                "credential_name": "tinkpad登录",
                "connection_id": 29,
                "template_ids": [
                    163
                ],
                "template_list": [
                    {
                        "id": 163,
                        "name": "上海港",
                        "project": 83
                    }
                ],
                "computer_name": ""
            },
            {
                "id": "2d4e28d2-fe37-11ea-ac0f-000151a558a6",
                "resource": 1,
                "name": "181",
                "version": "1.0",
                "activate_state": "activated",
                "state": "offline",
                "ip": "172.16.0.181",
                "credential": 27,
                "last_time": 1605233775,
                "ctime": 1600932352,
                "atime": 1600992163,
                "remark": null,
                "state_name": "离线",
                "activate_state_name": "已激活",
                "credential_name": "windows机器",
                "connection_id": 11,
                "template_ids": [
                    132
                ],
                "template_list": [
                    {
                        "id": 132,
                        "name": "测试",
                        "project": 56
                    }
                ],
                "computer_name": ""
            }
        ]
    }



**机器人列表错误返回示例：**
::

    {
        "detail":"资源组获取失败"
    }
