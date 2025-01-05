## font

此类型表示一个字体对象。内部使用 **FreeType** 库来栅格化字体字形。

> 此类型继承自 [`font_base`](/api/draw/managed/font-base "此类型表示字体类型的基类。你不能直接创建此类型的实例。请使用子类型。") 类型。其所有基类方法和字段在此类型中同样可用。

## __call

[![Constructor][这是此类型的构造函数定义。]rw]

构造一个字体对象。

> 传递无效指针或内存区域小于所需大小将导致 **崩溃**。

**参数**

*1. 从文件加载：*

| 名称 | 类型 | 描述 |
| ---- | ---- | ----------- |
| `path` | `string` | ttf/otf 文件的路径。 |
| `size` | `float` | 字体高度，以像素为单位。 |
| `fl` | [`font_flags`](/api/draw/managed/font-base/font-flags "此枚举确定字体对象应具备哪些标志。设置这些标志仅在类型构造期间可能。") | 字体标志。使用 `bit` 库构建它们。默认为 `0`。 |
| `mi` | `int` | 起始 codepoint。默认为 `0`。 |
| `ma` | `int` | 结束 codepoint。默认为 `255`（整个 ASCII 码页）。 |

*2. 从内存加载：*

| 名称 | 类型 | 描述 |
| ---- | ---- | ----------- |
| `mem` | [`ptr`](/api/common-types/ptr "此类型是一个指针。") | 指向内存中字体 **文件** 的指针。 |
| `sz` | `int` | 字体 **文件** 大小，以字节为单位。 |
| `size` | `float` | 字体高度，以像素为单位。 |
| `fl` | [`font_flags`](/api/draw/managed/font-base/font-flags "此枚举确定字体对象应具备哪些标志。设置这些标志仅在类型构造期间可能。") | 字体标志。使用 `bit` 库构建它们。默认为 `0`。 |
| `mi` | `int` | 起始 codepoint。默认为 `0`。 |
| `ma` | `int` | 结束 codepoint。默认为 `255`（整个 ASCII 码页）。 |

*3. 从内存加载，并带有 codepoint 对：*

| 名称 | 类型 | 描述 |
| ---- | ---- | ----------- |
| `mem` | [`ptr`](/api/common-types/ptr "此类型是一个指针。") | 指向内存中字体 **文件** 的指针。 |
| `sz` | `int` | 字体 **文件** 大小，以字节为单位。 |
| `size` | `float` | 字体高度，以像素为单位。 |
| `fl` | [`font_flags`](/api/draw/managed/font-base/font-flags "此枚举确定字体对象应具备哪些标志。设置这些标志仅在类型构造期间可能。") | 字体标志。使用 `bit` 库构建它们。默认为 `0`。 |
| `pairs` | `table[{int, int}...]` | 最小/最大对。这是一个由 {int, int} 对组成的标准数组。 |

**返回值**

| 类型 | 描述 |
| ---- | ----------- |
| `font` | 字体对象。 |

**示例**

```lua
local cool_font = draw.font('myfont.ttf', 16);
```