# 矢量场

合格名称：`manim.mobject.vector\_field.VectorField`


```py

```

向量场。

矢量场基于在每个位置定义矢量的函数。[`Mobject`](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject")默认情况下，此类不包含任何可见元素，但提供沿矢量场移动其他元素的方法。

参数

- **func** ( _Callable_ _\[_ _\[_ _np.ndarray_ _\]_ _,_ _np.ndarray_ \_\] ) – 定义\_VectorField 每个位置的变化率的函数。
- **color** ( _Color_ _|_ _None_ ) – 矢量场的颜色。如果设置，则禁用特定于位置的着色。
- **color_scheme** ( _Callable_ _\[_ _\[_ _np.ndarray_ _\]_ _,_ _float_ _\]_ _|_ _None_ ) – 将向量映射到单个值的函数。该值给出使用 min_color_scheme_value、max_color_scheme_value 和 Colors 定义的颜色渐变中的位置。
- **min_color_scheme_value** ( *float ) – 要映射到*颜色中第一个颜色的 color_scheme 函数的值。较低的值也会导致渐变的第一种颜色。
- **max_color_scheme_value** ( *float ) – 要映射到*颜色中最后一个颜色的 color_scheme 函数的值。较高的值也会导致渐变的最后一种颜色。
- **颜色**( _Sequence_ _\[_ _Color_ _\]_ ) – 定义矢量场颜色渐变的颜色。
- **kwargs** – 要传递给[`VGroup`](manim.mobject.types.vectorized_mobject.VGroup.html#manim.mobject.types.vectorized_mobject.VGroup "manim.mobject.types.vectorized_mobject.VGroup")构造函数的附加参数

方法

[`fit_to_coordinate_system`](#manim.mobject.vector_field.VectorField.fit_to_coordinate_system "manim.mobject.vector_field.VectorField.fit_to_coordinate_system")

缩放矢量场以适合坐标系。

[`get_colored_background_image`](#manim.mobject.vector_field.VectorField.get_colored_background_image "manim.mobject.vector_field.VectorField.get_colored_background_image")

生成显示矢量场的图像。

[`get_nudge_updater`](#manim.mobject.vector_field.VectorField.get_nudge_updater "manim.mobject.vector_field.VectorField.get_nudge_updater")

获取更新函数以[`Mobject`](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject")沿矢量场移动 a。

[`get_vectorized_rgba_gradient_function`](#manim.mobject.vector_field.VectorField.get_vectorized_rgba_gradient_function "manim.mobject.vector_field.VectorField.get_vectorized_rgba_gradient_function")

生成 rgbas 的梯度作为 numpy 数组

[`nudge`](#manim.mobject.vector_field.VectorField.nudge "manim.mobject.vector_field.VectorField.nudge")

[`Mobject`](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject")沿着矢量场微移 a 。

[`nudge_submobjects`](#manim.mobject.vector_field.VectorField.nudge_submobjects "manim.mobject.vector_field.VectorField.nudge_submobjects")

沿矢量场对所有子对象应用微移。

[`scale_func`](#manim.mobject.vector_field.VectorField.scale_func "manim.mobject.vector_field.VectorField.scale_func")

缩放矢量场函数。

[`shift_func`](#manim.mobject.vector_field.VectorField.shift_func "manim.mobject.vector_field.VectorField.shift_func")

平移向量场函数。

[`start_submobject_movement`](#manim.mobject.vector_field.VectorField.start_submobject_movement "manim.mobject.vector_field.VectorField.start_submobject_movement")

开始沿着矢量场连续移动所有子对象。

[`stop_submobject_movement`](#manim.mobject.vector_field.VectorField.stop_submobject_movement "manim.mobject.vector_field.VectorField.stop_submobject_movement")

停止使用 开始的连续运动[`start_submobject_movement()`](#manim.mobject.vector_field.VectorField.start_submobject_movement "manim.mobject.vector_field.VectorField.start_submobject_movement")。

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

适合坐标系统（_坐标系统_）[\[来源\]](../_modules/manim/mobject/vector_field.html#VectorField.fit_to_coordinate_system)[#](#manim.mobject.vector_field.VectorField.fit_to_coordinate_system "此定义的固定链接")

缩放矢量场以适合坐标系。

当矢量场定义在与用于显示矢量场的坐标系不同的坐标系中时，此方法非常有用。

该方法只能使用一次，因为它会变换每个向量的原点。

参数

**axis_system** ( [_CoordinateSystem_](manim.mobject.graphing.coordinate_systems.CoordinateSystem.html#manim.mobject.graphing.coordinate_systems.CoordinateSystem "manim.mobject.graphing.coordinate_systems.坐标系统") ) – 用于拟合向量场的坐标系。

获取彩色背景图像（_采样率= 5_）[\[来源\]](../_modules/manim/mobject/vector_field.html#VectorField.get_colored_background_image)[#](#manim.mobject.vector_field.VectorField.get_colored_background_image "此定义的固定链接")

生成显示矢量场的图像。

每个位置的颜色是通过一系列步骤传递定位来计算的：计算该位置的向量场函数，使用 self.color_scheme 将该向量映射到单个值，最后使用颜色渐变从该值生成颜色。

参数

**Sample_rate** ( _int_ ) – 像素包含在图像中的步长。较低的值可提供更准确的结果，但可能需要很长时间才能计算。

退货

矢量场图像。

返回类型

图像.Imgae

get*nudge_updater（*速度= 1*，*逐点= False\_）[\[来源\]](../_modules/manim/mobject/vector_field.html#VectorField.get_nudge_updater)[#](#manim.mobject.vector_field.VectorField.get_nudge_updater "此定义的固定链接")

获取更新函数以[`Mobject`](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject")沿矢量场移动 a。

当与 一起使用时[`add_updater()`](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject.add_updater "manim.mobject.mobject.Mobject.add_updater")，mobject 将沿着矢量场移动，其速度由矢量场的大小决定。

参数

- **speed** ( _float_ ) – 当 speed=1 时，物体每秒移动的距离等于沿其路径的矢量场的大小。速度值缩放此类对象的速度。
- **pointwise** ( _bool_ ) – 是否沿着向量场移动对象。[`nudge()`](#manim.mobject.vector_field.VectorField.nudge "manim.mobject.vector_field.VectorField.nudge")详情请参阅。

退货

更新功能。

返回类型

可调用\[\[ [Mobject](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject") , float\], [Mobject](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject") \]

get*vectorized_rgba_gradient_function（*开始*，*结束*，*颜色\_）[\[来源\]](../_modules/manim/mobject/vector_field.html#VectorField.get_vectorized_rgba_gradient_function)[#](#manim.mobject.vector_field.VectorField.get_vectorized_rgba_gradient_function "此定义的固定链接")

生成 rgbas 的梯度作为 numpy 数组

参数

- **start** ( _float_ ) – 用于逆插值的起始值[`inverse_interpolate()`](manim.utils.bezier.html#manim.utils.bezier.inverse_interpolate "manim.utils.bezier.inverse_interpolate")
- **end** ( _float_ ) – 用于逆插值的最终值[`inverse_interpolate()`](manim.utils.bezier.html#manim.utils.bezier.inverse_interpolate "manim.utils.bezier.inverse_interpolate")
- **颜色**( _Iterable_ ) – 生成渐变的颜色列表

返回类型

函数将梯度生成为代表 rgba 值的 numpy 数组

微移（_mob_， _dt = 1_，_子步= 1_，_逐点= False_）[\[来源\]](../_modules/manim/mobject/vector_field.html#VectorField.nudge)[#](#manim.mobject.vector_field.VectorField.nudge "此定义的固定链接")

[`Mobject`](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject")沿着矢量场微移 a 。

参数

- **mob** ( [_Mobject_](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject") ) – 沿着矢量场移动的 mobject
- **dt** ( _float_ ) – 对象沿矢量场移动量的标量。实际距离基于矢量场的大小。
- **substeps** ( _int_ ) – 整个微移分为的步数。值越高，近似值越准确。
- **pointwise** ( _bool_ ) – 是否沿着向量场移动对象。如果为 False，矢量场在给定 的中心生效 [`Mobject`](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject")。如果为 True，矢量场会影响 的各个点的点[`Mobject`](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject")，可能会使其变形。

退货

这个向量场。

返回类型

[矢量场](#manim.mobject.vector_field.VectorField "manim.mobject.vector_field.VectorField")

例子

示例：轻推[¶](#nudging)

```py

```


nudge*submobjects ( \_dt = 1* , _substeps = 1_ , _pointwise = False_ )[\[来源\]](../_modules/manim/mobject/vector_field.html#VectorField.nudge_submobjects)[#](#manim.mobject.vector_field.VectorField.nudge_submobjects "此定义的固定链接")

沿矢量场对所有子对象应用微移。

参数

- **dt** ( _float_ ) – 对象沿矢量场移动量的标量。实际距离基于矢量场的大小。
- **substeps** ( _int_ ) – 整个微移分为的步数。值越高，近似值越准确。
- **pointwise** ( _bool_ ) – 是否沿着向量场移动对象。[`nudge()`](#manim.mobject.vector_field.VectorField.nudge "manim.mobject.vector_field.VectorField.nudge")详情请参阅。

退货

这个向量场。

返回类型

[矢量场](#manim.mobject.vector_field.VectorField "manim.mobject.vector_field.VectorField")

_静态_ scale*func（*函数*，*标量\_）[\[来源\]](../_modules/manim/mobject/vector_field.html#VectorField.scale_func)[#](#manim.mobject.vector_field.VectorField.scale_func "此定义的固定链接")

缩放矢量场函数。

参数

- **func** ( _Callable_ _\[_ _\[_ _ndarray_ _\]_ _,_ _ndarray_ _\]_ ) – 定义向量场的函数。
- **scalar** ( _float_ ) – 应用于向量场的标量。

返回类型

_可调用_\[\[ _ndarray_ \], _ndarray_ \]

例子

示例：ScaleVectorFieldFunction [¶](#scalevectorfieldfunction)

```py

```


退货

缩放后的向量场函数。

返回类型

可调用\[\[np.ndarray\]，np.ndarray\]

参数

- **func** (_可调用\_\_\[_ _\[_ _ndarray_ _\]_ _,_ _ndarray_ _\]_ ) –
- **标量**（_浮点数_）–

_静态_ shift*func（\_func*， _shift_vector_）[\[来源\]](../_modules/manim/mobject/vector_field.html#VectorField.shift_func)[#](#manim.mobject.vector_field.VectorField.shift_func "此定义的固定链接")

平移向量场函数。

参数

- **func** ( _Callable_ _\[_ _\[_ _ndarray_ _\]_ _,_ _ndarray_ _\]_ ) – 定义向量场的函数。
- **shift_vector** ( _ndarray_ ) – 应用于向量场的移位。

退货

平移向量场函数。

返回类型

可调用\[\[np.ndarray\]，np.ndarray\]

start*submobject_movement（*速度= 1*，*逐点= False\_）[\[来源\]](../_modules/manim/mobject/vector_field.html#VectorField.start_submobject_movement)[#](#manim.mobject.vector_field.VectorField.start_submobject_movement "此定义的固定链接")

开始沿着矢量场连续移动所有子对象。

多次调用此方法将导致删除此方法创建的先前更新程序。

参数

- **speed** ( _float_ ) – 移动子对象的速度。[`get_nudge_updater()`](#manim.mobject.vector_field.VectorField.get_nudge_updater "manim.mobject.vector_field.VectorField.get_nudge_updater")详情请参阅。
- **pointwise** ( _bool_ ) – 是否沿着向量场移动对象。[`nudge()`](#manim.mobject.vector_field.VectorField.nudge "manim.mobject.vector_field.VectorField.nudge")详情请参阅。

退货

这个向量场。

返回类型

[矢量场](#manim.mobject.vector_field.VectorField "manim.mobject.vector_field.VectorField")

stop_submobject_movement ( )[\[来源\]](../_modules/manim/mobject/vector_field.html#VectorField.stop_submobject_movement)[#](#manim.mobject.vector_field.VectorField.stop_submobject_movement "此定义的固定链接")

停止使用 开始的连续运动[`start_submobject_movement()`](#manim.mobject.vector_field.VectorField.start_submobject_movement "manim.mobject.vector_field.VectorField.start_submobject_movement")。

退货

这个向量场。

返回类型

[矢量场](#manim.mobject.vector_field.VectorField "manim.mobject.vector_field.VectorField")
