# 动画

合格名称：`manim.animation.animation.Animation`

```py
class Animation(mobject=None, *args, use_override=True, **kwargs)
```

Bases: `object`

一部动画。

动画有固定的时间跨度。

参数

- **mobject** – 要动画的 mobject。并非所有类型的动画都需要这样做。
- **lag_ratio**–

  定义动画应用于子对象之前的延迟。此延迟与动画的持续时间相关。

  这不会影响动画的总运行时间。相反，会调整各个动画的运行时间，以便完整的动画具有定义的运行时间。

- **run_time** – 动画的持续时间（以秒为单位）。
- **rate_func**–

  该函数根据相对运行时间定义动画进度（请参阅 [`rate_functions`]()）。

  例如`rate_func(0.5)`，动画运行时间一半后完成的动画比例。



`reverse_rate_function`

反转动画的速率函数。设置对或`reverse_rate_function` None影响。如果介绍者动画应转变为移除者动画，则需要明确设置这些，反之亦然。` remover``introducer `



`name`

动画的名称。这会在渲染动画时显示。默认为 <类名>(<Mobject-name>)。


`remover`

在此动画之后是否应从场景中删除给定的对象。


`suspend_mobject_updating`

动画期间是否应暂停 mobject 的更新程序。


> 笔记

> 在此类的当前实现中，指定的速率函数在调用中应用，[`Animation.interpolate_mobject()`]()作为调用的一部分 `Animation.interpolate_submobject()`。对于[`Animation`]() 通过重写实现的子类[`interpolate_mobject()`]()，必须手动应用速率函数（例如，通过传递`self.rate_func(alpha)`而不是仅仅`alpha`）。


例子

示例：滞后比率

```py
from manim import *

class LagRatios(Scene):
    def construct(self):
        ratios = [0, 0.1, 0.5, 1, 2]  # demonstrated lag_ratios

        # Create dot groups
        group = VGroup(*[Dot() for _ in range(4)]).arrange_submobjects()
        groups = VGroup(*[group.copy() for _ in ratios]).arrange_submobjects(buff=1)
        self.add(groups)

        # Label groups
        self.add(Text("lag_ratio = ", font_size=36).next_to(groups, UP, buff=1.5))
        for group, ratio in zip(groups, ratios):
            self.add(Text(str(ratio), font_size=36).next_to(group, UP))

        #Animate groups with different lag_ratios
        self.play(AnimationGroup(*[
            group.animate(lag_ratio=ratio, run_time=1.5).shift(DOWN * 2)
            for group, ratio in zip(groups, ratios)
        ]))

        # lag_ratio also works recursively on nested submobjects:
        self.play(groups.animate(run_time=1, lag_ratio=0.1).shift(UP * 2))
```

方法


|||
|-|-|
[`begin`]()|开始动画。
[`clean_up_from_scene`]()|[`Scene`]()完成动画后清理。
[`copy`]()|创建动画的副本。
`create_starting_mobject`|
[`finish`]()|完成动画。
`get_all_families_zipped`|
[`get_all_mobjects`]()|获取动画中涉及的所有 mobject。
[`get_all_mobjects_to_update`]()|获取所有要在动画期间更新的 mobject。
[`get_rate_func`]()|获取动画的速率函数。
[`get_run_time`]()|获取动画的运行时间。
[`get_sub_alpha`]()|获取任何子对象子动画的动画进度。
[`interpolate`]()|设置动画进度。
[`interpolate_mobject`]()|根据 alpha 值对 mobject 进行插值[`Animation`]()。
`interpolate_submobject`|
[`is_introducer`]()|测试动画是否是介绍人。
[`is_remover`]()|测试动画是否是移除器。
[`set_name`]()|设置动画的名称。
[`set_rate_func`]()|设置动画的速率函数。
[`set_run_time`]()|设置动画的运行时间。
[`update_mobjects`]()|更新诸如 starting_mobject 和（对于变换）target_mobject 之类的内容。



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


`copy()`

创建动画的副本。

返回

`self`的副本

返回类型

[Animation]()


`finish()`

完成动画。

动画结束时会调用此方法。

返回类型

None


`get_all_mobjects()`

获取动画中涉及的所有 mobject。

顺序必须与 interpolate_submobject 的参数顺序匹配

返回

mobject 的序列。

返回类型

Sequence\[ [Mobject]() \]


`get_all_mobjects_to_update()`

获取所有要在动画期间更新的 mobject。

返回

动画期间要更新的 mobject 列表。

返回类型

List\[ [Mobject]() \]


`get_rate_func()`

获取动画的速率函数。

返回

动画的速率函数。

返回类型

Callable\[\[float\], float\]


`get_run_time()`

获取动画的运行时间。

返回

动画所花费的时间（以秒为单位）。

返回类型

float


`get_sub_alpha(alpha, index, num_submobjects)`

获取任何子对象子动画的动画进度。

参数

- **alpha** ( _float_ ) – 整体动画进度
- **index** ( _int_ ) – 子动画的索引。
- **num_submobjects** ( _int_ ) – 子动画的总数。

返回

子动画的进度。

返回类型

float


`interpolate(alpha)`

设置动画进度。

动画期间的每一帧都会调用此方法。

参数

**alpha** ( _float_ ) – 设置动画的相对时间，0 表示开始，1 表示结束。

返回类型

None


`interpolate_mobject(alpha)`

根据 alpha 值对 mobject 进行插值[`Animation`]()。

参数

**alpha** ( _float_ ) – 0 到 1 之间的浮点数，表示动画完成的比例。例如，alpha 值 0、0.5 和 1 分别对应于动画完成的 0%、50% 和 100%。

返回类型

None


`is_introducer()`

测试动画是否是介绍人。

返回

`True`如果动画是介绍人，`False`否则。

返回类型

bool


`is_remover()`

测试动画是否是移除器。

返回

`True`如果动画是去除剂，`False`否则。

返回类型

bool


`set_name(name)`

设置动画的名称。

参数

**name** ( _str_ ) – 动画的新名称。

返回

`self`

返回类型

[Animation]()


`set_rate_func(rate_func)`

设置动画的速率函数。

参数

**rate_func** ( _Callable_ _\[_ _\[_ _float_ _\]_ _,_ _float_ _\]_ ) – 根据相对运行时间定义动画进度的新函数（请参阅[`rate_functions`]()）。

返回

`self`

返回类型

[Animation]()


`set_run_time(run_time)`

设置动画的运行时间。

参数

- **run_time** ( _float_ ) – 动画应花费的新时间（以秒为单位）。
- **注意::** ( _.._ ) – 动画运行时不应更改其运行时间。

返回

`self`

返回类型

[Animation]()



`update_mobjects(dt)`

更新诸如 starting_mobject 和（对于变换）target_mobject 之类的内容。请注意，由于通常（总是？） self.mobject 会在动画期间暂停其更新，因此这对 self.mobject None作用。

参数

**dt**（_float_）–

返回类型

None
