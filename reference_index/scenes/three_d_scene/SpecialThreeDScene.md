# 特别三维场景[#](#specialthreedscene "此标题的固定链接")

合格名称：`manim.scene.three\_d\_scene.SpecialThreeDScene`

_class_ SpecialThreeDScene ( _cut_axes_at_radius = True_ , _camera_config = {'exponential_projection': True, 'should_apply_shading': True}_ , _Three_d_axes_config = {'axis_config': {'numbers_with_elongated_ticks': \[0, 1, 2\], 'lines_width': 2, '刻度频率': 1, '单位大小': 2}, 'num_axis_pieces': 1}_ , _sphere_config = {'半径': 2, '分辨率': (24, 48)}_ ,_默认角度相机位置= {'phi': 1.2217304763960306, 'theta': \- 1.9198621771937625}_ , _low_quality_config = {'camera_config': {'should_apply_shading': False}, 'sphere_config': {'分辨率': (12, 24)}, ' Three_d_axes_config' : {'num_axis_pieces': 1}}_ , _\*\* kwargs_ )[\[来源\]](../_modules/manim/scene/three_d_scene.html#SpecialThreeDScene)[#](#manim.scene.three_d_scene.SpecialThreeDScene "此定义的固定链接")

基地：[`ThreeDScene`](manim.scene.three_d_scene.ThreeDScene.html#manim.scene.three_d_scene.ThreeDScene "manim.scene. Three_d_scene.ThreeDScene")

具有更多设置的扩展[`ThreeDScene`](manim.scene.three_d_scene.ThreeDScene.html#manim.scene.three_d_scene.ThreeDScene "manim.scene. Three_d_scene.ThreeDScene")。

它有一些针对轴、球体的额外配置，以及低质量渲染的覆盖。进一步的主要区别是：

- 默认情况下，相机会对适用的 3DM 对象进行着色，除非以低质量渲染。
- 添加了球体和轴的一些默认参数。

方法

[`get_axes`](#manim.scene.three_d_scene.SpecialThreeDScene.get_axes "manim.scene. Three_d_scene.SpecialThreeDScene.get_axes")

返回一组 3D 轴。

[`get_default_camera_position`](#manim.scene.three_d_scene.SpecialThreeDScene.get_default_camera_position "manim.scene. Three_d_scene.SpecialThreeDScene.get_default_camera_position")

返回 default_angle_camera 位置。

[`get_sphere`](#manim.scene.three_d_scene.SpecialThreeDScene.get_sphere "manim.scene. Three_d_scene.SpecialThreeDScene.get_sphere")

返回一个球体，其中传递的关键字参数作为属性。

[`set_camera_to_default_position`](#manim.scene.three_d_scene.SpecialThreeDScene.set_camera_to_default_position "manim.scene. Three_d_scene.SpecialThreeDScene.set_camera_to_default_position")

将相机设置为其默认位置。

属性

`camera`

获取轴( )[\[来源\]](../_modules/manim/scene/three_d_scene.html#SpecialThreeDScene.get_axes)[#](#manim.scene.three_d_scene.SpecialThreeDScene.get_axes "此定义的固定链接")

返回一组 3D 轴。

退货

一组 3D 轴。

返回类型

[`ThreeDAxes`](manim.mobject.graphing.coordinate_systems.ThreeDAxes.html#manim.mobject.graphing.coordinate_systems.ThreeDAxes "manim.mobject.graphing.coordinate_systems.ThreeDAxes")

获取默认相机位置( )[\[来源\]](../_modules/manim/scene/three_d_scene.html#SpecialThreeDScene.get_default_camera_position)[#](#manim.scene.three_d_scene.SpecialThreeDScene.get_default_camera_position "此定义的固定链接")

返回 default_angle_camera 位置。

退货

phi、theta、focal_distance 和 gamma 的字典。

返回类型

词典

get*sphere ( *\*\* kwargs\_ )[\[来源\]](../_modules/manim/scene/three_d_scene.html#SpecialThreeDScene.get_sphere)[#](#manim.scene.three_d_scene.SpecialThreeDScene.get_sphere "此定义的固定链接")

返回一个球体，其中传递的关键字参数作为属性。

参数

\***\*kwargs**[`Sphere`](manim.mobject.three_d.three_dimensions.Sphere.html#manim.mobject.three_d.three_dimensions.Sphere "manim.mobject. Three_d. Three_dimensions.Sphere") –或 的任何有效参数[`Surface`](manim.mobject.three_d.three_dimensions.Surface.html#manim.mobject.three_d.three_dimensions.Surface "manim.mobject. Three_d. Three_dimensions.Surface")。

退货

球体对象。

返回类型

[`Sphere`](manim.mobject.three_d.three_dimensions.Sphere.html#manim.mobject.three_d.three_dimensions.Sphere "manim.mobject. Three_d. Three_dimensions.Sphere")

设置相机到默认位置( )[\[来源\]](../_modules/manim/scene/three_d_scene.html#SpecialThreeDScene.set_camera_to_default_position)[#](#manim.scene.three_d_scene.SpecialThreeDScene.set_camera_to_default_position "此定义的固定链接")

将相机设置为其默认位置。
