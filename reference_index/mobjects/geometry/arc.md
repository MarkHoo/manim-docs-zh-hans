# 弧

弯曲的物体。

例子

示例：有用的注释

![../_images/UsefulAnnotations-1.png](../_images/UsefulAnnotations-1.png)

from manim import \*

class UsefulAnnotations(Scene):
def construct(self):
m0 = Dot()
m1 = AnnotationDot()
m2 = LabeledDot("ii")
m3 = LabeledDot(MathTex(r"\\alpha").set_color(ORANGE))
m4 = CurvedArrow(2*LEFT, 2*RIGHT, radius= -5)
m5 = CurvedArrow(2*LEFT, 2*RIGHT, radius= 8)
m6 = CurvedDoubleArrow(ORIGIN, 2\*RIGHT)

        self.add(m0, m1, m2, m3, m4, m5, m6)
        for i, mobj in enumerate(self.mobjects):
            mobj.shift(DOWN * (i-3))

Copy to clipboard

课程

[`AnnotationDot`](manim.mobject.geometry.arc.AnnotationDot.html#manim.mobject.geometry.arc.AnnotationDot "manim.mobject.geometry.arc.AnnotationDot")

具有较大半径和粗笔画的点来注释场景。

[`AnnularSector`](manim.mobject.geometry.arc.AnnularSector.html#manim.mobject.geometry.arc.AnnularSector "manim.mobject.geometry.arc.AnnularSector")

参数内半径

环形扇区的内半径。

[`Annulus`](manim.mobject.geometry.arc.Annulus.html#manim.mobject.geometry.arc.Annulus "manim.mobject.geometry.arc.Annulus")

两个同心圆之间的区域[`Circles`](manim.mobject.geometry.arc.Circle.html#manim.mobject.geometry.arc.Circle "manim.mobject.geometry.arc.Circle")。

[`Arc`](manim.mobject.geometry.arc.Arc.html#manim.mobject.geometry.arc.Arc "manim.mobject.geometry.arc.Arc")

一个圆弧。

[`ArcBetweenPoints`](manim.mobject.geometry.arc.ArcBetweenPoints.html#manim.mobject.geometry.arc.ArcBetweenPoints "manim.mobject.geometry.arc.ArcBetweenPoints")

继承自 Arc，并另外获取弧跨越的 2 个点。

[`ArcPolygon`](manim.mobject.geometry.arc.ArcPolygon.html#manim.mobject.geometry.arc.ArcPolygon "manim.mobject.geometry.arc.ArcPolygon")

允许用弧连接点的广义多边形。

[`ArcPolygonFromArcs`](manim.mobject.geometry.arc.ArcPolygonFromArcs.html#manim.mobject.geometry.arc.ArcPolygonFromArcs "manim.mobject.geometry.arc.ArcPolygonFromArcs")

允许用弧连接点的广义多边形。

[`Circle`](manim.mobject.geometry.arc.Circle.html#manim.mobject.geometry.arc.Circle "manim.mobject.geometry.arc.Circle")

一个圆圈。

[`CubicBezier`](manim.mobject.geometry.arc.CubicBezier.html#manim.mobject.geometry.arc.CubicBezier "manim.mobject.geometry.arc.CubicBezier")

例子

[`CurvedArrow`](manim.mobject.geometry.arc.CurvedArrow.html#manim.mobject.geometry.arc.CurvedArrow "manim.mobject.geometry.arc.CurvedArrow")

[`CurvedDoubleArrow`](manim.mobject.geometry.arc.CurvedDoubleArrow.html#manim.mobject.geometry.arc.CurvedDoubleArrow "manim.mobject.geometry.arc.CurvedDoubleArrow")

[`Dot`](manim.mobject.geometry.arc.Dot.html#manim.mobject.geometry.arc.Dot "manim.mobject.geometry.arc.Dot")

一个半径很小的圆。

[`Ellipse`](manim.mobject.geometry.arc.Ellipse.html#manim.mobject.geometry.arc.Ellipse "manim.mobject.geometry.arc.Ellipse")

圆形；椭圆形、圆形。

[`LabeledDot`](manim.mobject.geometry.arc.LabeledDot.html#manim.mobject.geometry.arc.LabeledDot "manim.mobject.geometry.arc.LabeledDot")

A[`Dot`](manim.mobject.geometry.arc.Dot.html#manim.mobject.geometry.arc.Dot "manim.mobject.geometry.arc.Dot")的中心包含一个标签。

[`Sector`](manim.mobject.geometry.arc.Sector.html#manim.mobject.geometry.arc.Sector "manim.mobject.geometry.arc.Sector")

例子

[`TipableVMobject`](manim.mobject.geometry.arc.TipableVMobject.html#manim.mobject.geometry.arc.TipableVMobject "manim.mobject.geometry.arc.TipableVMobject")

用于圆弧和直线之间的共享功能。
