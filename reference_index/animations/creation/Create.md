# 创建

合格名称：`manim.animation.creation.Create`

```py
class Create(mobject=None, *args, use_override=True, **kwargs)
```

Bases: ShowPartial

增量显示 VMobject。

参数

**mobject** – 要设置动画的 VMobject。

提高

**TypeError** – 如果`mobject`不是 的实例[`VMobject`](manim.mobject.types.vectorized_mobject.VMobject.html#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject")。

例子

示例：创建场景[¶](#createscene)

```py
from manim import *

class CreateScene(Scene):
    def construct(self):
        self.play(Create(Square()))
```


也可以看看

[`ShowPassingFlash`](manim.animation.indication.ShowPassingFlash.html#manim.animation.indication.ShowPassingFlash "manim.animation.inspiration.ShowPassingFlash")

方法
