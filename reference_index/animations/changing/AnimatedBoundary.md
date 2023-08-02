# 动画边界

合格名称：`manim.animation.changing.AnimatedBoundary`

```py
class AnimatedBoundary(vmobject, colors=['#29ABCA', '#9CDCEB', '#236B8E', '#736357'], max_stroke_width=3, cycle_rate=0.5, back_and_forth=True, draw_rate_func=<function smooth>, fade_rate_func=<function smooth>, **kwargs)
```

基地：[`VGroup`]()

具有动画颜色变化的边界[`VMobject`](manim.mobject.types.vectorized_mobject.VMobject.html#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject")。

例子

示例：AnimatedBoundaryExample 

```py
from manim import *

class AnimatedBoundaryExample(Scene):
    def construct(self):
        text = Text("So shiny!")
        boundary = AnimatedBoundary(text, colors=[RED, GREEN, BLUE],
                                    cycle_rate=3)
        self.add(text, boundary)
        self.wait(2)
```

方法

|||
|-|-|
`full_family_become_partial`|
`update_boundary_copies`|


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
