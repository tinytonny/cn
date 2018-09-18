# startInstance


## 描述
启动单个云主机，只能启动<b>stopped</b>状态的云主机，云主机没有正在进行中的任务才可启动。<br>
只能启动正常计费状态的云主机。


## 请求方式
POST

## 请求地址
https://vm.jdcloud-api.com/v1/regions/{regionId}/instances/{instanceId}:startInstance

|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**instanceId**|String|True||云主机ID|
|**regionId**|String|True||地域ID|

## 请求参数
无


## 返回参数
|名称|类型|描述|
|---|---|---|



## 返回码
|返回码|描述|
|---|---|
|**400**|Invalid parameter|
|**401**|Authentication failed|
|**404**|Not found|
|**503**|Service unavailable|
|**200**|OK|
|**500**|Internal server error|
