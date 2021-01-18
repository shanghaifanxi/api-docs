主机清单
======================

说明
-----------------------------------------------------------------------------------------------------------------------
- 获取主机清单


1、主机清单查询
-----------------------------------------------------------------------------------------------------------------------


**请求方式：**   GET

**请求地址：**   /api/control/inventory


**Content-Type：**
::

    application/x-www-form-urlencoded —— 表示通过表单方式提交
    application/json —— 表示传入数据为json格式字符串


**查询参数：**

+------------------------+------------+------------+----------------------------------------+
|**参数**                |**数据类型** |**是否必须** |**说明**                                |
+------------------------+------------+------------+----------------------------------------+
| id                     | string     | 是         | 流程ID                                 |
+------------------------+------------+------------+----------------------------------------+


**返回数据示例：**

-  Content-Type: 'application/json'

::

    {
    "count": 57,
    "next": "http://opsgrat-tst.opsgrat.com/api/project/inventory?limit=20&offset=20",
    "previous": null,
    "results": [
  
        {
            "id": 559,
            "resource": 1,
            "name": "xxxx",
            "description": "",
            "variables": "",
            "cuser": "admin",
            "credential_id": null,
            "status_health": 0,
            "status_running": 0,
            "status_exception": 0,
            "status_disabled": 0,
            "group_counts": 0,
            "host_counts": 0,
            "has_host_source": false,
            "credential": null,
            "source": "internal",
            "source_name": "手工录入"
        },
        {
            "id": 156,
            "resource": 6,
            "name": "测试009",
            "description": "",
            "variables": "",
            "cuser": "xiaofeng",
            "credential_id": null,
            "status_health": 0,
            "status_running": 0,
            "status_exception": 0,
            "status_disabled": 0,
            "group_counts": 3,
            "host_counts": 2,
            "has_host_source": false,
            "credential": null,
            "source": "internal",
            "source_name": "手工录入"
        },
        {
            "id": 142,
            "resource": 1,
            "name": "本机(localhost)",
            "description": "",
            "variables": "",
            "cuser": "admin",
            "credential_id": 34,
            "status_health": 0,
            "status_running": 0,
            "status_exception": 1,
            "status_disabled": 0,
            "group_counts": 0,
            "host_counts": 1,
            "has_host_source": false,
            "credential_name": "101gitlab凭据",
            "credential": 34,
            "source": "internal",
            "source_name": "手工录入"
        },

    ]
}


