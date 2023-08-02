# 三角形

合格名称：`manim.mobject.geometry.polygram.Triangle`

```py
class Triangle(**kwargs)
```

Bases: `RegularPolygon`

一个等边三角形。

参数

**kwargs** – 要传递给的附加参数[`RegularPolygon`]()

例子

示例：三角形示例

![TriangleExample-1.png](../static/TriangleExample-1.png)


```py
from manim import *

class TriangleExample(Scene):
    def construct(self):
        triangle_1 = Triangle()
        triangle_2 = Triangle().scale(2).rotate(60*DEGREES)
        tri_group = Group(triangle_1, triangle_2).arrange(buff=1)
        self.add(tri_group)
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
