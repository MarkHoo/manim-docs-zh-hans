# 螺旋[#](#spiralin "此标题的固定链接")

合格名称：`manim.animation.creation.SpiralIn`

_类_ SpiralIn ( _mobject = None_ , _\* args_ , _use_override = True_ , _\*\* kwargs_ )[\[来源\]](../_modules/manim/animation/creation.html#SpiralIn)[#](#manim.animation.creation.SpiralIn "此定义的固定链接")

基地：[`Animation`](manim.animation.animation.Animation.html#manim.animation.animation.Animation "manim.animation.animation.Animation")

创建具有沿螺旋轨迹飞行的子 Mobject 的 Mobject。

参数

- **Shapes** – 要操作的 Mobject。
- **scale_factor** – 用于缩放效果的因子。
- **fade_in_fraction** – 子 Mobject 向内飞行时初始淡入的分数持续时间。

例子

示例：SpiralInExample [¶](#spiralinexample)

from manim import \*

class SpiralInExample(Scene):
def construct(self):
pi = MathTex(r"\\pi").scale(7)
pi.shift(2.25 _ LEFT + 1.5 _ UP)
circle = Circle(color=GREEN_C, fill_opacity=1).shift(LEFT)
square = Square(color=BLUE_D, fill_opacity=1).shift(UP)
shapes = VGroup(pi, circle, square)
self.play(SpiralIn(shapes))

Copy to clipboard

方法

[`interpolate_mobject`](#manim.animation.creation.SpiralIn.interpolate_mobject "manim.animation.creation.SpiralIn.interpolate_mobject")

根据 alpha 值对 mobject 进行插值`Animation`。

interpolate*mobject (*阿尔法\_)[\[来源\]](../_modules/manim/animation/creation.html#SpiralIn.interpolate_mobject)[#](#manim.animation.creation.SpiralIn.interpolate_mobject "此定义的固定链接")

根据 alpha 值对 mobject 进行插值`Animation`。

参数

**alpha** ( _float_ ) – 0 到 1 之间的浮点数，表示动画完成的比例。例如，alpha 值 0、0.5 和 1 分别对应于动画完成的 0%、50% 和 100%。

返回类型

没有任何
