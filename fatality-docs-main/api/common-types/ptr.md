## ptr

此类型是一个字面意义上的指针。

为了保持与 C++ 的互操作性，某些函数返回 `void*` 类型，这些类型随后被转换为 `light_userdata`。由于你不能直接将 FFI 类型转换为 `light_userdata`，我们引入了一个专门的类型来帮助进行这种转换。

在将指针转换为 API 支持的类型之前，你需要将其强制转换为 `uintptr_t`。这可以通过以下方式完成：

```lua
local ptr_num = ffi.cast('uintptr_t', ptr_cdata);
```

然后，你可以使用这个转换后的值作为此类型的构造函数的参数。

## __call

[![Constructor][这是此类型的构造函数定义]rw]

将数字转换为指针。

**参数**

| 名称 | 类型 | 描述 |
| ---- | ---- | ----------- |
| `num` | `int` | 以数字形式表示的指针。 |

**返回值**

| 名称 | 描述 |
| ---- | ----------- |
| `ptr` | 以 `light_userdata` 形式表示的指针。 |

**示例**

```lua
-- 首先将指针转换为数字
local ptr_num = ffi.cast('uintptr_t', ptr_cdata);

-- 然后将数字转换为 light_userdata
local ptr_ld = ptr(ptr_num);
```

### 注意事项

- **必须先将指针转换为 `uintptr_t`**：这是因为 Lua 的 FFI（Foreign Function Interface）不支持直接将 C 指针转换为 `light_userdata`。
- **使用 `ptr` 类型的构造函数**：通过传递转换后的数字 (`uintptr_t`) 来创建一个新的 `ptr` 实例，该实例将以 `light_userdata` 的形式表示原始指针。