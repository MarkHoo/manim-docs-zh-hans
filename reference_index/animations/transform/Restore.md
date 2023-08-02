# 恢复

合格名称：`manim.animation.transform.Restore`

```py
class Restore(mobject=None, *args, use_override=True, **kwargs)
```

Bases: ApplyMethod

将 mobject 转换为其上次保存的状态。

要保存 mobject 的状态，请使用[`save_state()`]()方法。

例子

示例：恢复示例

```py
from manim import *

class RestoreExample(Scene):
    def construct(self):
        s = Square()
        s.save_state()
        self.play(FadeIn(s))
        self.play(s.animate.set_color(PURPLE).set_opacity(0.5).shift(2*LEFT).scale(3))
        self.play(s.animate.shift(5*DOWN).rotate(PI/4))
        self.wait()
        self.play(Restore(s), run_time=2)
```

方法

属性

`path_arc`
`path_func`
