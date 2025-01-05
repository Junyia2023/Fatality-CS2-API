## text_params

此类型用于确定文本对齐方式。

> 行对齐仅在文本有多行时才有意义。默认情况下，所有下一行将从文本的左侧开始。您可以通过使用带有 `line` 参数的函数来更改此行为。例如，如果您将 `right` 传递给行对齐，则所有下一行将从右侧开始。文本对齐方式将根据 `v` 和 `h` 参数进行设置。

## with_v

[![Function][此字段是一个函数，必须使用点 (.) 调用]rw]

创建具有垂直对齐方式的 `text_params` 实例。

**参数**

| 名称 | 类型 | 描述 |
| ---- | ---- | ----------- |
| `v` | [`text_alignment`](/api/draw/layer/text-params/text-alignment "此枚举确定绘制文本时如何对齐文本。") | 垂直对齐方式。 |

**返回值**

| 类型 | 描述 |
| ---- | ----------- |
| `text_params` | 创建的文本参数。 |

**示例**

```lua
local align_top = draw.text_params.with_v(draw.text_alignment.top);
```

## with_h

[![Function][此字段是一个函数，必须使用点 (.) 调用]rw]

创建具有水平对齐方式的 `text_params` 实例。

**参数**

| 名称 | 类型 | 描述 |
| ---- | ---- | ----------- |
| `h` | [`text_alignment`](/api/draw/layer/text-params/text-alignment "此枚举确定绘制文本时如何对齐文本。") | 水平对齐方式。 |

**返回值**

| 类型 | 描述 |
| ---- | ----------- |
| `text_params` | 创建的文本参数。 |

**示例**

```lua
local align_right = draw.text_params.with_h(draw.text_alignment.right);
```

## with_line

[![Function][此字段是一个函数，必须使用点 (.) 调用]rw]

创建具有行对齐方式的 `text_params` 实例。

**参数**

| 名称 | 类型 | 描述 |
| ---- | ---- | ----------- |
| `line` | [`text_alignment`](/api/draw/layer/text-params/text-alignment "此枚举确定绘制文本时如何对齐文本。") | 行对齐方式。 |

**返回值**

| 类型 | 描述 |
| ---- | ----------- |
| `text_params` | 创建的文本参数。 |

**示例**

```lua
local lines_center = draw.text_params.with_line(draw.text_alignment.center);
```

## with_vh

[![Function][此字段是一个函数，必须使用点 (.) 调用]rw]

创建具有垂直和水平对齐方式的 `text_params` 实例。

**参数**

| 名称 | 类型 | 描述 |
| ---- | ---- | ----------- |
| `v` | [`text_alignment`](/api/draw/layer/text-params/text-alignment "此枚举确定绘制文本时如何对齐文本。") | 垂直对齐方式。 |
| `h` | [`text_alignment`](/api/draw/layer/text-params/text-alignment "此枚举确定绘制文本时如何对齐文本。") | 水平对齐方式。 |

**返回值**

| 类型 | 描述 |
| ---- | ----------- |
| `text_params` | 创建的文本参数。 |

**示例**

```lua
local align_bottom_right = draw.text_params.with_vh(draw.text_alignment.bottom, draw.text_alignment.right);
```

## with_vline

[![Function][此字段是一个函数，必须使用点 (.) 调用]rw]

创建具有垂直和行对齐方式的 `text_params` 实例。

**参数**

| 名称 | 类型 | 描述 |
| ---- | ---- | ----------- |
| `v` | [`text_alignment`](/api/draw/layer/text-params/text-alignment "此枚举确定绘制文本时如何对齐文本。") | 垂直对齐方式。 |
| `line` | [`text_alignment`](/api/draw/layer/text-params/text-alignment "此枚举确定绘制文本时如何对齐文本。") | 行对齐方式。 |

**返回值**

| 类型 | 描述 |
| ---- | ----------- |
| `text_params` | 创建的文本参数。 |

**示例**

```lua
local align = draw.text_params.with_vline(draw.text_alignment.bottom, draw.text_alignment.center);
```

## with_hline

[![Function][此字段是一个函数，必须使用点 (.) 调用]rw]

创建具有水平和行对齐方式的 `text_params` 实例。

**参数**

| 名称 | 类型 | 描述 |
| ---- | ---- | ----------- |
| `h` | [`text_alignment`](/api/draw/layer/text-params/text-alignment "此枚举确定绘制文本时如何对齐文本。") | 水平对齐方式。 |
| `line` | [`text_alignment`](/api/draw/layer/text-params/text-alignment "此枚举确定绘制文本时如何对齐文本。") | 行对齐方式。 |

**返回值**

| 类型 | 描述 |
| ---- | ----------- |
| `text_params` | 创建的文本参数。 |

**示例**

```lua
local align = draw.text_params.with_hline(draw.text_alignment.center, draw.text_alignment.center);
```

## with_vhline

[![Function][此字段是一个函数，必须使用点 (.) 调用]rw]

创建具有垂直、水平和行对齐方式的 `text_params` 实例。

**参数**

| 名称 | 类型 | 描述 |
| ---- | ---- | ----------- |
| `v` | [`text_alignment`](/api/draw/layer/text-params/text-alignment "此枚举确定绘制文本时如何对齐文本。") | 垂直对齐方式。 |
| `h` | [`text_alignment`](/api/draw/layer/text-params/text-alignment "此枚举确定绘制文本时如何对齐文本。") | 水平对齐方式。 |
| `line` | [`text_alignment`](/api/draw/layer/text-params/text-alignment "此枚举确定绘制文本时如何对齐文本。") | 行对齐方式。 |

**返回值**

| 类型 | 描述 |
| ---- | ----------- |
| `text_params` | 创建的文本参数。 |

**示例**

```lua
local align = draw.text_params.with_vhline(draw.text_alignment.center, draw.text_alignment.center);
```