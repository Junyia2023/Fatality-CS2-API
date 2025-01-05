## 第一步

既然您已经了解了基础知识，是时候开始编写脚本了。

## 启动文本编辑器
您可以自由选择任何您喜欢的文本编辑器：[Visual Studio Code](https://code.visualstudio.com/)、[Notepad++](https://notepad-plus-plus.org/downloads/)，甚至是简单的记事本。

本地脚本位于以下路径：`<CS2_Directory>/game/csgo/fatality/scripts`。您可能会注意到还有一个 `lib` 目录，但我们会稍后再讨论它。

创建一个以 `.lua` 结尾的新文件，并开始编写您的脚本。

> `.ljbc` 格式无法从本地源加载。

## 编写第一个脚本

典型的“Hello world!”示例可能过于简单，因此我们尝试编写稍微复杂一点的内容。

```lua
local 函数 on_present_queue()
    local d = draw.surface;
    d.font = draw.fonts['gui_main'];
    d:add_text(draw.vec2(50, 50),
        'Hello drawing! My first script speaking.',
         draw.color.white()
    );
end

events.present_queue:add(on_present_queue);
```

现在，让我们分解这个示例脚本：

### 定义回调函数

大多数脚本将在我们提供的[多个回调](/api/events "Fatality 提供了许多可以在 API 中使用的事件 - 从各种钩子到游戏内事件。每个事件条目都是 event_t 对象。此表记录了脚本可以使用的事件。")中运行。每个事件都有其自己的**签名**，因此请注意回调函数应接受的参数。`present_queue` 不提供任何参数，因此我们的函数也不需要任何参数。

```lua
local 函数 on_present_queue()
end
```

> 定义局部变量是可选的，但建议这样做以更好地管理作用域。

### 访问绘图层

定义了回调函数后，让我们实际在屏幕上绘制一些东西！

为此，您首先需要访问[绘图层](/api/draw#surface "类型: layer")。我们提供了一个可以在**游戏线程**中安全使用的绘图层。由于游戏内部的工作方式，强烈不建议在其他线程中调用游戏函数。幸运的是，**我们所有的事件都在游戏线程中运行**。

这种设置不仅允许您绘制，还可以查询玩家生命值或其他实体的信息。

要访问该层，只需引用 `draw` 表中的 `surface` 字段：

```lua
local d = draw.surface;
```

> 您不必将其存储在变量中，但如果每次不需要输入 `draw.surface` 更好，对吧？

### 设置字体

检索到绘图层后，必须设置一个字体对象才能在屏幕上绘制任何文本。这纯粹是为了性能考虑，因此您不必每次绘制文本时都传递一个沉重的字体对象。

所有字体都存储在 [`draw.fonts`](## "类型: accessor<font_base>") 中。要访问字体，可以使用点语法或将其视为字典：

```lua
d.font = draw.fonts['gui_main'];
```

### 绘制文本

设置字体后，是时候绘制一些文本了。

在图层上调用 [`add_text`](## "添加文本。") 方法。请注意，它是使用冒号语法调用的：`obj:fn()`，因为这是一个**方法**。

> 您也可以使用点语法调用方法，只要提供对象作为第一个参数即可。两种调用：`obj:fn()` 和 `obj.fn(obj)` 是相同的。

```lua
d:add_text(draw.vec2(50, 50),
    'Hello drawing! My first script speaking brev.',
    draw.color.white()
);
```

### 注册回调

现在您已经创建了第一个回调，您需要注册它以便 Fatality 知道调用它。这是通过在 [`events.present_queue`](## "每当游戏排队渲染帧时调用。这是唯一允许在屏幕上绘制的位置。") 上调用 [`add`](## "向事件添加回调。") 方法完成的。

```lua
events.present_queue:add(on_present_queue);
```