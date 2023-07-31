# 球体[#](#sphere "此标题的固定链接")

合格名称：`manim.mobject.three\_d.three\_dimensions.Sphere`

球体*类*（_中心= array(\[0., 0., 0.\])_，_半径= 1_，_分辨率= None_， _u_range = (0, 6.283185307179586)_， _v_range = (0, 3.141592653589793)_， _\*\* kwargs_ )[\[来源\]](../_modules/manim/mobject/three_d/three_dimensions.html#Sphere)[#](#manim.mobject.three_d.three_dimensions.Sphere "此定义的固定链接")

基地：[`Surface`](manim.mobject.three_d.three_dimensions.Surface.html#manim.mobject.three_d.three_dimensions.Surface "manim.mobject. Three_d. Three_dimensions.Surface")

三维球体。

参数

- **center** ( _Sequence_ _\[_ _float_ _\]_ ) – 的中心[`Sphere`](#manim.mobject.three_d.three_dimensions.Sphere "manim.mobject. Three_d. Three_dimensions.Sphere")。
- **radius** ( _float_ ) – 的半径[`Sphere`](#manim.mobject.three_d.three_dimensions.Sphere "manim.mobject. Three_d. Three_dimensions.Sphere")。
- **分辨率**( _Sequence_ _\[_ _int_ _\]_ ) – 所采集的样本数[`Sphere`](#manim.mobject.three_d.three_dimensions.Sphere "manim.mobject. Three_d. Three_dimensions.Sphere")。元组可用于分别定义`u`和的不同分辨率`v`。
- **u_range** ( _Sequence_ _\[_ _float_ _\]_ ) – 变量的范围`u`：。`(u_min, u_max)`
- **v_range** ( _Sequence_ _\[_ _float_ _\]_ ) – 变量的范围`v`：。`(v_min, v_max)`

例子

示例：ExampleSphere [¶](#examplesphere)

![../_images/ExampleSphere-1.png](../_images/ExampleSphere-1.png)

from manim import \*

class ExampleSphere(ThreeDScene):
def construct(self):
self.set_camera_orientation(phi=PI / 6, theta=PI / 6)
sphere1 = Sphere(
center=(3, 0, 0),
radius=1,
resolution=(20, 20),
u_range=\[0.001, PI - 0.001\],
v_range=\[0, TAU\]
)
sphere1.set_color(RED)
self.add(sphere1)
sphere2 = Sphere(center=(-1, -3, 0), radius=2, resolution=(18, 18))
sphere2.set_color(GREEN)
self.add(sphere2)
sphere3 = Sphere(center=(-1, 2, 0), radius=2, resolution=(16, 16))
sphere3.set_color(BLUE)
self.add(sphere3)

Copy to clipboard

方法

[`func`](#manim.mobject.three_d.three_dimensions.Sphere.func "manim.mobject. Three_d. Three_dimensions.Sphere.func")

定义所绘制的 z 值[`Sphere`](#manim.mobject.three_d.three_dimensions.Sphere "manim.mobject. Three_d. Three_dimensions.Sphere")。

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

函数（_u_， _v_）[\[来源\]](../_modules/manim/mobject/three_d/three_dimensions.html#Sphere.func)[#](#manim.mobject.three_d.three_dimensions.Sphere.func "此定义的固定链接")

定义所绘制的 z 值[`Sphere`](#manim.mobject.three_d.three_dimensions.Sphere "manim.mobject. Three_d. Three_dimensions.Sphere")。

退货

定义 的 z 值[`Sphere`](#manim.mobject.three_d.three_dimensions.Sphere "manim.mobject. Three_d. Three_dimensions.Sphere")。

返回类型

`numpy.array`

参数

- **u**（_浮动_）–
- **v**（_浮动_）–
