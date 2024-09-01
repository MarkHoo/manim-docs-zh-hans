# 从点开始扩大

合格名称：`manim.animation.growing.GrowFromPoint`

```py
class GrowFromPoint(mobject=None, *args, use_override=True, **kwargs)
```
Bases: `Transform`

[`Mobject`]()通过从一点增长来引入。

参数

- **mobject** – 要引入的 mobject。
- **point** – 对象生长的点。
- **point_color** – mobject 在增长到其完整大小之前的初始颜色。留空以匹配对象的颜色。


例子

示例：GrowFromPointExample 

```py
from manim import *

class GrowFromPointExample(Scene):
    def construct(self):
        dot = Dot(3 * UR, color=GREEN)
        squares = [Square() for _ in range(4)]
        VGroup(*squares).set_x(0).arrange(buff=1)
        self.add(dot)
        self.play(GrowFromPoint(squares[0], ORIGIN))
        self.play(GrowFromPoint(squares[1], [-2, 2, 0]))
        self.play(GrowFromPoint(squares[2], [3, -2, 0], RED))
        self.play(GrowFromPoint(squares[3], dot, dot.get_color()))
```

方法

|||
|-|-|
`create_starting_mobject`|
`create_target`|

属性

|||
|-|-|
`path_arc`|
`path_func`|
