# 淡入淡出颜色[#](#fadetocolor "此标题的固定链接")

合格名称：`manim.animation.transform.FadeToColor`

_类_ FadeToColor ( _mobject = None_ , _\* args_ , _use_override = True_ , _\*\* kwargs_ )[\[来源\]](../_modules/manim/animation/transform.html#FadeToColor)[#](#manim.animation.transform.FadeToColor "此定义的固定链接")

基地：[`ApplyMethod`](manim.animation.transform.ApplyMethod.html#manim.animation.transform.ApplyMethod "manim.animation.transform.ApplyMethod")

改变对象颜色的动画。

例子

示例：FadeToColorExample [¶](#fadetocolorexample)

from manim import \*

class FadeToColorExample(Scene):
def construct(self):
self.play(FadeToColor(Text("Hello World!"), color=RED))

Copy to clipboard

方法

属性

`path_arc`

`path_func`
