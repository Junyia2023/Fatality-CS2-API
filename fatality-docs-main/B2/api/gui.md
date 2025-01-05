## gui

用法: `gui.{func_or_字段}`

此表暴露了软件的GUI系统。

> 所有在子部分中描述的类型和枚举必须以 `gui.` 为前缀。

## ctx

![字段][此字段是一个普通字段，必须使用点 (.) 访问。]rw

类型: [`context`](/api/gui/context "此类型表示GUI上下文。")

GUI上下文。

## notify

![字段][此字段是一个普通字段，必须使用点 (.) 访问。]rw

类型: [`notification_system`](/api/gui/notification-system "此类型表示一个通知系统。")

通知系统。

## make_control

![函数][此字段是一个函数，必须使用点 (.) 调用]rw

将控件包装在一个由标签和该特定控件组成的布局中。如果你想让你的控件显示得更美观，应该将**这个**新控件添加到分组框中。此外，你可以向返回的控件添加任何额外的控件——这些控件将堆叠在初始控件的左侧。

**参数**

| 名称 | 类型 | 描述 |
| ---- | ---- | ----------- |
| `text` | `string` | 标签值。 |
| `c` | [`control`](/api/gui/control "此类型表示一个抽象的GUI控件。") | 控件对象。 |

**返回值**

| 类型 | 描述 |
| ---- | ----------- |
| [`layout`](/api/gui/container/control-container/layout "此类型表示一个布局控件。") | 布局对象。 |

**示例**

```lua
local row = gui.make_control('Hello checkbox!', my_cb);