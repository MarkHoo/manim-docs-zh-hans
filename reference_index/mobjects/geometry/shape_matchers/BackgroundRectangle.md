# 背景矩形

合格名称：`manim.mobject.geometry.shape\_matchers.BackgroundRectangle`

```py
class BackgroundRectangle(mobject, color=None, stroke_width=0, stroke_opacity=0, fill_opacity=0.75, buff=0, **kwargs)
```

Bases: `SurroundingRectangle`

背景矩形。它的默认颜色是场景的背景颜色。

例子

示例：示例背景矩形

![ExampleBackgroundRectangle-1.png](../static/ExampleBackgroundRectangle-1.png)


```py
from manim import *

class ExampleBackgroundRectangle(Scene):
    def construct(self):
        circle = Circle().shift(LEFT)
        circle.set_stroke(color=GREEN, width=20)
        triangle = Triangle().shift(2 * RIGHT)
        triangle.set_fill(PINK, opacity=0.5)
        backgroundRectangle1 = BackgroundRectangle(circle, color=WHITE, fill_opacity=0.15)
        backgroundRectangle2 = BackgroundRectangle(triangle, color=WHITE, fill_opacity=0.15)
        self.add(backgroundRectangle1)
        self.add(backgroundRectangle2)
        self.add(circle)
        self.add(triangle)
        self.play(Rotate(backgroundRectangle1, PI / 4))
        self.play(Rotate(backgroundRectangle2, PI / 2))
```


方法

|||
|-|-|
[`get_fill_color`]()|如果有多种颜色（对于渐变），则返回第一个颜色
[`pointwise_become_partial`]()|给定两个边界 a 和 b，将自身 vmobject 的点转换为相对于边界作为参数传递的 vmobject 的点。
`set_style`|


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


参数

- **color**（[_Colors_]()_|\_None_）–
- **stroke_width**（_float_）-
- **stroke_opacity**（_float_）-
- **fill_opacity** (_float_) –
- **buff**(_float_) –


`get_fill_color()`

如果有多种颜色（对于渐变），则返回第一个颜色

`pointwise_become_partial(mobject, a, b)`

给定两个边界 a 和 b，将自身 vmobject 的点转换为相对于边界作为参数传递的 vmobject 的点。这里的点代表贝塞尔曲线的控制点（锚点和手柄）

参数

- **vmobject** – 将用作模型的 vmobject。
- **a** — 上限。
- **b** – 下界

返回

`self`

返回类型

`VMobject`
