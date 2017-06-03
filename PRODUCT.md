
# Opensearch 产品接口

更改产品内容, 更改代理改产品得所有经销商对应信息

 * URL: /api/product 
 * Method: POST

### 例子如下

```
POST http://192.168.0.57:81/api/product/20161130152550253-3CE4A138-390A-4F74-881A-3D570449AD80 HTTP/1.1
User-Agent: Fiddler
Host: 192.168.0.57:81
Content-Length: 0
```

```
POST http://192.168.0.57:81/api/product/ HTTP/1.1
User-Agent: Fiddler
Host: 192.168.0.57:81
Content-Length: 65
Content-Type: application/json

{
id:'20161130152550253-3CE4A138-390A-4F74-881A-3D570449AD80'
}
```

```
POST http://192.168.0.57:81/api/product HTTP/1.1
User-Agent: Fiddler
Host: localhost:7820
Content-Length: 57
Content-Type: application/x-www-form-urlencoded; charset=UTF-8

id=20161130152550253-3CE4A138-390A-4F74-881A-3D570449AD80
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

>多个产品 id 用逗号(,)分隔
>
>更新产品内容 eds_product eds_product_value
>
>更新代理该产品得所有经销商得对应信息 ds_user_product