# 查询api v2版本详情


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