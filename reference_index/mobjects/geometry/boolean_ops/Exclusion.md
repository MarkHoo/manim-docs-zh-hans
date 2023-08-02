# 排除

合格名称：`manim.mobject.geometry.boolean\_ops.Exclusion`

```py
class Exclusion(subject, clip, **kwargs)
```

Bases: `_BooleanOps`


求两个 之间的异或[`VMobject`]()。这将创建一个新的[`VMobject`]()区域，该区域由其中一个区域所覆盖。

参数

- **主题**——第一[`VMobject`]()。
- **剪辑**– 第二个[`VMobject`]()

例子

示例：Intersection 示例

![IntersectionExample-1.png](../static/IntersectionExample-1.png)

```py
from manim import *

class IntersectionExample(Scene):
    def construct(self):
        sq = Square(color=RED, fill_opacity=1)
        sq.move_to([-2, 0, 0])
        cr = Circle(color=BLUE, fill_opacity=1)
        cr.move_to([-1.3, 0.7, 0])
        un = Exclusion(sq, cr, color=GREEN, fill_opacity=1)
        un.move_to([1.5, 0.4, 0])
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
