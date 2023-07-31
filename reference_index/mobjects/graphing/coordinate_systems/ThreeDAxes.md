# 三轴[#](#threedaxes "此标题的固定链接")

合格名称：`manim.mobject.graphing.coordinate\_systems.ThreeDAxes`

_类_ ThreeDAxes ( _x_range = (\- 6, 6, 1)_ , _y_range = (\- 5, 5, 1)_ , _z_range = (\- 4, 4, 1)_ , _x_length = 10.5_ , _y_length = 10.5_ , _z_length = 6.5_ , _z_axis_config =无_， _z_normal = array(\[0., \- 1., 0.\])_， _num_axis_pieces = 20_，_light_source = array(\[- 7., \- 9., 10.\])_，_深度= None_，_光泽度= 0.5_， _\*\* kwargs_ )[\[来源\]](../_modules/manim/mobject/graphing/coordinate_systems.html#ThreeDAxes)[#](#manim.mobject.graphing.coordinate_systems.ThreeDAxes "此定义的固定链接")

基地：[`Axes`](manim.mobject.graphing.coordinate_systems.Axes.html#manim.mobject.graphing.coordinate_systems.Axes "manim.mobject.graphing.coordinate_systems.Axes")

一组 3 维轴。

参数

- **x_range** ( _Sequence_ _\[_ _float_ _\]_ _|_ _None_ ) – x 轴的值。`[x_min, x_max, x_step]`
- **y_range** ( _Sequence_ _\[_ _float_ _\]_ _|_ _None_ ) – y 轴的值。`[y_min, y_max, y_step]`
- **z_range** ( _Sequence_ _\[_ _float_ _\]_ _|_ _None_ ) – z 轴的值。`[z_min, z_max, z_step]`
- **x_length** ( _float_ _|_ _None_ ) – x 轴的长度。
- **y_length** ( _float_ _|_ _None_ ) – y 轴的长度。
- **z_length** ( _float_ _|_ _None_ ) – z 轴的长度。
- **z_axis_config** ( _dict_ _|_ _None_ ) – 传递给[`NumberLine`](manim.mobject.graphing.number_line.NumberLine.html#manim.mobject.graphing.number_line.NumberLine "manim.mobject.graphing.number_line.NumberLine")影响 z 轴的参数。
- **z_normal** ( _Sequence_ _\[_ _float_ _\]_ ) – 法线方向。
- **num_axis_pieces** ( _int_ ) – 用于构造轴的块数。
- **light_source** ( _Sequence_ _\[_ _float_ _\]_ ) – 光源的方向。
- **深度**– 目前不起作用。
- **光泽**– 目前不起作用。
- **kwargs** – 要传递给 的附加参数[`Axes`](manim.mobject.graphing.coordinate_systems.Axes.html#manim.mobject.graphing.coordinate_systems.Axes "manim.mobject.graphing.coordinate_systems.Axes")。

方法

[`get_axis_labels`](#manim.mobject.graphing.coordinate_systems.ThreeDAxes.get_axis_labels "manim.mobject.graphing.coordinate_systems.ThreeDAxes.get_axis_labels")

定义图形的 x_axis 和 y_axis 的标签。

[`get_y_axis_label`](#manim.mobject.graphing.coordinate_systems.ThreeDAxes.get_y_axis_label "manim.mobject.graphing.coordinate_systems.ThreeDAxes.get_y_axis_label")

生成 y 轴标签。

[`get_z_axis_label`](#manim.mobject.graphing.coordinate_systems.ThreeDAxes.get_z_axis_label "manim.mobject.graphing.coordinate_systems.ThreeDAxes.get_z_axis_label")

生成 z 轴标签。

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

get*axis_labels ( \_x_label = 'x'* , _y_label = 'y'_ , _z_label = 'z'_ )[\[来源\]](../_modules/manim/mobject/graphing/coordinate_systems.html#ThreeDAxes.get_axis_labels)[#](#manim.mobject.graphing.coordinate_systems.ThreeDAxes.get_axis_labels "此定义的固定链接")

定义图形的 x_axis 和 y_axis 的标签。

为了增强对标签位置的控制，请使用[`get_x_axis_label()`](manim.mobject.graphing.coordinate_systems.CoordinateSystem.html#manim.mobject.graphing.coordinate_systems.CoordinateSystem.get_x_axis_label "manim.mobject.graphing.coordinate_systems.CooperativeSystem.get_x_axis_label")、 [`get_y_axis_label()`](#manim.mobject.graphing.coordinate_systems.ThreeDAxes.get_y_axis_label "manim.mobject.graphing.coordinate_systems.ThreeDAxes.get_y_axis_label")和 [`get_z_axis_label()`](#manim.mobject.graphing.coordinate_systems.ThreeDAxes.get_z_axis_label "manim.mobject.graphing.coordinate_systems.ThreeDAxes.get_z_axis_label")。

参数

- **x_label** ( _float_ _|_ _str_ _|_ [_Mobject_](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject") ) – x\_轴的标签。默认为[`MathTex`](manim.mobject.text.tex_mobject.MathTex.html#manim.mobject.text.tex_mobject.MathTex "manim.mobject.text.tex_mobject.MathTex")for`str`和`float`输入。
- **y_label** ( _float_ _|_ _str_ _|_ [_Mobject_](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject") ) – y 轴的标签。默认为[`MathTex`](manim.mobject.text.tex_mobject.MathTex.html#manim.mobject.text.tex_mobject.MathTex "manim.mobject.text.tex_mobject.MathTex")for`str`和`float`输入。
- **z_label** ( _float_ _|_ _str_ _|_ [_Mobject_](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject") ) – z 轴的标签。默认为[`MathTex`](manim.mobject.text.tex_mobject.MathTex.html#manim.mobject.text.tex_mobject.MathTex "manim.mobject.text.tex_mobject.MathTex")for`str`和`float`输入。

退货

[`VGroup`](manim.mobject.types.vectorized_mobject.VGroup.html#manim.mobject.types.vectorized_mobject.VGroup "manim.mobject.types.vectorized_mobject.VGroup")x_axis、y_axis 和 z_axis 的标签。

返回类型

[`VGroup`](manim.mobject.types.vectorized_mobject.VGroup.html#manim.mobject.types.vectorized_mobject.VGroup "manim.mobject.types.vectorized_mobject.VGroup")

也可以看看

[`get_x_axis_label()`](manim.mobject.graphing.coordinate_systems.CoordinateSystem.html#manim.mobject.graphing.coordinate_systems.CoordinateSystem.get_x_axis_label "manim.mobject.graphing.coordinate_systems.CooperativeSystem.get_x_axis_label") [`get_y_axis_label()`](#manim.mobject.graphing.coordinate_systems.ThreeDAxes.get_y_axis_label "manim.mobject.graphing.coordinate_systems.ThreeDAxes.get_y_axis_label") [`get_z_axis_label()`](#manim.mobject.graphing.coordinate_systems.ThreeDAxes.get_z_axis_label "manim.mobject.graphing.coordinate_systems.ThreeDAxes.get_z_axis_label")

例子

示例：GetAxisLabelsExample [¶](#getaxislabelsexample)

![../_images/GetAxisLabelsExample-2.png](../_images/GetAxisLabelsExample-2.png)

from manim import \*

class GetAxisLabelsExample(ThreeDScene):
def construct(self):
self.set_camera_orientation(phi=2\*PI/5, theta=PI/5)
axes = ThreeDAxes()
labels = axes.get_axis_labels(
Tex("x-axis").scale(0.7), Text("y-axis").scale(0.45), Text("z-axis").scale(0.45)
)
self.add(axes, labels)

Copy to clipboard

get*y_axis*label (_标签_,_边缘=数组(\[1., 1., 0.\])_ ,_方向=数组(\[1., 1., 0.\])_ , \_buff = 0.1* ,*旋转= 1.5707963267948966* ,*旋转轴=数组(\[0 ., 0., 1.\])_ , _\*\* kwargs\_ )[\[来源\]](../_modules/manim/mobject/graphing/coordinate_systems.html#ThreeDAxes.get_y_axis_label)[#](#manim.mobject.graphing.coordinate_systems.ThreeDAxes.get_y_axis_label "此定义的固定链接")

生成 y 轴标签。

参数

- **label** ( _float_ _|_ _str_ _|_ [_Mobject_](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject") ) – 标签。默认为[`MathTex`](manim.mobject.text.tex_mobject.MathTex.html#manim.mobject.text.tex_mobject.MathTex "manim.mobject.text.tex_mobject.MathTex")for`str`和`float`输入。
- **edge** ( _Sequence_ _\[_ _float_ _\]_ ) – 默认情况下将添加标签的 y 轴边缘`UR`。
- **方向**( _Sequence_ _\[_ _float_ _\]_ ) – 默认情况下，允许从边缘进一步定位标签`UR`。
- **buff** ( _float_ ) – 默认情况下，标签距线条的距离`SMALL_BUFF`。
- **旋转**– 默认情况下旋转标签的角度`PI/2`。
- **rotation_axis** – 默认情况下旋转标签的轴`OUT`。

退货

定位的标签。

返回类型

[`Mobject`](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject")

例子

示例：GetYAxisLabelExample [¶](#getyaxislabelexample)

![../_images/GetYAxisLabelExample-2.png](../_images/GetYAxisLabelExample-2.png)

from manim import \*

class GetYAxisLabelExample(ThreeDScene):
def construct(self):
ax = ThreeDAxes()
lab = ax.get_y_axis_label(Tex("$y$-label"))
self.set_camera_orientation(phi=2\*PI/5, theta=PI/5)
self.add(ax, lab)

Copy to clipboard

get*z_axis*label (_标签_,_边缘=数组(\[0., 0., 1.\])_ ,_方向=数组(\[1., 0., 0.\])_ , \_buff = 0.1* ,*旋转= 1.5707963267948966* ,*旋转轴=数组(\[1 ., 0., 0.\])_ , _\*\* kwargs\_ )[\[来源\]](../_modules/manim/mobject/graphing/coordinate_systems.html#ThreeDAxes.get_z_axis_label)[#](#manim.mobject.graphing.coordinate_systems.ThreeDAxes.get_z_axis_label "此定义的固定链接")

生成 z 轴标签。

参数

- **label** ( _float_ _|_ _str_ _|_ [_Mobject_](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject") ) – 标签。默认为[`MathTex`](manim.mobject.text.tex_mobject.MathTex.html#manim.mobject.text.tex_mobject.MathTex "manim.mobject.text.tex_mobject.MathTex")for`str`和`float`输入。
- **edge** ( _Sequence_ _\[_ _float_ _\]_ ) – 默认情况下将添加标签的 z 轴边缘`OUT`。
- **方向**( _Sequence_ _\[_ _float_ _\]_ ) – 默认情况下，允许从边缘进一步定位标签`RIGHT`。
- **buff** ( _float_ ) – 默认情况下，标签距线条的距离`SMALL_BUFF`。
- **旋转**– 默认情况下旋转标签的角度`PI/2`。
- **rotation_axis** – 默认情况下旋转标签的轴`RIGHT`。

退货

定位的标签。

返回类型

[`Mobject`](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject")

例子

示例：获取 ZAxisLabelExample [¶](#getzaxislabelexample)

![../_images/GetZAxisLabelExample-1.png](../_images/GetZAxisLabelExample-1.png)

from manim import \*

class GetZAxisLabelExample(ThreeDScene):
def construct(self):
ax = ThreeDAxes()
lab = ax.get_z_axis_label(Tex("$z$-label"))
self.set_camera_orientation(phi=2\*PI/5, theta=PI/5)
self.add(ax, lab)

Copy to clipboard
