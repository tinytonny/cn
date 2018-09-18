# describeVpcPeering


## 描述
查询VpcPeering资源详情

## 请求方式
GET

## 请求地址
https://vpc.jdcloud-api.com/v1/regions/{regionId}/vpcPeerings/{vpcPeeringId}

|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**regionId**|String|True||Region ID|
|**vpcPeeringId**|String|True||vpcPeeringId ID|

## 请求参数
无


## 返回参数
|名称|类型|描述|
|---|---|---|
|**requestId**|String|请求ID|
|**result**|Result|返回结果|


### <a name="Result">Result</a>
|名称|类型|描述|
|---|---|---|
|**vpcPeering**|VpcPeering|VpcPeering资源信息|
### <a name="VpcPeering">VpcPeering</a>
|名称|类型|描述|
|---|---|---|
|**createdTime**|String|VpcPeering创建时间|
|**description**|String|VpcPeering 描述，可为空值，取值范围：0-256个中文、英文大小写的字母、数字和下划线分隔符|
|**remoteVpcInfo**|VpcPeeringVpcInfo|对端的Vpc信息|
|**vpcInfo**|VpcPeeringVpcInfo|发起VpcPeering的Vpc信息|
|**vpcPeeringId**|String|VpcPeering的Id|
|**vpcPeeringName**|String|VpcPeering名称，同账号下不允许重名，取值范围：1-32个中文、英文大小写的字母、数字和下划线分隔符|
|**vpcPeeringState**|String|状态，取值为Connected，Disconnected，Initiated|
### <a name="VpcPeeringVpcInfo">VpcPeeringVpcInfo</a>
|名称|类型|描述|
|---|---|---|
|**addressPrefix**|String[]|如果为空，则不限制网段，如果不为空，10.0.0.0/8、172.16.0.0/12和192.168.0.0/16及它们包含的子网，且子网掩码长度为16-28之间|
|**vpcId**|String|子网所属VPC的Id|
|**vpcName**|String|私有网络名称，取值范围：1-60个中文、英文大小写的字母、数字和下划线分隔符|

## 返回码
|返回码|描述|
|---|---|
|**200**|OK|
