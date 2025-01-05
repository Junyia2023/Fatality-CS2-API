## texture

此类型表示一个纹理对象。

> 此类型继承自 [`managed`](/api/draw/managed "此类型表示一个托管对象。你不能直接创建此类型的实例。") 类型。其所有基类方法和字段在此类型中同样可用。

> 支持的纹理格式包括：
> * JPEG (.jpg, .jpeg) - 不支持 12 bpc/算术编码
> * PNG (.png)
> * TGA (.tga)
> * BMP (.bmp) - 不支持 1 bpp 和 RLE 变体
> * PSD (.psd) - 仅支持合成视图，不支持额外通道，8/16 bpc
> * GIF (.gif) - 仅支持第一帧，对于动画 GIF，请使用 [`animated_texture`](/api/draw/managed/texture/animated-texture "此类型是动画纹理。此纹理类型仅支持 GIF 类型，不支持 APNG。")
> * HDR (.hdr)
> * PIC (.pic)
> * PNM (.pnm, .ppm, .pgm) - 仅支持二进制 PPM 和 PGM

## __call

[![构造函数][这是此类型的构造函数定义。]rw]

构造此类型的实例。

> 传递无效指针或内存区域小于所需大小将导致 **崩溃**。

**参数**

*1. 从文件加载：*

| 名称 | 类型 | 描述 |
| ---- | ---- | ----------- |
| `path` | `string` | 纹理文件的有效路径。 |

*2. 从内存加载：*

| 名称 | 类型 | 描述 |
| ---- | ---- | ----------- |
| `data` | [`ptr`](/api/common-types/ptr "此类型是一个指针。") | 指向内存中纹理 **文件** 数据的指针。 |
| `sz` | `int` | 纹理 **文件** 数据的大小。 |

*3. 从 RGBA 数据加载：*

| 名称 | 类型 | 描述 |
| ---- | ---- | ----------- |
| `data` | [`ptr`](/api/common-types/ptr "此类型是一个指针。") | 指向内存中 **RGBA** 数据的指针。 |
| `w` | `int` | 宽度。 |
| `h` | `int` | 高度（行数）。 |
| `p` | `int` | 行距（每行宽度）。这是每行的 **字节数**。 |

**返回值**

| 类型 | 描述 |
| ---- | ----------- |
| `texture` | 纹理对象。 |

**示例**

```lua
local tex = draw.texture('funny_meme.png');
```

## is_animated

[![字段][这是一个普通字段，必须使用点 (.) 访问。]rw]
[![Read Only][这是一个只读字段，无法更改其值。这不适用于任何子字段。]r]

**类型:** `bool`

如果这是 [`animated_texture`](/api/draw/managed/texture/animated-texture "此类型是动画纹理。此纹理类型仅支持 GIF 类型，不支持 APNG。") 的实例，则设置为 `true`。

## get_size

[![方法][此字段是方法，必须使用冒号 (:) 调用。]rw]

返回此纹理的尺寸。

**参数**

无。

**返回值**

| 类型 | 描述 |
| ---- | ----------- |
| [`vec2`](/api/draw/common-types/vec2 "此类型是渲染系统中使用的二维向量。") | 纹理尺寸。 |

**示例**

```lua
local sz = tex:get_size();
```