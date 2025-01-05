## draw

用法：`draw.{func_or_字段}`

此表描述了软件的渲染系统。

> 所有在子部分中描述的类型和枚举**必须**以 `draw.` 为前缀。这样做是为了避免特定类型与其他类型混淆，例如渲染和游戏中存在的不同 `color` 类型。

## adapter

[[字段]]
[![只读][此字段是只读字段，无法更改其值。这不适用于任何子字段（如果有）。]r]

类型：`adapter`

渲染适配器。

## frame_time

[[字段]]
[![只读][此字段是只读字段，无法更改其值。这不适用于任何子字段（如果有）。]r]

类型：`float`

渲染帧时间。它是 [`global_vars_t.frame_time`](/api/game/global-vars-t?id=frame_time "类型：float") 的别名。

## time

[[字段]]
[![只读][此字段是只读字段，无法更改其值。这不适用于任何子字段（如果有）。]r]

类型：`float`

时间，以秒为单位。它是 [`global_vars_t.real_time`](/api/game/global-vars-t?id=real_time "类型：float") 的别名。

## scale

[[字段]]
[![只读][此字段是只读字段，无法更改其值。这不适用于任何子字段（如果有）。]r]

类型：`float`

全局 DPI 缩放比例。

## display

[[字段]]
[![只读][此字段是只读字段，无法更改其值。这不适用于任何子字段（如果有）。]r]

类型：[`vec2`](/api/draw/common-types/vec2 "此类型是在渲染系统中使用的二维向量。")

显示区域大小（视口尺寸）。[`cengine_client:get_screen_size`](/api/game/cengine-client?id=get_screen_size "返回客户端窗口屏幕尺寸。") 将返回完全相同的值。覆盖此向量的任何值将导致未定义行为。

## textures

[[字段]]
[![只读][此字段是只读字段，无法更改其值。这不适用于任何子字段（如果有）。]r]

类型：[`accessor<texture>`](/api/draw/common-types/accessor "此类型表示一种安全访问映射的方式。")

所有托管纹理的字符串到 [`texture`](/api/draw/managed/texture "此类型表示一个纹理对象。") 映射。您可以使用自定义 ID 查询和推送纹理。当您将纹理添加到此映射时，它将在需要时自动销毁并重新创建（例如，当 DX11 设备丢失时）。

> 内置纹理：
> * `gui_loading`：加载动画
> * `gui_user_avatar`：当前用户的头像。如果没有设置头像，则可能为 nil
> * `gui_icon_up`：向上箭头
> * `gui_icon_down`：向下箭头
> * `gui_icon_copy`：复制图标
> * `gui_icon_paste`：粘贴图标
> * `gui_icon_add`：添加图标
> * `gui_icon_search`：搜索图标
> * `gui_icon_settings`：设置图标（齿轮）
> * `gui_icon_bug`：错误图标
> * `gui_icon_key`.N：键盘/鼠标键图标。将 N 替换为所需按钮的字符代码
> * `icon_rage`：RAGE 标签图标
> * `icon_legit`：LEGIT 标签图标
> * `icon_visuals`：VISUALS 标签图标
> * `icon_misc`：MISC 标签图标
> * `icon_scripts`：LUA 标签图标
> * `icon_skins`：SKINS 标签图标
> * `icon_cloud`：云图标
> * `icon_file`：文件图标
> * `icon_refresh`：刷新图标
> * `icon_save`：保存图标
> * `icon_configs`："配置"弹出窗口图标
> * `icon_keys`：键盘图标
> * `icon_info`："关于"弹出窗口图标
> * `icon_close`：关闭图标（叉号）
> * `icon_load`：加载图标
> * `icon_import`：导入图标
> * `icon_export`：导出图标
> * `icon_delete`：删除图标
> * `icon_autoload`："自动加载"图标
> * `icon_allow_insecure`："允许不安全"图标
> * `icon_cloud_upd`：云更新图标
> * `player_texture`：玩家预览纹理

## fonts

[[字段]]
[![只读][此字段是只读字段，无法更改其值。这不适用于任何子字段（如果有）。]r]

类型：[`accessor<font_base>`](/api/draw/common-types/accessor "此类型表示一种安全访问映射的方式。")

所有托管字体的字符串到 [`font_base`](/api/draw/managed/font-base "此类型是字体类型的基类。您不能创建此类的实例。而是使用子类型。") 映射。您可以使用自定义 ID 查询和推送字体。当您将字体添加到此映射时，它将在需要时自动销毁并重新创建（例如，当 DX11 设备丢失时）。

> 内置字体：
> * `gui_debug`：Verdana, 13px
> * `gui_title`：Figtree ExtraBold, 23px
> * `gui_main`：Figtree Medium, 14px
> * `gui_main_shadow`：Figree Medium, 14px，带阴影
> * `gui_main_fb`：Segoe UI Semibold, 14px
> * `gui_bold`：Figtree ExtraBold, 14px
> * `gui_bold_fb`：Segoe UI Black, 14px
> * `gui_semi_bold`：Figtree SemiBold, 14px
> * `gui_semi_bold_fb`：Segoe UI Bold, 14px

## shaders

[[字段]]
[![只读][此字段是只读字段，无法更改其值。这不适用于任何子字段（如果有）。]r]

类型：[`accessor<shader>`](/api/draw/common-types/accessor "此类型表示一种安全访问映射的方式。")

所有托管着色器的字符串到 [`shader`](/api/draw/managed/shader "此类型表示一个着色器。HLSL 文档") 映射。您可以使用自定义 ID 查询和推送着色器。当您将着色器添加到此映射时，它将在需要时自动销毁并重新创建（例如，当 DX11 设备丢失时）。

> 内置着色器：
> * `blur_f`：高斯模糊着色器

## surface

[[字段]]
[![只读][此字段是只读字段，无法更改其值。这不适用于任何子字段（如果有）。]r]

类型：[`layer`](/api/draw/layer "层是一种用于存储渲染命令、顶点和索引数据的类型。这是推送形状和控制渲染状态的唯一方法。")

可以渲染的图层。
```