# 替换变换

合格名称：`manim.animation.transform.ReplacementTransform`

```py
class ReplacementTransform(mobject=None, *args, use_override=True, **kwargs)
```

Bases: Transform

将 mobject 替换并变形为目标 mobject。

参数

- **mobject** – 起始[`Mobject`]().
- **target_mobject** – 目标[`Mobject`]()。
- **kwargs** – 传递给 的更多关键字参数[`Transform`]()。

例子

示例：替换变换或变换

```py
from manim import *

class ReplacementTransformOrTransform(Scene):
    def construct(self):
        # set up the numbers
        r_transform = VGroup(*[Integer(i) for i in range(1,4)])
        text_1 = Text("ReplacementTransform", color=RED)
        r_transform.add(text_1)

        transform = VGroup(*[Integer(i) for i in range(4,7)])
        text_2 = Text("Transform", color=BLUE)
        transform.add(text_2)

        ints = VGroup(r_transform, transform)
        texts = VGroup(text_1, text_2).scale(0.75)
        r_transform.arrange(direction=UP, buff=1)
        transform.arrange(direction=UP, buff=1)

        ints.arrange(buff=2)
        self.add(ints, texts)

        # The mobs replace each other and none are left behind
        self.play(ReplacementTransform(r_transform[0], r_transform[1]))
        self.play(ReplacementTransform(r_transform[1], r_transform[2]))

        # The mobs linger after the Transform()
        self.play(Transform(transform[0], transform[1]))
        self.play(Transform(transform[1], transform[2]))
        self.wait()
```

方法

属性

`path_arc`
`path_func`
