# 极地平面[#](#polarplane "此标题的固定链接")

合格名称：`manim.mobject.graphing.coordinate\_systems.PolarPlane`

_类_ PolarPlane ( _radius_max = 4.0_、 _size = None_、 _radius_step = 1_、 _azimuth_step = None_、 _azimuth_units = 'PI 弧度'_、 _azimuth_compact_fraction = True_、 _azimuth_offset = 0_、 _azimuth_direction = 'CCW'_、 _azimuth_label_buff = 0.1_、 *azimuth_label_font*大小= 24*，*半径配置=没有任何*，\_background_line_style = None*，_faded_line_style = None_，_faded_line_ratio = 1_，_make_smooth_after_applying_functions = True_，_\*\* kwargs_）[\[来源\]](../_modules/manim/mobject/graphing/coordinate_systems.html#PolarPlane)[#](#manim.mobject.graphing.coordinate_systems.PolarPlane "此定义的固定链接")

基地：[`Axes`](manim.mobject.graphing.coordinate_systems.Axes.html#manim.mobject.graphing.coordinate_systems.Axes "manim.mobject.graphing.coordinate_systems.Axes")

创建带有背景线的极平面。

参数

- **azimuth_step** ( _float_ _|_ _None_ ) –

  方位角（也称为角坐标或极角）的划分数。如果`None`指定，则它将使用由以下指定的默认值`azimuth_units`：

  - `"PI radians"`或：20`"TAU radians"`
  - `"degrees"`：36
  - `"gradians"`：40
  - `None`: 1

  非整数值将导致在圆末端部分除法。

- **size** ( _float_ _|_ _None_ ) – 平面的直径。
- **radius_step** ( _float_ ) – 褪色半径线之间的距离。
- **radius_max** ( _float_ ) – 半径的最大值。
- **azimuth_units** ( _str_ _|_ _None_ ) –

  指定方位角的默认标签系统。选项有：

  - `"PI radians"`：区间内的分数标签\[0,2π\]和 π 作为常数。
  - `"TAU radians"`：区间内的分数标签\[0,τ\]（在哪里 τ=2π） 和 τ 作为常数。
  - `"degrees"`: 区间内的小数标签\[0,360\]拥有学位（∘） 象征。
  - `"gradians"`: 区间内的小数标签\[0,400\]带有上标“g”（g）。
  - `None`: 区间内的小数标签\[0,1\]。

- **azimuth_compact_fraction** ( _bool_ ) – 如果`azimuth_units`选项有小数标签，则选择是否以紧凑形式组合常量 xuy 相对于 xyu， 在哪里 u 是常数。
- **azimuth_offset** ( _float_ ) – 方位角的角度偏移，以弧度表示。
- **方位角方向**( _str_ ) –

  方位角的方向。

  - `"CW"`： 顺时针。
  - `"CCW"`: 逆时针方向。

- **azimuth_label_buff** ( _float_ ) – 方位角标签的缓冲区。
- **azimuth_label_font_size** ( _float_ ) – 方位角标签的字体大小。
- **radius_config** ( _dict_ _|_ _None_ ) – 半径的轴配置。
- **background_line_style** ( _dict_ _|_ _None_ ) –
- **faded_line_style** ( _dict_ _|_ _None_ ) –
- **faded_line_ratio** ( _int_ ) –
- **make_smooth_after_applying_functions** ( _bool_ ) –

例子

示例：PolarPlane 示例[¶](#polarplaneexample)

![../_images/PolarPlaneExample-1.png](../_images/PolarPlaneExample-1.png)

from manim import \*

class PolarPlaneExample(Scene):
def construct(self):
polarplane_pi = PolarPlane(
azimuth_units="PI radians",
size=6,
azimuth_label_font_size=33.6,
radius_config={"font_size": 33.6},
).add_coordinates()
self.add(polarplane_pi)

Copy to clipboard

参考：[`PolarPlane`](#manim.mobject.graphing.coordinate_systems.PolarPlane "manim.mobject.graphing.coordinate_systems.PolarPlane")

方法

[`add_coordinates`](#manim.mobject.graphing.coordinate_systems.PolarPlane.add_coordinates "manim.mobject.graphing.coordinate_systems.PolarPlane.add_coordinates")

添加坐标。

[`get_axes`](#manim.mobject.graphing.coordinate_systems.PolarPlane.get_axes "manim.mobject.graphing.coordinate_systems.PolarPlane.get_axes")

获取轴。

[`get_coordinate_labels`](#manim.mobject.graphing.coordinate_systems.PolarPlane.get_coordinate_labels "manim.mobject.graphing.coordinate_systems.PolarPlane.get_coefficient_labels")

获取坐标的标签

`get_radian_label`

`get_vector`

`prepare_for_nonlinear_transform`

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

添加坐标（_r_values = None_， _a_values = None_）[\[来源\]](../_modules/manim/mobject/graphing/coordinate_systems.html#PolarPlane.add_coordinates)[#](#manim.mobject.graphing.coordinate_systems.PolarPlane.add_coordinates "此定义的固定链接")

添加坐标。

参数

- **r_values** ( _Iterable_ _\[_ _float_ _\]_ _|_ _None_ ) – 沿半径的可迭代值，默认为 None。
- **a_values** ( _Iterable_ _\[_ _float_ _\]_ _|_ _None_ ) – 沿方位角的可迭代值，默认为 None。

获取轴( )[\[来源\]](../_modules/manim/mobject/graphing/coordinate_systems.html#PolarPlane.get_axes)[#](#manim.mobject.graphing.coordinate_systems.PolarPlane.get_axes "此定义的固定链接")

获取轴。

退货

一对轴。

返回类型

[`VGroup`](manim.mobject.types.vectorized_mobject.VGroup.html#manim.mobject.types.vectorized_mobject.VGroup "manim.mobject.types.vectorized_mobject.VGroup")

get*coordinate_labels ( \_r_values = None* , _a_values = None_ , _\*\* kwargs_ )[\[来源\]](../_modules/manim/mobject/graphing/coordinate_systems.html#PolarPlane.get_coordinate_labels)[#](#manim.mobject.graphing.coordinate_systems.PolarPlane.get_coordinate_labels "此定义的固定链接")

获取坐标的标签

参数

- **r_values** ( _Iterable_ _\[_ _float_ _\]_ _|_ _None_ ) – 沿半径的可迭代值，默认为 None。
- **a_values** ( _Iterable_ _\[_ _float_ _\]_ _|_ _None_ ) – 沿方位角的可迭代值，默认为 None。

退货

半径和方位角值的标签。

返回类型

[虚拟词典](manim.mobject.types.vectorized_mobject.VDict.html#manim.mobject.types.vectorized_mobject.VDict "manim.mobject.types.vectorized_mobject.VDict")
