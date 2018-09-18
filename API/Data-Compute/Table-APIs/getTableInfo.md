# getTableInfo


## 描述
查询用户实例的指定数据表信息

## 请求方式
GET

## 请求地址
https://xdata.jdcloud-api.com/v1/regions/{regionId}/dwTable/{tableName}

|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**regionId**|String|True||地域ID|
|**tableName**|String|True||数据表名|

## 请求参数
|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**databaseName**|String|True||数据库名称|
|**instanceName**|String|True||实例名称|


## 返回参数
|名称|类型|描述|
|---|---|---|
|**requestId**|String||
|**result**|Result||


### <a name="Result">Result</a>
|名称|类型|描述|
|---|---|---|
|**data**|DwTable||
|**message**|String||
|**status**|Boolean||
### <a name="DwTable">DwTable</a>
|名称|类型|描述|
|---|---|---|
|**category**|String|类别|
|**comments**|String|描述信息|
|**createTime**|String|创建时间|
|**dbName**|String|数据库名|
|**encryption**|String|是否加密|
|**hiveFileFormat**|String|文件存储类型|
|**hiveObjectPrivileges**|DwHiveObjectPrivileges|hive表权限信息|
|**id**|Integer|数据库id|
|**lastUpdateTime**|String|最新更新时间|
|**location**|String|位置|
|**owner**|String|所有者|
|**parameters**|Object|参数|
|**physicalStorageCapacity**|String|物理存储量|
|**source**|String|来源|
|**tableName**|String|表名|
|**userName**|String|用户名|
### <a name="DwHiveObjectPrivileges">DwHiveObjectPrivileges</a>
|名称|类型|描述|
|---|---|---|
|**alter**|Boolean|alter权限|
|**create**|Boolean|create权限|
|**delete**|Boolean|delete权限|
|**drop**|Boolean|drop权限|
|**insert**|Boolean|insert权限|
|**message**|String|返回信息|
|**owner**|Boolean|是否为此表所有者|
|**select**|Boolean|select权限|
|**status**|Boolean|状态|
|**update**|Boolean|update权限|

## 返回码
|返回码|描述|
|---|---|
|**200**|OK|
|**500**|Internal server error|
