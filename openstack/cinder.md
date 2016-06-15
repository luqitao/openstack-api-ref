# cinder
## 公共字段
### 公共请求头

|请求头|类型|说明|
| :------------- |:-------------|:-----|
|Content-Type|string|指定请求内容类型，一般为: application/json|
|Accept|string|指定返回内容类型，一般为: application/json|
|X-Auth-Token|string|请求openstack各服务REST API时要求在请求头中带上的经过认证的Token|
|Accept-Language|string|请求服务端返回的语言类型|

### 公共返回头

|返回头|类型|说明|
| :------------- |:-------------|:-----|
| Content-Type | string |表明返回内容类型|

### 常见HTTP返回码

|HTTP错误码|原因|说明|
| :------- |:-------------|:-----|
| 200 | Normal             |操作成功，正常返回 |
| 201 |	Created	           | 一般指创建资源成功，正常返回 |
| 400 |	BadRequest	       | 请求错误 |
| 401 |	Unauthorized       | 请求所带的Token没有经过认证或者认证失败 |
| 403 |	Forbidden	       | 操作禁止 |
| 404 |	ItemNotFound       | 没找到对象 |
| 405 |	BadMethod          | 不支持的HTTP方法 |
| 413 |	OverLimit          | 超过请求频率的限制 |
| 503 |	ServiceUnavailable | 超过请求频率的限制 |

## API versions

查询块存储接口所有版本信息。
test



