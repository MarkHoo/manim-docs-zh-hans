# 沿路径移动[#](#movealongpath "此标题的固定链接")

合格名称：`manim.animation.movement.MoveAlongPath`

_类_ MoveAlongPath ( _mobject = None_ , _\* args_ , _use_override = True_ , _\*\* kwargs_ )[\[来源\]](../_modules/manim/animation/movement.html#MoveAlongPath)[#](#manim.animation.movement.MoveAlongPath "此定义的固定链接")

基地：[`Animation`](manim.animation.animation.Animation.html#manim.animation.animation.Animation "manim.animation.animation.Animation")

使一个 mobject 沿着另一 mobject 的路径移动。.. 标题:: 示例

示例：MoveAlongPathExample [¶](#movealongpathexample)

from manim import \*

class MoveAlongPathExample(Scene):
def construct(self):
d1 = Dot().set_color(ORANGE)
l1 = Line(LEFT, RIGHT)
l2 = VMobject()
self.add(d1, l1, l2)
l2.add_updater(lambda x: x.become(Line(LEFT, d1.get_center()).set_color(ORANGE)))
self.play(MoveAlongPath(d1, l1), rate_func=linear)

Copy to clipboard

方法

[`interpolate_mobject`](#manim.animation.movement.MoveAlongPath.interpolate_mobject "manim.animation.movement.MoveAlongPath.interpolate_mobject")

根据 alpha 值对 mobject 进行插值`Animation`。

interpolate*mobject (*阿尔法\_)[\[来源\]](../_modules/manim/animation/movement.html#MoveAlongPath.interpolate_mobject)[#](#manim.animation.movement.MoveAlongPath.interpolate_mobject "此定义的固定链接")

根据 alpha 值对 mobject 进行插值`Animation`。

参数

**alpha** ( _float_ ) – 0 到 1 之间的浮点数，表示动画完成的比例。例如，alpha 值 0、0.5 和 1 分别对应于动画完成的 0%、50% 和 100%。

返回类型

没有任何
