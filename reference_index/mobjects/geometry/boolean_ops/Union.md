# 联盟

合格名称：`manim.mobject.geometry.boolean\_ops.Union`

```py
class Union(*vmobjects, **kwargs)
```

Bases: `_BooleanOps`

两个或多个[`VMobject`]()s 的并集。这将返回 s 的公共区域`VMobject`。

参数

**vmobjects** ( [_VMobject_]() ) –[`VMobject`]()要查找并集的 s。

提高

**ValueError**[`VMobject`]() – 如果经过的时间少于 2 秒。

例子

示例：UnionExample 

![UnionExample-1.png](../static/UnionExample-1.png)

```py
from manim import *

class UnionExample(Scene):
    def construct(self):
        sq = Square(color=RED, fill_opacity=1)
        sq.move_to([-2, 0, 0])
        cr = Circle(color=BLUE, fill_opacity=1)
        cr.move_to([-1.3, 0.7, 0])
        un = Union(sq, cr, color=GREEN, fill_opacity=1)
        un.move_to([1.5, 0.3, 0])
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
