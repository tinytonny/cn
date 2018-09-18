# getAvaliableNum


## 描述
获取当前用户剩余可创建资源数

## 请求方式
GET

## 请求地址
https://idata-jmr-api.jcloud.com/v1/regions/{regionId}/avaliableNum

|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**regionId**|String|True||地域ID|

## 请求参数
无


## 返回参数
|名称|类型|描述|
|---|---|---|
|**requestId**|String||
|**result**|Result||


### <a name="Result">Result</a>
|名称|类型|描述|
|---|---|---|
|**data**|AvailableNumData|剩余可创建资源数|
|**message**|String||
|**status**|String||
### <a name="AvailableNumData">AvailableNumData</a>
|名称|类型|描述|
|---|---|---|
|**serverNum**|Integer|可用服务数|

## 返回码
|返回码|描述|
|---|---|
|**200**|OK|
|**500**|Internal server error|
