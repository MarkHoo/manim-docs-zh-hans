# 焦点

合格名称：`manim.animation.indication.FocusOn`

```py
class FocusOn(mobject=None, *args, use_override=True, **kwargs)
```

Bases: Transform


将聚光灯缩小到某个位置。

参数

- **focus_point** – 缩小聚光灯的点。如果是 a，`Mobject`则将使用其中心。
- **opacity**– 聚光灯的不透明度。
- **color**– 聚光灯的颜色。
- **run_time** – 动画的持续时间。
- **kwargs** – 要传递给[`Succession`]()构造函数的附加参数

例子

示例：使用 FocusOn 

```py
from manim import *

class UsingFocusOn(Scene):
    def construct(self):
        dot = Dot(color=YELLOW).shift(DOWN)
        self.add(Tex("Focusing on the dot below:"), dot)
        self.play(FocusOn(dot))
        self.wait()
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
