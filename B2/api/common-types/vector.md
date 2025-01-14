## vector

此类型表示一个常见的三维向量（x, y, z）。

> 此类型支持操作，如 `+`、`-`、`/`、`*` 和 `==`。

## x

[![字段][此字段是一个普通字段，必须使用点 (.) 访问]rw]

类型: `float`

X 坐标。

## y

[![字段][此字段是一个普通字段，必须使用点 (.) 访问]rw]

类型: `float`

Y 坐标。

## z

[![字段][此字段是一个普通字段，必须使用点 (.) 访问]rw]

类型: `float`

Z 坐标。

## __call

[![构造函数][这是此类型的构造函数定义]rw]

构造一个向量。

**参数**

*1. 默认向量 (0, 0, 0).* 

无参数。

*2. 单个值.*

| 名称 | 类型 | 描述 |
| ---- | ---- | ----------- |
| `value` | `float` | X、Y 和 Z 坐标。|

*3. XYZ 值.*

| 名称 | 类型 | 描述 |
| ---- | ---- | ----------- |
| `x` | `float` | X 坐标。|
| `y` | `float` | Y 坐标。|
| `z` | `float` | Z 坐标。|

**返回值**

| 类型 | 描述 |
| ---- | ----------- |
| `vector` | 向量。|

**示例**

```lua
local vec = vector(5, 25, 12);
```

## is_zero

[[字段]]

如果此向量在容差范围内，则返回 `true`。

**参数**

| 名称 | 类型 | 描述 |
| ---- | ---- | ----------- |
| `tolerance` | `float` | 最大允许的容差。默认值为 `0.01`。|

**返回值**

| 类型 | 描述 |
| ---- | ----------- |
| `bool` | 如果所有坐标值在 `-tolerance` 和 `tolerance` 之间，则返回 `true`。|

**示例**

```lua
local vec = vector(0, 0.1, 0.5);
print(tostring(vec:is_zero(1))); -- 将打印 'true'，因为每个值都在 -1 和 1 的范围内
```

## dist

[[字段]]

返回到另一个向量的距离。

**参数**

| 名称 | 类型 | 描述 |
| ---- | ---- | ----------- |
| `other` | `vector` | 计算距离的目标向量。|

**返回值**

| 类型 | 描述 |
| ---- | ----------- |
| `float` | 到另一个向量的距离。|

**示例**

```lua
local vec1 = vector(0, 0, 0);
local vec2 = vector(1, 1, 5);
print(tostring(vec1:dist(vec2)));
```

## dist_sqr

[[字段]]

返回到另一个向量的平方距离。

> 此方法实际上比非平方版本更快。如果您需要额外的性能，请使用它。

**参数**

| 名称 | 类型 | 描述 |
| ---- | ---- | ----------- |
| `other` | `vector` | 计算距离的目标向量。|

**返回值**

| 类型 | 描述 |
| ---- | ----------- |
| `float` | 到另一个向量的平方距离。|

**示例**

```lua
local vec1 = vector(0, 0, 0);
local vec2 = vector(1, 1, 5);
print(tostring(vec1:dist_sqr(vec2)));
```

## dist_2d

[[字段]]

返回到另一个向量的二维距离（仅计算 `x` 和 `y` 值）。

**参数**

| 名称 | 类型 | 描述 |
| ---- | ---- | ----------- |
| `other` | `vector` | 计算距离的目标向量。|

**返回值**

| 类型 | 描述 |
| ---- | ----------- |
| `float` | 到另一个向量的距离。|

**示例**

```lua
local vec1 = vector(0, 0, 0);
local vec2 = vector(1, 1, 5);
print(tostring(vec1:dist_2d(vec2)));
```

## dist_2d_sqr

[[字段]]

返回到另一个向量的平方二维距离（仅计算 `x` 和 `y` 值）。

> 此方法实际上比非平方版本更快。如果您需要额外的性能，请使用它。

**参数**

| 名称 | 类型 | 描述 |
| ---- | ---- | ----------- |
| `other` | `vector` | 计算距离的目标向量。|

**返回值**

| 类型 | 描述 |
| ---- | ----------- |
| `float` | 到另一个向量的平方距离。|

**示例**

```lua
local vec1 = vector(0, 0, 0);
local vec2 = vector(1, 1, 5);
print(tostring(vec1:dist_2d_sqr(vec2)));
```

## cross

[[字段]]

返回与另一个向量的叉积。

**参数**

| 名称 | 类型 | 描述 |
| ---- | ---- | ----------- |
| `other` | `vector` | 计算叉积的目标向量。|

**返回值**

| 类型 | 描述 |
| ---- | ----------- |
| `vector` | 叉积。|

**示例**

```lua
local vec1 = vector(0, 0, 0);
local vec2 = vector(1, 1, 5);
local cross = vec1:cross(vec2);
```

## is_valid

[[字段]]

如果此向量的所有值都是有限的，则返回 `true`。

**参数**

无。

**返回值**

| 类型 | 描述 |
| ---- | ----------- |
| `bool` | 如果所有值都是有限的，则返回 `true`。|

**示例**

```lua
local vec = vector(5, 1, 6);
if vec:is_valid() then
    -- ...
end
```

## length

[[字段]]

返回此向量的长度。

**参数**

无。

**返回值**

| 类型 | 描述 |
| ---- | ----------- |
| `float` | 此向量的长度。|

**示例**

```lua
local vec = vector(5, 1, 6);
local length = vec:length();
```

## length_sqr

[[字段]]

返回此向量的平方长度。

> 此方法实际上比非平方版本更快。如果您需要额外的性能，请使用它。

**参数**

无。

**返回值**

| 类型 | 描述 |
| ---- | ----------- |
| `float` | 此向量的平方长度。|

**示例**

```lua
local vec = vector(5, 1, 6);
local length = vec:length_sqr();
```

## length_2d

[[字段]]

返回此向量的二维长度（仅计算 `x` 和 `y` 值）。

**参数**

无。

**返回值**

| 类型 | 描述 |
| ---- | ----------- |
| `float` | 此向量的长度。|

**示例**

```lua
local vec = vector(5, 1, 6);
local length = vec:length_2d();
```

## length_2d_sqr

[[字段]]

返回此向量的平方二维长度（仅计算 `x` 和 `y` 值）。

> 此方法实际上比非平方版本更快。如果您需要额外的性能，请使用它。

**参数**

无。

**返回值**

| 类型 | 描述 |
| ---- | ----------- |
| `float` | 此向量的平方长度。|

**示例**

```lua
local vec = vector(5, 1, 6);
local length = vec:length_2d_sqr();
```

## dot

[[字段]]

返回两个向量的点积。

**参数**

| 名称 | 类型 | 描述 |
| ---- | ---- | ----------- |
| `other` | `vector` | 计算点积的目标向量。|

**返回值**

| 类型 | 描述 |
| ---- | ----------- |
| `float` | 点积。|

**示例**

```lua
local vec1 = vector(0, 0, 0);
local vec2 = vector(1, 1, 5);
local dot = vec1:dot(vec2);
```