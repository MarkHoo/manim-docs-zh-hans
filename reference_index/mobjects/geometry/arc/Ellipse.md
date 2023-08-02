# 椭圆

合格名称：`manim.mobject.geometry.arc.Ellipse`

```py
class Ellipse(width=2, height=1, **kwargs)
```

Bases: Circle

圆形；椭圆形、圆形。

参数

- **width** ( _float_ ) – 椭圆的水平宽度。
- **height** ( _float_ ) – 椭圆的垂直高度。
- **kwargs** – 要传递给 的附加参数[`Circle`]()。

例子

示例：椭圆示例

![EllipseExample-1.png](../static/EllipseExample-1.png)

```py
from manim import *

class EllipseExample(Scene):
    def construct(self):
        ellipse_1 = Ellipse(width=2.0, height=4.0, color=BLUE_B)
        ellipse_2 = Ellipse(width=4.0, height=1.0, color=BLUE_D)
        ellipse_group = Group(ellipse_1,ellipse_2).arrange(buff=1)
        self.add(ellipse_group)
```

方法



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
