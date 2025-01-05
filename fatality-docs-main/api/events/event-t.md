## event_t

事件用户类型。此类型的实例可以在 [`events`](/api/events "Fatality 提供了许多可以通过 API 使用的事件，从各种钩子到游戏内事件。每个事件条目都是 event_t 类型的对象。此表记录了脚本中要使用的事件。") 中找到。

## add

[![Method][此字段是一个方法，必须使用冒号 (:) 调用。]rw]

向事件添加回调函数。

**参数**

| 名称 | 类型 | 描述 |
| ---- | ---- | ----------- |
| `fn` | `function` | 回调函数。函数接受的参数由事件实例决定。 |

**返回值**

无。

**示例**

```lua
events.present_queue:add(function ()
    -- 每次游戏排队渲染帧时都会调用
end);
```

## remove

[![Method][此字段是一个方法，必须使用冒号 (:) 调用。]rw]

从事件中移除回调函数。

**参数**

| 名称 | 类型 | 描述 |
| ---- | ---- | ----------- |
| `fn` | `function` | 之前传递给 `add()` 函数的回调函数。 |

**返回值**

无。

**示例**

```lua
local function on_present()
    if some_condition then
        events.present_queue:remove(on_present)
    end
end

events.present_queue:add(on_present)
```
```