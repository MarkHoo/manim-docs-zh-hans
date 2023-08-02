# 等待

合格名称：`manim.animation.animation.Wait`

```py
class Wait(mobject=None, *args, use_override=True, **kwargs)
```

Bases: Animation

“无操作”动画。

参数

- **run_time** – 应该经过的时间量。
- **stop_condition** – 没有位置参数、计算结果为布尔值的函数。渲染每个新帧后都会评估该函数。在返回值为 true 或指定时间`run_time`结束后，播放动画停止。
- **freeze_frame** – 控制等待动画是否是静态的，即对应于冻结帧。如果`False`通过，渲染循环仍然像往常一样在动画中进行，并且（除其他外）继续调用更新程序函数。如果`None`（默认值），则[`Scene.play()`](manim.scene.scene.Scene.html#manim.scene.scene.Scene.play "manim.场景.场景.场景.play")调用尝试通过 确定 Wait 调用本身是否可以是静态的`Scene.should_mobjects_update()`。
- **kwargs** – 要传递给父类的关键字参数[`Animation`](manim.animation.animation.Animation.html#manim.animation.animation.Animation "manim.animation.animation.Animation")。

方法

|||
|-|-|
|[`begin`](#manim.animation.animation.Wait.begin "manim.animation.animation.Wait.begin")|开始动画。|
|[`clean_up_from_scene`](#manim.animation.animation.Wait.clean_up_from_scene "manim.animation.animation.Wait.clean_up_from_scene")|[`Scene`](manim.scene.scene.Scene.html#manim.scene.scene.Scene "手动场景.场景.场景")完成动画后清理。|
|[`finish`](#manim.animation.animation.Wait.finish "manim.animation.animation.Wait.finish")|完成动画。|
|[`interpolate`](#manim.animation.animation.Wait.interpolate "manim.animation.animation.Wait.interpolate")|设置动画进度。|
|[`update_mobjects`](#manim.animation.animation.Wait.update_mobjects "manim.animation.animation.Wait.update_mobjects")|更新诸如 starting_mobject 和（对于变换）target_mobject 之类的内容。|



开始( )

开始动画。

该方法在动画播放时被调用。尽可能多的初始化，尤其是任何 mobject 复制，应该存在于这个方法中。

返回类型

没有任何

clean_up_from*scene（*场景\_）

[`Scene`](manim.scene.scene.Scene.html#manim.scene.scene.Scene "手动场景.场景.场景")完成动画后清理。

如果动画是移除器，则这包括[`remove()`](manim.scene.scene.Scene.html#manim.scene.scene.Scene.remove "manim.scene.scene.Scene.remove")动画 [`Mobject`](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject")。

参数

**scene** ( [_Scene_](manim.scene.scene.Scene.html#manim.scene.scene.Scene "手动场景.场景.场景") ) – 应清除动画的场景。

返回类型

没有任何

完成( )[\[来源\]](../_modules/manim/animation/animation.html#Wait.finish)[#](#manim.animation.animation.Wait.finish "此定义的固定链接")

完成动画。

动画结束时会调用此方法。

返回类型

没有任何

插值(_阿尔法_)[\[来源\]](../_modules/manim/animation/animation.html#Wait.interpolate)[#](#manim.animation.animation.Wait.interpolate "此定义的固定链接")

设置动画进度。

动画期间的每一帧都会调用此方法。

参数

**alpha** ( _float_ ) – 设置动画的相对时间，0 表示开始，1 表示结束。

返回类型

没有任何

update*mobjects ( \_dt* )[\[来源\]](../_modules/manim/animation/animation.html#Wait.update_mobjects)[#](#manim.animation.animation.Wait.update_mobjects "此定义的固定链接")

更新诸如 starting_mobject 和（对于变换）target_mobject 之类的内容。请注意，由于通常（总是？） self.mobject 会在动画期间暂停其更新，因此这对 self.mobject 没有任何作用。

参数

**dt**（_浮动_）–

返回类型

没有任何
