# 等待

合格名称：`manim.animation.animation.Wait`

```py
class Wait(mobject=None, *args, use_override=True, **kwargs)
```

Bases: `Animation`

“无操作”动画。

参数

- **run_time** – 应该经过的时间量。
- **stop_condition** – 没有位置参数、计算结果为布尔值的函数。渲染每个新帧后都会评估该函数。在返回值为 true 或指定时间`run_time`结束后，播放动画停止。
- **freeze_frame** – 控制等待动画是否是静态的，即对应于冻结帧。如果`False`通过，渲染循环仍然像往常一样在动画中进行，并且（除其他外）继续调用更新程序函数。如果`None`（默认值），则[`Scene.play()`]()调用尝试通过 确定 Wait 调用本身是否可以是静态的`Scene.should_mobjects_update()`。
- **kwargs** – 要传递给父类的关键字参数[`Animation`]()。

方法

|||
|-|-|
|[`begin`]()|开始动画。|
|[`clean_up_from_scene`]()|[`Scene`]()完成动画后清理。|
|[`finish`]()|完成动画。|
|[`interpolate`]()|设置动画进度。|
|[`update_mobjects`]()|更新诸如 starting_mobject 和（对于变换）target_mobject 之类的内容。|



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
