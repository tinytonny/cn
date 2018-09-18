# getPySparkExecuteState


## 描述
获取用户PySpark脚本的执行状态

## 请求方式
GET

## 请求地址
https://xdata.jdcloud-api.com/v1/regions/{regionId}/dwQuery:getPySparkExecuteState

|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**regionId**|String|True||地域ID|

## 请求参数
|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**queryId**|String|True||查询id|
|**userName**|String|True||用户名称|


## 返回参数
|名称|类型|描述|
|---|---|---|
|**requestId**|String||
|**result**|Result||


### <a name="Result">Result</a>
|名称|类型|描述|
|---|---|---|
|**data**|String||
|**message**|String||
|**status**|Boolean||

## 返回码
|返回码|描述|
|---|---|
|**200**|OK|
|**500**|Internal server error|
