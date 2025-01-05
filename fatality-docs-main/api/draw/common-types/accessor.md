## accessor

此类型表示一种安全访问映射（maps）的方式。

> 注意，`<type>` 表示此实例持有的具体类型。例如，`accessor<texture>` 意味着 `get` 将返回一个 `texture` 实例，而 `set` 仅接受 `texture` 类型作为其 `obj` 参数。

## __index

[![Function][此字段是一个函数，必须使用点 (.) 调用]rw]

通过键返回对象。

**参数**

| 名称 | 类型 | 描述 |
| ---- | ---- | ----------- |
| `key` | `string` | 对象键。 |

**返回值**

| 类型 | 描述 |
| ---- | ----------- |
| `<type>` | 对象。 |

**示例**

```lua
local main_font = draw.fonts['gui_main'];

-- 这种方式也有效
local main_font_2 = draw.fonts.gui_main;
```

## __newindex

[![Function][此字段是一个函数，必须使用点 (.) 调用]rw]

通过键设置对象。

**参数**

| 名称 | 类型 | 描述 |
| ---- | ---- | ----------- |
| `key` | `string` | 对象键。 |
| `obj` | `<type>` | 对象。 |

**返回值**

无。

**示例**

```lua
draw.fonts['my_font'] = my_font;

-- 这种方式也有效
draw.fonts.my_font = my_font;
```