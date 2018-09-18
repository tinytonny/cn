# getClusterJobCount


## 描述
获取集群的作业数

## 请求方式
POST

## 请求地址
https://idata-jmr-api.jcloud.com/v1/regions/{regionId}/clusterJob/{clusterId}:count

|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**clusterId**|String|True||集群ID|
|**regionId**|String|True||地域ID|

## 请求参数
|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|


## 返回参数
|名称|类型|描述|
|---|---|---|
|**requestId**|String||
|**result**|Result||


### <a name="Result">Result</a>
|名称|类型|描述|
|---|---|---|
|**data**|Integer|集群作业数量|
|**message**|String||
|**status**|String||

## 返回码
|返回码|描述|
|---|---|
|**200**|OK|
|**500**|Internal server error|
