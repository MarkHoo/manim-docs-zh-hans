# 取消创建

合格名称：`manim.animation.creation.Uncreate`

```py
class Uncreate(mobject=None, *args, use_override=True, **kwargs)
```

Bases: Create

类似[`Create`]()，但相反。

例子

示例：显示取消创建

```py
from manim import *

class ShowUncreate(Scene):
    def construct(self):
        self.play(Uncreate(Square()))
```


> 也可以看看

> [`Create`]()

方法
