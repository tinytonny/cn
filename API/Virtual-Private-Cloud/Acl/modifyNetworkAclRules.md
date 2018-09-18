# modifyNetworkAclRules


## 描述
修改networkAcl接口

## 请求方式
POST

## 请求地址
https://vpc.jdcloud-api.com/v1/regions/{regionId}/networkAcls/{networkAclId}:modifyNetworkAclRules

|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**networkAclId**|String|True||networkAclId ID|
|**regionId**|String|True||Region ID|

## 请求参数
|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**modifyNetworkAclRuleSpecs**|ModifyNetworkAclRuleSpec[]|True||networkAcl规则列表|

### <a name="ModifyNetworkAclRuleSpec">ModifyNetworkAclRuleSpec</a>
|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**addressPrefix**|String|False||匹配地址前缀|
|**description**|String|False||描述,允许输入UTF-8编码下的全部字符，不超过256字符|
|**fromPort**|Integer|False||规则限定起始传输层端口, 取值范围:1-65535, 若protocol为传输层协议，默认值为1，若protocol不是传输层协议，设置无效，恒为0。如果规则只限定一个端口号，fromPort和toPort填写同一个值|
|**priority**|Integer|False||规则匹配优先级，取值范围为[1,32768]，优先级数字越小优先级越高|
|**protocol**|String|False||规则限定协议。取值范围：All,TCP,UDP,ICMP|
|**ruleAction**|String|False||访问控制策略：allow:允许，deny：拒绝|
|**ruleId**|String|True||networkAcl规则ID|
|**toPort**|Integer|False||规则限定终止传输层端口, 取值范围:1-65535, 若protocol为传输层协议，默认值为65535，若protocol不是传输层协议，设置无效，恒为0。如果规则只限定一个端口号，fromPort和toPort填写同一个值|

## 返回参数
|名称|类型|描述|
|---|---|---|
|**requestId**|String|请求ID|



## 返回码
|返回码|描述|
|---|---|
|**200**|Successful operation|
|**400**|Invalid parameter|
|**404**|Not found|
|**500**|Internal error|
