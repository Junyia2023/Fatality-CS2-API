## entity_entry_t

表示一个实体条目。

## entity

[![字段][此字段是一个常规字段，必须使用点 (.) 访问。]rw]

类型: `<type>`

实体实例。类型取决于您从中获取的列表。

## had_dataupdate

[![字段][此字段是一个常规字段，必须使用点 (.) 访问。]rw]

类型: `bool`

如果客户端至少一次接收到此实体的任何更新，则为 `true`。

## handle

[![字段][此字段是一个常规字段，必须使用点 (.) 访问。]rw]

类型: `chandle<type>`

实体的句柄。如果需要全局访问实体，您 **可以** 将其存储在其他地方。

## avatar

[![字段][此字段是一个常规字段，必须使用点 (.) 访问。]rw]

类型: `texture`

> 此字段仅在使用 `cs2_player_controller` 类型的条目中可用。

玩家的个人资料图片。如果尚未初始化，将为 `nil`。