# 交叉口

合格名称：`manim.mobject.geometry.boolean\_ops.Intersection`

`class Intersection(*vmobjects, **kwargs)`

Bases: `_BooleanOps`

找到两个 s 的交集[`VMobject`]()。这使得零件被两个[`VMobject`]()s 覆盖。

参数

**vmobjects** –[`VMobject`]()寻找交集。

提高

**ValueError** – 如果小于 2，[`VMobject`]()则通过。

例子

示例：Intersection 示例

![IntersectionExample-2.png](../static/IntersectionExample-2.png)

```py
from manim import *

class IntersectionExample(Scene):
    def construct(self):
        sq = Square(color=RED, fill_opacity=1)
        sq.move_to([-2, 0, 0])
        cr = Circle(color=BLUE, fill_opacity=1)
        cr.move_to([-1.3, 0.7, 0])
        un = Intersection(sq, cr, color=GREEN, fill_opacity=1)
        un.move_to([1.5, 0, 0])
        self.add(sq, cr, un)
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
