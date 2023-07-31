# 角柱体

合格名称：`manim.mobject.three\_d.three\_dimensions.Prism`

Prism*类*（_维度= \[3, 2, 1\]_ , _\*\* kwargs_）[\[来源\]](../_modules/manim/mobject/three_d/three_dimensions.html#Prism)[#](#manim.mobject.three_d.three_dimensions.Prism "此定义的固定链接")

基地：[`Cube`](manim.mobject.three_d.three_dimensions.Cube.html#manim.mobject.three_d.three_dimensions.Cube "manim.mobject. Three_d. Three_dimensions.Cube")

直立长方体（或长方体）。由格式中每边的长度定义。`[x, y, z]`

参数

**Dimensions** ( _Sequence_ _\[_ _int_ _\]_ ) – [`Prism`](#manim.mobject.three_d.three_dimensions.Prism "manim.mobject. Three_d. Three_dimensions.Prism")in 格式的维度。`[x, y, z]`

例子

示例：ExamplePrism [¶](#exampleprism)

![../_images/ExamplePrism-1.png](../_images/ExamplePrism-1.png)

from manim import \*

class ExamplePrism(ThreeDScene):
def construct(self):
self.set*camera_orientation(phi=60 * DEGREES, theta=150 \_ DEGREES)
prismSmall = Prism(dimensions=\[1, 2, 3\]).rotate(PI / 2)
prismLarge = Prism(dimensions=\[1.5, 3, 4.5\]).move_to(\[2, 0, 0\])
self.add(prismSmall, prismLarge)

Copy to clipboard

方法

[`generate_points`](#manim.mobject.three_d.three_dimensions.Prism.generate_points "manim.mobject. Three_d. Three_dimensions.Prism.generate_points")

创建 的侧面[`Prism`](#manim.mobject.three_d.three_dimensions.Prism "manim.mobject. Three_d. Three_dimensions.Prism")。

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

生成点( )[\[来源\]](../_modules/manim/mobject/three_d/three_dimensions.html#Prism.generate_points)[#](#manim.mobject.three_d.three_dimensions.Prism.generate_points "此定义的固定链接")

创建 的侧面[`Prism`](#manim.mobject.three_d.three_dimensions.Prism "manim.mobject. Three_d. Three_dimensions.Prism")。

返回类型

没有任何