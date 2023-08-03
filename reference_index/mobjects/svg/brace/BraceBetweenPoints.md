# 点之间的大括号

合格名称：`manim.mobject.svg.brace.BraceBetweenPoints`


```py
class BraceBetweenPoints(point_1, point_2, direction=array([0., 0., 0.]), **kwargs)
```

Bases: `Brace`

与 Brace 类似，但它不使用 mobject，而是使用 2 个点来放置支架。

计算支架的安装方向，但仍然可以手动覆盖它。如果点从左到右，则从下方绘制支撑。交换点会将支撑放在另一侧。

参数

- **point_1** ( _Sequence_ _\[_ _float_ _\]_ _|_ _None_ ) – 第一个点。
- **point_2** ( _Sequence_ _\[_ _float_ _\]_ _|_ _None_ ) – 第二个点。
- **Direction** ( _Sequence_ _\[_ _float_ _\]_ _|_ _None_ ) – 支撑面向点的方向。

例子

示例：BraceBP 示例

```py
from manim import *

class BraceBPExample(Scene):
    def construct(self):
        p1 = [0,0,0]
        p2 = [1,2,0]
        brace = BraceBetweenPoints(p1,p2)
        self.play(Create(NumberPlane()))
        self.play(Create(brace))
        self.wait(2)
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
