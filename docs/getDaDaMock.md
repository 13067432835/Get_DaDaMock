    
**简要描述：** 

- 模拟达达订单状态变更接口

**请求URL：** 
- ` http://172.18.50.59:8090/api/getDaDaMock `
  
**请求方式：**
- POST 

**参数：** 

|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|env |否  |string |环境（不传则默认qa环境）   |
|type |是  |string |模拟类型   |
|paramterInput |是  |string | 订单编号   |


    
-  type类型

|类型|含义|
|:----    |:-------    |
|1	  |模拟接单     |
|2 |订单过期 |
|3 |取消接单 |
|4     |模拟取货 |
|5 |订单派送完成     |
|6 |模拟拒收     |

**请求参数示例**

|参数名|数据|
|:----    |:-------    |
|env	  |qa     |
|type |1 |
|paramterInput |123456 |






 **返回成功示例**

``` 
{
    "code": 1,
    "msg": null,
    "请求类型": "模拟拒收",
    "data": {
        "monitorTrackId": "fff0582e-9be1-4c1d-a177-9d6fa3c139c7",
        "processResult": true,
        "responseVo": "{\"status\":\"true\",\"errorCode\":2005,\"code\":2005,\"msg\":\"成功\"}",
        "returnCode": "000000",
        "returnMsg": "处理成功",
        "successForMornitor": true,
        "timestamp": "1563440532695"
    }
}
```

 **返回错误示例**

``` 
{
    "code": 1,
    "msg": "发生未知错误,请联系微盟测试龙伟强,错误日志为:HTTPConnectionPool(host='1.1.1.116', port=8080): Max retries exceeded with url: /service (Caused by NewConnectionError('<urllib3.connection.HTTPConnection object at 0x000002784767B0B8>: Failed to establish a new connection: [WinError 10060] 由于连接方在一段时间后没有正确答复或连接的主机没有反应，连接尝试失败。'))",
    "请求类型": null,
    "data": null
}
```



