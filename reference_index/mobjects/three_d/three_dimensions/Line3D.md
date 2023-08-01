# 线 3D 

合格名称：`manim.mobject.three\_d.three\_dimensions.Line3D`

_类_ Line3D ( _start = array(\[- 1., 0., 0.\])_ , _end = array(\[1., 0., 0.\])_ ,_厚度= 0.02_ , _color = None_ , _\*\* kwargs_ )[\[来源\]](../_modules/manim/mobject/three_d/three_dimensions.html#Line3D)[#](#manim.mobject.three_d.three_dimensions.Line3D "此定义的固定链接")

基地：[`Cylinder`](manim.mobject.three_d.three_dimensions.Cylinder.html#manim.mobject.three_d.three_dimensions.Cylinder "manim.mobject. Three_d. Three_dimensions.Cylinder")

圆柱线，用于 ThreeDScene。

参数

- **start** ( _np.ndarray_ ) – 线的起点。
- **end** ( _np.ndarray_ ) – 线的终点。
- **厚度**( _float_ ) – 线条的粗细。
- **颜色**( _Color_ ) – 线条的颜色。

例子

示例：ExampleLine3D [¶](#exampleline3d)

![../_images/ExampleLine3D-1.png](../_images/ExampleLine3D-1.png)

from manim import \*

class ExampleLine3D(ThreeDScene):
def construct(self):
axes = ThreeDAxes()
line = Line3D(start=np.array(\[0, 0, 0\]), end=np.array(\[2, 2, 2\]))
self.set*camera_orientation(phi=75 * DEGREES, theta=30 \_ DEGREES)
self.add(axes, line)

Copy to clipboard

方法

[`get_end`](#manim.mobject.three_d.three_dimensions.Line3D.get_end "manim.mobject. Three_d. Three_dimensions.Line3D.get_end")

返回 的结束点[`Line3D`](#manim.mobject.three_d.three_dimensions.Line3D "manim.mobject. Three_d. Three_dimensions.Line3D")。

[`get_start`](#manim.mobject.three_d.three_dimensions.Line3D.get_start "manim.mobject. Three_d. Three_dimensions.Line3D.get_start")

返回 的起点[`Line3D`](#manim.mobject.three_d.three_dimensions.Line3D "manim.mobject. Three_d. Three_dimensions.Line3D")。

[`parallel_to`](#manim.mobject.three_d.three_dimensions.Line3D.parallel_to "manim.mobject. Three_d. Three_dimensions.Line3D.parallel_to")

返回与穿过给定点的另一条线平行的线。

[`perpendicular_to`](#manim.mobject.three_d.three_dimensions.Line3D.perpendicular_to "manim.mobject. Three_d. Three_dimensions.Line3D.perpendular_to")

返回与穿过给定点的另一条线垂直的线。

[`pointify`](#manim.mobject.three_d.three_dimensions.Line3D.pointify "manim.mobject. Three_d. Three_dimensions.Line3D.pointify")

获取代表 的中心的点[`Mobjects`](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject")。

[`set_start_and_end_attrs`](#manim.mobject.three_d.three_dimensions.Line3D.set_start_and_end_attrs "manim.mobject. Three_d. Three_dimensions.Line3D.set_start_and_end_attrs")

设置线的起点和终点。

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

获取结束( )[\[来源\]](../_modules/manim/mobject/three_d/three_dimensions.html#Line3D.get_end)[#](#manim.mobject.three_d.three_dimensions.Line3D.get_end "此定义的固定链接")

返回 的结束点[`Line3D`](#manim.mobject.three_d.three_dimensions.Line3D "manim.mobject. Three_d. Three_dimensions.Line3D")。

退货

**end** – 的结束点[`Line3D`](#manim.mobject.three_d.three_dimensions.Line3D "manim.mobject. Three_d. Three_dimensions.Line3D")。

返回类型

`numpy.array`

获取开始（）[\[来源\]](../_modules/manim/mobject/three_d/three_dimensions.html#Line3D.get_start)[#](#manim.mobject.three_d.three_dimensions.Line3D.get_start "此定义的固定链接")

返回 的起点[`Line3D`](#manim.mobject.three_d.three_dimensions.Line3D "manim.mobject. Three_d. Three_dimensions.Line3D")。

退货

**start** – 的起点[`Line3D`](#manim.mobject.three_d.three_dimensions.Line3D "manim.mobject. Three_d. Three_dimensions.Line3D")。

返回类型

`numpy.array`

_类方法_ parallel*to ( \_line* , _point = array(\[0., 0., 0.\])_ , _length = 5_ , _\*\* kwargs_ )[\[来源\]](../_modules/manim/mobject/three_d/three_dimensions.html#Line3D.parallel_to)[#](#manim.mobject.three_d.three_dimensions.Line3D.parallel_to "此定义的固定链接")

返回与穿过给定点的另一条线平行的线。

参数

- **line** ( [_Line3D_](#manim.mobject.three_d.three_dimensions.Line3D "manim.mobject. Three_d. Three_dimensions.Line3D") ) – 要平行的线。
- **point** ( _Sequence_ _\[_ _float_ _\]_ ) – 要经过的点。
- **length** ( _float_ ) – 平行线的长度。
- **kwargs** – 要传递给类的附加参数。

退货

平行于 的线`line`。

返回类型

[`Line3D`](#manim.mobject.three_d.three_dimensions.Line3D "manim.mobject. Three_d. Three_dimensions.Line3D")

例子

示例：平行线示例[¶](#parallellineexample)

![../_images/ParallelLineExample-1.png](../_images/ParallelLineExample-1.png)

from manim import \*

class ParallelLineExample(ThreeDScene):
def construct(self):
self.set_camera_orientation(PI / 3, -PI / 4)
ax = ThreeDAxes((-5, 5), (-5, 5), (-5, 5), 10, 10, 10)
line1 = Line3D(RIGHT \* 2, UP + OUT, color=RED)
line2 = Line3D.parallel_to(line1, color=YELLOW)
self.add(ax, line1, line2)

Copy to clipboard

_类方法_ Vertical*to ( \_line* , _point = array(\[0., 0., 0.\])_ , _length = 5_ , _\*\* kwargs_ )[\[来源\]](../_modules/manim/mobject/three_d/three_dimensions.html#Line3D.perpendicular_to)[#](#manim.mobject.three_d.three_dimensions.Line3D.perpendicular_to "此定义的固定链接")

返回与穿过给定点的另一条线垂直的线。

参数

- **line** ( [_Line3D_](#manim.mobject.three_d.three_dimensions.Line3D "manim.mobject. Three_d. Three_dimensions.Line3D") ) – 要垂直的线。
- **point** ( _Sequence_ _\[_ _float_ _\]_ ) – 要经过的点。
- **length** ( _float_ ) – 垂直线的长度。
- **kwargs** – 要传递给类的附加参数。

退货

垂直于 的线`line`。

返回类型

[`Line3D`](#manim.mobject.three_d.three_dimensions.Line3D "manim.mobject. Three_d. Three_dimensions.Line3D")

例子

示例：PerpLineExample [¶](#perplineexample)

![../_images/PerpLineExample-1.png](../_images/PerpLineExample-1.png)

from manim import \*

class PerpLineExample(ThreeDScene):
def construct(self):
self.set_camera_orientation(PI / 3, -PI / 4)
ax = ThreeDAxes((-5, 5), (-5, 5), (-5, 5), 10, 10, 10)
line1 = Line3D(RIGHT \* 2, UP + OUT, color=RED)
line2 = Line3D.perpendicular_to(line1, color=BLUE)
self.add(ax, line1, line2)

Copy to clipboard

pointify ( _mob_or_point_，_方向= None_ )[\[来源\]](../_modules/manim/mobject/three_d/three_dimensions.html#Line3D.pointify)[#](#manim.mobject.three_d.three_dimensions.Line3D.pointify "此定义的固定链接")

获取代表 的中心的点[`Mobjects`](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject")。

参数

- **mob_or_point** ( [_Mobject_](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject") _|_ _float_ ) –[`Mobjects`](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject")或应返回其中心的点。
- **Direction** ( _np.ndarray_ ) – 如果应返回 a 的边[`Mobjects`](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject")，则为该边的方向。

退货

或点的中心[`Mobjects`](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject")，或边缘（如果给定方向）。

返回类型

`numpy.array`

set*start_and_end_attrs (*开始*,*结束*, *\*\* kwargs\_ )[\[来源\]](../_modules/manim/mobject/three_d/three_dimensions.html#Line3D.set_start_and_end_attrs)[#](#manim.mobject.three_d.three_dimensions.Line3D.set_start_and_end_attrs "此定义的固定链接")

设置线的起点和终点。

如果 或`start`是`end`，[`Mobjects`](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject")这给出了它们的中心。

参数

- **start** ( _ndarray_ ) – 起始点或`Mobject`.
- **end** ( _ndarray_ ) – 结束点或`Mobject`.

返回类型

没有任何
