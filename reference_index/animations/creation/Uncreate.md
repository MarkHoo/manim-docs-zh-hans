# 取消创建[#](#uncreate "此标题的固定链接")

合格名称：`manim.animation.creation.Uncreate`

_类_ Uncreate ( _mobject = None_ , _\* args_ , _use_override = True_ , _\*\* kwargs_ )[\[来源\]](../_modules/manim/animation/creation.html#Uncreate)[#](#manim.animation.creation.Uncreate "此定义的固定链接")

基地：[`Create`](manim.animation.creation.Create.html#manim.animation.creation.Create "manim.animation.creation.Create")

类似[`Create`](manim.animation.creation.Create.html#manim.animation.creation.Create "manim.animation.creation.Create")，但相反。

例子

示例：显示取消创建[¶](#showuncreate)

from manim import \*

class ShowUncreate(Scene):
def construct(self):
self.play(Uncreate(Square()))

Copy to clipboard

也可以看看

[`Create`](manim.animation.creation.Create.html#manim.animation.creation.Create "manim.animation.creation.Create")

方法
