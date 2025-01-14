## bits

此类型表示一个bitset值。

> 此类型的最大位数为 **63**。设置或获取超出此范围的任何位将导致 **崩溃**。

### reset

[[字段]]

重置值。

**参数**

无。

**返回**

无。

**示例**

```lua
bits:reset();
```

### get_raw

[[字段]]

返回原始值。

**参数**

无。

**返回**

| 类型 | 描述 |
| ---- | ----------- |
| `int` | 原始值。 |

**示例**

```lua
local raw = bits:get_raw();
```

### set_raw

[[字段]]

设置原始值。

**参数**

| 名称 | 类型 | 描述 |
| ---- | ---- | ----------- |
| `val` | `int` | 原始值。 |

**返回**

无。

**示例**

```lua
bits:set_raw(long_long_value);
```

### none

[[字段]]

如果没有任何位被设置，则返回true。

**参数**

无。

**返回**

| 类型 | 描述 |
| ---- | ----------- |
| `bool` | 如果没有任何位被设置，则返回 `true`。 |

**示例**

```lua
if bits:none() then
    -- ...
end
```

### set

[[字段]]

启用一个位。

**参数**

| 名称 | 类型 | 描述 |
| ---- | ---- | ----------- |
| `bit` | `int` | 位编号。 |

**返回**

无。

**示例**

```lua
bits:set(5); -- 设置位 #5（与 bit.bor(val, bit.lshift(1, 5)) 相同）
```

### unset

[[字段]]

禁用一个位。

**参数**

| 名称 | 类型 | 描述 |
| ---- | ---- | ----------- |
| `bit` | `int` | 位编号。 |

**返回**

无。

**示例**

```lua
bits:unset(5);
```

### get

[[字段]]

返回位状态。

**参数**

| 名称 | 类型 | 描述 |
| ---- | ---- | ----------- |
| `bit` | `int` | 位编号。 |

**返回**

| 名称 | 描述 |
| ---- | ----------- |
| `bool` | 位状态。 |

**示例**

```lua
if bits:get(5) then
    -- ...
end
```

### toggle

[[字段]]

切换位状态。

**参数**

| 名称 | 类型 | 描述 |
| ---- | ---- | ----------- |
| `bit` | `int` | 位编号。 |

**返回**

无。

**示例**

```lua
bits:toggle(5);
```