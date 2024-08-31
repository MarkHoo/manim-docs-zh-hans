# 改变速度

合格名称：`manim.animation.speedmodifier.ChangeSpeed`

```py
class ChangeSpeed(mobject=None, *args, use_override=True, **kwargs)
```

Bases: `Animation`

修改传递动画的速度。 还可以使用`AnimationGroup`with different 将多个动画合并为一个。`lag_ratio`改变传递的动画`run_time`的 来修改速度。

参数

- **anim** – 要修改速度的动画。
- **speedinfo** – 包含节点（ 的百分比`run_time`）及其相应的速度因子。
- **rate_func** – 覆盖`rate_func`传递的动画，在更改速度之前应用。


例子

示例：速度修改器示例

```py
from manim import *

class SpeedModifierExample(Scene):
    def construct(self):
        a = Dot().shift(LEFT * 4)
        b = Dot().shift(RIGHT * 4)
        self.add(a, b)
        self.play(
            ChangeSpeed(
                AnimationGroup(
                    a.animate(run_time=1).shift(RIGHT * 8),
                    b.animate(run_time=1).shift(LEFT * 8),
                ),
                speedinfo={0.3: 1, 0.4: 0.1, 0.6: 0.1, 1: 1},
                rate_func=linear,
            )
        )
```


示例：SpeedModifierUpdater 示例

```py
from manim import *

class SpeedModifierUpdaterExample(Scene):
    def construct(self):
        a = Dot().shift(LEFT * 4)
        self.add(a)

        ChangeSpeed.add_updater(a, lambda x, dt: x.shift(RIGHT * 4 * dt))
        self.play(
            ChangeSpeed(
                Wait(2),
                speedinfo={0.4: 1, 0.5: 0.2, 0.8: 0.2, 1: 1},
                affects_speed_updaters=True,
            )
        )
```


示例：SpeedModifierUpdaterExample2 

```py
from manim import *

class SpeedModifierUpdaterExample2(Scene):
    def construct(self):
        a = Dot().shift(LEFT * 4)
        self.add(a)

        ChangeSpeed.add_updater(a, lambda x, dt: x.shift(RIGHT * 4 * dt))
        self.wait()
        self.play(
            ChangeSpeed(
                Wait(),
                speedinfo={1: 0},
                affects_speed_updaters=True,
            )
        )
```


方法

|||
|-|-|
[`add_updater`]()|此静态方法可用于对更新程序应用速度更改。
[`begin`]()|开始动画。
[`clean_up_from_scene`]()|[`Scene`]()完成动画后清理。
[`finish`]()|完成动画。
[`get_scaled_total_time`]()|假设 为`run_time`1 时动画所花费的时间。
[`interpolate`]()|设置动画进度。
`setup`|
[`update_mobjects`]()|更新诸如 starting_mobject 和（对于变换）target_mobject 之类的内容。


属性

|||
|-|-|
`dt`|
`is_changing_dt`|


```py
classmethod add_updater(mobject, update_function, index=None, call_updater=False)
```

此静态方法可用于对更新程序应用速度更改。

[`ChangeSpeed`]() 此更新程序将遵循正在播放的任何动画的速度和速率函数`affects_speed_updaters=True`。默认情况下，通过常规[`Mobject.add_updater()`]()方法添加的更新程序函数不考虑动画速度的变化。

参数

- **mobject** ( [_Mobject_]() ) – 更新程序应附加到的 mobject。
- **update_function** ( _Updater_ ) – 渲染新帧时调用的函数。
- **index** ( _int_ _|_ _None_ ) – 函数在 mobject 更新器列表中应插入的位置。
- **call_updater** ( _bool_ ) – 如果为`True`，则在将其附加到 mobject 时调用更新函数。

> 也可以看看

> [`ChangeSpeed`](),[`Mobject.add_updater()`]()



`begin()`

开始动画。

该方法在动画播放时被调用。尽可能多的初始化，尤其是任何 mobject 复制，应该存在于这个方法中。

返回类型

None


`clean_up_from_scene(scene)`

[`Scene`]()完成动画后清理。

如果动画是移除器，则这包括[`remove()`]()动画 [`Mobject`]()。

参数

**scene** ( [_Scene_]() ) – 应清除动画的场景。

返回类型

None


`finish()`

完成动画。

动画结束时会调用此方法。

返回类型

None


`get_scaled_total_time()`

假设 为`run_time`1 时动画所花费的时间。

返回类型

float


`interpolate(alpha)`

设置动画进度。

动画期间的每一帧都会调用此方法。

参数

**alpha** ( _float_ ) – 设置动画的相对时间，0 表示开始，1 表示结束。

返回类型

None


`update_mobjects(dt)`

更新诸如 starting_mobject 和（对于变换）target_mobject 之类的内容。请注意，由于通常（总是？） self.mobject 会在动画期间暂停其更新，因此这对 self.mobject None作用。

参数

**dt**（_float_）–

返回类型

None
