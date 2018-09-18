# modifyInstance


## 描述
修改云物理服务器部分信息，包括名称、描述

## 请求方式
POST

## 请求地址
https://cps.jdcloud-api.com/v1/regions/{regionId}/instances/{instanceId}:modifyInstance

|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**instanceId**|String|True||云物理服务器ID|
|**regionId**|String|True||地域ID，可调用接口（describeRegiones）获取云物理服务器支持的地域|

## 请求参数
|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**description**|String|False||云物理服务器描述|
|**name**|String|False||云物理服务器名称|


## 返回参数
|名称|类型|描述|
|---|---|---|
|**requestId**|String||
|**result**|Result||


### <a name="Result">Result</a>
|名称|类型|描述|
|---|---|---|
|**description**|String|云物理服务器描述|
|**name**|String|云物理服务器名称|

## 返回码
|返回码|描述|
|---|---|
|**200**|OK|
|**400**|Bad request|
|**404**|Not found|
|**500**|Internal server error|
|**503**|Service unavailable|
