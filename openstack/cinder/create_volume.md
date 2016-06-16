# 创建卷
## 请求
|HTTP方法|URI|说明|
|:------|:---|:---|
|POST|/v2/{tenant_id}/volumes|创建一个卷。|

### 请求body
|参数|样式|类型|说明|
|:------|:---|:---|:---|
|tenant_id|URI|csapi:UUID|租户UUID|
|volume|plain|xsd:dict|一个卷对象|
|size|plain|xsd:int|卷大小，单位：GB|
|availability_zone(可选)|plain|xsd:string|可用域|
|source_volid(可选)|plain|csapi:UUID|源卷UUID，克隆卷后会创建一个和源卷大小一样的新卷|
|description(可选)|plain|xsd:string|描述信息|
|multiattach(可选)|plain|xsd:boolean|如果要允许一个卷同时挂载到多台虚拟机，将该值设置为true，缺省为false|
|snapshot_id(可选)|plain|csapi:UUID|快照UUID，从快照创建的卷和快照具有相同大小，且在同一个可用域内|
|name(可选)|plain|xsd:string|卷名称|
|imageRef(可选)|plain|csapi:UUID|镜像UUID，创建一个可启动卷时需要传镜像id|
|volume_type(可选)|plain|xsd:string|卷名称|
|metadata(可选)|plain|xsd:string|卷名称|
|source_replica(可选)|plain|xsd:string|卷名称|
|consistencygroup_id(可选)|plain|xsd:string|卷名称|
|scheduler_hints(可选)|plain|xsd:string|卷名称|
## 响应
|返回码|描述|
|:---|:---|
|200|成功|
## 响应body
|参数|样式|类型|说明|
|:---|:---|:---|:---|
|location|plain|xsd:anyURI|Full URL to a service or server.|
## 示例
