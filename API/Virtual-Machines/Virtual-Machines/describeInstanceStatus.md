# describeInstanceStatus


## 描述
批量查询云主机状态

## 请求方式
GET

## 请求地址
https://vm.jdcloud-api.com/v1/regions/{regionId}/instanceStatus

|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**regionId**|String|True||地域ID|

## 请求参数
|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**filters**|Filter[]|False||instanceId - 云主机ID，精确匹配，支持多个<br>privateIpAddress - 主网卡内网主IP地址，模糊匹配，支持多个<br>vpcId - 私有网络ID，精确匹配，支持多个<br>status - 云主机状态，精确匹配，支持多个，<a href="https://www.jdcloud.com/help/detail/3869/isCatalog/1">参考云主机状态</a><br>name - 云主机名称，模糊匹配，支持单个<br>imageId - 镜像ID，精确匹配，支持多个<br>networkInterfaceId - 弹性网卡ID，精确匹配，支持多个<br>subnetId - 子网ID，精确匹配，支持多个<br>|
|**pageNumber**|Integer|False|1|页码；默认为1|
|**pageSize**|Integer|False|20|分页大小；默认为20；取值范围[10, 100]|

### <a name="Filter">Filter</a>
|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**name**|String|True||过滤条件的名称|
|**operator**|String|False||过滤条件的操作符，默认eq|
|**values**|String[]|True||过滤条件的值|

## 返回参数
|名称|类型|描述|
|---|---|---|
|**requestId**|String||
|**result**|Result||


### <a name="Result">Result</a>
|名称|类型|描述|
|---|---|---|
|**instanceStatuses**|InstanceStatus[]||
|**totalCount**|Number||
### <a name="InstanceStatus">InstanceStatus</a>
|名称|类型|描述|
|---|---|---|
|**instanceId**|String|云主机ID|
|**status**|String|<a href="https://www.jdcloud.com/help/detail/3869/isCatalog/1">参考云主机状态</a>|

## 返回码
|返回码|描述|
|---|---|
|**400**|Invalid parameter|
|**401**|Authentication failed|
|**404**|Not found|
|**503**|Service unavailable|
|**200**|OK|
|**500**|Internal server error|
