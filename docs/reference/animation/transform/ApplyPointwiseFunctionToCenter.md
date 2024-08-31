# 应用点向函数到中心

合格名称：`manim.animation.transform.ApplyPointwiseFunctionToCenter`

```py
class ApplyPointwiseFunctionToCenter(mobject=None, *args, use_override=True, **kwargs)
```

Bases: `ApplyPointwiseFunction`


方法

|||
|-|-|
[`begin`]()|开始动画。


属性

`path_arc`
`path_func`



`begin()`

开始动画。

该方法在动画播放时被调用。尽可能多的初始化，尤其是任何 mobject 复制，应该存在于这个方法中。

返回类型

None
