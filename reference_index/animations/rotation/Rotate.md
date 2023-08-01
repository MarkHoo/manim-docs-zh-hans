# 旋转

合格名称：`manim.animation.rotation.Rotate`

```py
class Rotate(mobject=None, *args, use_override=True, **kwargs)
```

Bases: Transform

旋转 Mobject 的动画。

参数

- **mobject** – 要旋转的 mobject。
- **angle**– 旋转角度。
- **axis** – numpy 向量形式的旋转轴。
- **about_point** – 旋转中心。
- **about_edge** – 如果，则此参数指定要作为旋转中心的边界框点的方向。` about_point``is ``None `

例子

示例：使用旋转

```py
from manim import *

class UsingRotate(Scene):
    def construct(self):
        self.play(
            Rotate(
                Square(side_length=0.5).shift(UP * 2),
                angle=2*PI,
                about_point=ORIGIN,
                rate_func=linear,
            ),
            Rotate(Square(side_length=0.5), angle=2*PI, rate_func=linear),
            )
```

方法

|||
|-|-|
`create_target`|

属性

|||
|-|-|
`path_arc`|
`path_func`|
