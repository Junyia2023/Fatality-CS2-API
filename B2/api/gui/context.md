## context

此类型表示GUI上下文。

## find

[[字段]]

通过ID查找控件。

**参数**

| 名称 | 类型 | 描述 |
| ---- | ---- | ----------- |
| `id` | `string` | 控件ID。 |

**返回值**

| 名称 | 描述 |
| ---- | ----------- |
| `<control>?` | 转换后的控件。如果未找到控件或转换失败，则返回 `nil`。 |

**示例**

```lua
local some_cb = ctx:find('some_cb');