# 自旋从无[#](#spininfromnothing "此标题的固定链接")

合格名称：`manim.animation.growing.SpinInFromNothing`

_类_ SpinInFromNothing ( _mobject = None_ , _\* args_ , _use_override = True_ , _\*\* kwargs_ )[\[来源\]](../_modules/manim/animation/growing.html#SpinInFromNothing)[#](#manim.animation.growing.SpinInFromNothing "此定义的固定链接")

基地：[`GrowFromCenter`](manim.animation.growing.GrowFromCenter.html#manim.animation.growing.GrowFromCenter "manim.animation.growing.GrowFromCenter")

引入[`Mobject`](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject")旋转并从中心开始生长。

参数

- **mobject** – 要引入的 mobject。
- **角度**– 物体达到其完整尺寸之前的旋转量。例如，2\*PI 表示物体在完全引入之前将完成一整圈旋转。
- **point_color** – mobject 在增长到其完整大小之前的初始颜色。留空以匹配对象的颜色。

例子

示例：SpinInFromNothingExample [¶](#spininfromnothingexample)

from manim import \*

class SpinInFromNothingExample(Scene):
def construct(self):
squares = \[Square() for \_ in range(3)\]
VGroup(_squares).set_x(0).arrange(buff=2)
self.play(SpinInFromNothing(squares\[0\]))
self.play(SpinInFromNothing(squares\[1\], angle=2 _ PI))
self.play(SpinInFromNothing(squares\[2\], point_color=RED))

Copy to clipboard

方法

属性

`path_arc`

`path_func`
