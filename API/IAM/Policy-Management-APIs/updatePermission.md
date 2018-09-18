# updatePermission


## 描述
修改策略

## 请求方式
PUT

## 请求地址
https://iam.jdcloud-api.com/v1/regions/{regionId}/permission/{permissionId}

|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**permissionId**|Integer|True||权限id|
|**regionId**|String|True||Region ID|

## 请求参数
|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**updatePermissionInfo**|UpdatePermissionInfo|True||权限信息|

### <a name="UpdatePermissionInfo">UpdatePermissionInfo</a>
|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**content**|PermissionDetail[]|True||权限详细信息|
|**description**|String|False||描述，0~256个字符|
|**name**|String|True||权限名称，1~32位数字、字符、中文、中划线、下划线|
### <a name="PermissionDetail">PermissionDetail</a>
|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**permission**|String|True||权限类型，只读-R、删除-D、修改-M|
|**resource**|Resource[]|True||资源信息|
### <a name="Resource">Resource</a>
|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**ids**|String[]|True||资源id集合，传*表示对所有id生效|
|**type**|String|True||资源类型，云主机-server、镜像-image、云硬盘-volume、vpc-vpc、公网Ip-floatingIp、负载均衡-loadbalance、云数据库(mysql)-database、云缓存-cache|

## 返回参数
|名称|类型|描述|
|---|---|---|
|**requestId**|String||



## 返回码
|返回码|描述|
|---|---|
|**200**|OK|
