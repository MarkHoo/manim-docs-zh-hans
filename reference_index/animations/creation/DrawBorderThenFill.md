# 绘制边框然后填充

合格名称：`manim.animation.creation.DrawBorderThenFill`

```py
class DrawBorderThenFill(mobject=None, *args, use_override=True, **kwargs)
```

Bases: `Animation`

先绘制边框，然后显示填充。

例子

示例：ShowDrawBorderThenFill

```py
from manim import *

class ShowDrawBorderThenFill(Scene):
    def construct(self):
        self.play(DrawBorderThenFill(Square(fill_opacity=1, fill_color=ORANGE)))
```

方法

|||
|-|-|
[`begin`]()|开始动画。
[`get_all_mobjects`]()|获取动画中涉及的所有 mobject。
`get_outline`|
`get_stroke_color`|
`interpolate_submobject`|



`begin()`

开始动画。

该方法在动画播放时被调用。尽可能多的初始化，尤其是任何 mobject 复制，应该存在于这个方法中。

返回类型

None



`get_all_mobjects()`

获取动画中涉及的所有 mobject。

顺序必须与 interpolate_submobject 的参数顺序匹配

返回

mobject 的序列。

返回类型

Sequence\[ [Mobject]() \]
