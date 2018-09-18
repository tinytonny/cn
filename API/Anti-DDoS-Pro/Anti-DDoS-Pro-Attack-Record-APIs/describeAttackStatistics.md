# describeAttackStatistics


## 描述
查询攻击次数及流量峰值

## 请求方式
GET

## 请求地址
https://ipanti.jdcloud-api.com/v1/regions/{regionId}/attacklog/describeAttackStatistics

|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**regionId**|String|True||Region ID|

## 请求参数
|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**endTime**|String|True||查询的结束时间, UTC 时间, 格式：yyyy-MM-dd'T'HH:mm:ssZ|
|**instanceId**|String[]|False||高防实例 ID|
|**startTime**|String|True||开始时间, 只能查询最近 60 天以内的数据, UTC 时间, 格式：yyyy-MM-dd'T'HH:mm:ssZ|
|**type**|Integer|True||攻击类型, 0 为 DDos, 1 为 CC|


## 返回参数
|名称|类型|描述|
|---|---|---|
|**requestId**|String||
|**result**|Result||


### <a name="Result">Result</a>
|名称|类型|描述|
|---|---|---|
|**count**|Integer|攻击次数|
|**flow**|Number|攻击流量峰值|
|**unit**|String|流量单位, bps、Kbps、Mbps、Gbps|

## 返回码
|返回码|描述|
|---|---|
|**200**|OK|
