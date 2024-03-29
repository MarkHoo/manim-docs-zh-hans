# 差异

合格名称：`manim.mobject.geometry.boolean\_ops.Difference`

```py
class Difference(subject, clip, **kwargs)
```

Bases: `_BooleanOps`

从一个中减去[`VMobject`]()另一个。

参数

- **subject** — 第一个[`VMobject`]()。
- **clip** – 第二个[`VMobject`]()

例子

示例：差异示例

![DifferenceExample-1.png](../../static/DifferenceExample-1.png)

```py
from manim import *

class DifferenceExample(Scene):
    def construct(self):
        sq = Square(color=RED, fill_opacity=1)
        sq.move_to([-2, 0, 0])
        cr = Circle(color=BLUE, fill_opacity=1)
        cr.move_to([-1.3, 0.7, 0])
        un = Difference(sq, cr, color=GREEN, fill_opacity=1)
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
