# 复杂值追踪器

合格名称：`manim.mobject.value\_tracker.ComplexValueTracker`


```py

```

跟踪复值参数。

当通过 设置该值时`animate`，该值将从源点到目标点采取直线路径。

例子

示例：ComplexValueTrackerExample [¶](#complexvaluetrackerexample)

```py

```


方法

[`get_value`](#manim.mobject.value_tracker.ComplexValueTracker.get_value "manim.mobject.value_tracker.ComplexValueTracker.get_value")

获取此值跟踪器的当前值（复数形式）。

[`set_value`](#manim.mobject.value_tracker.ComplexValueTracker.set_value "manim.mobject.value_tracker.ComplexValueTracker.set_value")

为 ComplexValueTracker 设置新的复数值

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

获取值( )[\[来源\]](../_modules/manim/mobject/value_tracker.html#ComplexValueTracker.get_value)[#](#manim.mobject.value_tracker.ComplexValueTracker.get_value "此定义的固定链接")

获取此值跟踪器的当前值（复数形式）。

该值在内部存储为点数组 \[a, b, 0\]。可以直接访问它以几何方式表示值，请参阅使用示例。

设置值( _z_ )[\[来源\]](../_modules/manim/mobject/value_tracker.html#ComplexValueTracker.set_value)[#](#manim.mobject.value_tracker.ComplexValueTracker.set_value "此定义的固定链接")

为 ComplexValueTracker 设置新的复数值
