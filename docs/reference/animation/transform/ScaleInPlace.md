# 原地缩放

合格名称：`manim.animation.transform.ScaleInPlace`

```py
class ScaleInPlace(mobject=None, *args, use_override=True, **kwargs)
```

Bases: `ApplyMethod`

按特定因子缩放对象的动画。


例子

示例：ScaleInPlace 示例

```py
from manim import *

class ScaleInPlaceExample(Scene):
    def construct(self):
        self.play(ScaleInPlace(Text("Hello World!"), 2))
```


方法



属性

`path_arc`
`path_func`
