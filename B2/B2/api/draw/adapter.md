## adapter

此类型表示渲染系统中使用的渲染适配器。

## get_back_buffer

[![方法][此字段是方法，必须使用冒号 (:) 调用。]rw]

返回一个后缓冲区纹理。如果后缓冲区纹理未更新，则可能返回空白或过时的纹理。

**参数**

无。

**返回值**

| 类型 | 描述 |
| ---- | ----------- |
| [`ptr`](/api/common-types/ptr "此类型是一个指针。") | 后缓冲区纹理指针。 |

**示例**

```lua
local bb = adapter:get_back_buffer();
```

## get_back_buffer_downsampled

[![方法][此字段是方法，必须使用冒号 (:) 调用。]rw]

返回后缓冲区纹理的 4 倍降采样版本。

**参数**

无。

**返回值**

| 类型 | 描述 |
| ---- | ----------- |
| [`ptr`](/api/common-types/ptr "此类型是一个指针。") | 降采样后的后缓冲区纹理指针。 |

**示例**

```lua
local ds = adapter:get_back_buffer_downsampled();
```

## get_shared_texture

[![方法][此字段是方法，必须使用冒号 (:) 调用。]rw]

返回一个共享纹理。此纹理通常复制降采样后的后缓冲区纹理，尽管它在每一帧渲染开始前会自动更新一次。

**参数**

无。

**返回值**

| 类型 | 描述 |
| ---- | ----------- |
| [`ptr`](/api/common-types/ptr "此类型是一个指针。") | 共享纹理指针。 |

**示例**

```lua
local shared = adapter:get_shared_texture();
```