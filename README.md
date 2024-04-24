# xProto

xProto是一个应用间通信协议，其通过json定义接口。接口包括方法与事件。

可以作为调用者，调用xProto中的方法和监听其中的事件。
也可以作为实现者，实现xProto中的方法和触发其中的事件。

下方是一个xProto示例：

```json
{
  "exampleInput": {
    "name": "example input",
    "description": "a example input, any app can",
    "return": {
      "properties": {
        "success": { "type": "bool" }
      }
    },
    "param": {
      "properties": {
        "name": { "type": "string" }
      }
    }
  }
}
```
