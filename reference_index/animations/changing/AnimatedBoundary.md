# 动画边界[#](#animatedboundary "此标题的固定链接")

合格名称：`manim.animation.changing.AnimatedBoundary`

_class_ AnimatedBoundary ( _vmobject, color=\['#29ABCA', '#9CDCEB', '#236B8E', '#736357'\], max_lines_width=3, Cycle_rate=0.5, back_and_forth=True, draw_rate_func=<函数 平滑>, fade_rate_func= <函数 平滑>, \*\*kwargs_ )[\[来源\]](../_modules/manim/animation/changing.html#AnimatedBoundary)[#](#manim.animation.changing.AnimatedBoundary "此定义的固定链接")

基地：[`VGroup`](manim.mobject.types.vectorized_mobject.VGroup.html#manim.mobject.types.vectorized_mobject.VGroup "manim.mobject.types.vectorized_mobject.VGroup")

具有动画颜色变化的边界[`VMobject`](manim.mobject.types.vectorized_mobject.VMobject.html#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject")。

例子

示例：AnimatedBoundaryExample [¶](#animatedboundaryexample)

from manim import \*

class AnimatedBoundaryExample(Scene):
def construct(self):
text = Text("So shiny!")
boundary = AnimatedBoundary(text, colors=\[RED, GREEN, BLUE\],
cycle_rate=3)
self.add(text, boundary)
self.wait(2)

Copy to clipboard

方法

`full_family_become_partial`

`update_boundary_copies`

属性

`animate`

用于对 的任何方法的应用程序进行动画处理`self`。

`animation_overrides`

`color`

`depth`

对象的深度。

`fill_color`

如果有多种颜色（对于渐变），则返回第一个颜色

`height`

mobject 的高度。

`n_points_per_curve`

`sheen_factor`

`stroke_color`

`width`

mobject 的宽度。
