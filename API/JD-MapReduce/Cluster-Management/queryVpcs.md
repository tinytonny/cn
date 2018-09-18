# queryVpcs


## 描述
获取vpc集合

## 请求方式
POST

## 请求地址
https://idata-jmr-api.jcloud.com/v1/regions/{regionId}/vpcs:query

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
|**data**|QueryVpcs[]|VPC集合|
|**message**|String||
|**status**|String||
### <a name="QueryVpcs">QueryVpcs</a>
|名称|类型|描述|
|---|---|---|
|**vpcId**|String|VPC id|
|**vpcName**|String|VPC 名称|

## 返回码
|返回码|描述|
|---|---|
|**200**|OK|
|**500**|Internal server error|
