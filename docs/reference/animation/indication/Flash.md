# 闪光

合格名称：`manim.animation.indication.Flash`

```py
class Flash(mobject=None, *args, use_override=True, **kwargs)
```

Bases: `AnimationGroup`


向各个方向发出线路。

参数

- **point**– 闪光线的中心。如果是 a，`Mobject`则将使用其中心。
- **line_length** – 闪光线的长度。
- **num_lines** – 闪存行数。
- **flash_radius** –距闪光线起始点的距离。
- **line_lines_width** – 闪烁线的描边宽度。
- **color**– 闪光线的颜色。
- **time_width** – 用于闪烁线的时间宽度。请参阅`ShowPassingFlash`了解更多详情。
- **run_time** – 动画的持续时间。
- **kwargs** – 要传递给[`Succession`]()构造函数的附加参数


例子

示例：使用 Flash 

```py
from manim import *

class UsingFlash(Scene):
    def construct(self):
        dot = Dot(color=YELLOW).shift(DOWN)
        self.add(Tex("Flash the dot below:"), dot)
        self.play(Flash(dot))
        self.wait()
```


示例：FlashOnCircle 

```py
from manim import *

class FlashOnCircle(Scene):
    def construct(self):
        radius = 2
        circle = Circle(radius)
        self.add(circle)
        self.play(Flash(
            circle, line_length=1,
            num_lines=30, color=RED,
            flash_radius=radius+SMALL_BUFF,
            time_width=0.3, run_time=2,
            rate_func = rush_from
        ))
```


方法

|||
|-|-|
`create_line_anims`|
`create_lines`|
