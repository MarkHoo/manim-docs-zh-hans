# 三次贝塞尔曲线

合格名称：`manim.mobject.geometry.arc.CubicBezier`

CubicBezier_类_（_start_anchor_、 _start_handle_、 _end_handle_、 _end_anchor_、 _\*\* kwargs_）[\[来源\]](../_modules/manim/mobject/geometry/arc.html#CubicBezier)[#](#manim.mobject.geometry.arc.CubicBezier "此定义的固定链接")

基地：[`VMobject`](manim.mobject.types.vectorized_mobject.VMobject.html#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject")

例子

示例：BezierSpline示例[¶](#beziersplineexample)

![../_images/BezierSplineExample-1.png](../_images/BezierSplineExample-1.png)

from manim import *

class BezierSplineExample(Scene):
    def construct(self):
        p1 = np.array(\[-3, 1, 0\])
        p1b = p1 + \[1, 0, 0\]
        d1 = Dot(point=p1).set_color(BLUE)
        l1 = Line(p1, p1b)
        p2 = np.array(\[3, -1, 0\])
        p2b = p2 - \[1, 0, 0\]
        d2 = Dot(point=p2).set_color(RED)
        l2 = Line(p2, p2b)
        bezier = CubicBezier(p1b, p1b + 3 * RIGHT, p2b - 3 * RIGHT, p2b)
        self.add(l1, d1, l2, d2, bezier)

Copy to clipboard

方法

  

属性

  

`animate`

用于对 的任何方法的应用程序进行动画处理`self`。

`animation_overrides`

`color`

`depth`

对象的深度。

`fill_color`

如果有多种颜色（对于渐变），则返回第一个颜色

`height`

mobject 的高度。

`n_points_per_curve`

`sheen_factor`

`stroke_color`

`width`

mobject 的宽度。