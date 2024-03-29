# 多边形

合格名称：`manim.mobject.geometry.polygram.Polygon`

```py
class Polygon(*vertices, **kwargs)
```

Bases: `Polygram`

一种由一个闭环顶点组成的形状。

参数

- **vertices** ( _Sequence_ _\[_ _float_ _\]_ ) – 的顶点[`Polygon`]()。
- **kwargs** – 转发到父构造函数。

例子

示例：多边形示例

![PolygonExample-1.png](../../static/PolygonExample-1.png)


```py
from manim import *

class PolygonExample(Scene):
    def construct(self):
        isosceles = Polygon([-5, 1.5, 0], [-2, 1.5, 0], [-3.5, -2, 0])
        position_list = [
            [4, 1, 0],  # middle right
            [4, -2.5, 0],  # bottom right
            [0, -2.5, 0],  # bottom left
            [0, 3, 0],  # top left
            [2, 1, 0],  # middle
            [4, 3, 0],  # top right
        ]
        square_and_triangles = Polygon(*position_list, color=PURPLE_B)
        self.add(isosceles, square_and_triangles)
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
