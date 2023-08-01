# 背景矩形

合格名称：`manim.mobject.geometry.shape\_matchers.BackgroundRectangle`

_类_ BackgroundRectangle（_mobject_，_颜色=无_，_描边宽度= 0_，_描边不透明度= 0_，_填充不透明度= 0.75_，_缓冲= 0_， _\*\* kwargs_）

基地：[`SurroundingRectangle`]()

背景矩形。它的默认颜色是场景的背景颜色。

例子

示例：示例背景矩形

![ExampleBackgroundRectangle-1.png](../static/ExampleBackgroundRectangle-1.png)


```py

```


方法

[`get_fill_color`]()
如果有多种颜色（对于渐变），则返回第一个颜色
[`pointwise_become_partial`]()
给定两个边界 a 和 b，将自身 vmobject 的点转换为相对于边界作为参数传递的 vmobject 的点。
`set_style`


属性


`animate`
用于对 的任何方法的应用程序进行动画处理`self`。
`animation_overrides`
`color`
`depth`
对象的深度。
`fill_color`
如果有多种颜色（对于渐变），则返回第一个颜色
`height`
mobject 的高度。
`n_points_per_curve`
`sheen_factor`
`stroke_color`
`width`
mobject 的宽度。


参数

- **颜色**（[_颜色_]()_|\_\_无_）–
- **笔画宽度**（_浮动_）-
- **描边不透明度**（_浮动_）-
- **fill_opacity** (_浮动_) –
- **增益**(_浮动_) –

获取填充颜色( )

如果有多种颜色（对于渐变），则返回第一个颜色

pointwise*become_partial ( \_mobject* , _a_ , _b_ )

给定两个边界 a 和 b，将自身 vmobject 的点转换为相对于边界作为参数传递的 vmobject 的点。这里的点代表贝塞尔曲线的控制点（锚点和手柄）

参数

- **vmobject** – 将用作模型的 vmobject。
- **a——**上限。
- **b** – 下界

退货

`self`

返回类型

`VMobject`
