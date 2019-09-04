`Access-Control-Expose-Headers` 响应报头指示哪些报头可以公开为通过列出他们的名字的响应的一部分。
默认情况下，只显示6个简单的响应标头：
- `Cache-Control`
- `Content-Language`
- `Content-Type`
- `Expires`
- `Last-Modified`
- `Pragma`
  
如果您希望客户端能够访问其他响应标头，则必须使用Access-Control-Expose-Headers标题列出它们。  
  
  |  标题类型  |  响应标题  |
  |:-------:|:--------:|
  |  禁止标题名称  |  没有  |


## 句法
> Access-Control-Expose-Headers: <header-name>, <header-name>, ...

## 指令
<header-name>暴露的头部列表，其中包含零个或多个头部名称，而不是资源可能使用并可能暴露的简单响应头部。

## 例子
要公开一个非简单的响应头，你可以指定：
> Access-Control-Expose-Headers: Content-Length
要另外公开一个自定义标题，例如X-Kuma-Revision，您可以指定用逗号分隔的多个标题：
> Access-Control-Expose-Headers: Content-Length, X-Kuma-Revision

## 产品规格
|  规范  |  状态  |
|:-------:|:--------:|
|  在该规范中获取'Access-Control-Expose-Headers'的定义。  |    |
  
