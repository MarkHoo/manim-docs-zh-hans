# 周围矩形

合格名称：`manim.mobject.geometry.shape\_matchers.SurroundingRectangle`

_类_ SurroundingRectangle ( _mobject_ , _color = '#FFFF00'_ , _buff = 0.1_ , _corner_radius = 0.0_ , _\*\* kwargs_ )[\[来源\]](../_modules/manim/mobject/geometry/shape_matchers.html#SurroundingRectangle)[#](#manim.mobject.geometry.shape_matchers.SurroundingRectangle "此定义的固定链接")

基地：[`RoundedRectangle`](manim.mobject.geometry.polygram.RoundedRectangle.html#manim.mobject.geometry.polygram.RoundedRectangle "manim.mobject.geometry.polygram.RoundedRectangle")

一个矩形包围一个[`Mobject`](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject")

例子

示例：SurroundingRectExample [¶](#surroundingrectexample)

![../_images/Sur​​roundingRectExample-1.png](../_images/SurroundingRectExample-1.png)

from manim import \*

class SurroundingRectExample(Scene):
def construct(self):
title = Title("A Quote from Newton")
quote = Text(
"If I have seen further than others, \\n"
"it is by standing upon the shoulders of giants.",
color=BLUE,
).scale(0.75)
box = SurroundingRectangle(quote, color=YELLOW, buff=MED_LARGE_BUFF)

        t2 = Tex(r"Hello World").scale(1.5)
        box2 = SurroundingRectangle(t2, corner_radius=0.2)
        mobjects = VGroup(VGroup(box, quote), VGroup(t2, box2)).arrange(DOWN)
        self.add(title, mobjects)

Copy to clipboard

方法

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
