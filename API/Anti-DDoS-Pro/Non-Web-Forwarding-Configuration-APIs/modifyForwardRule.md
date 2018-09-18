# modifyForwardRule


## 描述
更新非网站类规则

## 请求方式
PATCH

## 请求地址
https://ipanti.jdcloud-api.com/v1/regions/{regionId}/instances/{instanceId}/forwardRules/{forwardRuleId}

|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**forwardRuleId**|String|True||转发规则 ID|
|**instanceId**|String|True||实例 ID|
|**regionId**|String|True||Region ID|

## 请求参数
|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**forwardRuleSpec**|ForwardRuleSpec|True||更新非网站类规则请求参数|

### <a name="ForwardRuleSpec">ForwardRuleSpec</a>
|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**algorithm**|String|False||转发规则：wrr->带权重的轮询，wlc->加权最小连接，rr->不带权重的轮询，sh->源地址hash|
|**onlineAddr**|String[]|False|||
|**originAddr**|OriginAddrItem[]|False|||
|**originDomain**|String|False||回源域名|
|**originPort**|Integer|False||回源端口号|
|**originType**|String|False||回源类型，ip或者domain|
|**port**|Integer|False||端口号|
|**protocol**|String|False||协议：TCP或者UDP|
### <a name="OriginAddrItem">OriginAddrItem</a>
|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**inJdCloud**|Boolean|False||是否为京东云内公网ip|
|**ip**|String|False||回源ip|
|**weight**|Integer|False||权重|

## 返回参数
|名称|类型|描述|
|---|---|---|
|**requestId**|String||



## 返回码
|返回码|描述|
|---|---|
|**200**|OK|
|**400**|BAD_REQUEST|
|**404**|NOT_FOUND|
|**500**|INTERNAL_SERVER_ERROR|
