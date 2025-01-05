## cengine_client

用法：`game.engine.{方法}`

此类型的实例提供了一种与Source 2的引擎到客户端服务接口的方法。

## get_last_timestamp

[[字段]]

返回最后的时间戳，以秒为单位。

**参数**

无。

**返回值**

| 类型 | 描述 |
| ---- | ----------- |
| `float` | 时间戳，以秒为单位。 |

**示例**

```lua
local last_time = game.engine:get_last_timestamp();
```

## get_last_server_tick

[[字段]]

返回最后的服务器tick编号。

**参数**

无。

**返回值**

| 类型 | 描述 |
| ---- | ----------- |
| `int` | 服务器tick编号。 |

**示例**

```lua
local server_tick = game.engine:get_last_server_tick();
```

## in_game

[[字段]]

返回客户端当前是否在游戏中。

**参数**

无。

**返回值**

| 类型 | 描述 |
| ---- | ----------- |
| `bool` | 游戏状态。 |

**示例**

```lua
if game.engine:in_game() then
    print("我在游戏中！");
end
```

## is_connected

[[字段]]

返回客户端当前是否连接到游戏服务器。

**参数**

无。

**返回值**

| 类型 | 描述 |
| ---- | ----------- |
| `bool` | 如果已连接则为`true`。 |

**示例**

```lua
if game.engine:is_connected() then
    print("我已连接！");
end
```

## get_netchan

[[字段]]

返回用于网络通信的网络通道。

**参数**

无。

**返回值**

| 类型 | 描述 |
| ---- | ----------- |
| [`cnet_chan`](/api/game/cengine-client/cnet-chan "提供一种与网络通道类接口的方法") | 网络通道，如果不存在则返回`nil`。 |

**示例**

```lua
local chan = game.engine:get_netchan();
```

## client_cmd

[[字段]]

执行客户端控制台命令。

**参数**

| 名称 | 类型 | 描述 |
| ---- | ---- | ----------- |
| `cmd` | `string` | 要执行的命令。 |
| `bool` | `unrestricted` | 是否应保留任何限制进行执行。默认为`false`。 |

**返回值**

无。

**示例**

```lua
game.engine:client_cmd('say Hello!');
```

## get_screen_size

[[字段]]

返回客户端窗口屏幕尺寸。

**参数**

无。

**返回值**

| 类型 | 描述 |
| ---- | ----------- |
| `int` | 宽度。 |
| `int` | 高度。 |

**示例**

```lua
local w, h = game.engine:get_screen_size();
```
```