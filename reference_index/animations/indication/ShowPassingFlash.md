# 显示传递 Flash 

合格名称：`manim.animation.indication.ShowPassingFlash`

```py
class ShowPassingFlash(mobject=None, *args, use_override=True, **kwargs)
```

Bases: `ShowPartial`

每帧仅显示 VMobject 的一小部分。

参数

- **mobject** – 其笔划具有动画效果的 mobject。
- **time_width** – 条子的长度相对于笔划的长度。


例子

示例：时间宽度值

```py
from manim import *

class TimeWidthValues(Scene):
    def construct(self):
        p = RegularPolygon(5, color=DARK_GRAY, stroke_width=6).scale(3)
        lbl = VMobject()
        self.add(p, lbl)
        p = p.copy().set_color(BLUE)
        for time_width in [0.2, 0.5, 1, 2]:
            lbl.become(Tex(r"\texttt{time\_width={{%.1f}}}"%time_width))
            self.play(ShowPassingFlash(
                p.copy().set_color(BLUE),
                run_time=2,
                time_width=time_width
            ))
```

> 也可以看看

> [`Create`]()


方法

|||
|-|-|
[`clean_up_from_scene`]()|[`Scene`]()完成动画后清理。



`clean_up_from_scene(scene)`

[`Scene`]()完成动画后清理。

如果动画是移除器，则这包括[`remove()`]()动画 [`Mobject`]()。

参数

**scene** ( [_Scene_]() ) – 应清除动画的场景。

返回类型

None
