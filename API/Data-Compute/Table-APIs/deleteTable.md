# deleteTable


## 描述
删除用户实例的指定数据表

## 请求方式
DELETE

## 请求地址
https://xdata.jdcloud-api.com/v1/regions/{regionId}/dwTable/{tableName}

|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**regionId**|String|True||地域ID|
|**tableName**|String|True||数据表名|

## 请求参数
|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**databaseName**|String|True||数据库名称|
|**instanceName**|String|True||实例名称|


## 返回参数
|名称|类型|描述|
|---|---|---|
|**requestId**|String||
|**result**|Result||


### <a name="Result">Result</a>
|名称|类型|描述|
|---|---|---|
|**data**|Object||
|**message**|String||
|**status**|Boolean||

## 返回码
|返回码|描述|
|---|---|
|**200**|OK|
|**500**|Internal server error|
