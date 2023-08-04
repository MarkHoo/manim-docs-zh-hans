# TransformMatchingTex 

合格名称：`manim.animation.transform\_matching\_parts.TransformMatchingTex`

```py
class TransformMatchingTex(mobject=None, *args, use_override=True, **kwargs)
```

Bases: `TransformMatchingAbstractBase`

尝试转换渲染的 LaTeX 字符串的转换。

如果两个子对象匹配，则它们`tex_string`匹配。

> 也可以看看

> [`TransformMatchingAbstractBase`]()


例子

示例：匹配方程部分

```py
from manim import *

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
```


方法

`get_mobject_key`
`get_mobject_parts`
