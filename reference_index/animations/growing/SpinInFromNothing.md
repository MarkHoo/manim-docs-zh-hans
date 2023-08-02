# 自旋从无

合格名称：`manim.animation.growing.SpinInFromNothing`

```py
class SpinInFromNothing(mobject=None, *args, use_override=True, **kwargs)
```

Bases: GrowFromCenter

引入[`Mobject`]()旋转并从中心开始生长。

参数

- **mobject** – 要引入的 mobject。
- **角度**– 物体达到其完整尺寸之前的旋转量。例如，2\*PI 表示物体在完全引入之前将完成一整圈旋转。
- **point_color** – mobject 在增长到其完整大小之前的初始颜色。留空以匹配对象的颜色。

例子

示例：SpinInFromNothingExample 

```py
from manim import *

class SpinInFromNothingExample(Scene):
    def construct(self):
        squares = [Square() for _ in range(3)]
        VGroup(*squares).set_x(0).arrange(buff=2)
        self.play(SpinInFromNothing(squares[0]))
        self.play(SpinInFromNothing(squares[1], angle=2 * PI))
        self.play(SpinInFromNothing(squares[2], point_color=RED))
```

方法

属性

|||
|-|-|
`path_arc`|
`path_func`|
