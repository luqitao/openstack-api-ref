# 创建卷
如果要创建一个可启动的卷，那么在请求body体中就必须包含imageRef参数；
如果卷状态一直处于creating或error状态，表示创建失败。
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
|volume_type(可选)|plain|xsd:string|卷类型，在多后端环境中，必须要指定卷类型来创卷，缺省值为None|
|metadata(可选)|plain|xsd:dict|元数据，给卷设置一个或多个键值对形式的元数据|
|source_replica(可选)|plain|csapi:UUID|用来克隆的主卷UUID|
|consistencygroup_id(可选)|plain|csapi:UUID|一致性组UUID|
|scheduler_hints(可选)|plain|xsd:dict|传递给scheduler的数据|
## 响应
|返回码|描述|
|:---|:---|
|202|成功|
|400|参数错误，例如从镜像创建卷时卷大小比镜像小|
## 响应body
|参数|样式|类型|说明|
|:---|:---|:---|:---|
|volume|plain|xsd:dict|一个volume对象|
|status|plain|xsd:string|卷状态|
|migration_status|plain|xsd:string|卷的迁移状态|
|user_id|plain|csapi:UUID|用户UUID|
|attachments|plain|xsd:list|虚拟机挂载信息，|
## 示例
