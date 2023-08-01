# 淡入淡出颜色

合格名称：`manim.animation.transform.FadeToColor`

```py
class FadeToColor(mobject=None, *args, use_override=True, **kwargs)
```

Bases: ApplyMethod

改变对象颜色的动画。

例子

示例：FadeToColorExample

```py
from manim import *

class FadeToColorExample(Scene):
    def construct(self):
        self.play(FadeToColor(Text("Hello World!"), color=RED))
```

方法

属性

`path_arc`
`path_func`
