
# Opensearch 经销商接口

经销商代理动作,更新经销商代理所有产品 ,更新经销商代理的产品(一个或多个),删除代理,分组请求(更新多个经销商代理所有产品)

 * URL: /api/dealer
 * Method: POST

### 例子如下


## 更新经销商代理的产品(一个或多个)
```
POST  http://192.168.0.57:81/api/dealer HTTP/1.1
User-Agent: Fiddler
Host: localhost:7820
Content-Length: 110
Content-Type: application/x-www-form-urlencoded; charset=UTF-8

dealerid=4bb65088-0851-448f-9fc3-6ab19bcf4a3c&productid=20161130151207563-C3EE1669-4307-4E06-B54E-D8067121D1B6
```

```
POST http://192.168.0.57:81/api/dealer HTTP/1.1
User-Agent: Fiddler
Host: 192.168.0.57:81
Content-Length: 121
Content-Type: application/json

{
 dealerid:'4bb65088-0851-448f-9fc3-6ab19bcf4a3c',
 productid:'20161130151207563-C3EE1669-4307-4E06-B54E-D8067121D1B6'
}
```


## 更新经销商代理所有产品

```
POST http://192.168.0.57:81/api/dealer/4bb65088-0851-448f-9fc3-6ab19bcf4a3c HTTP/1.1
User-Agent: Fiddler
Host: 192.168.0.57:81
Content-Length: 0
```


##分组请求接口 更新多个经销商

```
POST http://192.168.0.57:81/api/dealer/group HTTP/1.1
User-Agent: Fiddler
Host: 192.168.0.57:81
Content-Length: 121
Content-Type: application/json

{
 dealerid:'4bb65088-0851-448f-9fc3-6ab19bcf4a3c,a9477646-4a5e-4f03-8f54-ec7aca0e46a9'
}
```


``` 
200 请求成功

返回
status : OK 成功
["{\n    \"request_id\": \"149647518417780173396907\",\n    \"status\": \"OK\"\n}","{\n    \"request_id\": \"149647519117780173321105\",\n    \"status\": \"OK\"\n}","20161130152550253-3CE4A138-390A-4F74-881A-3D570449AD80"]


其他的
看返回结果看错误原因
```

[阿里云错误码说明](https://help.aliyun.com/document_detail/29146.html?spm=5176.doc29140.2.1.ZPZUKD)

>多个产品 productid 用逗号(,)分隔
>
>多个经销商dealerid 用逗号(,)分隔
