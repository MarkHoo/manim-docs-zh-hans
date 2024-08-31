# 3D摄相机

合格名称：`manim.camera.three\_d\_camera.ThreeDCamera`

```py
class ThreeDCamera(focal_distance=20.0, shading_factor=0.2, default_distance=5.0, light_source_start_point=array([- 7., - 9., 10.]), should_apply_shading=True, exponential_projection=False, phi=0, theta=- 1.5707963267948966, gamma=0, zoom=1, **kwargs)
```

Bases: `Camera`

初始化 ThreeDCamera

参数

**\*kwargs** – Camera 的任何关键字参数。

方法

|||
|-|-|
[`add_fixed_in_frame_mobjects`]()|此方法允许对象具有固定位置，即使相机四处移动。
[`add_fixed_orientation_mobjects`]()|此方法允许 mobject 具有固定的方向，即使相机四处移动也是如此。
[`capture_mobjects`]()|通过将 mobject 打印在 上来捕获它们`pixel_array`。
[`generate_rotation_matrix`]()|根据相机的当前位置生成旋转矩阵。
[`get_fill_rgbas`]()|返回传入的 VMobject 的填充的 RGBA 数组
[`get_focal_distance`]()|返回相机的焦点距离。
[`get_gamma`]()|返回相机围绕从 ORIGIN 到相机的向量的旋转。
[`get_mobjects_to_display`]()|用于获取要通过相机显示的对象列表。
[`get_phi`]()|返回极角（与 Z_AXIS 的角度）phi。
[`get_rotation_matrix`]()|返回相机当前位置对应的矩阵。
[`get_stroke_rgbas`]()|获取传递的 VMobject 笔画的 RGBA 数组。
[`get_theta`]()|返回方位角，即相机绕 Z_AXIS 旋转的角度。
[`get_value_trackers`]()|phi、theta、focal_distance、gamma 和 Zoom 的列表[`ValueTrackers`]()。
[`get_zoom`]()|返回相机的变焦量。
`modified_rgbas`|
[`project_point`]()|将当前的 rotation_matrix 作为投影矩阵应用到传递的点。
[`project_points`]()|将当前的 rotation_matrix 作为投影矩阵应用于传递的点数组。
[`remove_fixed_in_frame_mobjects`]()|如果一个 mobject 通过传递它而被固定在框架中[`add_fixed_in_frame_mobjects()`]()，那么这将撤消该固定。
[`remove_fixed_orientation_mobjects`]()|如果一个 mobject 通过穿过 来固定其方向[`add_fixed_orientation_mobjects()`]()，那么这将撤消该固定。
[`reset_rotation_matrix`]()|将 self.rotation_matrix 的值设置为相机当前位置对应的矩阵
[`set_focal_distance`]()|设置相机的 focal_distance。
[`set_gamma`]()|设置相机围绕从 ORIGIN 到相机的矢量的旋转角度。
[`set_phi`]()|设置极角，即 Z_AXIS 和相机通过 ORIGIN 之间的角度（以弧度表示）。
[`set_theta`]()|设置方位角，即相机围绕 Z_AXIS 旋转的角度（以弧度为单位）。
[`set_zoom`]()|设置相机的变焦量。
`transform_points_pre_display`|



属性

`background_color`

`background_opacity`

`frame_center`



`add_fixed_in_frame_mobjects(*mobjects)`

此方法允许对象具有固定位置，即使相机四处移动。EG 如果通过这个方法，在框架的顶部，它将继续显示在框架的顶部。

在显示标题或公式等时非常有用。

参数

\***\*mobjects** ( [_Mobject_]() ) – 要在框架中修复的 mobject。


```py
add_fixed_orientation_mobjects(*mobjects, use_static_center_func=False, center_func=None)
```

此方法允许 mobject 具有固定的方向，即使相机四处移动也是如此。EG 如果通过此方法，面向相机，即使相机移动，它也会继续面向相机。在向图表等添加标签时非常有用。

参数

- **\*mobjects** ( [_Mobject_]() ) – 方向必须固定的 mobject。
- **use_static_center_func** ( _bool_ ) – 是否使用以 mobject 的中心为中心点的函数，默认为 False
- **center_func** ( _Callable_ _\[_ _\[_ _\]_ _,_ _np.ndarray_ _\]_ _|_ _None_ ) – 返回 mobject 将相对于其定向的中心点的函数，默认为 None



`capture_mobjects(mobjects, **kwargs)`

通过将 mobject 打印在 上来捕获它们`pixel_array`。

这是将场景的内容转换为数组的基本函数，然后将其转换为图像或视频。

参数

- **mobjects** – 要捕获的 Mobjects。
- **kwargs** – 要传递给 的关键字参数[`get_mobjects_to_display()`]()。

笔记

有关当前可以呈现的类的列表，请参阅`display_funcs()`。



`generate_rotation_matrix()`

根据相机的当前位置生成旋转矩阵。

返回

相机当前位置对应的矩阵。

返回类型

np.array


`get_fill_rgbas(vmobject)`

返回传入的 VMobject 的填充的 RGBA 数组

参数

**vmobject** – VMobject

返回

VMobject 填充的 RGBA 数组

返回类型

np.array



`get_focal_distance()`

返回相机的焦点距离。

返回

相机的焦距（以 MUnit 为单位）。

返回类型

float


`get_gamma()`

返回相机围绕从 ORIGIN 到相机的向量的旋转。

返回

相机围绕从 ORIGIN 到相机的矢量旋转的角度（以弧度为单位）

返回类型

float



`get_mobjects_to_display(*args, **kwargs)`

用于获取要通过相机显示的对象列表。

参数

- **mobjects** – Mobjects
- **include_submobjects** – 是否包含 mobjects 的子 mobjects，默认 True
- **excepted_mobjects** – 任何要排除的 mobjects，默认为 None

返回

对象列表

返回类型

list



`get_phi()`

返回极角（与 Z_AXIS 的角度）phi。

返回

以弧度表示的极角。

返回类型

float



`get_rotation_matrix()`

返回相机当前位置对应的矩阵。

返回

相机当前位置对应的矩阵。

返回类型

np.array



`get_stroke_rgbas(vmobject, background=False)`

获取传递的 VMobject 笔画的 RGBA 数组。

参数

- **vmobject** – VMobject
- **background** – 获取描边 RGBAs 时是否考虑背景，默认为 False

返回

笔画的 RGBA 数组。

返回类型

np.ndarray



`get_theta()`

返回方位角，即相机绕 Z_AXIS 旋转的角度。

返回

以弧度表示的方位角。

返回类型

float


`get_value_trackers()`

phi、theta、focal_distance、gamma 和 Zoom 的列表[`ValueTrackers`]()。

返回

ValueTracker 对象列表

返回类型

list



`get_zoom()`

返回相机的变焦量。

返回

相机的变焦量。

返回类型

float



`project_point(point)`

将当前的 rotation_matrix 作为投影矩阵应用到传递的点。

参数

**point** ( _list_ _|_ _np.ndarray_ ) – 投影点。

返回

投影后的点。

返回类型

np.array



`project_points(points)`

将当前的 rotation_matrix 作为投影矩阵应用于传递的点数组。

参数

**points** ( _np.ndarray_ _|_ _list_ ) – 要投影的点的列表。

返回

投影后的点。

返回类型

np.array


`remove_fixed_in_frame_mobjects(*mobjects)`

如果一个 mobject 通过传递它而被固定在框架中 [)，那么这将撤消该固定。Mobject 将不再固定在框架中。

参数

**mobjects** ( [_Mobject_]() ) – 不再需要在框架中固定的 mobjects。



`remove_fixed_orientation_mobjects(*mobjects)`

如果一个 mobject 通过穿过 来固定其方向 [`add_fixed_orientation_mobjects()`]()，那么这将撤消该固定。Mobject 将不再具有固定方向。

参数

**mobjects** ( [_Mobject_]() ) – 方向不再需要固定的 mobject。



`reset_rotation_matrix()`

将 self.rotation_matrix 的值设置为相机当前位置对应的矩阵



`set_focal_distance(value)`

设置相机的 focal_distance。

参数

**value** ( _float_ ) – 相机的焦距。



`set_gamma(value)`

设置相机围绕从 ORIGIN 到相机的矢量的旋转角度。

参数

**value** ( _float_ ) – 相机的新旋转角度。



`set_phi(value)`

设置极角，即 Z_AXIS 和相机通过 ORIGIN 之间的角度（以弧度表示）。

参数

**value** ( _float_ ) – 极角的新值（以弧度为单位）。



`set_theta(value)`

设置方位角，即相机围绕 Z_AXIS 旋转的角度（以弧度为单位）。

参数

**value** ( _float_ ) – 方位角的新值（以弧度为单位）。



`set_zoom(value)`

设置相机的变焦量。

参数

**value** ( _float_ ) – 相机的变焦量。
