# 圆弧多边形

合格名称：`manim.mobject.geometry.arc.ArcPolygon`

```py
class ArcPolygon(*vertices, angle=0.7853981633974483, radius=None, arc_config=None, **kwargs)
```

Bases: `VMobject`

允许用弧连接点的广义多边形。

这个版本试图坚持接近`Polygon`使用的方式。可以直接将点传递给它，用于生成相应的弧（使用[`ArcBetweenPoints`]()）。可以将角度或半径传递给它以在所有弧上使用，但要单独配置弧，`arc_config`必须使用下面解释的语法传递列表。

参数

- **vertices** ( _list_ _|_ _np.ndarray_ ) – 弧线段的顶点、起点和终点的列表。
- **angle** ( _float_ ) – 用于构建弧线的角度。如果没有设置其他参数，则使用该角度来构造所有圆弧。
- **radius** ( _float_ _|_ _None_ ) – 用于构造圆弧的圆半径。如果指定，则覆盖指定的`angle`.
- **arc_config** ( _list_ _\[_ _dict_ _\]_ _|_ _None_ ) – 传递 a 时`dict`，其内容将作为关键字参数传递给[`ArcBetweenPoints`](). 否则，可以传递包含作为每个单独弧的关键字参数传递的值的字典列表。
- **kwargs** – 传递给 的构造函数的更多关键字参数 [`VMobject`]()。

弧线

根据输入参数创建的弧：

```sh
>>> from manim import ArcPolygon
>>> ap = ArcPolygon([0, 0, 0], [2, 0, 0], [0, 2, 0])
>>> ap.arcs
[ArcBetweenPoints, ArcBetweenPoints, ArcBetweenPoints]
```

类型

`list`

> 提示

> 两个的实例也[`ArcPolygon`]()可以正确地相互转换。请注意，使用 初始化的任何圆弧`angle=0` 实际上都是直线，因此，如果直线部分应无缝转换为弧形部分，反之亦然，请使用可忽略的角度（例如 ）来初始化直线部分`angle=0.0001`。

> 笔记

> 有一个替代版本 ( [`ArcPolygonFromArcs`]())，它使用预定义的弧进行实例化。

> 也可以看看

> [`ArcPolygonFromArcs`]()

例子

示例：几个 ArcPolygons

```py
from manim import *

class SeveralArcPolygons(Scene):
    def construct(self):
        a = [0, 0, 0]
        b = [2, 0, 0]
        c = [0, 2, 0]
        ap1 = ArcPolygon(a, b, c, radius=2)
        ap2 = ArcPolygon(a, b, c, angle=45*DEGREES)
        ap3 = ArcPolygon(a, b, c, arc_config={'radius': 1.7, 'color': RED})
        ap4 = ArcPolygon(a, b, c, color=RED, fill_opacity=1,
                                    arc_config=[{'radius': 1.7, 'color': RED},
                                    {'angle': 20*DEGREES, 'color': BLUE},
                                    {'radius': 1}])
        ap_group = VGroup(ap1, ap2, ap3, ap4).arrange()
        self.play(*[Create(ap) for ap in [ap1, ap2, ap3, ap4]])
        self.wait()
```

有关更多示例，请参见[`ArcPolygonFromArcs`]()。


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
