## cview_setup

描述视图设置参数。

## fov

[![Field][此字段是一个普通字段，必须使用点 (.) 访问]rw]

类型: `float`

当前视野（Field of View，FOV）。

## fov_viewmodel

[![Field][此字段是一个普通字段，必须使用点 (.) 访问]rw]

类型: `float`

当前视图模型的视野（FOV）。

## origin

[![Field][此字段是一个普通字段，必须使用点 (.) 访问]rw]

类型: `vector`

当前视图原点。

## view

[![Field][此字段是一个普通字段，必须使用点 (.) 访问]rw]

类型: `vector`

当前视图角度。

## aspect_ratio

[![Field][此字段是一个普通字段，必须使用点 (.) 访问]rw]

类型: `float`

当前视图的宽高比（宽度 / 高度）。


### 示例代码

```lua
-- 获取和设置视图参数的示例
local setup = cview_setup()

-- 获取当前视野
local current_fov = setup.fov

-- 设置新的视野
setup.fov = 90.0

-- 获取当前视图模型的视野
local viewmodel_fov = setup.fov_viewmodel

-- 获取当前视图原点
local origin = setup.origin

-- 获取当前视图角度
local view_angles = setup.view

-- 获取当前视图的宽高比
local aspect = setup.aspect_ratio
```

这些字段允许你访问和修改视图的各种参数，以实现更精细的控制和自定义。