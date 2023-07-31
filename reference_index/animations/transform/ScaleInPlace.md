# 原地缩放[#](#scaleinplace "此标题的固定链接")

合格名称：`manim.animation.transform.ScaleInPlace`

_类_ ScaleInPlace ( _mobject = None_ , _\* args_ , _use_override = True_ , _\*\* kwargs_ )[\[来源\]](../_modules/manim/animation/transform.html#ScaleInPlace)[#](#manim.animation.transform.ScaleInPlace "此定义的固定链接")

基地：[`ApplyMethod`](manim.animation.transform.ApplyMethod.html#manim.animation.transform.ApplyMethod "manim.animation.transform.ApplyMethod")

按特定因子缩放对象的动画。

例子

示例：ScaleInPlace 示例[¶](#scaleinplaceexample)

from manim import \*

class ScaleInPlaceExample(Scene):
def construct(self):
self.play(ScaleInPlace(Text("Hello World!"), 2))

Copy to clipboard

方法

属性

`path_arc`

`path_func`
