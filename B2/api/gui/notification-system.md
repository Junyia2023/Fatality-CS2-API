## 通知系统

此类型表示一个通知系统。

## add

[[字段]]

向列表中添加一个通知。

**参数**

| 名称 | 类型 | 描述 |
| ---- | ---- | ----------- |
| `notif` | [`notification`](/api/gui/notification-system/notification "此类型表示一个通知项。") | 通知对象。 |

**返回值**

无。

**示例**

```lua
notif:add(my_notification);