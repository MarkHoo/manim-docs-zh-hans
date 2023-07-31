# 顺时针变换[#](#clockwisetransform "此标题的固定链接")

合格名称：`manim.animation.transform.ClockwiseTransform`

_类_ ClockwiseTransform ( _mobject = None_ , _\* args_ , _use_override = True_ , _\*\* kwargs_ )[\[来源\]](../_modules/manim/animation/transform.html#ClockwiseTransform)[#](#manim.animation.transform.ClockwiseTransform "此定义的固定链接")

基地：[`Transform`](manim.animation.transform.Transform.html#manim.animation.transform.Transform "manim.animation.transform.Transform")

沿顺时针方向的弧变换对象的点。

也可以看看

[`Transform`](manim.animation.transform.Transform.html#manim.animation.transform.Transform "manim.animation.transform.Transform"),[`CounterclockwiseTransform`](manim.animation.transform.CounterclockwiseTransform.html#manim.animation.transform.CounterclockwiseTransform "manim.animation.transform.CounterclockedTransform")

例子

示例：顺时针示例[¶](#clockwiseexample)

from manim import \*

class ClockwiseExample(Scene):
def construct(self):
dl, dr = Dot(), Dot()
sl, sr = Square(), Square()

        VGroup(dl, sl).arrange(DOWN).shift(2*LEFT)
        VGroup(dr, sr).arrange(DOWN).shift(2*RIGHT)

        self.add(dl, dr)
        self.wait()
        self.play(
            ClockwiseTransform(dl, sl),
            Transform(dr, sr)
        )
        self.wait()

Copy to clipboard

方法

属性

`path_arc`

`path_func`
