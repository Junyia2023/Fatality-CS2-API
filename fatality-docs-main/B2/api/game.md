## game

用法：`game.{interface_or_函数}`

此表暴露了Fatality使用的各种内部服务和全局对象，并提供了获取任何其他所需服务的方法。

## global_vars

[[字段]]

类型：[`global_vars_t`](/api/game/global-vars-t "此类型的实例提供了一种读取游戏中使用的多个全局变量的方法。修改其中的任何值都不被支持，也永远不会被支持。")

此服务暴露了游戏中使用的全局变量，例如帧时间或当前服务器时间。

## engine

[[字段]]

类型：[`cengine_client`](/api/game/cengine-client "此类型的实例提供了一种与Source 2的引擎到客户端服务接口的方法。")

此服务暴露了引擎客户端，其中包括常用的引擎相关函数。