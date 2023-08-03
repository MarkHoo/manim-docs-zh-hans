# 十二面体

合格名称：`manim.mobject.three\_d.polyhedra.Dodecahedron`


```py
class Dodecahedron(edge_length=1, **kwargs)
```

Bases: `Polyhedron`

十二面体，五个柏拉图立体之一。它有 12 个面、30 条边和 20 个顶点。

参数

**edge_length** ( _float_ ) – 任意两个顶点之间的边的长度。


例子

示例：十二面体场景

![DodecahedronScene-1.png](../../static/DodecahedronScene-1.png)


```py
from manim import *

class DodecahedronScene(ThreeDScene):
    def construct(self):
        self.set_camera_orientation(phi=75 * DEGREES, theta=30 * DEGREES)
        obj = Dodecahedron()
        self.add(obj)
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
