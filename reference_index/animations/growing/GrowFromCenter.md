# 从中心成长[#](#growfromcenter "此标题的固定链接")

合格名称：`manim.animation.growing.GrowFromCenter`

_类_ GrowFromCenter ( _mobject = None_ , _\* args_ , _use_override = True_ , _\*\* kwargs_ )[\[来源\]](../_modules/manim/animation/growing.html#GrowFromCenter)[#](#manim.animation.growing.GrowFromCenter "此定义的固定链接")

基地：[`GrowFromPoint`](manim.animation.growing.GrowFromPoint.html#manim.animation.growing.GrowFromPoint "manim.animation.growing.GrowFromPoint")

[`Mobject`](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject")通过从中心生长来引入。

参数

- **mobject** – 要引入的 mobject。
- **point_color** – mobject 在增长到其完整大小之前的初始颜色。留空以匹配对象的颜色。

例子

示例：GrowFromCenterExample [¶](#growfromcenterexample)

from manim import \*

class GrowFromCenterExample(Scene):
def construct(self):
squares = \[Square() for \_ in range(2)\]
VGroup(\*squares).set_x(0).arrange(buff=2)
self.play(GrowFromCenter(squares\[0\]))
self.play(GrowFromCenter(squares\[1\], point_color=RED))

Copy to clipboard

方法

属性

`path_arc`

`path_func`
