# 圆柱

合格名称：`manim.mobject.three\_d.three\_dimensions.Cylinder`

_类_ Cylinder (_半径= 1_ ,_高度= 2_ ,_方向= array(\[0., 0., 1.\])_ , _v_range = \[0, 6.283185307179586\]_ , _show_ends = True_ ,_分辨率= (24, 24)_ , _\*\* kwargs_）[\[来源\]](../_modules/manim/mobject/three_d/three_dimensions.html#Cylinder)[#](#manim.mobject.three_d.three_dimensions.Cylinder "此定义的固定链接")

基地：[`Surface`](manim.mobject.three_d.three_dimensions.Surface.html#manim.mobject.three_d.three_dimensions.Surface "manim.mobject. Three_d. Three_dimensions.Surface")

圆柱体，由其高度、半径和方向定义，

参数

- **radius** ( _float_ ) – 圆柱体的半径。
- **height** ( _float_ ) – 圆柱体的高度。
- **Direction** ( _np.ndarray_ ) – 圆柱体中心轴的方向。
- **v_range** ( _Sequence_ _\[_ _float_ _\]_ ) – 沿高度轴（由方向给出）开始和结束的高度。
- **show_ends** ( _bool_ ) – 是否显示端盖。
- **分辨率**( _Sequence_ _\[_ _int_ _\]_ ) – 所采集的样本数[`Cylinder`](#manim.mobject.three_d.three_dimensions.Cylinder "manim.mobject. Three_d. Three_dimensions.Cylinder")。元组可用于分别定义`u`和的不同分辨率`v`。

例子

示例：示例圆柱体[¶](#examplecylinder)

![../_images/ExampleCylinder-1.png](../_images/ExampleCylinder-1.png)

from manim import \*

class ExampleCylinder(ThreeDScene):
def construct(self):
axes = ThreeDAxes()
cylinder = Cylinder(radius=2, height=3)
self.set*camera_orientation(phi=75 * DEGREES, theta=30 \_ DEGREES)
self.add(axes, cylinder)

Copy to clipboard

方法

[`add_bases`](#manim.mobject.three_d.three_dimensions.Cylinder.add_bases "manim.mobject. Three_d. Three_dimensions.Cylinder.add_bases")

添加气缸的端盖。

[`func`](#manim.mobject.three_d.three_dimensions.Cylinder.func "manim.mobject. Three_d. Three_dimensions.Cylinder.func")

从圆柱坐标转换为笛卡尔坐标。

[`get_direction`](#manim.mobject.three_d.three_dimensions.Cylinder.get_direction "manim.mobject. Three_d. Three_dimensions.Cylinder.get_direction")

返回 的中心轴方向[`Cylinder`](#manim.mobject.three_d.three_dimensions.Cylinder "manim.mobject. Three_d. Three_dimensions.Cylinder")。

[`set_direction`](#manim.mobject.three_d.three_dimensions.Cylinder.set_direction "manim.mobject. Three_d. Three_dimensions.Cylinder.set_direction")

设置 的中心轴方向[`Cylinder`](#manim.mobject.three_d.three_dimensions.Cylinder "manim.mobject. Three_d. Three_dimensions.Cylinder")。

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

添加碱基( )[\[来源\]](../_modules/manim/mobject/three_d/three_dimensions.html#Cylinder.add_bases)[#](#manim.mobject.three_d.three_dimensions.Cylinder.add_bases "此定义的固定链接")

添加气缸的端盖。

返回类型

没有任何

函数（_u_， _v_）[\[来源\]](../_modules/manim/mobject/three_d/three_dimensions.html#Cylinder.func)[#](#manim.mobject.three_d.three_dimensions.Cylinder.func "此定义的固定链接")

从圆柱坐标转换为笛卡尔坐标。

参数

- **u** ( _float_ ) – 高度。
- **v** ( _float_ ) – 方位角。

退货

定义 的点[`Cylinder`](#manim.mobject.three_d.three_dimensions.Cylinder "manim.mobject. Three_d. Three_dimensions.Cylinder")。

返回类型

`numpy.ndarray`

获取方向( )[\[来源\]](../_modules/manim/mobject/three_d/three_dimensions.html#Cylinder.get_direction)[#](#manim.mobject.three_d.three_dimensions.Cylinder.get_direction "此定义的固定链接")

返回 的中心轴方向[`Cylinder`](#manim.mobject.three_d.three_dimensions.Cylinder "manim.mobject. Three_d. Three_dimensions.Cylinder")。

退货

**方向**– 中心轴的方向[`Cylinder`](#manim.mobject.three_d.three_dimensions.Cylinder "manim.mobject. Three_d. Three_dimensions.Cylinder")。

返回类型

`numpy.array`

设置方向（_方向_）[\[来源\]](../_modules/manim/mobject/three_d/three_dimensions.html#Cylinder.set_direction)[#](#manim.mobject.three_d.three_dimensions.Cylinder.set_direction "此定义的固定链接")

设置 的中心轴方向[`Cylinder`](#manim.mobject.three_d.three_dimensions.Cylinder "manim.mobject. Three_d. Three_dimensions.Cylinder")。

参数

**方向**( `numpy.array`) – 的中心轴方向[`Cylinder`](#manim.mobject.three_d.three_dimensions.Cylinder "manim.mobject. Three_d. Three_dimensions.Cylinder")。

返回类型

没有任何
