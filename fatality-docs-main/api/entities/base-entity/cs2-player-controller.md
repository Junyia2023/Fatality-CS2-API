## cs2_player_controller

此类型表示 `CCSPlayerController` 类。

> 此类型继承自 [`base_entity`](/api/entities/base-entity "此类型表示一个基础游戏实体。") 类型。其所有基础方法和字段在此类型中也可用。

## is_enemy

[![方法][此字段是一个方法，必须使用冒号 (:) 调用。]rw]

如果此玩家是本地玩家的敌人，则返回 `true`。

**参数**

无。

**返回**

| 类型 | 描述 |
| ---- | ---- |
| `bool` | 如果是敌人则为 `true`。 |

**示例**

```lua
if player:is_enemy() then
    -- ...
end
```

## get_name

[![方法][此字段是一个方法，必须使用冒号 (:) 调用。]rw]

返回已净化的玩家名称。

**参数**

无。

**返回**

| 类型 | 描述 |
| ---- | ---- |
| `string` | 玩家名称。 |

**示例**

```lua
local name = player:get_name();
```

## get_pawn

[![方法][此字段是一个方法，必须使用冒号 (:) 调用。]rw]

返回附加到此控制器的 pawn。

**参数**

无。

**返回**

| 类型 | 描述 |
| ---- | ---- |
| [`cs2_player_pawn`](/api/entities/base-entity/cs2-player-pawn "此类型表示 C_CSPlayerPawn 类。") | Pawn 实例。 |

**示例**

```lua
local pawn = ctrl:get_pawn();
```

## get_active_weapon

[![方法][此字段是一个方法，必须使用冒号 (:) 调用。]rw]

返回当前的武器。

**参数**

无。

**返回**

| 类型 | 描述 |
| ---- | ---- |
| [`cs2_weapon_base_gun`](/api/entities/base-entity/cs2-weapon-base-gun "此类型表示 CCSWeaponBaseGun 类。") | 武器实例。 |

**示例**

```lua
local wep = player:get_active_weapon();
```

## get_observer_pawn

[![方法][此字段是一个方法，必须使用冒号 (:) 调用。]rw]

返回此控制器使用的观察者 pawn。

**参数**

无。

**返回**

| 类型 | 描述 |
| ---- | ---- |
| [`base_entity`](/api/entities/base-entity "此类型表示一个基础游戏实体。") | 实体。 |

**示例**

```lua
local obs_pawn = ctrl:get_observer_pawn();
```

## get_observer_target

[![方法][此字段是一个方法，必须使用冒号 (:) 调用。]rw]

返回此控制器当前观察的 pawn。

**参数**

无。

**返回**

| 类型 | 描述 |
| ---- | ---- |
| [`base_entity`](/api/entities/base-entity "此类型表示一个基础游戏实体。") | 实体。 |

**示例**

```lua
local obs = ctrl:get_observer_target();
```

## get_observer_mode

[![方法][此字段是一个方法，必须使用冒号 (:) 调用。]rw]

返回当前的观察者模式。

**参数**

无。

**返回**

| 类型 | 描述 |
| ---- | ---- |
| [`observer_mode_t`](/api/entities/observer-mode-t "此枚举表示游戏中可用的观察者模式。") | 观察者模式。 |

**示例**

```lua
local mode = ctrl:get_observer_mode();
```