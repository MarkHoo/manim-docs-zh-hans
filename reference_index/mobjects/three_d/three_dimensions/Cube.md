# 立方体[#](#cube "此标题的固定链接")

合格名称：`manim.mobject.three\_d.three\_dimensions.Cube`

_立方体_ 类（_边长= 2_，_填充不透明度= 0.75_，_填充颜色= '#58C4DD'_，_描边宽度= 0_， _\*\* kwargs_）[\[来源\]](../_modules/manim/mobject/three_d/three_dimensions.html#Cube)[#](#manim.mobject.three_d.three_dimensions.Cube "此定义的固定链接")

基地：[`VGroup`](manim.mobject.types.vectorized_mobject.VGroup.html#manim.mobject.types.vectorized_mobject.VGroup "manim.mobject.types.vectorized_mobject.VGroup")

三维立方体。

参数

- **side_length** ( _float_ ) – 各边的长度[`Cube`](#manim.mobject.three_d.three_dimensions.Cube "manim.mobject. Three_d. Three_dimensions.Cube")。
- **fill_opacity** ( _float_ ) – 的不透明度[`Cube`](#manim.mobject.three_d.three_dimensions.Cube "manim.mobject. Three_d. Three_dimensions.Cube")，从 0 表示完全透明到 1 表示完全不透明。默认为 0.75。
- **fill_color** ( _Color_ ) – 的颜色[`Cube`](#manim.mobject.three_d.three_dimensions.Cube "manim.mobject. Three_d. Three_dimensions.Cube")。
- **stroke_width** ( _float_ ) – 围绕每个面的描边宽度[`Cube`](#manim.mobject.three_d.three_dimensions.Cube "manim.mobject. Three_d. Three_dimensions.Cube")。

例子

示例：Cube 示例[¶](#cubeexample)

![../_images/CubeExample-1.png](../_images/CubeExample-1.png)

from manim import \*

class CubeExample(ThreeDScene):
def construct(self):
self.set_camera_orientation(phi=75*DEGREES, theta=-45*DEGREES)

        axes = ThreeDAxes()
        cube = Cube(side_length=3, fill_opacity=0.7, fill_color=BLUE)
        self.add(cube)

Copy to clipboard

方法

[`generate_points`](#manim.mobject.three_d.three_dimensions.Cube.generate_points "manim.mobject. Three_d. Three_dimensions.Cube.generate_points")

创建 的侧面[`Cube`](#manim.mobject.three_d.three_dimensions.Cube "manim.mobject. Three_d. Three_dimensions.Cube")。

[`init_points`](#manim.mobject.three_d.three_dimensions.Cube.init_points "manim.mobject. Three_d. Three_dimensions.Cube.init_points")

创建 的侧面[`Cube`](#manim.mobject.three_d.three_dimensions.Cube "manim.mobject. Three_d. Three_dimensions.Cube")。

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

生成点( )[\[来源\]](../_modules/manim/mobject/three_d/three_dimensions.html#Cube.generate_points)[#](#manim.mobject.three_d.three_dimensions.Cube.generate_points "此定义的固定链接")

创建 的侧面[`Cube`](#manim.mobject.three_d.three_dimensions.Cube "manim.mobject. Three_d. Three_dimensions.Cube")。

返回类型

没有任何

初始化点（）[#](#manim.mobject.three_d.three_dimensions.Cube.init_points "此定义的固定链接")

创建 的侧面[`Cube`](#manim.mobject.three_d.three_dimensions.Cube "manim.mobject. Three_d. Three_dimensions.Cube")。

返回类型

没有任何
