# updateTopic


## 描述
此接口可以用来更新主题，创建归档，修改归档，删除归档，传入不同的参数可以实现不同的功能。修改归档只需要修改相应归档的参数，删除归档只需要把归档参数置为空即可

## 请求方式
PUT

## 请求地址
https://streambus.jdcloud-api.com/v1/regions/{regionId}/topic

|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**regionId**|String|True||地域ID|

## 请求参数
|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**topicModel**|TopicModel|True||当更新主题时只需要修改topicModel中的topic中的属性即可；创建归档需要指定target以及归档的目的地(mysql,京东云 Elasticsearch,对象存储,数据计算服务)参数|

### <a name="TopicModel">TopicModel</a>
|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**parameterList**|Object[]|False||归档相关的具体参数，需要对归档进行新建，更新，删除，修改对应参数值即可。<br>ossFlag，bucketName，directory，objectName 这四个参数值与ossFlag有关，若ossFlag为false，后面三个可为空，若为true，后面三个为异常数据保存位置，按需要填写即可。<br> 1）如果归档到数据计算服务需要传database，table，type，example，delimiter，targetColumn，analysisColumn，partsTargetColumn，partsAnalysisColumn。<br>2）如果归档到JFS需要传bucket，prefix，infix。<br>3）如果归档到京东云 Elasticsearch需要传host，port，indexType，idType，indexName，indexReferField，timestampFieldFormat，timestampIndexFormat，typeName，idReferField，noResolve，username，password。<br> 4）如果归档到mysql，则需要传host，database，table，username，password，type，example，delimiter。 <br>5)如果要归档到京东云数据库则需要传rdsId，database，table，username，password，type，example，delimiter。|
|**target**|Target|False|||
|**topic**|Topic|False|||
### <a name="Target">Target</a>
|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**cycle**|Integer|False||进行归档任务的时间周期|
|**name**|String|False||需要归档的目的地|
|**recordSize**|Integer|False||当达到这个数据量时开始归档|
### <a name="Topic">Topic</a>
|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**archived**|Integer|False||是否归档（0：未归档，1：已归档）|
|**id**|Integer|False||主题id|
|**lifecycle**|Integer|False||数据写入后的保留时间|
|**name**|String|False||流数据总线中topic的名字|
|**partitionNum**|Integer|False||分区|
|**remark**|String|False||备注|
|**shardNum**|Integer|False||流数据总线shard的数量|

## 返回参数
|名称|类型|描述|
|---|---|---|
|**requestId**|String||
|**result**|Result||


### <a name="Result">Result</a>
|名称|类型|描述|
|---|---|---|
|**message**|String|状态信息|
|**status**|Boolean||

## 返回码
|返回码|描述|
|---|---|
|**200**|OK|
|**400**|ERROR|
