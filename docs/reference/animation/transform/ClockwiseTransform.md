# 顺时针变换

合格名称：`manim.animation.transform.ClockwiseTransform`

```py
class ClockwiseTransform(mobject=None, *args, use_override=True, **kwargs)
```

Bases: `Transform`

沿顺时针方向的弧变换对象的点。

> 也可以看看

> [`Transform`](),[`CounterclockwiseTransform`]()


例子

示例：顺时针示例

```py
from manim import *

class ClockwiseExample(Scene):
    def construct(self):
        dl, dr = Dot(), Dot()
        sl, sr = Square(), Square()

        VGroup(dl, sl).arrange(DOWN).shift(2*LEFT)
        VGroup(dr, sr).arrange(DOWN).shift(2*RIGHT)

        self.add(dl, dr)
        self.wait()
        self.play(
            ClockwiseTransform(dl, sl),
            Transform(dr, sr)
        )
        self.wait()
```


方法


属性

`path_arc`
`path_func`
