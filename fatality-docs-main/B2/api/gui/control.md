## control

此类型表示一个抽象的GUI控件。

## id

![字段][此字段是一个普通字段，必须使用点 (.) 访问。]rw
![只读][此字段是只读字段，无法更改其值。这不适用于子字段（如果有）。]r

类型：`int`

控件ID。

## id_string

![字段][此字段是一个普通字段，必须使用点 (.) 访问。]rw
![只读][此字段是只读字段，无法更改其值。这不适用于子字段（如果有）。]r

类型：`string`

控件ID的字符串表示形式。对于某些控件，这可能是空的。

## is_visible

![字段][此字段是一个普通字段，必须使用点 (.) 访问。]rw
![只读][此字段是只读字段，无法更改其值。这不适用于子字段（如果有）。]r

类型：`bool`

控件的可见状态。

## parent

![字段][此字段是一个普通字段，必须使用点 (.) 访问。]rw
![只读][此字段是只读字段，无法更改其值。这不适用于子字段（如果有）。]r

类型：`control?`

父控件。对于某些控件，这可能是 `nil`。

## type

![字段][此字段是一个普通字段，必须使用点 (.) 访问。]rw
![只读][此字段是只读字段，无法更改其值。这不适用于子字段（如果有）。]r

类型：[`control_type`](/api/gui/control/control-type "此枚举确定当前控件的类型。")

控件的类型。

## inactive

![字段][此字段是一个普通字段，必须使用点 (.) 访问。]rw

类型：`bool`

如果设置为 `true`，将标记此控件为非活动状态。

## inactive_text

![字段][此字段是一个普通字段，必须使用点 (.) 访问。]rw

类型：`string`

当控件处于非活动状态时显示的工具提示替代文本。

## inactive_color

![字段][此字段是一个普通字段，必须使用点 (.) 访问。]rw

类型：[`color`](/api/draw/common-types/color "此类型是在渲染系统中使用的颜色。")

非活动控件的标签颜色覆盖。

## tooltip

![字段][此字段是一个普通字段，必须使用点 (.) 访问。]rw

类型：`string`

工具提示文本。

## aliases

![字段][此字段是一个普通字段，必须使用点 (.) 访问。]rw

类型：`table[string]`

此控件的别名列表。用于搜索框以支持不同的命名（例如，如果用户搜索“Double tap”，将找到“Rapid fire”）。

## get_hotkey_state

![方法][此字段是一个方法，必须使用冒号 (:) 调用。]rw

如果控件的任何热键处于活动状态，则返回 `true`。

**参数**

无。

**返回值**

| 名称 | 描述 |
| ---- | ----------- |
| `bool` | 如果有任何热键处于活动状态则为 `true`。 |

**示例**

```lua
if ctrl:get_hotkey_state() then
    -- ...
end
```

## set_visible

![方法][此字段是一个方法，必须使用冒号 (:) 调用。]rw

更改此控件的可见状态。

> 在布局中有大量其他控件的情况下调用此方法将不可避免地导致性能问题，因为会自动堆叠。

**参数**

| 名称 | 类型 | 描述 |
| ---- | ---- | ----------- |
| `val` | `bool` | 可见状态。 |

**返回值**

无。

**示例**

```lua
ctrl:set_visible(false);
```

## add_callback

![方法][此字段是一个方法，必须使用冒号 (:) 调用。]rw

为此控件添加回调。

**参数**

| 名称 | 类型 | 描述 |
| ---- | ---- | ----------- |
| `cbk` | `函数` | 回调函数。 |

**返回值**

无。

**示例**

```lua
ctrl:add_callback(函数 ()
    print('Callback invoked!');
end);
```

## cast

![方法][此字段是一个方法，必须使用冒号 (:) 调用。]rw

尝试将控件转换为正确的类型。

> 由于Lua引擎的限制，无法自动向下转换变量。通常不需要调用此方法，除非您发现某个控件尚未转换为所需类型。`find()` 方法会自动执行到正确类型的转换。

**参数**

无。

**返回值**

| 名称 | 描述 |
| ---- | ----------- |
| `<control>` | 新类型（如果有）。 |

**示例**

```lua
local checkbox = maybe_checkbox:cast();
```

## reset

![方法][此字段是一个方法，必须使用冒号 (:) 调用。]rw

重置控件的状态。如果您直接通过交互更改了控件的值（例如使用 [`value_param`](/api/gui/control/value-param "此类型表示一些控件类型使用的值数据")），通常需要执行此操作。

**参数**

无。

**返回值**

无。

**示例**

```lua
ctrl:reset();
```
```