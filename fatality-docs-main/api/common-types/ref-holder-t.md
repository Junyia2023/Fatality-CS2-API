## ref_holder_t

此类型作为内部使用的引用变量的代理。由于 Lua 是一个**仅值传递**的语言，不支持引用。因此，使用此类型的实例来保持与 C++ 的互操作性。

> 注意，`<type>` 表示此实例持有的具体类型。例如，如果您看到 `ref_holder_t<float>`，这意味着 `val` 字段持有一个浮点数（float）值，并且在更新时**仅接受**浮点数值。

## val

[![Field][此字段是一个普通字段，必须使用点 (.) 访问]rw]

类型: `<type>`

值持有者。可以用作源值，或者覆盖它以更改内部值。

### 示例

```lua
-- 假设我们有一个 ref_holder_t<float> 实例
local holder = ref_holder_t<float>()

-- 获取当前值
local currentValue = holder.val

-- 设置新值
holder.val = 3.14
```

这个结构允许你在 Lua 中模拟 C++ 的引用行为，确保在需要引用语义的地方可以正确地操作和传递数据。