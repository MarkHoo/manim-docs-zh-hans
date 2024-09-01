# 动态数字

合格名称：`manim.animation.numbers.ChangingDecimal`

```py
class ChangingDecimal(mobject=None, *args, use_override=True, **kwargs)
```

Bases: `Animation`

方法

|||
|-|-|
`check_validity_of_input`|
[`interpolate_mobject`]()|根据 alpha 值对 mobject 进行插值`Animation`。



`interpolate_mobject(alpha)`

根据 alpha 值对 mobject 进行插值`Animation`。

参数

**alpha** ( _float_ ) – 0 到 1 之间的浮点数，表示动画完成的比例。例如，alpha 值 0、0.5 和 1 分别对应于动画完成的 0%、50% 和 100%。

返回类型

None
