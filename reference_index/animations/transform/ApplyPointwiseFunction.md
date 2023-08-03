# 应用逐点函数

合格名称：`manim.animation.transform.ApplyPointwiseFunction`

```py
class ApplyPointwiseFunction(mobject=None, *args, use_override=True, **kwargs)
```

Bases: `ApplyMethod`

将逐点函数应用于 mobject 的动画。


例子

示例：WarpSquare

```py
from manim import *

class WarpSquare(Scene):
    def construct(self):
        square = Square()
        self.play(
            ApplyPointwiseFunction(
                lambda point: complex_to_R3(np.exp(R3_to_complex(point))), square
            )
        )
        self.wait()
```

方法

属性

`path_arc`
`path_func`
