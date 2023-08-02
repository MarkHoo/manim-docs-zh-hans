# 摆动

合格名称：`manim.animation.indication.Wiggle`

```py
class Wiggle(mobject=None, *args, use_override=True, **kwargs)
```

Bases: Animation

摆动一个 Mobject。

参数

- **mobject** – 要摆动的 mobject。
- **scale_value** – mobject 将临时缩放的因子。
- **rotation_angle** – 摆动角度。
- **n_wiggles** – 摆动次数。
- **scale_about_point** – mobject 缩放的点。
- **rotate_about_point** – mobject 围绕其旋转的点。
- **run_time** – 动画的持续时间

例子

示例：应用 Waves [¶](#applyingwaves)

```py
from manim import *

class ApplyingWaves(Scene):
    def construct(self):
        tex = Tex("Wiggle").scale(3)
        self.play(Wiggle(tex))
        self.wait()
```

方法

`get_rotate_about_point`

`get_scale_about_point`

`interpolate_submobject`
