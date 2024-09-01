# 向量场

合格名称：`manim.mobject.vector\_field.VectorField`


```py
class VectorField(func, color=None, color_scheme=None, min_color_scheme_value=0, max_color_scheme_value=2, colors=['#236B8E', '#83C167', '#FFFF00', '#FC6255'], **kwargs)
```

Bases: `VGroup`

向量场。

矢量场基于在每个位置定义矢量的函数。[`Mobject`]()默认情况下，此类不包含任何可见元素，但提供沿矢量场移动其他元素的方法。

参数

- **func** ( _Callable_ _\[_ _\[_ _np.ndarray_ _\]_ _,_ _np.ndarray_ \_\] ) – 定义\_VectorField 每个位置的变化率的函数。
- **color** ( _Color_ _|_ _None_ ) – 矢量场的颜色。如果设置，则禁用特定于位置的着色。
- **color_scheme** ( _Callable_ _\[_ _\[_ _np.ndarray_ _\]_ _,_ _float_ _\]_ _|_ _None_ ) – 将向量映射到单个值的函数。该值给出使用 min_color_scheme_value、max_color_scheme_value 和 Colors 定义的颜色渐变中的位置。
- **min_color_scheme_value** ( *float ) – 要映射到*颜色中第一个颜色的 color_scheme 函数的值。较低的值也会导致渐变的第一种颜色。
- **max_color_scheme_value** ( *float ) – 要映射到*颜色中最后一个颜色的 color_scheme 函数的值。较高的值也会导致渐变的最后一种颜色。
- **colors**( _Sequence_ _\[_ _Color_ _\]_ ) – 定义矢量场颜色渐变的颜色。
- **kwargs** – 要传递给[`VGroup`]()构造函数的附加参数


方法

|||
|-|-|
[`fit_to_coordinate_system`]()|缩放矢量场以适合坐标系。
[`get_colored_background_image`]()|生成显示矢量场的图像。
[`get_nudge_updater`]()|获取更新函数以[`Mobject`]()沿矢量场移动 a。
[`get_vectorized_rgba_gradient_function`]()|生成 rgbas 的梯度作为 numpy 数组
[`nudge`]()|[`Mobject`]()沿着矢量场微移 a 。
[`nudge_submobjects`]()|沿矢量场对所有子对象应用微移。
[`scale_func`]()|缩放矢量场函数。
[`shift_func`]()|平移向量场函数。
[`start_submobject_movement`]()|开始沿着矢量场连续移动所有子对象。
[`stop_submobject_movement`]()|停止使用 开始的连续运动[`start_submobject_movement()`]()。


属性

|||
|-|-|
`animate`|用于对 的任何方法的应用程序进行动画处理`self`。
`animation_overrides`|
`color`|
`depth`|对象的深度。
`fill_color`|如果有多种颜色（对于渐变），则返回第一个颜色
`height`|mobject 的高度。
`n_points_per_curve`|
`sheen_factor`|
`stroke_color`|
`width`|mobject 的宽度。



`fit_to_coordinate_system(coordinate_system)`

缩放矢量场以适合坐标系。

当矢量场定义在与用于显示矢量场的坐标系不同的坐标系中时，此方法非常有用。

该方法只能使用一次，因为它会变换每个向量的原点。

参数

**axis_system** ( [_CoordinateSystem_]() ) – 用于拟合向量场的坐标系。



`get_colored_background_image(sampling_rate=5)`

生成显示矢量场的图像。

每个位置的颜色是通过一系列步骤传递定位来计算的：计算该位置的向量场函数，使用 self.color_scheme 将该向量映射到单个值，最后使用颜色渐变从该值生成颜色。

参数

**Sample_rate** ( _int_ ) – 像素包含在图像中的步长。较低的值可提供更准确的结果，但可能需要很长时间才能计算。

返回

矢量场图像。

返回类型

Image.Imgae



`get_nudge_updater(speed=1, pointwise=False)`

获取更新函数以[`Mobject`]()沿矢量场移动 a。

当与 一起使用时[`add_updater()`]()，mobject 将沿着矢量场移动，其速度由矢量场的大小决定。

参数

- **speed** ( _float_ ) – 当 speed=1 时，物体每秒移动的距离等于沿其路径的矢量场的大小。速度值缩放此类对象的速度。
- **pointwise** ( _bool_ ) – 是否沿着向量场移动对象。[`nudge()`]()详情请参阅。

返回

更新功能。

返回类型

Callable\[\[ [Mobject]() , float\], [Mobject]() \]



`get_vectorized_rgba_gradient_function(start, end, colors)`

生成 rgbas 的梯度作为 numpy 数组

参数

- **start** ( _float_ ) – 用于逆插值的起始值[`inverse_interpolate()`]()
- **end** ( _float_ ) – 用于逆插值的最终值[`inverse_interpolate()`]()
- **colors**( _Iterable_ ) – 生成渐变的颜色列表

返回类型

函数将梯度生成为代表 rgba 值的 numpy 数组



`nudge(mob, dt=1, substeps=1, pointwise=False)`

[`Mobject`]()沿着矢量场微移 a 。

参数

- **mob** ( [_Mobject_]() ) – 沿着矢量场移动的 mobject
- **dt** ( _float_ ) – 对象沿矢量场移动量的标量。实际距离基于矢量场的大小。
- **substeps** ( _int_ ) – 整个微移分为的步数。值越高，近似值越准确。
- **pointwise** ( _bool_ ) – 是否沿着向量场移动对象。如果为 False，矢量场在给定 的中心生效 [`Mobject`]()。如果为 True，矢量场会影响 的各个点的点[`Mobject`]()，可能会使其变形。

返回

这个向量场。

返回类型

[VectorField]()


例子

示例：轻推

```py
from manim import *

class Nudging(Scene):
    def construct(self):
        func = lambda pos: np.sin(pos[1] / 2) * RIGHT + np.cos(pos[0] / 2) * UP
        vector_field = ArrowVectorField(
            func, x_range=[-7, 7, 1], y_range=[-4, 4, 1], length_func=lambda x: x / 2
        )
        self.add(vector_field)
        circle = Circle(radius=2).shift(LEFT)
        self.add(circle.copy().set_color(GRAY))
        dot = Dot().move_to(circle)

        vector_field.nudge(circle, -2, 60, True)
        vector_field.nudge(dot, -2, 60)

        circle.add_updater(vector_field.get_nudge_updater(pointwise=True))
        dot.add_updater(vector_field.get_nudge_updater())
        self.add(circle, dot)
        self.wait(6)
```



`nudge_submobjects(dt=1, substeps=1, pointwise=False)`

沿矢量场对所有子对象应用微移。

参数

- **dt** ( _float_ ) – 对象沿矢量场移动量的标量。实际距离基于矢量场的大小。
- **substeps** ( _int_ ) – 整个微移分为的步数。值越高，近似值越准确。
- **pointwise** ( _bool_ ) – 是否沿着向量场移动对象。[`nudge()`]()详情请参阅。

返回

这个向量场。

返回类型

[VectorField]()



`static scale_func(func, scalar)`

缩放矢量场函数。

参数

- **func** ( _Callable_ _\[_ _\[_ _ndarray_ _\]_ _,_ _ndarray_ _\]_ ) – 定义向量场的函数。
- **scalar** ( _float_ ) – 应用于向量场的标量。

返回类型

_Callable_\[\[ _ndarray_ \], _ndarray_ \]


例子

示例：ScaleVectorFieldFunction 

```py
from manim import *

class ScaleVectorFieldFunction(Scene):
    def construct(self):
        func = lambda pos: np.sin(pos[1]) * RIGHT + np.cos(pos[0]) * UP
        vector_field = ArrowVectorField(func)
        self.add(vector_field)
        self.wait()

        func = VectorField.scale_func(func, 0.5)
        self.play(vector_field.animate.become(ArrowVectorField(func)))
        self.wait()
```

返回

缩放后的向量场函数。

返回类型

Callable\[\[np.ndarray\]，np.ndarray\]

参数

- **func** (_Callable\_\_\[_ _\[_ _ndarray_ _\]_ _,_ _ndarray_ _\]_ ) –
- **scalar**（_float_）–



`static shift_func(func, shift_vector)`

平移向量场函数。

参数

- **func** ( _Callable_ _\[_ _\[_ _ndarray_ _\]_ _,_ _ndarray_ _\]_ ) – 定义向量场的函数。
- **shift_vector** ( _ndarray_ ) – 应用于向量场的移位。

返回

平移向量场函数。

返回类型

Callable\[\[np.ndarray\]，np.ndarray\]


`start_submobject_movement(speed=1, pointwise=False)`

开始沿着矢量场连续移动所有子对象。

多次调用此方法将导致删除此方法创建的先前更新程序。

参数

- **speed** ( _float_ ) – 移动子对象的速度。[`get_nudge_updater()`]()详情请参阅。
- **pointwise** ( _bool_ ) – 是否沿着向量场移动对象。[`nudge()`]()详情请参阅。

返回

这个向量场。

返回类型

[VectorField]()



`stop_submobject_movement()`

停止使用 开始的连续运动[`start_submobject_movement()`]()。

返回

这个向量场。

返回类型

[VectorField]()
