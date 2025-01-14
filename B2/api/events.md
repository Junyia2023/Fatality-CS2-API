## events

用法：`events.{event_name}`

Fatality 在 API 中提供了许多事件，从各种钩子到游戏内事件。每个事件条目都是 [`event_t`](/api/events/event-t "事件用户类型。此类型的实例可以在 events 中找到。") 类型的对象。本表记录了脚本中可使用的事件。

> 当你的脚本卸载时，无需手动移除事件。API 引擎会自动处理。

## present_queue

[[字段]]

每次游戏将帧排队进行渲染时调用。这是唯一允许在屏幕上绘制的合法位置。

**参数**

无。

## frame_stage_notify

[[字段]]

每当游戏进入另一个帧阶段时调用。此事件在游戏处理新帧阶段之前触发。

**参数**

| 名称 | 类型 | 描述 |
| ---- | ---- | ----------- |
| `stage` | [`client_frame_stage`](/api/common-enums/client-frame-stage "包含各种帧渲染阶段的键。") | 当前帧阶段。 |

## render_start_pre

[[字段]]

每当游戏开始场景渲染过程时调用。此事件在游戏函数运行之前触发。

**参数**

无。

## render_start_post

[[字段]]

每当游戏开始场景渲染过程时调用。此事件在游戏函数运行之后触发。

**参数**

| 名称 | 类型 | 描述 |
| ---- | ---- | ----------- |
| `setup` | [`cview_setup`](/api/common-types/cview-setup "描述视图设置参数。") | 视图设置信息。 |

## setup_view_pre

[[字段]]

每当游戏设置视图时调用。此事件在游戏函数运行之前触发。

**参数**

无。

## setup_view_post

[[字段]]

每当游戏设置视图信息时调用。此事件在游戏函数运行之后触发。

> 你可以从 `game.view_render` 服务中获取视图信息。

**参数**

无。

## override_view

[[字段]]

每当游戏内部覆盖视图信息时调用。你可以自由更改提供的视图设置中的任何内容。

**参数**

| 名称 | 类型 | 描述 |
| ---- | ---- | ----------- |
| `setup` | [`cview_setup`](/api/common-types/cview-setup "描述视图设置参数。") | 视图设置信息。 |

## event

[[字段]]

每当游戏事件触发时调用。

> 我们不会监听游戏中存在的每一个事件。如果你需要监听我们未监听的事件，请使用 [`mods.events`](/api/events/event-t "此模块允许你管理自定义游戏内事件监听器。")

| 名称 | 类型 | 描述 |
| ---- | ---- | ----------- |
| `event` | [`game_event_t`](/api/common-types/game-event-t "描述一个游戏事件。") | 游戏事件。 |

## handle_input

[[字段]]

每当游戏处理鼠标/控制器输入时调用。如果需要，这是一个修改鼠标移动的好地方。

**参数**

| 名称 | 类型 | 描述 |
| ---- | ---- | ----------- |
| `type` | [`input_type_t`](/api/common-enums/input-type-t "包含值输入选项的键。") | 输入类型。 |
| `value` | [`ref_holder_t<float>`](/api/common-types/ref-holder-t "此类型作为内部使用的引用变量的代理。由于 Lua 是仅值语言，不支持引用。因此，使用此类型的实例以保持与 C++ 的互操作性。") | 输入值。 |