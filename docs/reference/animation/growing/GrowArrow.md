# 扩大箭头

合格名称：`manim.animation.growing.GrowArrow`

```py
class GrowArrow(mobject=None, *args, use_override=True, **kwargs)
```

Bases: `GrowFromPoint`

[`Arrow`]()通过从开始向尖端生长来引入。

参数

- **arrow** – 要引入的箭头。
- **point_color** – 箭头在增长到完整尺寸之前的初始颜色。留空以匹配箭头的颜色。


例子

示例：GrowArrowExample

```py
from manim import *

class GrowArrowExample(Scene):
    def construct(self):
        arrows = [Arrow(2 * LEFT, 2 * RIGHT), Arrow(2 * DR, 2 * UL)]
        VGroup(*arrows).set_x(0).arrange(buff=2)
        self.play(GrowArrow(arrows[0]))
        self.play(GrowArrow(arrows[1], point_color=RED))
```

方法

|||
|-|-|
`create_starting_mobject`|


属性

|||
|-|-|
`path_arc`|
`path_func`|
