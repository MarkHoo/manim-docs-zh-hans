# 淡入[#](#fadein "此标题的固定链接")

合格名称：`manim.animation.fading.FadeIn`

_类_ FadeIn ( _mobject = None_ , _\* args_ , _use_override = True_ , _\*\* kwargs_ )[\[来源\]](../_modules/manim/animation/fading.html#FadeIn)[#](#manim.animation.fading.FadeIn "此定义的固定链接")

基地：`_Fade`

淡入[`Mobject`](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject")s。

参数

- **mobjects** – 要淡入的 mobjects。
- **shift** – 对象在淡入时移动的向量。
- **target_position** – 淡入时 mobject 开始的位置。如果指定另一个 mobject 作为目标位置，则使用其中心。
- **缩放**– 淡入时对象在重新缩放至原始大小之前最初缩放的系数。

例子

示例：淡入示例[¶](#fadeinexample)

from manim import \*

class FadeInExample(Scene):
def construct(self):
dot = Dot(UP * 2 + LEFT)
self.add(dot)
tex = Tex(
"FadeIn with ", "shift ", " or target\\\_position", " and scale"
).scale(1)
animations = \[
FadeIn(tex\[0\]),
FadeIn(tex\[1\], shift=DOWN),
FadeIn(tex\[2\], target_position=dot),
FadeIn(tex\[3\], scale=1.5),
\]
self.play(AnimationGroup(*animations, lag_ratio=0.5))

Copy to clipboard

方法

`create_starting_mobject`

`create_target`

属性

`path_arc`

`path_func`
