# 从复制转换

合格名称：`manim.animation.transform.TransformFromCopy`

```py
class TransformFromCopy(mobject=None, *args, use_override=True, **kwargs)
```

Bases: `Transform`

执行反向变换


方法

|||
|-|-|
[`interpolate`]()|设置动画进度。


属性

`path_arc`
`path_func`



`interpolate(alpha)`

设置动画进度。

动画期间的每一帧都会调用此方法。

参数

**alpha** ( _float_ ) – 设置动画的相对时间，0 表示开始，1 表示结束。

返回类型

None
