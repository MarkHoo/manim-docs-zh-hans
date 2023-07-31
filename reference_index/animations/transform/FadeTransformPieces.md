# 淡入淡出变换片段[#](#fadetransformpieces "此标题的固定链接")

合格名称：`manim.animation.transform.FadeTransformPieces`

_类_ FadeTransformPieces ( _mobject = None_ , _\* args_ , _use_override = True_ , _\*\* kwargs_ )[\[来源\]](../_modules/manim/animation/transform.html#FadeTransformPieces)[#](#manim.animation.transform.FadeTransformPieces "此定义的固定链接")

基地：[`FadeTransform`](manim.animation.transform.FadeTransform.html#manim.animation.transform.FadeTransform "manim.animation.transform.FadeTransform")

将一个对象的子对象淡入另一对象的子对象。

也可以看看

[`FadeTransform`](manim.animation.transform.FadeTransform.html#manim.animation.transform.FadeTransform "manim.animation.transform.FadeTransform")

例子

示例：FadeTransformSubmobjects [¶](#fadetransformsubmobjects)

from manim import \*

class FadeTransformSubmobjects(Scene):
def construct(self):
src = VGroup(Square(), Circle().shift(LEFT + UP))
src.shift(3*LEFT + 2*UP)
src_copy = src.copy().shift(4\*DOWN)

        target = VGroup(Circle(), Triangle().shift(RIGHT + DOWN))
        target.shift(3*RIGHT + 2*UP)
        target_copy = target.copy().shift(4*DOWN)

        self.play(FadeIn(src), FadeIn(src_copy))
        self.play(
            FadeTransform(src, target),
            FadeTransformPieces(src_copy, target_copy)
        )
        self.play(*\[FadeOut(mobj) for mobj in self.mobjects\])

Copy to clipboard

方法

[`begin`](#manim.animation.transform.FadeTransformPieces.begin "manim.animation.transform.FadeTransformPieces.begin")

动画的初始设置。

[`ghost_to`](#manim.animation.transform.FadeTransformPieces.ghost_to "manim.animation.transform.FadeTransformPieces.ghost_to")

将源子对象替换为目标子对象并将不透明度设置为 0。

属性

`path_arc`

`path_func`

开始( )[\[来源\]](../_modules/manim/animation/transform.html#FadeTransformPieces.begin)[#](#manim.animation.transform.FadeTransformPieces.begin "此定义的固定链接")

动画的初始设置。

该动画绑定到的 mobject 是由起始 mobject 和结束 mobject 组成的组。开始时，结束 mobject 取代起始 mobject（并且完全褪色）。最终，事情注定会适得其反。

Ghost*to（*源*，*目标\_）[\[来源\]](../_modules/manim/animation/transform.html#FadeTransformPieces.ghost_to)[#](#manim.animation.transform.FadeTransformPieces.ghost_to "此定义的固定链接")

将源子对象替换为目标子对象并将不透明度设置为 0。
