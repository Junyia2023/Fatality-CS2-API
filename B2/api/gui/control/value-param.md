## value_param

此类型表示一些控件类型使用的值数据。

> 注意，这部分：`<type>` 用于指定此类型的实例持有的确切类型。例如，当它说 `value_param<bool>` 时，意味着 `get` 将返回一个 `bool` 类型的值，并且 `set` 只接受 `bool` 类型作为其 `val` 参数。

## get

[[字段]]

返回值。

**参数**

无。

**返回**

| 名称 | 描述 |
| ---- | ---- |
| `<type>` | 值。 |

**示例**

```lua
ctrl:get_value():get();
```

## set

[[字段]]

设置值。

> 建议使用控件的 `set_value` 方法（如果有）。

**参数**

| 名称 | 类型 | 描述 |
| ---- | ---- | ---- |
| `val` | `<type>` | 值。 |

**返回**

无。

**示例**

```lua
ctrl:get_value():set(123);
```

## get_hotkey_state

[[字段]]

如果存在任何激活的热键，则返回 `true`。

**参数**

无。

**返回**

| 名称 | 描述 |
| ---- | ---- |
| `bool` | 如果有任何热键处于激活状态，则返回 `true`。 |

**示例**

```lua
if ctrl:get_value():get_hotkey_state() then
    -- ...
end
```

## disable_hotkeys

[[字段]]

禁用所有激活的热键。这允许你覆盖该值。

**参数**

无。

**返回**

无。

**示例**

```lua
ctrl:get_value():disable_hotkeys();
```
```