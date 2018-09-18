# getJobTypeList


## 描述
获取指定集群下的作业类型列表

## 请求方式
POST

## 请求地址
https://idata-jmr-api.jcloud.com/v1/regions/{regionId}/jobType:list

|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**regionId**|String|True||地域ID|

## 请求参数
|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**clusterId**|String|True||集群Id|


## 返回参数
|名称|类型|描述|
|---|---|---|
|**requestId**|String||
|**result**|Result||


### <a name="Result">Result</a>
|名称|类型|描述|
|---|---|---|
|**data**|String[]|返回的作业类型列表|
|**message**|String||
|**status**|String||

## 返回码
|返回码|描述|
|---|---|
|**200**|OK|
|**500**|Internal server error|
