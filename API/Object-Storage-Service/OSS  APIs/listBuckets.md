# listBuckets


## 描述
该操作对服务地址进行Get请求，可以返回请求者拥有的所有Bucket。


## 请求方式
GET

## 请求地址
https://oss.jdcloud-api.com/v1/regions/{regionId}/buckets

|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**regionId**|String|True|无|Region ID，例如：cn-north-1|

## 请求参数
无


## 返回参数
|名称|类型|描述|
|---|---|---|
|**requestId**|String|请求ID|
|**result**|[Result](##Result)|返回结果集合|


### <a name="Result">Result</a>
|名称|类型|描述|
|---|---|---| 
|**buckets**|[Bucket[]](##Bucket)|所有bucket信息集合|
|**owner**|[User](##User)|拥有者信息|
### <a name="Bucket">Bucket</a>
|名称|类型|描述|
|---|---|---|
|**creationDate**|String|创建时间|
|**name**|String|bucket名称|
### <a name="User">User</a>
|名称|类型|描述|
|---|---|---|
|**displayName**|String|拥有者名称|
|**id**|String|拥有者ID|

## 返回码
|返回码|描述|
|---|---|
|**200**|OK|
|**400**|Invalid Argument|
|**403**|Access Denied|

## 示例
### 请求示例
```
GET /v1/regions/cn-north-1/buckets HTTP/1.1
Accept-Encoding: gzip
Authorization: signatureValue
Content-Type: application/json
User-Agent: JdcloudSdkJava/0.9.2 oss/v1 Google-HTTP-Java-Client/1.22.0 (gzip)
x-jdcloud-nonce: 77ff34dd-4faf-4eb4-a6b7-7c0965db97cf
x-jdcloud-date: 20180822T102649Z
Host: oss.jdcloud-api.com
Connection: Keep-Alive
```
### 返回示例
```
HTTP/1.1 200 OK
Date: Wed, 22 Aug 2018 10:26:54 GMT
Content-Type: text/xml;charset=UTF-8
Transfer-Encoding: chunked
Connection: close
x-jdcloud-limit-minute: 1000
x-jdcloud-remaining-minute: 999
Server: JDCloudOSS
Vary: Accept-Encoding
x-req-id: 9F83347D7B30CDBB
x-jss-service: GET.service
x-jdcloud-request-id: bdvjks919u5c9wp90gertik9n498cr2i
Content-Encoding: gzip
x-jdcloud-upstream-latency: 332
x-jdcloud-proxy-latency: 81
x-jdcloud-via: jdcloud

{"requestId":"8E8E4E8E21F73CB0","result":{"owner":{"id":"243035305301","displayName":"jcloudiaas4"},"buckets":[{"name":"jss-test","creationDate":"2017-07-18T10:52:21.000Z"}]}}
```