# VMobjectFromSVGPath 

合格名称：`manim.mobject.svg.svg\_mobject.VMobjectFromSVGPath`


```py
class VMobjectFromSVGPath(path_obj, long_lines=False, should_subdivide_sharp_curves=False, should_remove_null_curves=False, **kwargs)
```

Bases: `VMobject`

表示 SVG 路径的矢量化 mobject。

> 笔记

> `long_lines`、` should_subdivide_sharp_curves`、`should_remove_null_curves ` 关键字参数仅适用于 OpenGL 渲染器

参数

- **path_obj** ( _se.Path_ ) – 已解析的 SVG 路径对象。
- **long_lines** ( _bool_ ) – 矢量化对象中的直线是否以一段或两段绘制。
- **should_subdivide_sharp_curves** ( _bool_ ) – 如果两条线段以比给定阈值更尖锐的角度相交，是否进一步细分子曲线。
- **should_remove_null_curves** ( _bool_ ) – 是否删除长度为 0 的子曲线。
- **kwargs** – 更多关键字参数传递给父类。

方法

|||
|-|-|
[`generate_points`]()|初始化`points`并因此初始化形状。
`handle_commands`|
`init_points`|

属性

|||
|-|-|
`animate`|用于对 的任何方法的应用程序进行动画处理`self`。
`animation_overrides`|
`color`|
`depth`|对象的深度。
`fill_color`|如果有多种颜色（对于渐变），则返回第一个颜色
`height`|mobject 的高度。
`n_points_per_curve`|
`sheen_factor`|
`stroke_color`|
`width`|mobject 的宽度。


`generate_points()`

初始化`points`并因此初始化形状。

在创造时被调用。这是一个空方法，可以由子类实现。

返回类型

None
