# 环面

合格名称：`manim.mobject.three\_d.three\_dimensions.Torus`

环面*类*（_major_radius = 3_， _minor_radius = 1_， _u_range = （ 0，6.283185307179586）_， _v_range = （ 0，6.283185307179586）_，_分辨率= None_， _\*\* kwargs_）[\[来源\]](../_modules/manim/mobject/three_d/three_dimensions.html#Torus)[#](#manim.mobject.three_d.three_dimensions.Torus "此定义的固定链接")

基地：[`Surface`](manim.mobject.three_d.three_dimensions.Surface.html#manim.mobject.three_d.three_dimensions.Surface "manim.mobject. Three_d. Three_dimensions.Surface")

一个环面。

参数

- **Major_radius** ( _float_ ) – 从管中心到圆环中心的距离。
- **secondary_radius** ( _float_ ) – 管的半径。
- **u_range** ( _Sequence_ _\[_ _float_ _\]_ ) – 变量的范围`u`：。`(u_min, u_max)`
- **v_range** ( _Sequence_ _\[_ _float_ _\]_ ) – 变量的范围`v`：。`(v_min, v_max)`
- **分辨率**( _Sequence_ _\[_ _int_ _\]_ ) – 所采集的样本数[`Torus`](#manim.mobject.three_d.three_dimensions.Torus "manim.mobject. Three_d. Three_dimensions.Torus")。元组可用于分别定义`u`和的不同分辨率`v`。

例子

示例：ExampleTorus [¶](#exampletorus)

![../_images/ExampleTorus-1.png](../_images/ExampleTorus-1.png)

from manim import \*

class ExampleTorus(ThreeDScene):
def construct(self):
axes = ThreeDAxes()
torus = Torus()
self.set*camera_orientation(phi=75 * DEGREES, theta=30 \_ DEGREES)
self.add(axes, torus)

Copy to clipboard

方法

[`func`](#manim.mobject.three_d.three_dimensions.Torus.func "manim.mobject. Three_d. Three_dimensions.Torus.func")

定义所绘制的 z 值[`Torus`](#manim.mobject.three_d.three_dimensions.Torus "manim.mobject. Three_d. Three_dimensions.Torus")。

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

函数（_u_， _v_）[\[来源\]](../_modules/manim/mobject/three_d/three_dimensions.html#Torus.func)[#](#manim.mobject.three_d.three_dimensions.Torus.func "此定义的固定链接")

定义所绘制的 z 值[`Torus`](#manim.mobject.three_d.three_dimensions.Torus "manim.mobject. Three_d. Three_dimensions.Torus")。

退货

定义 的 z 值[`Torus`](#manim.mobject.three_d.three_dimensions.Torus "manim.mobject. Three_d. Three_dimensions.Torus")。

返回类型

`numpy.ndarray`

参数

- **u**（_浮动_）–
- **v**（_浮动_）–
