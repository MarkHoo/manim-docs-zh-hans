# 滞后启动映射

合格名称：`manim.animation.composition.LaggedStartMap`

```py
class LaggedStartMap(mobject=None, *args, use_override=True, **kwargs)
```

基地：[`LaggedStart`]()

[`Animation`]()将函数映射到子对象时播放一系列内容。

参数

- **AnimationClass** –[`Animation`]()应用于 mobject。
- **mobject** –[`Mobject`]()将应用其子对象动画和可选的函数。
- **arg_creator** – 将应用于[`Mobject`]().
- **run_time** – 动画的持续时间（以秒为单位）。

例子

示例：LaggedStartMapExample
```py
from manim import *

class LaggedStartMapExample(Scene):
    def construct(self):
        title = Tex("LaggedStartMap").to_edge(UP, buff=LARGE_BUFF)
        dots = VGroup(
            *[Dot(radius=0.16) for _ in range(35)]
            ).arrange_in_grid(rows=5, cols=7, buff=MED_LARGE_BUFF)
        self.add(dots, title)

        # Animate yellow ripple effect
        for mob in dots, title:
            self.play(LaggedStartMap(
                ApplyMethod, mob,
                lambda m : (m.set_color, YELLOW),
                lag_ratio = 0.1,
                rate_func = there_and_back,
                run_time = 2
            ))
```

方法
