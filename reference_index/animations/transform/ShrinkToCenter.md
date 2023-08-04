# 收缩到中心

合格名称：`manim.animation.transform.ShrinkToCenter`

```py
class ShrinkToCenter(mobject=None, *args, use_override=True, **kwargs)
```

Bases: `ScaleInPlace`

使对象收缩到中心的动画。


例子

示例：ShrinkToCenter 示例

```py
from manim import *

class ShrinkToCenterExample(Scene):
    def construct(self):
        self.play(ShrinkToCenter(Text("Hello World!")))
```


方法



属性

`path_arc`
`path_func`
