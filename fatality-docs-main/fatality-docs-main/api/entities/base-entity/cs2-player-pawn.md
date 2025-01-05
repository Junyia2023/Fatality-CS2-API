## cs2_player_pawn

此类型表示 `C_CSPlayerPawn` 类。

> 此类型继承自 [`base_entity`](/api/entities/base-entity "此类型表示基础游戏实体。") 类型。它的所有基础方法和字段在此类型中也可用。

## should_draw

[[字段]]

如果游戏将在屏幕上绘制此玩家，则返回 `true`。

**参数**

无。

**返回值**

| 类型 | 描述 |
| ---- | ---- |
| `bool` | 如果将绘制则为 `true`。 |

**示例**

```lua
if player:should_draw() then
    -- ...
end
```

## is_left_handed

[[字段]]

如果启用了左手模式，则返回 `true`。

**参数**

无。

**返回值**

| 类型 | 描述 |
| ---- | ---- |
| `bool` | 如果是左手模式则为 `true`。 |

**示例**

```lua
if player:is_left_handed() then
    -- ...
end
```

## get_abs_origin

[[字段]]

返回绝对原点（用于渲染的原点）。

**参数**

无。

**返回值**

| 类型 | 描述 |
| ---- | ---- |
| [`vector`](/api/common-types/vector "此类型是一个常见的3D向量（x, y, z）。") | 原点。 |

**示例**

```lua
local org = player:get_abs_origin();
```

## get_abs_angles

[[字段]]

返回绝对角度（用于渲染的角度）。

**参数**

无。

**返回值**

| 类型 | 描述 |
| ---- | ---- |
| [`vector`](/api/common-types/vector "此类型是一个常见的3D向量（x, y, z）。") | 角度。 |

**示例**

```lua
local ang = player:get_abs_angles();
```

## set_abs_origin

[[字段]]

设置新的绝对原点。

**参数**

| 名称 | 类型 | 描述 |
| ---- | ---- | ---- |
| `vec` | [`vector`](/api/common-types/vector "此类型是一个常见的3D向量（x, y, z）。") | 新原点。 |

**返回值**

无。

**示例**

```lua
player:set_abs_origin(my_vec);
```

## set_abs_angles

[[字段]]

设置新的绝对角度。

**参数**

| 名称 | 类型 | 描述 |
| ---- | ---- | ---- |
| `ang` | [`vector`](/api/common-types/vector "此类型是一个常见的3D向量（x, y, z）。") | 新角度。 |

**返回值**

无。

**示例**

```lua
player:set_abs_angles(my_ang);
```

## is_alive

[[字段]]

如果玩家还活着，则返回 `true`。

**参数**

无。

**返回值**

| 类型 | 描述 |
| ---- | ---- |
| `bool` | 如果还活着则为 `true`。 |

**示例**

```lua
if player:is_alive() then
    -- ...
end
```

## is_enemy

[[字段]]

如果此玩家是本地玩家的敌人，则返回 `true`。

**参数**

无。

**返回值**

| 类型 | 描述 |
| ---- | ---- |
| `bool` | 如果是敌人则为 `true`。 |

**示例**

```lua
if player:is_enemy() then
    -- ...
end
```

## is_enemy_to

[[字段]]

返回此玩家是否是另一个实体的敌人。

**参数**

| 名称 | 类型 | 描述 |
| ---- | ---- | ---- |
| `ent` | [`base_entity`](/api/entities/base-entity "此类型表示基础游戏实体。") | 其他实体。 |

**返回值**

| 类型 | 描述 |
| ---- | ---- |
| `bool` | 如果是敌人则为 `true`。 |

**示例**

```lua
if player:is_enemy_to(other_player) then
    -- ...
end
```

## get_active_weapon

[[字段]]

返回当前使用的武器。

**参数**

无。

**返回值**

| 类型 | 描述 |
| ---- | ---- |
| [`cs2_weapon_base_gun`](/api/entities/base-entity/cs2-weapon-base-gun "此类型表示 CCSWeaponBaseGun 类。") | 武器实例。 |

**示例**

```lua
local wep = player:get_active_weapon();
```

## get_name

[[字段]]

返回已净化的玩家名称。

**参数**

无。

**返回值**

| 类型 | 描述 |
| ---- | ---- |
| `string` | 玩家名称。 |

**示例**

```lua
local name = player:get_name();
```

## get_view_offset

[[字段]]

返回玩家的视角偏移（相对于玩家原点的眼睛位置）。

**参数**

无。

**返回值**

| 类型 | 描述 |
| ---- | ---- |
| [`vector`](/api/common-types/vector "此类型是一个常见的3D向量（x, y, z）。") | 视角偏移。 |

**示例**

```lua
local vo = player:get_view_offset();
```

## get_eye_pos

[[字段]]

返回玩家的眼睛位置。

**参数**

无。

**返回值**

| 类型 | 描述 |
| ---- | ---- |
| [`vector`](/api/common-types/vector "此类型是一个常见的3D向量（x, y, z）。") | 眼睛位置。 |

**示例**

```lua
local eyes = player:get_eye_pos();
```