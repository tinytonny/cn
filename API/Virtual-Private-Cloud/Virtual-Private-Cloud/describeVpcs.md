# describeVpcs


## 描述
查询私有网络列表

## 请求方式
GET

## 请求地址
https://vpc.jdcloud-api.com/v1/regions/{regionId}/vpcs/

|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**regionId**|String|True||Region ID|

## 请求参数
|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**filters**|Filter[]|False||vpcIds - vpc ID列表，支持多个<br>vpcNames - vpc名称列表,支持多个<br>|
|**pageNumber**|Integer|False|1|页码, 默认为1, 取值范围：[1,∞), 页码超过总页数时, 显示最后一页|
|**pageSize**|Integer|False|20|分页大小，默认为20，取值范围：[10,100]|

### <a name="Filter">Filter</a>
|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**name**|String|True||过滤条件的名称|
|**operator**|String|False||过滤条件的操作符，默认eq|
|**values**|String[]|True||过滤条件的值|

## 返回参数
|名称|类型|描述|
|---|---|---|
|**requestId**|String|请求ID|
|**result**|Result|返回结果|


### <a name="Result">Result</a>
|名称|类型|描述|
|---|---|---|
|**totalCount**|Number|总数量|
|**vpcs**|Vpc[]|Vpc资源信息列表|
### <a name="Vpc">Vpc</a>
|名称|类型|描述|
|---|---|---|
|**aclIds**|String[]||
|**addressPrefix**|String|如果为空，则不限制网段，如果不为空，10.0.0.0/8、172.16.0.0/12和192.168.0.0/16及它们包含的子网，且子网掩码长度为16-28之间|
|**createdTime**|String|vpc创建时间|
|**description**|String|VPC 描述，取值范围：1~120个字符|
|**routeTableIds**|String[]||
|**subnets**|Subnet[]|私有网络包含的子网列表|
|**vpcId**|String|Vpc的Id|
|**vpcName**|String|私有网络名称，取值范围：1-60个中文、英文大小写的字母、数字和下划线分隔符|
### <a name="Subnet">Subnet</a>
|名称|类型|描述|
|---|---|---|
|**aclId**|String|子网关联的acl Id|
|**addressPrefix**|String|子网网段，vpc内子网网段不能重叠，cidr的取值范围：10.0.0.0/8、172.16.0.0/12和192.168.0.0/16及它们包含的子网，且子网掩码长度为16-28之间，如果VPC含有Cidr，则必须为VPC所在Cidr的子网|
|**availableIpCount**|Number|子网可用ip数量|
|**createdTime**|String|子网创建时间|
|**description**|String|子网描述信息|
|**endIp**|String|子网的结束地址，子网第1个地位为路由器网关保留，第2个地址为dhcp服务保留|
|**routeTableId**|String|子网关联的路由表Id|
|**startIp**|String|子网的起始地址，子网第1个地位为路由器网关保留，第2个地址为dhcp服务保留|
|**subnetId**|String|Subnet的Id|
|**subnetName**|String|子网名称|
|**vpcId**|String|子网所属VPC的Id|

## 返回码
|返回码|描述|
|---|---|
|**200**|OK|
