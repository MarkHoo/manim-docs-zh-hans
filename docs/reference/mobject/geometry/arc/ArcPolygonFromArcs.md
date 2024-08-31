# 弧多边形

合格名称：`manim.mobject.geometry.arc.ArcPolygonFromArcs`

```py
class ArcPolygonFromArcs(*arcs, **kwargs)
```

Bases: `VMobject`

允许用弧连接点的广义多边形。

该版本采用预定义的弧来生成弧多边形，并引入了一些新语法。但与它不同的是，`Polygon`它不能直接用点创建。

为了获得正确的外观，传递的弧应该无缝连接： `[a,b][b,c][c,a]`

如果圆弧之间有任何间隙，这些间隙将用直线填充，可以有意用于任何直线部分。圆弧也可以作为直线传递，例如用 初始化的圆弧`angle=0`。

参数

- **arcs** ( [_Arc_]() _|_ [_ArcBetweenPoints_]() ) – 这些是组装 arcpolygon 的弧。
- **kwargs** – 传递给 的构造函数的关键字参数 [`VMobject`]()。影响 ArcPolygon 本身的绘制方式，但不影响传递的弧。

弧线

用于初始化 ArcPolygonFromArcs 的弧：

```sh
>>> from manim import ArcPolygonFromArcs, Arc, ArcBetweenPoints
>>> ap = ArcPolygonFromArcs(Arc(), ArcBetweenPoints([1,0,0], [0,1,0]), Arc())
>>> ap.arcs
[Arc, ArcBetweenPoints, Arc]
```

> 提示

> 两个的实例也[`ArcPolygon`]()可以正确地相互转换。请注意，使用 初始化的任何圆弧`angle=0` 实际上都是直线，因此，如果直线部分应无缝转换为弧形部分，反之亦然，请使用可忽略的角度（例如 ）来初始化直线部分`angle=0.0001`。

> 笔记

> 有一个替代版本 ( [`ArcPolygon`]()) 可以用点实例化。

> 也可以看看

> [`ArcPolygon`]()

例子

弧形多边形的一个例子是鲁洛三角形。鲁洛三角形不是由 3 条直线连接外部点，而是由 3 条弧线连接这些点，形成宽度恒定的形状。

传递的弧作为子对象存储在 arcpolygon 中。这意味着弧与弧多边形一起改变，例如当它移动时，并且可以在弧多边形初始化后操作这些弧。

此外，还会绘制 中包含的弧[`ArcPolygonFromArcs`]()以及 arcpolygon 本身，这会影响[`Create`]() 例如中的绘制时间。在大多数情况下，弧线本身不需要绘制，在这种情况下，它们可以作为不可见的传递。

示例：ArcPolygon 示例

```py
from manim import *

class ArcPolygonExample(Scene):
    def construct(self):
        arc_conf = {"stroke_width": 0}
        poly_conf = {"stroke_width": 10, "stroke_color": BLUE,
              "fill_opacity": 1, "color": PURPLE}
        a = [-1, 0, 0]
        b = [1, 0, 0]
        c = [0, np.sqrt(3), 0]
        arc0 = ArcBetweenPoints(a, b, radius=2, **arc_conf)
        arc1 = ArcBetweenPoints(b, c, radius=2, **arc_conf)
        arc2 = ArcBetweenPoints(c, a, radius=2, **arc_conf)
        reuleaux_tri = ArcPolygonFromArcs(arc0, arc1, arc2, **poly_conf)
        self.play(FadeIn(reuleaux_tri))
        self.wait(2)
```

弧形多边形本身也可以隐藏，以便只绘制包含的弧。这可用于轻松调试弧或突出显示它们。

示例：ArcPolygonExample2 

```py
from manim import *

class ArcPolygonExample2(Scene):
    def construct(self):
        arc_conf = {"stroke_width": 3, "stroke_color": BLUE,
            "fill_opacity": 0.5, "color": GREEN}
        poly_conf = {"color": None}
        a = [-1, 0, 0]
        b = [1, 0, 0]
        c = [0, np.sqrt(3), 0]
        arc0 = ArcBetweenPoints(a, b, radius=2, **arc_conf)
        arc1 = ArcBetweenPoints(b, c, radius=2, **arc_conf)
        arc2 = ArcBetweenPoints(c, a, radius=2, stroke_color=RED)
        reuleaux_tri = ArcPolygonFromArcs(arc0, arc1, arc2, **poly_conf)
        self.play(FadeIn(reuleaux_tri))
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
