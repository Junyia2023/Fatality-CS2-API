## game_event_t

描述一个游戏事件。

## get_name

[![Method][此字段是一个方法，必须使用冒号 (:) 调用]rw]

返回事件名称。

**参数**

无。

**返回值**

| 类型 | 描述 |
| ---- | ----------- |
| `string` | 事件名称。 |

**示例**

```lua
if event:get_name() == 'player_hurt' then
    -- ...
end
```

## get_bool

[![Method][此字段是一个方法，必须使用冒号 (:) 调用]rw]

根据键返回布尔值。

**参数**

| 名称 | 类型 | 描述 |
| ---- | ---- | ----------- |
| `key` | `string` | 条目键。 |

**返回值**

| 类型 | 描述 |
| ---- | ----------- |
| `bool` | 条目值。如果未找到该键，则返回 `false`。 |

**示例**

```lua
event:get_bool('some_key');
```

## get_int

[![Method][此字段是一个方法，必须使用冒号 (:) 调用]rw]

根据键返回整数值。

**参数**

| 名称 | 类型 | 描述 |
| ---- | ---- | ----------- |
| `key` | `string` | 条目键。 |

**返回值**

| 类型 | 描述 |
| ---- | ----------- |
| `int` | 条目值。如果未找到该键，则返回 `0`。 |

**示例**

```lua
event:get_int('some_key');
```

## get_float

[![Method][此字段是一个方法，必须使用冒号 (:) 调用]rw]

根据键返回浮点数值。

**参数**

| 名称 | 类型 | 描述 |
| ---- | ---- | ----------- |
| `key` | `string` | 条目键。 |

**返回值**

| 类型 | 描述 |
| ---- | ----------- |
| `float` | 条目值。如果未找到该键，则返回 `0.0`。 |

**示例**

```lua
event:get_float('some_key');
```

## get_string

[![Method][此字段是一个方法，必须使用冒号 (:) 调用]rw]

根据键返回字符串值。

**参数**

| 名称 | 类型 | 描述 |
| ---- | ---- | ----------- |
| `key` | `string` | 条目键。 |

**返回值**

| 类型 | 描述 |
| ---- | ----------- |
| `string` | 条目值。如果未找到该键，则返回 `''`。 |

**示例**

```lua
event:get_string('some_key');
```

## get_controller

[![Method][此字段是一个方法，必须使用冒号 (:) 调用]rw]

根据键返回控制器。

**参数**

| 名称 | 类型 | 描述 |
| ---- | ---- | ----------- |
| `key` | `string` | 条目键。 |

**返回值**

| 类型 | 描述 |
| ---- | ----------- |
| [`cs2_player_controller`](/api/entities/base-entity/cs2-player-controller "此类型表示 CCSPlayerController 类。") | 控制器。 |

**示例**

```lua
event:get_controller('userid');
```

## get_pawn_from_id

[![Method][此字段是一个方法，必须使用冒号 (:) 调用]rw]

根据键返回棋子（Pawn）。

**参数**

| 名称 | 类型 | 描述 |
| ---- | ---- | ----------- |
| `key` | `string` | 条目键。 |

**返回值**

| 类型 | 描述 |
| ---- | ----------- |
| [`cs2_player_pawn`](/api/entities/base-entity/cs2-player-pawn "此类型表示 C_CSPlayerPawn 类。") | 棋子（Pawn）。 |

**示例**

```lua
event:get_pawn_from_id('userid');
```