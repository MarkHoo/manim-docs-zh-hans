# 从点成长[#](#growfrompoint "此标题的固定链接")

合格名称：`manim.animation.growing.GrowFromPoint`

_类_ GrowFromPoint ( _mobject = None_ , _\* args_ , _use_override = True_ , _\*\* kwargs_ )[\[来源\]](../_modules/manim/animation/growing.html#GrowFromPoint)[#](#manim.animation.growing.GrowFromPoint "此定义的固定链接")

基地：[`Transform`](manim.animation.transform.Transform.html#manim.animation.transform.Transform "manim.animation.transform.Transform")

[`Mobject`](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject")通过从一点增长来引入。

参数

- **mobject** – 要引入的 mobject。
- **point** – 对象生长的点。
- **point_color** – mobject 在增长到其完整大小之前的初始颜色。留空以匹配对象的颜色。

例子

示例：GrowFromPointExample [¶](#growfrompointexample)

from manim import \*

class GrowFromPointExample(Scene):
def construct(self):
dot = Dot(3 * UR, color=GREEN)
squares = \[Square() for \_ in range(4)\]
VGroup(*squares).set_x(0).arrange(buff=1)
self.add(dot)
self.play(GrowFromPoint(squares\[0\], ORIGIN))
self.play(GrowFromPoint(squares\[1\], \[-2, 2, 0\]))
self.play(GrowFromPoint(squares\[2\], \[3, -2, 0\], RED))
self.play(GrowFromPoint(squares\[3\], dot, dot.get_color()))

Copy to clipboard

方法

`create_starting_mobject`

`create_target`

属性

`path_arc`

`path_func`
