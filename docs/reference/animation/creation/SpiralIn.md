# 螺旋

合格名称：`manim.animation.creation.SpiralIn`

```py
class SpiralIn(mobject=None, *args, use_override=True, **kwargs)
```

Bases: `Animation`

创建具有沿螺旋轨迹飞行的子 Mobject 的 Mobject。

参数

- **Shapes** – 要操作的 Mobject。
- **scale_factor** – 用于缩放效果的因子。
- **fade_in_fraction** – 子 Mobject 向内飞行时初始淡入的分数持续时间。


例子

示例：SpiralInExample 

```py
from manim import *

class SpiralInExample(Scene):
    def construct(self):
        pi = MathTex(r"\pi").scale(7)
        pi.shift(2.25 * LEFT + 1.5 * UP)
        circle = Circle(color=GREEN_C, fill_opacity=1).shift(LEFT)
        square = Square(color=BLUE_D, fill_opacity=1).shift(UP)
        shapes = VGroup(pi, circle, square)
        self.play(SpiralIn(shapes))
```


方法

|||
|-|-|
[`interpolate_mobject`]()|根据 alpha 值对 mobject 进行插值`Animation`。



`interpolate_mobject(alpha)`

根据 alpha 值对 mobject 进行插值`Animation`。

参数

**alpha** ( _float_ ) – 0 到 1 之间的浮点数，表示动画完成的比例。例如，alpha 值 0、0.5 和 1 分别对应于动画完成的 0%、50% 和 100%。

返回类型

None
