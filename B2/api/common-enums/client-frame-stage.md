## client_frame_stage

包含各种帧渲染阶段的键。

## undefined

[![字段][此字段是一个普通字段，必须使用点 (.) 访问]rw]

此阶段未定义。实际上，你不太可能收到这种类型的值。

## start

[![字段][此字段是一个普通字段，必须使用点 (.) 访问]rw]

帧构建过程开始。

## render_start

[![字段][此字段是一个普通字段，必须使用点 (.) 访问]rw]

帧渲染过程开始。

## net_update_start

[![字段][此字段是一个普通字段，必须使用点 (.) 访问]rw]

网络更新过程开始。

## net_update_preprocess

[![字段][此字段是一个普通字段，必须使用点 (.) 访问]rw]

引擎即将处理网络更新。

## net_pre_entity_packet

[![字段][此字段是一个普通字段，必须使用点 (.) 访问]rw]

游戏即将处理传入的实体数据包。

## net_update_postdataupdate_start

[![字段][此字段是一个普通字段，必须使用点 (.) 访问]rw]

实体信息即将被更新。

## net_update_postdataupdate_end

[![字段][此字段是一个普通字段，必须使用点 (.) 访问]rw]

实体信息更新即将完成。

## net_update_end

[![字段][此字段是一个普通字段，必须使用点 (.) 访问]rw]

网络更新过程结束。

## net_creation

[![字段][此字段是一个普通字段，必须使用点 (.) 访问]rw]

新实体即将被创建。

## render_end

[![字段][此字段是一个普通字段，必须使用点 (.) 访问]rw]

帧渲染过程结束。

### 示例说明

这些字段定义了客户端帧渲染的不同阶段，帮助你在代码中区分和处理各个渲染阶段的事件，例如：

- **start**：在帧构建开始时触发，可以用于初始化或准备数据。
- **render_start**：在帧渲染开始时触发，可以用于设置渲染参数。
- **net_update_start** 和 **net_update_end**：在网络更新开始和结束时触发，可以用于处理网络相关的逻辑。
- **render_end**：在帧渲染结束时触发，可以用于清理或后续处理。