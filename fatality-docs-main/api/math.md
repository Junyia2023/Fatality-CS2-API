## math

用法：
`math.{func}`

此表扩展了 Lua 中现有的 `math` 表。

## calc_angle

[![Function][此字段是一个函数，必须使用点 (.) 调用]rw]

计算两个向量之间的角度。

**参数**

| 名称 | 类型 | 描述 |
| ---- | ---- | ----------- |
| `src` | [`vector`](/api/common-types/vector "此类型是一个常见的3D向量 (x, y, z)") | 源向量。 |
| `dst` | [`vector`](/api/common-types/vector "此类型是一个常见的3D向量 (x, y, z)") | 目标向量。 |

**返回值**

| 类型 | 描述 |
| ---- | ----------- |
| [`vector`](/api/common-types/vector "此类型是一个常见的3D向量 (x, y, z)") | 角度。 |

**示例**

```lua
local ang = math.calc_angle(vec1, vec2);
```

## angle_normalize

[![Function][此字段是一个函数，必须使用点 (.) 调用]rw]

归一化角度。

**参数**

| 名称 | 类型 | 描述 |
| ---- | ---- | ----------- |
| `angle` | `float` | 输入角度。 |

**返回值**

| 类型 | 描述 |
| ---- | ----------- |
| `float` | 归一化后的角度。 |

**示例**

```lua
local norm = math.angle_normalize(560);
```

## approach_angles

[![Function][此字段是一个函数，必须使用点 (.) 调用]rw]

在一段时间内接近一个角度。

**参数**

| 名称 | 类型 | 描述 |
| ---- | ---- | ----------- |
| `from` | [`vector`](/api/common-types/vector "此类型是一个常见的3D向量 (x, y, z)") | 起始角度。 |
| `to` | [`vector`](/api/common-types/vector "此类型是一个常见的3D向量 (x, y, z)") | 结束角度。 |
| `speed` | `float` | 接近速度。 |

**返回值**

| 类型 | 描述 |
| ---- | ----------- |
| [`vector`](/api/common-types/vector "此类型是一个常见的3D向量 (x, y, z)") | 角度差。 |

**示例**

```lua
local ang = math.approach_angles(from, to, 1.0 / game.global_vars.frametime);
```

## edge_point

[![Function][此字段是一个函数，必须使用点 (.) 调用]rw]

返回盒子边缘上的一个点。

**参数**

| 名称 | 类型 | 描述 |
| ---- | ---- | ----------- |
| `mins` | [`vector`](/api/common-types/vector "此类型是一个常见的3D向量 (x, y, z)") | 盒子最小值。 |
| `maxs` | [`vector`](/api/common-types/vector "此类型是一个常见的3D向量 (x, y, z)") | 盒子最大值。 |
| `dir` | [`vector`](/api/common-types/vector "此类型是一个常见的3D向量 (x, y, z)") | 点的方向（角度）。 |
| `radius` | `float` | 区域半径。 |

**返回值**

| 类型 | 描述 |
| ---- | ----------- |
| [`vector`](/api/common-types/vector "此类型是一个常见的3D向量 (x, y, z)") | 点。 |

**示例**

```lua
local point = math.edge_point(mins, maxs, dir, 5);
```

## lerp

[![Function][此字段是一个函数，必须使用点 (.) 调用]rw]

线性插值。

**参数**

| 名称 | 类型 | 描述 |
| ---- | ---- | ----------- |
| `t1` | `float` | 起始值。 |
| `t2` | `float` | 结束值。 |
| `progress` | `float` | 插值进度。 |

**返回值**

| 类型 | 描述 |
| ---- | ----------- |
| `float` | 插值后的值。 |

**示例**

```lua
local mid = math.lerp(0, 100, 0.5);
```

## vector_angles

[![Function][此字段是一个函数，必须使用点 (.) 调用]rw]

从向量计算角度。

**参数**

| 名称 | 类型 | 描述 |
| ---- | ---- | ----------- |
| `forward` | [`vector`](/api/common-types/vector "此类型是一个常见的3D向量 (x, y, z)") | 源向量。 |
| `up` | [`vector`](/api/common-types/vector "此类型是一个常见的3D向量 (x, y, z)") | 向上向量，默认为 `nil`。 |

**返回值**

| 类型 | 描述 |
| ---- | ----------- |
| [`vector`](/api/common-types/vector "此类型是一个常见的3D向量 (x, y, z)") | 角度。 |

**示例**

```lua
local ang = math.vector_angles(fw);
```

## world_to_screen

[![Function][此字段是一个函数，必须使用点 (.) 调用]rw]

将游戏世界中的一个点转换到视口上。

**参数**

| 名称 | 类型 | 描述 |
| ---- | ---- | ----------- |
| `xyz` | [`vector`](/api/common-types/vector "此类型是一个常见的3D向量 (x, y, z)") | 世界中的点。 |
| `round` | `bool` | 是否应该对输出进行四舍五入，默认为 `true`。 |

**返回值**

| 类型 | 描述 |
| ---- | ----------- |
| [`vec2`](/api/draw/common-types/vec2 "此类型是渲染系统中使用的2D向量") | 视口上的点。 |

**示例**

```lua
local point = math.world_to_screen(game_point);
```

## clamp

[![Function][此字段是一个函数，必须使用点 (.) 调用]rw]

将值限制在最小值和最大值之间。

**参数**

| 名称 | 类型 | 描述 |
| ---- | ---- | ----------- |
| `n` | `float` | 值。 |
| `lower` | `float` | 最小值。 |
| `upper` | `float` | 最大值。 |

**返回值**

| 类型 | 描述 |
| ---- | ----------- |
| `float` | 限制后的值。 |

**示例**

```lua
local x = math.clamp(50, 5, 25); -- 25
```

## remap_val

[![Function][此字段是一个函数，必须使用点 (.) 调用]rw]

将值从一个范围映射到另一个范围。

**参数**

| 名称 | 类型 | 描述 |
| ---- | ---- | ----------- |
| `val` | `float` | 值。 |
| `a` | `float` | 源范围的最小值。 |
| `b` | `float` | 源范围的最大值。 |
| `c` | `float` | 目标范围的最小值。 |
| `d` | `float` | 目标范围的最大值。 |

**返回值**

| 类型 | 描述 |
| ---- | ----------- |
| `float` | 映射后的值。 |

**示例**

```lua
local mapped = math.remap_val(0.5, 0, 1, 0, 100); -- 50
```

## remap_val_clamped

[![Function][此字段是一个函数，必须使用点 (.) 调用]rw]

将值从一个范围映射到另一个范围。此外，根据源范围对值进行限制。

**参数**

| 名称 | 类型 | 描述 |
| ---- | ---- | ----------- |
| `val` | `float` | 值。 |
| `a` | `float` | 源范围的最小值。 |
| `b` | `float` | 源范围的最大值。 |
| `c` | `float` | 目标范围的最小值。 |
| `d` | `float` | 目标范围的最大值。 |

**返回值**

| 类型 | 描述 |
| ---- | ----------- |
| `float` | 映射后的值。 |

**示例**

```lua
local mapped = math.remap_val_clamped(5, 0, 1, 0, 100); -- 100
```

## vec2

[![Function][此字段是一个函数，必须使用点 (.) 调用]rw]

[`draw.vec2()`](/api/draw/common-types/vec2#call "此类型是渲染系统中使用的2D向量") 的别名。

**示例**

```lua
local vec = math.vec2(5, 5);
```

## vec3

[![Function][此字段是一个函数，必须使用点 (.) 调用]rw]

[`vector()`](/api/common-types/vector#call "构造一个向量") 的别名。

**示例**

```lua
local vec = math.vec3(5, 12, 5);
```
```