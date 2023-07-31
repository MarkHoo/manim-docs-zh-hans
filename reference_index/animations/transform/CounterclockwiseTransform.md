# 逆时针变换[#](#counterclockwisetransform "此标题的固定链接")

合格名称：`manim.animation.transform.CounterclockwiseTransform`

逆时针变换*类*（_mobject = None_， _\* args_， _use_override = True_， _\*\* kwargs_）[\[来源\]](../_modules/manim/animation/transform.html#CounterclockwiseTransform)[#](#manim.animation.transform.CounterclockwiseTransform "此定义的固定链接")

基地：[`Transform`](manim.animation.transform.Transform.html#manim.animation.transform.Transform "manim.animation.transform.Transform")

沿逆时针方向的弧变换对象的点。

也可以看看

[`Transform`](manim.animation.transform.Transform.html#manim.animation.transform.Transform "manim.animation.transform.Transform"),[`ClockwiseTransform`](manim.animation.transform.ClockwiseTransform.html#manim.animation.transform.ClockwiseTransform "manim.animation.transform.ClockwiseTransform")

例子

示例：逆时针 Transform_vs_Transform [¶](#counterclockwisetransform_vs_transform)

from manim import \*

class CounterclockwiseTransform_vs_Transform(Scene):
def construct(self):
\# set up the numbers
c_transform = VGroup(DecimalNumber(number=3.141, num_decimal_places=3), DecimalNumber(number=1.618, num_decimal_places=3))
text_1 = Text("CounterclockwiseTransform", color=RED)
c_transform.add(text_1)

        transform = VGroup(DecimalNumber(number=1.618, num\_decimal\_places=3), DecimalNumber(number=3.141, num\_decimal\_places=3))
        text_2 = Text("Transform", color=BLUE)
        transform.add(text_2)

        ints = VGroup(c_transform, transform)
        texts = VGroup(text_1, text_2).scale(0.75)
        c_transform.arrange(direction=UP, buff=1)
        transform.arrange(direction=UP, buff=1)

        ints.arrange(buff=2)
        self.add(ints, texts)

        \# The mobs move in clockwise direction for ClockwiseTransform()
        self.play(CounterclockwiseTransform(c_transform\[0\], c_transform\[1\]))

        \# The mobs move straight up for Transform()
        self.play(Transform(transform\[0\], transform\[1\]))

Copy to clipboard

方法

属性

`path_arc`

`path_func`
