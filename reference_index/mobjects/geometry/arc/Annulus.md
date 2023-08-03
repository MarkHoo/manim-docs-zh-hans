# 环带

合格名称：`manim.mobject.geometry.arc.Annulus`

```py
class Annulus(inner_radius=1, outer_radius=2, fill_opacity=1, stroke_width=0, color='#FFFFFF', mark_paths_closed=False, **kwargs)
```

Bases: Circle

两个同心圆之间的区域[`Circles`]()。

参数

- **inner_radius** ( _float_ _|_ _None_ ) – 内部的半径[`Circle`]()。
- **outer_radius** ( _float_ _|_ _None_ ) – 外部的半径[`Circle`]()。
- **kwargs** – 要传递给的附加参数[`Annulus`]()

例子

示例： Annulus 示例

![AnnulusExample-1.png](../../static/AnnulusExample-1.png)

```py
from manim import *

class AnnulusExample(Scene):
    def construct(self):
        annulus_1 = Annulus(inner_radius=0.5, outer_radius=1).shift(UP)
        annulus_2 = Annulus(inner_radius=0.3, outer_radius=0.6, color=RED).next_to(annulus_1, DOWN)
        self.add(annulus_1, annulus_2)
```

方法

|||
|-|-|
[`generate_points`]()|初始化`points`并因此初始化形状。
[`init_points`]()|初始化`points`并因此初始化形状。

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


`generate_points()`

初始化`points`并因此初始化形状。

被创造召唤。这是一个空方法，可以由子类实现。

`init_points()`

初始化`points`并因此初始化形状。

被创造召唤。这是一个空方法，可以由子类实现。
