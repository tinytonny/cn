# downloadDDosAttackLogs


## 描述
下载 DDos 攻击日志

## 请求方式
GET

## 请求地址
https://ipanti.jdcloud-api.com/v1/regions/{regionId}/attacklog:ddos/download

|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**regionId**|String|True||Region ID|

## 请求参数
|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**endTime**|String|True||查询的结束时间, UTC 时间, 格式：yyyy-MM-dd'T'HH:mm:ssZ|
|**instanceId**|String[]|False||高防实例 ID|
|**startTime**|String|True||开始时间, 只能下载最近 60 天以内的数据, UTC 时间, 格式：yyyy-MM-dd'T'HH:mm:ssZ|


## 返回参数
|名称|类型|描述|
|---|---|---|



## 返回码
|返回码|描述|
|---|---|
|**200**|OK|
