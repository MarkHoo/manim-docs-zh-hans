# UpdateFromAlphaFunc

合格名称：`manim.animation.updaters.update.UpdateFromAlphaFunc`

```py
class UpdateFromAlphaFunc(mobject=None, *args, use_override=True, **kwargs)
```

Bases: `UpdateFromFunc`


方法

|||
|-|-|
[`interpolate_mobject`]()|根据 alpha 值对`Animation`的 mobject 进行插值。




`interpolate_mobject(alpha)`

根据 alpha 值对`Animation`的 mobject 进行插值。

参数

**alpha** ( _float_ ) – 0 到 1 之间的浮点数，表示动画完成的比例。例如，alpha 值 0、0.5 和 1 分别对应于动画完成的 0%、50% 和 100%。

返回类型

None
