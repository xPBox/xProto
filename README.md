# xProto

xProto是一个模块间通信协议，其通过json定义接口。接口包括方法与事件。

模块可以作为调用者，调用xProto中的方法和监听其中的事件。
也可以作为实现者，实现xProto中的方法和触发其中的事件。

下方是一个xProto示例：


```
{
	"sign": "",
	"access": "private",
	"class": "System",
	"version": "1.0.0",
	"types": {

	},
	"methods": {
		"addModule": {
			"name": "添加Dll模块",
			"description": "添加Dll模块",
			"ret": {
				"properties": {
					"success": { "type": "bool" }
				}
			},
			"param": {
				"properties": {
					"name": { "type": "string" }
				},
				"required": ["name"]
			}
		},
		"exit": {
			"name": "退出应用",
			"description": "退出应用"
		},
		"showLicenseWindow": {
			"name": "显示许可窗口",
			"description": "显示许可窗口"
		},
		"getShortCode": {
			"name": "获取短代码",
			"description": "获取短代码",
			"ret": {
				"properties": {
					"shortCode": { "type": "string" }
				}
			}
		},
		"getLicenceId": {
			"name": "取许可ID",
			"description": "取许可ID",
			"ret": {
				"properties": {
					"success": {
						"licenceId": "string"
					}
				}
			}
		}
	}
}
```
