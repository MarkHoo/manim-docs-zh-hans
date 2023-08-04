# 淡出

合格名称：`manim.animation.fading.FadeOut`


```py
class FadeOut(mobject=None, *args, use_override=True, **kwargs)
```

Bases: `_Fade`

淡出[`Mobject`]()s.

参数

- **mobjects** – 要淡出的 mobjects。
- **shift** – 对象在淡出时移动的向量。
- **target_position** – mobject 在淡出时移动到的位置。如果另一个 mobject 被指定为目标位置，则使用其中心。
- **scale**– 对象在淡出时缩放的系数。


例子

示例：淡入示例

```py
from manim import *

class FadeInExample(Scene):
    def construct(self):
        dot = Dot(UP * 2 + LEFT)
        self.add(dot)
        tex = Tex(
            "FadeOut with ", "shift ", " or target\_position", " and scale"
        ).scale(1)
        animations = [
            FadeOut(tex[0]),
            FadeOut(tex[1], shift=DOWN),
            FadeOut(tex[2], target_position=dot),
            FadeOut(tex[3], scale=0.5),
        ]
        self.play(AnimationGroup(*animations, lag_ratio=0.5))
```

方法

|||
|-|-|
[`clean_up_from_scene`]()|[`Scene`]()完成动画后清理。
`create_target`|

属性

|||
|-|-|
`path_arc`|
`path_func`|



`clean_up_from_scene(scene=None)`

[`Scene`]()完成动画后清理。

如果动画是移除器，则这包括[`remove()`]()动画 [`Mobject`]()。

参数

**scene** (_Optional\_\_\[_ [_Scene_]() _\]_ ) – 应清除动画的场景。

返回类型

None
