# 动画组

合格名称：`manim.animation.composition.AnimationGroup`

```py
class AnimationGroup(mobject=None, *args, use_override=True, **kwargs)
```

Bases: Animation

播放一组或一系列的[`Animation`]().

参数

- **animations**[`Animation`]()–要播放的对象序列。
- **group**– 一组多个[`Mobject`]().
- **run_time** – 动画的持续时间（以秒为单位）。
- **rate_func** – 根据相对运行时间定义动画进度的函数（请参阅[`rate_functions`]()）。
- **lag_ratio**–

  定义动画应用于子对象之前的延迟。lag_ratio `n.nn`表示当前动画播放完毕后将播放`nnn%`下一个动画。默认为 0.0，表示所有动画将一起播放。

  这不会影响动画的总运行时间。相反，会调整各个动画的运行时间，以便完整的动画具有定义的运行时间。

方法

|||
|-|-|
[`begin`](")|开始动画。
[`build_animations_with_timings`]()|创建 (anim, start_time, end_time) 形式的三元组列表。
[`clean_up_from_scene`]()|[`Scene`]()完成动画后清理。
[`finish`]()|完成动画。
[`get_all_mobjects`]()|获取动画中涉及的所有 mobject。
[`init_run_time`]()|如果与 不同，则计算动画的运行时间`run_time`。
[`interpolate`]()|设置动画进度。
[`update_mobjects`]()|更新诸如 starting_mobject 和（对于变换）target_mobject 之类的内容。



开始( )

开始动画。

该方法在动画播放时被调用。尽可能多的初始化，尤其是任何 mobject 复制，应该存在于这个方法中。

返回类型

没有任何

build_animations_with_timings ( )

创建 (anim, start_time, end_time) 形式的三元组列表。

返回类型

没有任何

clean_up_from*scene（*场景\_）

[`Scene`](manim.scene.scene.Scene.html#manim.scene.scene.Scene "手动场景.场景.场景")完成动画后清理。

如果动画是移除器，则这包括[`remove()`]()动画 [`Mobject`]()。

参数

**scene** ( [_Scene_]() ) – 应清除动画的场景。

返回类型

没有任何

完成( )

完成动画。

动画结束时会调用此方法。

返回类型

没有任何

获取所有对象( )

获取动画中涉及的所有 mobject。

顺序必须与 interpolate_submobject 的参数顺序匹配

退货

mobject 的序列。

返回类型

序列\[ [Mobject]() \]

初始化运行时间（_运行时间_）

如果与 不同，则计算动画的运行时间`run_time`。

参数

**run_time** – 动画的持续时间（以秒为单位）。

退货

动画的持续时间（以秒为单位）。

返回类型

运行

插值(_阿尔法_)

设置动画进度。

动画期间的每一帧都会调用此方法。

参数

**alpha** ( _float_ ) – 设置动画的相对时间，0 表示开始，1 表示结束。

返回类型

没有任何

update*mobjects ( \_dt* )

更新诸如 starting_mobject 和（对于变换）target_mobject 之类的内容。请注意，由于通常（总是？） self.mobject 会在动画期间暂停其更新，因此这对 self.mobject 没有任何作用。

参数

**dt**（_浮动_）–

返回类型

没有任何
