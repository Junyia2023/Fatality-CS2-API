## entity_list_t

此类型表示一个实体列表。

> 永远不要保存从这个列表中获取的任何实体，除非你知道自己在做什么！否则你可能会留下悬空指针，这将不可避免地导致崩溃。

## for_each

[![方法][此字段是一个方法，必须使用冒号 (:) 调用。]rw]

遍历实体。

**参数**

| 名称 | 类型 | 描述 |
| ---- | ---- | ----------- |
| `fn` | `function(entity_entry_t)` | 回调函数。 |

无返回值

**示例**

```lua
entities.players:for_each(function (entry)
    -- ...
end);
```

## for_each_z

[![方法][此字段是一个方法，必须使用冒号 (:) 调用。]rw]

以相反顺序遍历实体。

**参数**

| 名称 | 类型 | 描述 |
| ---- | ---- | ----------- |
| `fn` | `function(entity_entry_t)` | 回调函数。 |

无返回值

**示例**

```lua
entities.players:for_each_z(function (entry)
    -- ...
end);
```
``` 