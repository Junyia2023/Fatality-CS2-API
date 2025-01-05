## events_t

用法: `mods.events.{方法}`

此模块允许你管理自定义游戏内事件监听器。

> 请注意，游戏服务器**知道**你在监听哪些事件。内部而言，我们只监听那些无论如何都会发送给客户端的事件。如果你决定监听服务器通常不期望的事件，在官方服务器上**可能**会引起问题。

## add_listener

[[字段]]

将游戏事件添加到监听器。

> 内部我们监听以下事件：
> * `player_hurt`
> * `item_purchase`
> * `bullet_impact`
> * `weapon_fire`
> * `bomb_beginplant`
> * `bomb_abortplant`
> * `bomb_planted`
> * `bomb_defused`
> * `bomb_exploded`
> * `round_start`
> * `game_newmap`
> * `map_shutdown`
>
> 将这些事件添加到监听器是不必要的。

**参数**

| 名称 | 类型 | 描述 |
| ---- | ---- | ----------- |
| `name` | `string` | 事件名称。 |

**返回值**

无。

**示例**

```lua
mods.events:add_listener('round_end');