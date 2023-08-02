# 更新自函数

合格名称：`manim.animation.updaters.update.UpdateFromFunc`

```py
class UpdateFromFunc(mobject=None, *args, use_override=True, **kwargs)
```

Bases: Animation

update_function 形式为 func(mobject)，大概在一个 mobject 的状态依赖于另一个同时动画的 mobject 时使用


方法

|||
|-|-|
[`interpolate_mobject`]()|根据 alpha 值对 mobject 进行插值`Animation`。


interpolate*mobject (*阿尔法\_)

根据 alpha 值对 mobject 进行插值`Animation`。

参数

**alpha** ( _float_ ) – 0 到 1 之间的浮点数，表示动画完成的比例。例如，alpha 值 0、0.5 和 1 分别对应于动画完成的 0%、50% 和 100%。

返回类型

没有任何
