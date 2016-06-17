# 查询api版本详情
## 请求
|HTTP方法|URI|说明|
|:------|:---|:---|
|GET|/v1.0|查询块存储模块支持v1.0版本接口详情。|
|GET|/v2.0|查询块存储模块支持v2.0版本接口详情。|
### 请求body
无
## 响应
|返回码|描述|
|:---|:---|
|200|成功|
## 响应body
|参数|样式|类型|说明|
|:---|:---|:---|:---|
|location|plain|xsd:anyURI|访问服务的URL全路径地址.|
## 示例
查询v1.0接口详情
```
curl -s -g -X GET http://controller:8776/v1.0 \
           -H "User-Agent: python-cinderclient" \
           -H "Accept: application/json" \
           -H "X-Auth-Token: 1bc97cc4b40e4f56ad4d1c7719f4c604" \
           | python -m json.tool
{
    "choices": [
        {
            "id": "v1.0",
            "links": [
                {
                    "href": "http://controller:8776/v1/v1.0",
                    "rel": "self"
                }
            ],
            "media-types": [
                {
                    "base": "application/xml",
                    "type": "application/vnd.openstack.volume+xml;version=1"
                },
                {
                    "base": "application/json",
                    "type": "application/vnd.openstack.volume+json;version=1"
                }
            ],
            "status": "SUPPORTED"
        },
        {
            "id": "v2.0",
            "links": [
                {
                    "href": "http://controller:8776/v2/v1.0",
                    "rel": "self"
                }
            ],
            "media-types": [
                {
                    "base": "application/xml",
                    "type": "application/vnd.openstack.volume+xml;version=1"
                },
                {
                    "base": "application/json",
                    "type": "application/vnd.openstack.volume+json;version=1"
                }
            ],
            "status": "CURRENT"
        }
    ]
}
```
查询v2.0接口详情
```
curl -s -g -X GET http://controller:8776/v2.0 \
           -H "User-Agent: python-cinderclient" \
           -H "Accept: application/json" \
           -H "X-Auth-Token: 1bc97cc4b40e4f56ad4d1c7719f4c604" \
           | python -m json.tool
{
    "choices": [
        {
            "id": "v1.0",
            "links": [
                {
                    "href": "http://controller:8776/v1/v2.0",
                    "rel": "self"
                }
            ],
            "media-types": [
                {
                    "base": "application/xml",
                    "type": "application/vnd.openstack.volume+xml;version=1"
                },
                {
                    "base": "application/json",
                    "type": "application/vnd.openstack.volume+json;version=1"
                }
            ],
            "status": "SUPPORTED"
        },
        {
            "id": "v2.0",
            "links": [
                {
                    "href": "http://controller:8776/v2/v2.0",
                    "rel": "self"
                }
            ],
            "media-types": [
                {
                    "base": "application/xml",
                    "type": "application/vnd.openstack.volume+xml;version=1"
                },
                {
                    "base": "application/json",
                    "type": "application/vnd.openstack.volume+json;version=1"
                }
            ],
            "status": "CURRENT"
        }
    ]
}
```

