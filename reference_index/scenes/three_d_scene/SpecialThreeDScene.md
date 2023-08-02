# 特别三维场景

合格名称：`manim.scene.three\_d\_scene.SpecialThreeDScene`

```py
class SpecialThreeDScene(cut_axes_at_radius=True, camera_config={'exponential_projection': True, 'should_apply_shading': True}, three_d_axes_config={'axis_config': {'numbers_with_elongated_ticks': [0, 1, 2], 'stroke_width': 2, 'tick_frequency': 1, 'unit_size': 2}, 'num_axis_pieces': 1}, sphere_config={'radius': 2, 'resolution': (24, 48)}, default_angled_camera_position={'phi': 1.2217304763960306, 'theta': - 1.9198621771937625}, low_quality_config={'camera_config': {'should_apply_shading': False}, 'sphere_config': {'resolution': (12, 24)}, 'three_d_axes_config': {'num_axis_pieces': 1}}, **kwargs)
```

Bases: ThreeDScene

具有更多设置的扩展[`ThreeDScene`]()。

它有一些针对轴、球体的额外配置，以及低质量渲染的覆盖。进一步的主要区别是：

- 默认情况下，相机会对适用的 3DM 对象进行着色，除非以低质量渲染。
- 添加了球体和轴的一些默认参数。

方法

[`get_axes`]()
返回一组 3D 轴。
[`get_default_camera_position`]()
返回 default_angle_camera 位置。
[`get_sphere`]()
返回一个球体，其中传递的关键字参数作为属性。
[`set_camera_to_default_position`]()
将相机设置为其默认位置。



属性

`camera`

获取轴( )

返回一组 3D 轴。

退货

一组 3D 轴。

返回类型

[`ThreeDAxes`]()

获取默认相机位置( )

返回 default_angle_camera 位置。

退货

phi、theta、focal_distance 和 gamma 的字典。

返回类型

词典

get*sphere ( *\\*\* kwargs\_ )

返回一个球体，其中传递的关键字参数作为属性。

参数

\***\*kwargs**[`Sphere`]() –或 的任何有效参数[`Surface`]()。

退货

球体对象。

返回类型

[`Sphere`]()

设置相机到默认位置( )

将相机设置为其默认位置。
