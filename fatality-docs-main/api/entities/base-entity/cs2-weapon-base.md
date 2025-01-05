## cs2_weapon_base

此类型表示 `CCSWeaponBase` 实体。

> 此类型继承自 [`base_entity`](/api/entities/base-entity "此类型表示一个基础游戏实体。") 类型。它的所有基本方法和字段在此类型中也可用。

## get_abs_origin

[![方法][此字段是一个方法，必须使用冒号 (:) 调用。]rw]

返回绝对原点（用于渲染的原点）。

**参数**

无。

**返回**

| 类型 | 描述 |
| ---- | ---- |
| [`vector`](/api/common-types/vector "此类型是一个常见的3D向量 (x, y, z)。") | 原点。 |

**示例**

```lua
local org = wep:get_abs_origin();
```

## get_id

[![方法][此字段是一个方法，必须使用冒号 (:) 调用。]rw]

返回武器ID。

**参数**

无。

**返回**

| 类型 | 描述 |
| ---- | ---- |
| [`weapon_id`](/api/entities/weapon-id "此枚举表示游戏中各种武器的唯一标识符。") | 武器ID。 |

**示例**

```lua
local wep_id = wep:get_id();
```

## get_type

[![方法][此字段是一个方法，必须使用冒号 (:) 调用。]rw]

返回武器类型。

**参数**

无。

**返回**

| 类型 | 描述 |
| ---- | ---- |
| [`csweapon_type`](/api/entities/csweapon-type "此枚举表示游戏中的武器类型。") | 武器类型。 |

**示例**

```lua
local type = wep:get_type();
```

## get_data

[![方法][此字段是一个方法，必须使用冒号 (:) 调用。]rw]

返回武器静态数据。

**参数**

无。

**返回**

| 类型 | 描述 |
| ---- | ---- |
| [`ccsweapon_base_vdata`](/api/entities/ccsweapon-base-vdata "此类型表示武器的静态数据。") | 武器数据。 |

**示例**

```lua
local data = wep:get_data();
```