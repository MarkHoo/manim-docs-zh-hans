# 点之间的弧线

合格名称：`manim.mobject.geometry.arc.ArcBetweenPoints`

_类_ ArcBetweenPoints (_开始_,_结束_,_角度= 1.5707963267948966_ ,_半径=无_, _\*\* kwargs_ )[\[来源\]](../_modules/manim/mobject/geometry/arc.html#ArcBetweenPoints)[#](#manim.mobject.geometry.arc.ArcBetweenPoints "此定义的固定链接")

基地：[`Arc`](manim.mobject.geometry.arc.Arc.html#manim.mobject.geometry.arc.Arc "manim.mobject.geometry.arc.Arc")

继承自 Arc，并另外获取弧跨越的 2 个点。

例子

示例：ArcBetweenPoints示例[¶](#arcbetweenpointsexample)

from manim import *

class ArcBetweenPointsExample(Scene):
    def construct(self):
        circle = Circle(radius=2, stroke_color=GREY)
        dot_1 = Dot(color=GREEN).move_to(\[2, 0, 0\]).scale(0.5)
        dot\_1\_text = Tex("(2,0)").scale(0.5).next_to(dot_1, RIGHT).set_color(BLUE)
        dot_2 = Dot(color=GREEN).move_to(\[0, 2, 0\]).scale(0.5)
        dot\_2\_text = Tex("(0,2)").scale(0.5).next_to(dot_2, UP).set_color(BLUE)
        arc= ArcBetweenPoints(start=2 * RIGHT, end=2 * UP, stroke_color=YELLOW)
        self.add(circle, dot_1, dot_2, dot\_1\_text, dot\_2\_text)
        self.play(Create(arc))

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