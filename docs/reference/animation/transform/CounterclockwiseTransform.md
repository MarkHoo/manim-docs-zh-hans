# 逆时针变换

合格名称：`manim.animation.transform.CounterclockwiseTransform`

```py
class CounterclockwiseTransform(mobject=None, *args, use_override=True, **kwargs)
```

Bases: `Transform`

沿逆时针方向的弧变换对象的点。

> 也可以看看

> [`Transform`](),[`ClockwiseTransform`]()


例子

示例：逆时针 Transform_vs_Transform

```py
from manim import *

class CounterclockwiseTransform_vs_Transform(Scene):
    def construct(self):
        # set up the numbers
        c_transform = VGroup(DecimalNumber(number=3.141, num_decimal_places=3), DecimalNumber(number=1.618, num_decimal_places=3))
        text_1 = Text("CounterclockwiseTransform", color=RED)
        c_transform.add(text_1)

        transform = VGroup(DecimalNumber(number=1.618, num_decimal_places=3), DecimalNumber(number=3.141, num_decimal_places=3))
        text_2 = Text("Transform", color=BLUE)
        transform.add(text_2)

        ints = VGroup(c_transform, transform)
        texts = VGroup(text_1, text_2).scale(0.75)
        c_transform.arrange(direction=UP, buff=1)
        transform.arrange(direction=UP, buff=1)

        ints.arrange(buff=2)
        self.add(ints, texts)

        # The mobs move in clockwise direction for ClockwiseTransform()
        self.play(CounterclockwiseTransform(c_transform[0], c_transform[1]))

        # The mobs move straight up for Transform()
        self.play(Transform(transform[0], transform[1]))
```


方法



属性

`path_arc`
`path_func`
