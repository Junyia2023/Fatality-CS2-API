## cnet_chan

提供了一种与网络通道类接口的方法。

## get_address

[[字段]]

> 如果当前通道为 `null`，此函数将返回 `nil`。

返回远程机器的地址字符串。

**参数**

无。

**返回值**

| 类型 | 描述 |
| ---- | ----------- |
| `string?` | IP 地址或 Steam 服务器地址。 |

**示例**

```lua
local chan = game.engine:get_netchan();
if chan and not chan:is_null() then
    print(chan:get_address());
end
```

## is_loopback

[[字段]]

> 如果当前通道为 `null`，此函数将返回 `nil`。

返回当前通道是否连接到本地机器（回环地址）。

**参数**

无。

**返回值**

| 类型 | 描述 |
| ---- | ----------- |
| `bool?` | 如果连接到本地机器则为 `true`。 |

**示例**

```lua
local chan = game.engine:get_netchan();
if chan and not chan:is_null() and chan:is_loopback() then
    print('连接到 localhost！');
end
```

## is_null

[[字段]]

返回通道是否为空。

**参数**

无。

**返回值**

| 类型 | 描述 |
| ---- | ----------- |
| `bool` | 如果当前通道是虚拟通道则为 `true`。 |

**示例**

```lua
local chan = game.engine:get_netchan();
if not chan or chan:is_null() then
    print('未连接！');
end
```

## get_latency

[[字段]]

> 如果当前通道为 `null`，此函数将返回 `nil`。

返回当前到远程服务器的延迟（以秒为单位）。

**参数**

无。

**返回值**

| 类型 | 描述 |
| ---- | ----------- |
| `float?` | 延迟（以秒为单位）。 |

**示例**

```lua
local chan = game.engine:get_netchan();
if chan and not chan:is_null() then
    print('当前延迟: ' .. tostring(math.round(chan:get_latency() * 1000.0)) .. 'ms');
end
```
```