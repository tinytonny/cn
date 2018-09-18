# describeWhiteList


## 描述
查看RDS实例当前白名单。白名单是允许访问当前实例的IP/IP段列表，缺省情况下，白名单对本VPC开放。如果用户开启了外网访问的功能，还需要对外网的IP配置白名单。

## 请求方式
GET

## 请求地址
https://rds.jdcloud-api.com/v1/regions/{regionId}/instances/{instanceId}/whiteList

|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**instanceId**|String|True||RDS 实例ID，唯一标识一个RDS实例|
|**regionId**|String|True||地域代码，取值范围参见[《各地域及可用区对照表》](../Enum-Definitions/Regions-AZ.md)|

## 请求参数
无


## 返回参数
|名称|类型|描述|
|---|---|---|
|**result**|Result||


### <a name="Result">Result</a>
|名称|类型|描述|
|---|---|---|
|**whiteLists**|WhiteList[]|白名单列表|
### <a name="WhiteList">WhiteList</a>
|名称|类型|描述|
|---|---|---|
|**ips**|String|IP或IP段，不同的IP/IP段之间用英文逗号分隔，例如0.0.0.0/0,192.168.0.10|
|**name**|String|白名单名称|

## 返回码
|返回码|描述|
|---|---|
|**200**|OK|
