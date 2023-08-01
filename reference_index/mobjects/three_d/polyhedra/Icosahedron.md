# 二十面体

合格名称：`manim.mobject.three\_d.polyhedra.Icosahedron`

二十面*体类*（_edge_length = 1_， _\*\* kwargs_）[\[来源\]](../_modules/manim/mobject/three_d/polyhedra.html#Icosahedron)[#](#manim.mobject.three_d.polyhedra.Icosahedron "此定义的固定链接")

基地：[`Polyhedron`](manim.mobject.three_d.polyhedra.Polyhedron.html#manim.mobject.three_d.polyhedra.Polyhedron "manim.mobject.two_d.polyhedra.Polyhedron")

二十面体，五个柏拉图立体之一。它有 20 个面、30 条边和 12 个顶点。

参数

**edge_length** ( _float_ ) – 任意两个顶点之间的边的长度。

例子

示例：二十面体场景[¶](#icosahedronscene)

![../_images/二十面体Scene-1.png](../_images/IcosahedronScene-1.png)

from manim import \*

class IcosahedronScene(ThreeDScene):
def construct(self):
self.set*camera_orientation(phi=75 * DEGREES, theta=30 \_ DEGREES)
obj = Icosahedron()
self.add(obj)

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
