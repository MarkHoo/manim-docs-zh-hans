# 三维相机[#](#threedcamera "此标题的固定链接")

合格名称：`manim.camera.three\_d\_camera.ThreeDCamera`

_class_ ThreeDCamera ( _focal_distance = 20.0_ , _shading_factor = 0.2_ , _default_distance = 5.0_ , _light_source_start_point = array(\[- 7., \- 9., 10.\])_ , _should_apply_shading = True_ , _exponential_projection = False_ , _phi = 0_ , _theta = \- 1.5707963267948966_ ,_伽玛= 0_，_缩放= 1_，_\*\*夸格斯_）[\[来源\]](../_modules/manim/camera/three_d_camera.html#ThreeDCamera)[#](#manim.camera.three_d_camera.ThreeDCamera "此定义的固定链接")

基地：[`Camera`](manim.camera.camera.Camera.html#manim.camera.camera.Camera "manim.camera.camera.Camera")

初始化 ThreeDCamera

参数

**\*kwargs** – Camera 的任何关键字参数。

方法

[`add_fixed_in_frame_mobjects`](#manim.camera.three_d_camera.ThreeDCamera.add_fixed_in_frame_mobjects "manim.camera. Three_d_camera.ThreeDCamera.add_fixed_in_frame_mobjects")

此方法允许对象具有固定位置，即使相机四处移动。

[`add_fixed_orientation_mobjects`](#manim.camera.three_d_camera.ThreeDCamera.add_fixed_orientation_mobjects "manim.camera. Three_d_camera.ThreeDCamera.add_fixed_orientation_mobjects")

此方法允许 mobject 具有固定的方向，即使相机四处移动也是如此。

[`capture_mobjects`](#manim.camera.three_d_camera.ThreeDCamera.capture_mobjects "manim.camera. Three_d_camera.ThreeDCamera.capture_mobjects")

通过将 mobject 打印在 上来捕获它们`pixel_array`。

[`generate_rotation_matrix`](#manim.camera.three_d_camera.ThreeDCamera.generate_rotation_matrix "manim.camera. Three_d_camera.ThreeDCamera.generate_rotation_matrix")

根据相机的当前位置生成旋转矩阵。

[`get_fill_rgbas`](#manim.camera.three_d_camera.ThreeDCamera.get_fill_rgbas "manim.camera. Three_d_camera.ThreeDCamera.get_fill_rgbas")

返回传入的 VMobject 的填充的 RGBA 数组

[`get_focal_distance`](#manim.camera.three_d_camera.ThreeDCamera.get_focal_distance "manim.camera. Three_d_camera.ThreeDCamera.get_focal_distance")

返回相机的焦点距离。

[`get_gamma`](#manim.camera.three_d_camera.ThreeDCamera.get_gamma "manim.camera. Three_d_camera.ThreeDCamera.get_gamma")

返回相机围绕从 ORIGIN 到相机的向量的旋转。

[`get_mobjects_to_display`](#manim.camera.three_d_camera.ThreeDCamera.get_mobjects_to_display "manim.camera. Three_d_camera.ThreeDCamera.get_mobjects_to_display")

用于获取要通过相机显示的对象列表。

[`get_phi`](#manim.camera.three_d_camera.ThreeDCamera.get_phi "manim.camera. Three_d_camera.ThreeDCamera.get_phi")

返回极角（与 Z_AXIS 的角度）phi。

[`get_rotation_matrix`](#manim.camera.three_d_camera.ThreeDCamera.get_rotation_matrix "manim.camera. Three_d_camera.ThreeDCamera.get_rotation_matrix")

返回相机当前位置对应的矩阵。

[`get_stroke_rgbas`](#manim.camera.three_d_camera.ThreeDCamera.get_stroke_rgbas "manim.camera. Three_d_camera.ThreeDCamera.get_中风_rgbas")

获取传递的 VMobject 笔画的 RGBA 数组。

[`get_theta`](#manim.camera.three_d_camera.ThreeDCamera.get_theta "manim.camera. Three_d_camera.ThreeDCamera.get_theta")

返回方位角，即相机绕 Z_AXIS 旋转的角度。

[`get_value_trackers`](#manim.camera.three_d_camera.ThreeDCamera.get_value_trackers "manim.camera. Three_d_camera.ThreeDCamera.get_value_trackers")

phi、theta、focal_distance、gamma 和 Zoom 的列表[`ValueTrackers`](manim.mobject.value_tracker.ValueTracker.html#manim.mobject.value_tracker.ValueTracker "manim.mobject.value_tracker.ValueTracker")。

[`get_zoom`](#manim.camera.three_d_camera.ThreeDCamera.get_zoom "manim.camera. Three_d_camera.ThreeDCamera.get_zoom")

返回相机的变焦量。

`modified_rgbas`

[`project_point`](#manim.camera.three_d_camera.ThreeDCamera.project_point "manim.camera. Three_d_camera.ThreeDCamera.project_point")

将当前的 rotation_matrix 作为投影矩阵应用到传递的点。

[`project_points`](#manim.camera.three_d_camera.ThreeDCamera.project_points "manim.camera. Three_d_camera.ThreeDCamera.project_points")

将当前的 rotation_matrix 作为投影矩阵应用于传递的点数组。

[`remove_fixed_in_frame_mobjects`](#manim.camera.three_d_camera.ThreeDCamera.remove_fixed_in_frame_mobjects "manim.camera. Three_d_camera.ThreeDCamera.remove_fixed_in_frame_mobjects")

如果一个 mobject 通过传递它而被固定在框架中[`add_fixed_in_frame_mobjects()`](#manim.camera.three_d_camera.ThreeDCamera.add_fixed_in_frame_mobjects "manim.camera. Three_d_camera.ThreeDCamera.add_fixed_in_frame_mobjects")，那么这将撤消该固定。

[`remove_fixed_orientation_mobjects`](#manim.camera.three_d_camera.ThreeDCamera.remove_fixed_orientation_mobjects "manim.camera. Three_d_camera.ThreeDCamera.remove_fixed_orientation_mobjects")

如果一个 mobject 通过穿过 来固定其方向[`add_fixed_orientation_mobjects()`](#manim.camera.three_d_camera.ThreeDCamera.add_fixed_orientation_mobjects "manim.camera. Three_d_camera.ThreeDCamera.add_fixed_orientation_mobjects")，那么这将撤消该固定。

[`reset_rotation_matrix`](#manim.camera.three_d_camera.ThreeDCamera.reset_rotation_matrix "manim.camera. Three_d_camera.ThreeDCamera.reset_rotation_matrix")

将 self.rotation_matrix 的值设置为相机当前位置对应的矩阵

[`set_focal_distance`](#manim.camera.three_d_camera.ThreeDCamera.set_focal_distance "manim.camera. Three_d_camera.ThreeDCamera.set_focal_distance")

设置相机的 focal_distance。

[`set_gamma`](#manim.camera.three_d_camera.ThreeDCamera.set_gamma "manim.camera. Three_d_camera.ThreeDCamera.set_gamma")

设置相机围绕从 ORIGIN 到相机的矢量的旋转角度。

[`set_phi`](#manim.camera.three_d_camera.ThreeDCamera.set_phi "manim.camera. Three_d_camera.ThreeDCamera.set_phi")

设置极角，即 Z_AXIS 和相机通过 ORIGIN 之间的角度（以弧度表示）。

[`set_theta`](#manim.camera.three_d_camera.ThreeDCamera.set_theta "manim.camera. Three_d_camera.ThreeDCamera.set_theta")

设置方位角，即相机围绕 Z_AXIS 旋转的角度（以弧度为单位）。

[`set_zoom`](#manim.camera.three_d_camera.ThreeDCamera.set_zoom "manim.camera. Three_d_camera.ThreeDCamera.set_zoom")

设置相机的变焦量。

`transform_points_pre_display`

属性

`background_color`

`background_opacity`

`frame_center`

add*fixed_in_frame_mobjects ( *\* mobjects\_ )[\[来源\]](../_modules/manim/camera/three_d_camera.html#ThreeDCamera.add_fixed_in_frame_mobjects)[#](#manim.camera.three_d_camera.ThreeDCamera.add_fixed_in_frame_mobjects "此定义的固定链接")

此方法允许对象具有固定位置，即使相机四处移动。EG 如果通过这个方法，在框架的顶部，它将继续显示在框架的顶部。

在显示标题或公式等时非常有用。

参数

\***\*mobjects** ( [_Mobject_](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject") ) – 要在框架中修复的 mobject。

add*fixed_orientation*mobjects ( *\* mobjects* , \_use_static_center_func = False* , \_center_func = None* )[\[来源\]](../_modules/manim/camera/three_d_camera.html#ThreeDCamera.add_fixed_orientation_mobjects)[#](#manim.camera.three_d_camera.ThreeDCamera.add_fixed_orientation_mobjects "此定义的固定链接")

此方法允许 mobject 具有固定的方向，即使相机四处移动也是如此。EG 如果通过此方法，面向相机，即使相机移动，它也会继续面向相机。在向图表等添加标签时非常有用。

参数

- **\*mobjects** ( [_Mobject_](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject") ) – 方向必须固定的 mobject。
- **use_static_center_func** ( _bool_ ) – 是否使用以 mobject 的中心为中心点的函数，默认为 False
- **center_func** ( _Callable_ _\[_ _\[_ _\]_ _,_ _np.ndarray_ _\]_ _|_ _None_ ) – 返回 mobject 将相对于其定向的中心点的函数，默认为 None

capture*mobjects ( \_mobjects* , _\*\* kwargs_ )[\[来源\]](../_modules/manim/camera/three_d_camera.html#ThreeDCamera.capture_mobjects)[#](#manim.camera.three_d_camera.ThreeDCamera.capture_mobjects "此定义的固定链接")

通过将 mobject 打印在 上来捕获它们`pixel_array`。

这是将场景的内容转换为数组的基本函数，然后将其转换为图像或视频。

参数

- **mobjects** – 要捕获的 Mobjects。
- **kwargs** – 要传递给 的关键字参数[`get_mobjects_to_display()`](#manim.camera.three_d_camera.ThreeDCamera.get_mobjects_to_display "manim.camera. Three_d_camera.ThreeDCamera.get_mobjects_to_display")。

笔记

有关当前可以呈现的类的列表，请参阅`display_funcs()`。

生成旋转矩阵( )[\[来源\]](../_modules/manim/camera/three_d_camera.html#ThreeDCamera.generate_rotation_matrix)[#](#manim.camera.three_d_camera.ThreeDCamera.generate_rotation_matrix "此定义的固定链接")

根据相机的当前位置生成旋转矩阵。

退货

相机当前位置对应的矩阵。

返回类型

np.数组

get*fill_rgbas（\_vmobject*）[\[来源\]](../_modules/manim/camera/three_d_camera.html#ThreeDCamera.get_fill_rgbas)[#](#manim.camera.three_d_camera.ThreeDCamera.get_fill_rgbas "此定义的固定链接")

返回传入的 VMobject 的填充的 RGBA 数组

参数

**vmobject** – VMobject

退货

VMobject 填充的 RGBA 数组

返回类型

np.数组

获取焦点距离( )[\[来源\]](../_modules/manim/camera/three_d_camera.html#ThreeDCamera.get_focal_distance)[#](#manim.camera.three_d_camera.ThreeDCamera.get_focal_distance "此定义的固定链接")

返回相机的焦点距离。

退货

相机的焦距（以 MUnit 为单位）。

返回类型

漂浮

获取伽玛( )[\[来源\]](../_modules/manim/camera/three_d_camera.html#ThreeDCamera.get_gamma)[#](#manim.camera.three_d_camera.ThreeDCamera.get_gamma "此定义的固定链接")

返回相机围绕从 ORIGIN 到相机的向量的旋转。

退货

相机围绕从 ORIGIN 到相机的矢量旋转的角度（以弧度为单位）

返回类型

漂浮

get_mobjects_to*display ( *\* args* , *\*\* kwargs\_ )[\[来源\]](../_modules/manim/camera/three_d_camera.html#ThreeDCamera.get_mobjects_to_display)[#](#manim.camera.three_d_camera.ThreeDCamera.get_mobjects_to_display "此定义的固定链接")

用于获取要通过相机显示的对象列表。

参数

- **mobjects** – Mobjects
- **include_submobjects** – 是否包含 mobjects 的子 mobjects，默认 True
- **excepted_mobjects** – 任何要排除的 mobjects，默认为 None

退货

对象列表

返回类型

列表

获取\_phi ( )[\[来源\]](../_modules/manim/camera/three_d_camera.html#ThreeDCamera.get_phi)[#](#manim.camera.three_d_camera.ThreeDCamera.get_phi "此定义的固定链接")

返回极角（与 Z_AXIS 的角度）phi。

退货

以弧度表示的极角。

返回类型

漂浮

获取旋转矩阵( )[\[来源\]](../_modules/manim/camera/three_d_camera.html#ThreeDCamera.get_rotation_matrix)[#](#manim.camera.three_d_camera.ThreeDCamera.get_rotation_matrix "此定义的固定链接")

返回相机当前位置对应的矩阵。

退货

相机当前位置对应的矩阵。

返回类型

np.数组

get*lines_rgbas ( \_vmobject* ,_背景= False_ )[\[来源\]](../_modules/manim/camera/three_d_camera.html#ThreeDCamera.get_stroke_rgbas)[#](#manim.camera.three_d_camera.ThreeDCamera.get_stroke_rgbas "此定义的固定链接")

获取传递的 VMobject 笔画的 RGBA 数组。

参数

- **vmobject** – VMobject
- **background** – 获取描边 RGBAs 时是否考虑背景，默认为 False

退货

笔画的 RGBA 数组。

返回类型

np.ndarray

获取 θ ( )[\[来源\]](../_modules/manim/camera/three_d_camera.html#ThreeDCamera.get_theta)[#](#manim.camera.three_d_camera.ThreeDCamera.get_theta "此定义的固定链接")

返回方位角，即相机绕 Z_AXIS 旋转的角度。

退货

以弧度表示的方位角。

返回类型

漂浮

获取值跟踪器( )[\[来源\]](../_modules/manim/camera/three_d_camera.html#ThreeDCamera.get_value_trackers)[#](#manim.camera.three_d_camera.ThreeDCamera.get_value_trackers "此定义的固定链接")

phi、theta、focal_distance、gamma 和 Zoom 的列表[`ValueTrackers`](manim.mobject.value_tracker.ValueTracker.html#manim.mobject.value_tracker.ValueTracker "manim.mobject.value_tracker.ValueTracker")。

退货

ValueTracker 对象列表

返回类型

列表

获取缩放( )[\[来源\]](../_modules/manim/camera/three_d_camera.html#ThreeDCamera.get_zoom)[#](#manim.camera.three_d_camera.ThreeDCamera.get_zoom "此定义的固定链接")

返回相机的变焦量。

退货

相机的变焦量。

返回类型

漂浮

项目*点（*点\_）[\[来源\]](../_modules/manim/camera/three_d_camera.html#ThreeDCamera.project_point)[#](#manim.camera.three_d_camera.ThreeDCamera.project_point "此定义的固定链接")

将当前的 rotation_matrix 作为投影矩阵应用到传递的点。

参数

**point** ( _list_ _|_ _np.ndarray_ ) – 投影点。

退货

投影后的点。

返回类型

np.数组

项目点（_点_）[\[来源\]](../_modules/manim/camera/three_d_camera.html#ThreeDCamera.project_points)[#](#manim.camera.three_d_camera.ThreeDCamera.project_points "此定义的固定链接")

将当前的 rotation_matrix 作为投影矩阵应用于传递的点数组。

参数

**points** ( _np.ndarray_ _|_ _list_ ) – 要投影的点的列表。

退货

投影后的点。

返回类型

np.数组

删除*固定\_in_frame_mobjects ( *\* mobjects\_ )[\[来源\]](../_modules/manim/camera/three_d_camera.html#ThreeDCamera.remove_fixed_in_frame_mobjects)[#](#manim.camera.three_d_camera.ThreeDCamera.remove_fixed_in_frame_mobjects "此定义的固定链接")

如果一个 mobject 通过传递它而被固定在框架中 [`add_fixed_in_frame_mobjects()`](#manim.camera.three_d_camera.ThreeDCamera.add_fixed_in_frame_mobjects "manim.camera. Three_d_camera.ThreeDCamera.add_fixed_in_frame_mobjects")，那么这将撤消该固定。Mobject 将不再固定在框架中。

参数

**mobjects** ( [_Mobject_](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject") ) – 不再需要在框架中固定的 mobjects。

删除*固定*方向*mobjects ( *\* mobjects\_ )[\[来源\]](../_modules/manim/camera/three_d_camera.html#ThreeDCamera.remove_fixed_orientation_mobjects)[#](#manim.camera.three_d_camera.ThreeDCamera.remove_fixed_orientation_mobjects "此定义的固定链接")

如果一个 mobject 通过穿过 来固定其方向 [`add_fixed_orientation_mobjects()`](#manim.camera.three_d_camera.ThreeDCamera.add_fixed_orientation_mobjects "manim.camera. Three_d_camera.ThreeDCamera.add_fixed_orientation_mobjects")，那么这将撤消该固定。Mobject 将不再具有固定方向。

参数

**mobjects** ( [_Mobject_](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject") ) – 方向不再需要固定的 mobject。

重置旋转矩阵( )[\[来源\]](../_modules/manim/camera/three_d_camera.html#ThreeDCamera.reset_rotation_matrix)[#](#manim.camera.three_d_camera.ThreeDCamera.reset_rotation_matrix "此定义的固定链接")

将 self.rotation_matrix 的值设置为相机当前位置对应的矩阵

设置焦点距离（_值_）[\[来源\]](../_modules/manim/camera/three_d_camera.html#ThreeDCamera.set_focal_distance)[#](#manim.camera.three_d_camera.ThreeDCamera.set_focal_distance "此定义的固定链接")

设置相机的 focal_distance。

参数

**value** ( _float_ ) – 相机的焦距。

设置伽玛（_值_）[\[来源\]](../_modules/manim/camera/three_d_camera.html#ThreeDCamera.set_gamma)[#](#manim.camera.three_d_camera.ThreeDCamera.set_gamma "此定义的固定链接")

设置相机围绕从 ORIGIN 到相机的矢量的旋转角度。

参数

**value** ( _float_ ) – 相机的新旋转角度。

set*phi（*值\_）[\[来源\]](../_modules/manim/camera/three_d_camera.html#ThreeDCamera.set_phi)[#](#manim.camera.three_d_camera.ThreeDCamera.set_phi "此定义的固定链接")

设置极角，即 Z_AXIS 和相机通过 ORIGIN 之间的角度（以弧度表示）。

参数

**value** ( _float_ ) – 极角的新值（以弧度为单位）。

set*theta（*值\_）[\[来源\]](../_modules/manim/camera/three_d_camera.html#ThreeDCamera.set_theta)[#](#manim.camera.three_d_camera.ThreeDCamera.set_theta "此定义的固定链接")

设置方位角，即相机围绕 Z_AXIS 旋转的角度（以弧度为单位）。

参数

**value** ( _float_ ) – 方位角的新值（以弧度为单位）。

设置缩放（_值_）[\[来源\]](../_modules/manim/camera/three_d_camera.html#ThreeDCamera.set_zoom)[#](#manim.camera.three_d_camera.ThreeDCamera.set_zoom "此定义的固定链接")

设置相机的变焦量。

参数

**value** ( _float_ ) – 相机的变焦量。
