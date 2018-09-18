# isValidJobName


## 描述
校验作业名称是否有效

## 请求方式
POST

## 请求地址
https://idata-jmr-api.jcloud.com/v1/regions/{regionId}/jobName:Validate

|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**regionId**|String|True||地域ID|

## 请求参数
|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**jobId**|String|True||作为作业名校验依据|
|**jobName**|String|True||待校验的作业名|


## 返回参数
|名称|类型|描述|
|---|---|---|
|**requestId**|String||
|**result**|Result||


### <a name="Result">Result</a>
|名称|类型|描述|
|---|---|---|
|**message**|String||
|**status**|String||

## 返回码
|返回码|描述|
|---|---|
|**200**|OK|
|**500**|Internal server error|
