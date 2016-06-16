# Volumes
    
    卷是一种类似于U盘可插拔的块存储设备，它允许你在任意时间挂载到一台或多台虚拟机上。
snapshot_id和source_volid这两个参数表示该卷是从哪个快照id或卷id克隆而来，如果创建卷的时候既没有选择快照也没有选择源卷，那么这些值就是null。
以下是卷可能出现的状态列表：

|状态|描述|
|:---|:---|
|creating|创建中|
|available|可用|
|attaching|挂载中|
|in-use|使用中|
|deleting|删除中|
|error|错误|
|backing-up|备份中|
|restoring-backup|恢复中|
|error_restoring|恢复失败|
|error_extending|扩容失败|
|extending|扩容中|
|uploading|上传中|
|downloading|下载中|