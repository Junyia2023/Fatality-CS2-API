## 添加用户界面 (UI)

现在您已经了解了基础知识，让我们通过允许用户切换文本的方式扩展脚本。我们可以通过向菜单中添加一个**控件**来实现这一点。

## 创建控件

让我们从创建一个简单的复选框开始：

```lua
local cb = gui.checkbox(gui.control_id('my_checkbox'));
```

每个控件都有一个**唯一ID**，UI框架使用它来区分容器内的控件。确保您的控件ID不与其他控件冲突非常重要，因为这可能会导致状态损坏或更严重的问题。

要创建ID，请调用[`gui.control_id`](/api/gui/common-types/control-id#call "构造ID结构体。")并传递所需的ID。

然后，通过调用[`gui.checkbox`](/api/gui/control/checkbox?id=__call "构造复选框。")并传递您创建的ID结构体来创建复选框。

## 构建行布局

默认情况下，控件通常放置在**行**中——以特定方式堆叠元素的布局。我们提供了一个简单的辅助函数——[`gui.make_control`](/api/gui?id=make_control "将控件包装成包含标签和该特定控件的布局。如果您希望控件显示得美观，应将其添加到分组中。此外，您可以向返回的控件添加任何额外的控件——这些控件将被堆叠到左侧...")。

```lua
local row = gui.make_control('我的复选框', cb);
```

## 将行布局添加到分组

准备好控件和行布局后，让我们将它们添加到分组中。

> 要查看分组和控件ID，您可以在SCRIPTS选项卡中启用**调试模式**。

在本例中，我们将使用`lua>elements a`分组。首先，在全局上下文中找到该分组：

```lua
local group = gui.ctx:find('lua>elements a');
```

然后调用其[`add`](/api/gui/container?id=add "将控件添加到容器中。")方法以包含您的行布局：

```lua
group:add(row);
```

就是这样！

## 使用控件值

接下来，让我们修改之前的脚本，使文本仅在复选框被选中时显示。将绘制代码包裹在一个`if`语句中，然后再渲染文本：

```lua
if cb:get_value():get() then
```

并在后面关闭它。

最终脚本应如下所示：

```lua
local cb = gui.checkbox(gui.control_id('my_checkbox'));
local row = gui.make_control('我的复选框', cb);
local group = gui.ctx:find('lua>elements a');
group:add(row);

local function on_present_queue()
    if cb:get_value():get() then
        local d = draw.surface;
        d.font = draw.fonts['gui_main'];
        d:add_text(draw.vec2(50, 50),
            'Hello drawing! My first script speaking.',
            draw.color.white()
        );
    end
end

events.present_queue:add(on_present_queue);
```