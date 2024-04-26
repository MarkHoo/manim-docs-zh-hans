# mobject_update_utils

用于 mobject 连续动画的实用函数。

函数

`always(method, *args, **kwargs)`

参数：

**method** (Callable) –

返回类型：

[_Mobject_]()


`always_redraw(func)`

每帧重绘由函数构造的 mobject。

该函数返回一个带有附加更新器的 mobject，该更新器根据指定的函数不断重新生成 mobject。

参数：

**func** (_Callable[[], Mobject]_) – 没有（必需）输入参数且返回 mobject 的函数。

返回类型：

[_Mobject_]()

例子

示例：切线动画

[![视频缩略图](./static/)](https://docs.manim.community/en/stable/reference/TangentAnimation-1.mp4)

```py
from manim import *

class TangentAnimation(Scene):
    def construct(self):
        ax = Axes()
        sine = ax.plot(np.sin, color=RED)
        alpha = ValueTracker(0)
        point = always_redraw(
            lambda: Dot(
                sine.point_from_proportion(alpha.get_value()),
                color=BLUE
            )
        )
        tangent = always_redraw(
            lambda: TangentLine(
                sine,
                alpha=alpha.get_value(),
                color=YELLOW,
                length=4
            )
        )
        self.add(ax, sine, point, tangent)
        self.play(alpha.animate.set_value(1), rate_func=linear, run_time=2)
```


`always_rotate(mobject, rate=0.3490658503988659, **kwargs)`

以一定速率连续旋转的物体。

参数：

- **mobject** ( [_Mobject_]() ) – 要旋转的 mobject。
- **rate** ( _float_ ) – 对象旋转超过一秒的角度。
- **kwags** – 要传递给 的进一步参数[`Mobject.rotate()`]()。

返回类型：

[_Mobject_]()

例子

示例：旋转三角形

[![视频缩略图](./static/)](https://docs.manim.community/en/stable/reference/SpinningTriangle-1.mp4)

```py
from manim import *

class SpinningTriangle(Scene):
    def construct(self):
        tri = Triangle().set_fill(opacity=1).set_z_index(2)
        sq = Square().to_edge(LEFT)

        # will keep spinning while there is an animation going on
        always_rotate(tri, rate=2*PI, about_point=ORIGIN)

        self.add(tri, sq)
        self.play(sq.animate.to_edge(RIGHT), rate_func=linear, run_time=1)
```


`always_shift(mobject, direction=array([1., 0., 0.]), rate=0.1)`

以一定速率沿某个方向连续移动的物体。

参数：

- **mobject** ( [_Mobject_]() ) – 要移动的 mobject。
- **Direction** ( _ndarray_ _\[_ _float64_ _\]_ ) – 移动的方向。该向量已标准化，指定的幅度不相关。
- **rate** ( _float_ ) – 对象在一秒内沿着指定方向移动的长度（以 Manim 单位表示）。

返回类型：

[_Mobject_]()

例子

示例：平移方块

[![视频缩略图](./static/)](https://docs.manim.community/en/stable/reference/ShiftingSquare-1.mp4)

```py
from manim import *

class ShiftingSquare(Scene):
    def construct(self):
        sq = Square().set_fill(opacity=1)
        tri = Triangle()
        VGroup(sq, tri).arrange(LEFT)

        # construct a square which is continuously
        # shifted to the right
        always_shift(sq, RIGHT, rate=5)

        self.add(sq)
        self.play(tri.animate.set_fill(opacity=1))
```


`assert_is_mobject_method(method)`

参数：
**method** (_Callable_) –

返回类型：
None


`cycle_animation(animation, **kwargs)`

参数：

**animation** (_Animation_) –

返回类型：
[Mobject]()


`f_always(method, *arg_generators, **kwargs)`

更多功能版本，它不接受参数，而是接受输出相关参数的函数。

参数：

**method** (_Callable[[Mobject], None]_) –

返回类型：

[_Mobject_]()


`turn_animation_into_updater(animation, cycle=False, **kwargs)`

向动画的 mobject 添加更新程序，该更新程序应用动画的插值和更新功能

如果循环为 True，则此过程会一遍又一遍地重复。否则，更新程序将在完成后弹出

例子

示例：WelcomeToManim

[![视频缩略图](./static/)](https://docs.manim.community/en/stable/reference/WelcomeToManim-1.mp4)

```py
from manim import *

class WelcomeToManim(Scene):
    def construct(self):
        words = Text("Welcome to")
        banner = ManimBanner().scale(0.5)
        VGroup(words, banner).arrange(DOWN)

        turn_animation_into_updater(Write(words, run_time=0.9))
        self.add(words)
        self.wait(0.5)
        self.play(banner.expand(), run_time=0.5)
```

参数：
- **animation** (_Animation_) –
- **cycle** (_bool_) –

返回类型：
[Mobject]()
