# 值追踪器

合格名称：`manim.mobject.value\_tracker.ValueTracker`


```py

```

可用于跟踪（实值）参数的 mobject。对于动画参数更改很有用。

并不意味着要显示。相反，位置编码一些数字，通常是另一个动画或 Continual_animation 用于其更新功能的数字，并且通过将其视为 mobject，它仍然可以像其他任何东西一样进行动画和操作。

使用语法进行动画处理时，该值会不断变化`animate`。

例子

示例：ValueTrackerExample [¶](#valuetrackerexample)

```py

```


笔记

您还可以将 ValueTracker 链接到更新程序。在这种情况下，您必须确保将 ValueTracker 添加到场景中`add`

示例：ValueTrackerExample [¶](#valuetrackerexample)


```py

```


方法

[`get_value`](#manim.mobject.value_tracker.ValueTracker.get_value "manim.mobject.value_tracker.ValueTracker.get_value")

获取此 ValueTracker 的当前值。

[`increment_value`](#manim.mobject.value_tracker.ValueTracker.increment_value "manim.mobject.value_tracker.ValueTracker.increment_value")

向 ValueTracker 递增（添加）标量值

[`interpolate`](#manim.mobject.value_tracker.ValueTracker.interpolate "manim.mobject.value_tracker.ValueTracker.interpolate")

将 self 转换为 mobject1 和 mobject2 之间的插值。

[`set_value`](#manim.mobject.value_tracker.ValueTracker.set_value "manim.mobject.value_tracker.ValueTracker.set_value")

为 ValueTracker 设置新的标量值

属性

`animate`

用于对 的任何方法的应用程序进行动画处理`self`。

`animation_overrides`

`depth`

对象的深度。

`height`

mobject 的高度。

`width`

mobject 的宽度。

获取值( )[\[来源\]](../_modules/manim/mobject/value_tracker.html#ValueTracker.get_value)[#](#manim.mobject.value_tracker.ValueTracker.get_value "此定义的固定链接")

获取此 ValueTracker 的当前值。

返回类型

漂浮

增量值（*d*值\_）[\[来源\]](../_modules/manim/mobject/value_tracker.html#ValueTracker.increment_value)[#](#manim.mobject.value_tracker.ValueTracker.increment_value "此定义的固定链接")

向 ValueTracker 递增（添加）标量值

参数

**d_value** (_浮点数_) –

插值（_mobject1_、 _mobject2_、 _alpha_、 _path_func=<函数 插值>_）[\[来源\]](../_modules/manim/mobject/value_tracker.html#ValueTracker.interpolate)[#](#manim.mobject.value_tracker.ValueTracker.interpolate "此定义的固定链接")

将 self 转换为 mobject1 和 mobject2 之间的插值。

设置值（_值_）[\[来源\]](../_modules/manim/mobject/value_tracker.html#ValueTracker.set_value)[#](#manim.mobject.value_tracker.ValueTracker.set_value "此定义的固定链接")

为 ValueTracker 设置新的标量值

参数

**值**（_浮点数_）–
