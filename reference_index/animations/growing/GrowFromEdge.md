# 从边缘生长[#](#growfromedge "此标题的固定链接")

合格名称：`manim.animation.growing.GrowFromEdge`

_类_ GrowFromEdge ( _mobject = None_ , _\* args_ , _use_override = True_ , _\*\* kwargs_ )[\[来源\]](../_modules/manim/animation/growing.html#GrowFromEdge)[#](#manim.animation.growing.GrowFromEdge "此定义的固定链接")

基地：[`GrowFromPoint`](manim.animation.growing.GrowFromPoint.html#manim.animation.growing.GrowFromPoint "manim.animation.growing.GrowFromPoint")

[`Mobject`](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject")通过从其边界框边缘之一增长它来引入。

参数

- **mobject** – 要引入的 mobject。
- **edge** – 寻找 mobject 边界框边缘的方向。
- **point_color** – mobject 在增长到其完整大小之前的初始颜色。留空以匹配对象的颜色。

例子

示例：GrowFromEdgeExample [¶](#growfromedgeexample)

from manim import \*

class GrowFromEdgeExample(Scene):
def construct(self):
squares = \[Square() for \_ in range(4)\]
VGroup(\*squares).set_x(0).arrange(buff=1)
self.play(GrowFromEdge(squares\[0\], DOWN))
self.play(GrowFromEdge(squares\[1\], RIGHT))
self.play(GrowFromEdge(squares\[2\], UR))
self.play(GrowFromEdge(squares\[3\], UP, point_color=RED))

Copy to clipboard

方法

属性

`path_arc`

`path_func`
