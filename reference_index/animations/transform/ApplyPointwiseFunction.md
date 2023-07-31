# 应用逐点函数[#](#applypointwisefunction "此标题的固定链接")

合格名称：`manim.animation.transform.ApplyPointwiseFunction`

_类_ ApplyPointwiseFunction ( _mobject = None_ , _\* args_ , _use_override = True_ , _\*\* kwargs_ )[\[来源\]](../_modules/manim/animation/transform.html#ApplyPointwiseFunction)[#](#manim.animation.transform.ApplyPointwiseFunction "此定义的固定链接")

基地：[`ApplyMethod`](manim.animation.transform.ApplyMethod.html#manim.animation.transform.ApplyMethod "manim.animation.transform.ApplyMethod")

将逐点函数应用于 mobject 的动画。

例子

示例：WarpSquare [¶](#warpsquare)

from manim import \*

class WarpSquare(Scene):
def construct(self):
square = Square()
self.play(
ApplyPointwiseFunction(
lambda point: complex_to_R3(np.exp(R3_to_complex(point))), square
)
)
self.wait()

Copy to clipboard

方法

属性

`path_arc`

`path_func`
