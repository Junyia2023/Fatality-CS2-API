## 实体

此表表示内部实体列表。

> 请勿在全局范围内存储任何实体！任何实体都可能被删除，您将不再拥有该实体的有效实例，这将不可避免地导致崩溃。如果您需要在某处全局存储实体，我们强烈建议您存储一个[`chandle`](/api/entities/chandle "此类型表示实体句柄")的实例，并使用其[`get`](/api/entities/chandle?id=get "返回实体，或如果未找到则返回nil。")方法在需要时检索实体。

## 玩家

[[字段]]

类型：[`entity_list_t<cs2_player_pawn>`](/api/entities/entity-list-t "此类型表示实体列表。")

玩家角色。

## 控制器

[[字段]]

类型：[`entity_list_t<cs2_player_controller>`](/api/entities/entity-list-t "此类型表示实体列表。")

玩家控制器。

## 物品

[[字段]]

类型：[`entity_list_t<cs2_weapon_base>`](/api/entities/entity-list-t "此类型表示实体列表。")

持有的物品。

## 掉落物品

[[字段]]

类型：[`entity_list_t<cs2_weapon_base>`](/api/entities/entity-list-t "此类型表示实体列表。")

掉落的物品。

## 投射物

[[字段]]

类型：[`entity_list_t<cs2_grenade_projectile>`](/api/entities/entity-list-t "此类型表示实体列表。")

手榴弹投射物。

## 获取本地玩家的角色

[![函数][这是一个普通函数，必须使用点 (.) 调用。]rw]

返回本地玩家的角色。

**参数**

无。

**返回值**

| 类型 | 描述 |
| ---- | ----------- |
| [`cs2_player_pawn`](/api/entities/base-entity/cs2-player-pawn "此类型表示C_CSPlayerPawn类。") | 角色。 |

**示例**

```lua
local lp = entities.get_local_pawn();
```

## 获取本地玩家的控制器

[![函数][这是一个普通函数，必须使用点 (.) 调用。]rw]

返回本地玩家的控制器。

**参数**

无。

**返回值**

| 类型 | 描述 |
| ---- | ----------- |
| [`cs2_player_controller`](/api/entities/base-entity/cs2-player-controller "此类型表示CCSPlayerController类") | 控制器。 |

**示例**

```lua
local lp_ctrl = entities.get_local_controller();
```
``` 
