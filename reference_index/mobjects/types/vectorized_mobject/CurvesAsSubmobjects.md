# 曲线作为子对象

合格名称：`manim.mobject.types.vectorized\_mobject.CurvesAsSubmobjects`


```py
class CurvesAsSubmobjects(vmobject, **kwargs)
```

Bases: `VGroup`

将曲线的元素转换为子对象。

例子

示例：LineGradientExample

![LineGradientExample-1.png](../../static/LineGradientExample-1.png)

```py
from manim import *

class LineGradientExample(Scene):
    def construct(self):
        curve = ParametricFunction(lambda t: [t, np.sin(t), 0], t_range=[-PI, PI, 0.01], stroke_width=10)
        new_curve = CurvesAsSubmobjects(curve)
        new_curve.set_color_by_gradient(BLUE, RED)
        self.add(new_curve.shift(UP), curve)
```


方法



属性

|||
|-|-|
`animate`|用于对 的任何方法的应用程序进行动画处理`self`。
`animation_overrides`|
`color`|
`depth`|对象的深度。
`fill_color`|如果有多种颜色（对于渐变），则返回第一个颜色
`height`|mobject 的高度。
`n_points_per_curve`|
`sheen_factor`|
`stroke_color`|
`width`|mobject 的宽度。
