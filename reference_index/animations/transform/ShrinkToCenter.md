# 收缩到中心[#](#shrinktocenter "此标题的固定链接")

合格名称：`manim.animation.transform.ShrinkToCenter`

_类_ ShrinkToCenter ( _mobject = None_ , _\* args_ , _use_override = True_ , _\*\* kwargs_ )[\[来源\]](../_modules/manim/animation/transform.html#ShrinkToCenter)[#](#manim.animation.transform.ShrinkToCenter "此定义的固定链接")

基地：[`ScaleInPlace`](manim.animation.transform.ScaleInPlace.html#manim.animation.transform.ScaleInPlace "manim.animation.transform.ScaleInPlace")

使对象收缩到中心的动画。

例子

示例：ShrinkToCenter 示例[¶](#shrinktocenterexample)

from manim import \*

class ShrinkToCenterExample(Scene):
def construct(self):
self.play(ShrinkToCenter(Text("Hello World!")))

Copy to clipboard

方法

属性

`path_arc`

`path_func`
