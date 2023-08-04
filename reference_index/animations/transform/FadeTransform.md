# 淡入淡出变换

合格名称：`manim.animation.transform.FadeTransform`

```py
class FadeTransform(mobject=None, *args, use_override=True, **kwargs)
```

Bases: `Transform`

将一个对象淡入另一个对象。

参数

- **mobject** – 起始[`Mobject`]().
- **target_mobject** – 目标[`Mobject`]()。
- **stretch**– 控制目标[`Mobject`]()在动画过程中是否拉伸。默认值：`True`.
- **dim_to_match**[`Mobject`]() – 如果目标 mobject 没有自动拉伸，则可以在移入时调整目标的初始比例。分别将其设置为 0、1 和 2，使目标的长度与目标的长度相匹配[`Mobject`]()分别从 x、y 和 z 方向开始 。
- **kwargs** – 更多关键字参数传递给父类。


例子

示例：不同的淡入淡出变换

```py
from manim import *

class DifferentFadeTransforms(Scene):
    def construct(self):
        starts = [Rectangle(width=4, height=1) for _ in range(3)]
        VGroup(*starts).arrange(DOWN, buff=1).shift(3*LEFT)
        targets = [Circle(fill_opacity=1).scale(0.25) for _ in range(3)]
        VGroup(*targets).arrange(DOWN, buff=1).shift(3*RIGHT)

        self.play(*[FadeIn(s) for s in starts])
        self.play(
            FadeTransform(starts[0], targets[0], stretch=True),
            FadeTransform(starts[1], targets[1], stretch=False, dim_to_match=0),
            FadeTransform(starts[2], targets[2], stretch=False, dim_to_match=1)
        )

        self.play(*[FadeOut(mobj) for mobj in self.mobjects])
```


方法

|||
|-|-|
[`begin`]()|动画的初始设置。
[`clean_up_from_scene`]()|[`Scene`]()完成动画后清理。
`get_all_families_zipped`|
[`get_all_mobjects`]()|获取动画中涉及的所有 mobject。
[`ghost_to`]()|将源替换为目标并将不透明度设置为 0。


属性

`path_arc`
`path_func`



`begin()`

动画的初始设置。

该动画绑定到的 mobject 是由起始 mobject 和结束 mobject 组成的组。开始时，结束 mobject 取代起始 mobject（并且完全褪色）。最终，事情注定会适得其反。



`clean_up_from_scene(scene)`

[`Scene`]()完成动画后清理。

如果动画是移除器，则这包括[`remove()`]()动画 [`Mobject`]()。

参数

**scene** – 应该清除动画的场景。



`get_all_mobjects()`

获取动画中涉及的所有 mobject。

顺序必须与 interpolate_submobject 的参数顺序匹配

返回

mobject 的序列。

返回类型

Sequence\[ [Mobject]() \]



`ghost_to(source, target)`

将源替换为目标并将不透明度设置为 0。

如果提供的目标没有点，因此位置为 \[0, 0, 0\]，源将简单地淡出其当前所在位置。
