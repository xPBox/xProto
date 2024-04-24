# xProto

xProto是一个应用间通信协议，其通过json定义模式。通过xProto，可以实现两个应用之间的数据交互约定。应用可以作为调用者，调用xProto中的函数。也可以作为实现者，实现xProto中的函数。

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

## 约定

xProto最外层以函数名为key，函数信息包含name、description、return、param。

其中param是一个参数，作为xProto的函数，参数始终只有一个，可以是对象。同时返回值也只能有一个，并且也可以是对象。

param和return的结构使用JsonSchema进行定义。
