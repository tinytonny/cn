# createRouteTable


## 描述
创建路由表

## 请求方式
POST

## 请求地址
https://vpc.jdcloud-api.com/v1/regions/{regionId}/routeTables/

|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**regionId**|String|True||Region ID|

## 请求参数
|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**description**|String|False||描述,​ 允许输入UTF-8编码下的全部字符，不超过256字符|
|**routeTableName**|String|True||路由表名称，只允许输入中文、数字、大小写字母、英文下划线“_”及中划线“-”，不允许为空且不超过32字符。|
|**vpcId**|String|True||路由表所属的私有网络ID|


## 返回参数
|名称|类型|描述|
|---|---|---|
|**requestId**|String|请求ID|
|**result**|Result|返回结果|


### <a name="Result">Result</a>
|名称|类型|描述|
|---|---|---|
|**routeTableId**|String|路由表ID|

## 返回码
|返回码|描述|
|---|---|
|**200**|OK|
|**400**|invalid parameter|
|**404**|Resource not found|
|**500**|Internal server error|
