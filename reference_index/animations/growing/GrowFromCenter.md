# 从中心成长

合格名称：`manim.animation.growing.GrowFromCenter`

```py
class GrowFromCenter(mobject=None, *args, use_override=True, **kwargs)
```

Bases: `GrowFromPoint`

[`Mobject`]()通过从中心生长来引入。

参数

- **mobject** – 要引入的 mobject。
- **point_color** – mobject 在增长到其完整大小之前的初始颜色。留空以匹配对象的颜色。


例子

示例：GrowFromCenterExample

```py
from manim import *

class GrowFromCenterExample(Scene):
    def construct(self):
        squares = [Square() for _ in range(2)]
        VGroup(*squares).set_x(0).arrange(buff=2)
        self.play(GrowFromCenter(squares[0]))
        self.play(GrowFromCenter(squares[1], point_color=RED))
```

方法

属性

|||
|-|-|
`path_arc`|
`path_func`|
