
基础模块
======================

说明
-----------------------------------------------------------------------------------------------------------------------
- 将基础模块的yml格式的文件转成json文件

1、基础表列表 API
-----------------------------------------------------------------------------------------------------------------------

**请求方式：**   GET（查询）

**请求地址：**   /api/process/package/


**Content-Type：**
::

    新增数据的时候需要指定Content-Type，以下对Content-Type进行说明:

    application/x-www-form-urlencoded —— 表示通过表单方式提交
    application/json —— 表示传入数据为json格式字符串


**查询参数：**

+------------------------+------------+------------+------------------------------------------------+
|**参数**                |**数据类型**|**是否必须**|**说明**                                        |
+------------------------+------------+------------+------------------------------------------------+
| name                   | string     | 否         | 函数名                                         |
+------------------------+------------+------------+------------------------------------------------+
| title                  | string     | 否         | 标题                                           |
+------------------------+------------+------------+------------------------------------------------+
| description            | string     | 否         | 描述                                           |
+------------------------+------------+------------+------------------------------------------------+


**GET返回数据例子：**
::
    [
        {
            "title": "程序",
            "decription": null,
            "children":[
                {
                    "name": "code", 
                    "class": null, 
                    "namespace": "fxpa.fxprogramming", 
                    "title": "python代码块", 
                    "nodeType": "function", 
                    "description": "运行python代码块", 
                    "cls": 
                    {
                        "icon": null, 
                        "color": null
                    },
                    "ports": 
                    {
                        "in": [
                            {
                                "name": null, 
                                "portType": "flow", 
                                "title": null, 
                                "dataType": null, 
                                "value": null
                            }, 
                            {
                                "name": "content", 
                                "portType": "input", 
                                "title": "代码块", 
                                "dataType": "string", 
                                "elementType": "textarea", 
                                "value": null
                            }
                        ], 
                        "out": [
                        {
                            "name": null, 
                            "portType": "flow", 
                            "title": null, 
                            "dataType": null, 
                            "value": null
                        }
                        ]
                    }, 
                    "detailPanel": 
                    {
                        "common": [
                            {
                                "name": "before", 
                                "dataType": "number", 
                                "elementType": "input",
                                "value": 0,
                                "title": "前置延时(秒)"
                            }, 
                            {
                                "name": "after", 
                                "dataType": "number", 
                                "elementType": "input",
                                "value": 0, 
                                "title": "后置延时(秒)"
                            },
                            {
                                "name": "continueOnErr",
                                "dataType": "bool", 
                                "elementType": "checkbox", 
                                "choices": [
                                    True, 
                                    False
                                ], 
                                "value": False, 
                                "title": "错误继续执行"
                            }
                        ]
                    }
                },
            ]
        
        },
    ]   
        
    
2、查询 API
----------------------------------------------------------------------------------------------------------

**请求方式：**    GET（查询）

**请求地址：**    /api/process/package/?search="code"
::

    请求地址中code为函数名

**输入/输出参数：**   见章节1中输入和输出参数说明，修改数据时输入参数均为非必须

**返回数据例子：**
::
    [
        {
            "title": "程序",
            "decription": null,
            "children":[
                {
                    "name": "code", 
                    "class": null, 
                    "namespace": "fxpa.fxprogramming", 
                    "title": "python代码块", 
                    "nodeType": "function", 
                    "description": "运行python代码块", 
                    "cls": 
                    {
                        "icon": null, 
                        "color": null
                    },
                    "ports": 
                    {
                        "in": [
                            {
                                "name": null, 
                                "portType": "flow", 
                                "title": null, 
                                "dataType": null, 
                                "value": null
                            }, 
                            {
                                "name": "content", 
                                "portType": "input", 
                                "title": "代码块", 
                                "dataType": "string", 
                                "elementType": "textarea", 
                                "value": null
                            }
                        ], 
                        "out": [
                        {
                            "name": null, 
                            "portType": "flow", 
                            "title": null, 
                            "dataType": null, 
                            "value": null
                        }
                        ]
                    }, 
                    "detailPanel": 
                    {
                        "common": [
                            {
                                "name": "before", 
                                "dataType": "number", 
                                "elementType": "input",
                                "value": 0,
                                "title": "前置延时(秒)"
                            }, 
                            {
                                "name": "after", 
                                "dataType": "number", 
                                "elementType": "input",
                                "value": 0, 
                                "title": "后置延时(秒)"
                            },
                            {
                                "name": "continueOnErr",
                                "dataType": "bool", 
                                "elementType": "checkbox", 
                                "choices": [
                                    True, 
                                    False
                                ], 
                                "value": False, 
                                "title": "错误继续执行"
                            }
                        ]
                    }
                },
            ]
        
        },
    ]   

::

    dataType分类: string, number, date, password, array, bool, object
    elementType分类: input, textarea, checkbox,  select