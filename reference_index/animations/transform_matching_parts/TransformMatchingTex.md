# TransformMatchingTex [#](#transformmatchingtex "此标题的固定链接")

合格名称：`manim.animation.transform\_matching\_parts.TransformMatchingTex`

_类_ TransformMatchingTex ( _mobject = None_ , _\* args_ , _use_override = True_ , _\*\* kwargs_ )[\[来源\]](../_modules/manim/animation/transform_matching_parts.html#TransformMatchingTex)[#](#manim.animation.transform_matching_parts.TransformMatchingTex "此定义的固定链接")

基地：[`TransformMatchingAbstractBase`](manim.animation.transform_matching_parts.TransformMatchingAbstractBase.html#manim.animation.transform_matching_parts.TransformMatchingAbstractBase "manim.animation.transform_matching_parts.TransformMatchingAbstractBase")

尝试转换渲染的 LaTeX 字符串的转换。

如果两个子对象匹配，则它们`tex_string`匹配。

也可以看看

[`TransformMatchingAbstractBase`](manim.animation.transform_matching_parts.TransformMatchingAbstractBase.html#manim.animation.transform_matching_parts.TransformMatchingAbstractBase "manim.animation.transform_matching_parts.TransformMatchingAbstractBase")

例子

示例：匹配方程部分[¶](#matchingequationparts)

from manim import \*

class MatchingEquationParts(Scene):
def construct(self):
variables = VGroup(MathTex("a"), MathTex("b"), MathTex("c")).arrange_submobjects().shift(UP)

        eq1 = MathTex("{{x}}^2", "+", "{{y}}^2", "=", "{{z}}^2")
        eq2 = MathTex("{{a}}^2", "+", "{{b}}^2", "=", "{{c}}^2")
        eq3 = MathTex("{{a}}^2", "=", "{{c}}^2", "-", "{{b}}^2")

        self.add(eq1)
        self.wait(0.5)
        self.play(TransformMatchingTex(Group(eq1, variables), eq2))
        self.wait(0.5)
        self.play(TransformMatchingTex(eq2, eq3))
        self.wait(0.5)

Copy to clipboard

方法

`get_mobject_key`

`get_mobject_parts`
