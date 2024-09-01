# 显示

合格名称：`manim.animation.indication.Indicate`

```py
class Indicate(mobject=None, *args, use_override=True, **kwargs)
```

Bases: `Transform`


通过暂时调整 Mobject 的大小和重新着色来显示它。

参数

- **mobject** – 要指示的 mobject。
- **scale_factor** – 对象临时缩放的因子
- **color** – 对象暂时采用的颜色。
- **rate_func** – 定义每个时间点的动画进度的函数。
- **kwargs** – 要传递给[`Succession`]()构造函数的附加参数


例子

示例：使用显示

```py
from manim import *

class UsingIndicate(Scene):
    def construct(self):
        tex = Tex("Indicate").scale(3)
        self.play(Indicate(tex))
        self.wait()
```


方法

|||
|-|-|
`create_target`|

属性

|||
|-|-|
`path_arc`|
`path_func`|
