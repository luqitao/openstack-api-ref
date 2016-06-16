# 查询api版本列表

## 请求
|HTTP方法|URI|说明|
|:------|:---|:---|
|GET|/|查询块存储模块支持的所有接口版本列表。|
### 请求body
无
## 响应
|返回码|描述|
|:---|:---|
|200|成功|
## 响应body

见示例
## 示例
```
$ curl -s -g -X GET http://controller:8776/ \ 
             -H "User-Agent: python-cinderclient" \
             -H "Accept: application/json" \
             -H "X-Auth-Token: 1bc97cc4b40e4f56ad4d1c7719f4c604"  \ 
             | python -m json.tool
{
    "versions": [
        {
            "id": "v1.0",
            "links": [
                {
                    "href": "http://controller:8776/v1/",
                    "rel": "self"
                }
            ],
            "status": "SUPPORTED",
            "updated": "2014-06-28T12:20:21Z"
        },
        {
            "id": "v2.0",
            "links": [
                {
                    "href": "http://controller:8776/v2/",
                    "rel": "self"
                }
            ],
            "status": "CURRENT",
            "updated": "2012-11-21T11:33:21Z"
        }
    ]
}
```

