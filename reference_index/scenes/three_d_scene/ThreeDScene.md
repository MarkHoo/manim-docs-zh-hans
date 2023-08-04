# 三维场景

合格名称：`manim.scene.three\_d\_scene.ThreeDScene`

```py
class ThreeDScene(camera_class=<class 'manim.camera.three_d_camera.ThreeDCamera'>, ambient_camera_rotation=None, default_angled_camera_orientation_kwargs=None, **kwargs)
```

Bases: `Scene`

这是一个场景，具有特殊的配置和属性，使其适合三维场景。


方法

|||
|-|-|
[`add_fixed_in_frame_mobjects`]()|该方法用于防止相机移动时对象的旋转和移动。
[`add_fixed_orientation_mobjects`]()|此方法用于防止相机移动时对象旋转和倾斜。
[`begin_3dillusion_camera_rotation`]()|此方法围绕当前相机方向创建 3D 相机旋转错觉。
[`begin_ambient_camera_rotation`]()|此方法开始相机围绕 Z_AXIS 沿逆时针方向进行环境旋转
[`get_moving_mobjects`]()|此方法返回场景中正在移动的所有 Mobject 的列表，这些 Mobject 也在传递的动画中。
[`move_camera`]()|此方法将相机移动到给定的球面坐标。
[`remove_fixed_in_frame_mobjects`]()|此方法撤消了 add_fixed_in_frame_mobjects 所做的操作。
[`remove_fixed_orientation_mobjects`]()|此方法“取消固定”所传递的 mobject 的方向，这意味着它们将不再相对于相机处于相同的角度。
[`set_camera_orientation`]()|此方法设置场景中相机的方向。
[`set_to_default_angled_camera_orientation`]()|此方法将 default_angle_camera_orientation 设置为传递的关键字参数，并将相机设置为该方向。
[`stop_3dillusion_camera_rotation`]()|此方法停止所有幻觉相机旋转。
[`stop_ambient_camera_rotation`]()|此方法停止所有环境相机旋转。



属性

`camera`


```py
add_fixed_in_frame_mobjects(*mobjects)
```

该方法用于防止相机移动时对象的旋转和移动。mobject 本质上是重叠的，并且不会受到相机移动的任何影响。

参数

**\*mobjects** ( [_Mobject_]() ) – 方向必须固定的 Mobject。


```py
add_fixed_orientation_mobjects(*mobjects, **kwargs)
```

此方法用于防止相机移动时对象旋转和倾斜。mobject 仍然可以在 x、y、z 方向上移动，但始终处于通过此方法时的角度（相对于相机）。）

参数

- **\*mobjects** ( [_Mobject_]() ) – 方向必须固定的 Mobject。
- \***\*夸格斯**–

  一些有效的 kwargs 是

  use_static_center_func ：布尔 center_func ：函数

begin*3dillusion_camera*rotation（*速率= 1*， \_origin_phi =无*， \_origin_theta =无*）

此方法围绕当前相机方向创建 3D 相机旋转错觉。

参数

- **rate** ( _float_ ) – 相机旋转幻象运行的速率。
- **origin_phi** ( _float_ _|_ _None_ ) – 相机应移动的极角。默认为当前 phi 角度。
- **origin_theta** ( _float_ _|_ _None_ ) – 相机应移动的方位角。默认为当前 theta 角。

begin_ambient_camera*rotation（*速率= 0.02*，\*约= 'theta'\_）

此方法开始相机围绕 Z_AXIS 沿逆时针方向进行环境旋转

参数

- **rate** ( _float_ ) – 相机围绕 Z_AXIS 旋转的速率。负利率表示顺时针旋转。
- **about** ( _str_ ) – 3 个选项之一：\[“theta”、“phi”、“gamma”\]。默认为 θ。

get*moving_mobjects ( *\\*动画\_)

此方法返回场景中正在移动的所有 Mobject 的列表，这些 Mobject 也在传递的动画中。

参数

**\*animations** ( [_Animation_]() ) – 将检查其 mobject 的动画。

move*camera（\_phi =无*， _theta =无_， _gamma =无_，_变焦=无_， _focal_distance =无_， _frame_center =无_， _added_anims = \[\]_， _\*\* kwargs_）

此方法将相机移动到给定的球面坐标。

参数

- **phi** ( _float_ _|_ _None_ ) – 极角，即 Z_AXIS 和相机之间通过 ORIGIN 的角度（以弧度表示）。
- **theta** ( _float_ _|_ _None_ ) – 方位角，即相机绕 Z_AXIS 旋转的角度。
- **focus_distance** ( _float_ _|_ _None_ ) – ORIGIN 和相机之间的径向 focus_distance。
- **gamma** ( _float_ _|_ _None_ ) – 相机围绕从 ORIGIN 到相机的向量的旋转。
- **Zoom** ( _float_ _|_ _None_ ) – 相机的缩放系数。
- **frame_center** ( [_Mobject_]() _|_ _Sequence_ _\[_ _float_ _\]_ _|_ _None_ ) – 笛卡尔坐标中相机框架的新中心。
- **added_anims** ( _Iterable_ _\[_ [_Animation_]() _\]_ ) – 要同时播放的任何其他动画。

删除*固定\_in_frame_mobjects ( *\\* mobjects\_ )

> 此方法撤消了 add_fixed_in_frame_mobjects 所做的操作。它允许对象受到相机移动的影响。

参数

**\*mobjects** ( [_Mobject_]() ) – 位置和方向必须不固定的 Mobject。

删除*固定*方向*mobjects ( *\\* mobjects\_ )

此方法“取消固定”所传递的对象的方向，这意味着它们将不再相对于相机处于相同的角度。仅当 mobject 首先通过 add_fixed_orientation_mobjects 传递时，这才有意义。

参数

**\*mobjects** ( [_Mobject_]() ) – 方向必须不固定的 Mobject。

set*camera_orientation（\_phi =无*， _theta =无_， _gamma =无_，_变焦=无_， _focal_distance =无_， _frame_center =无_， _\*\* kwargs_）

此方法设置场景中相机的方向。

参数

- **phi** ( _float_ _|_ _None_ ) – 极角，即 Z_AXIS 和相机之间通过 ORIGIN 的角度（以弧度表示）。
- **theta** ( _float_ _|_ _None_ ) – 方位角，即相机绕 Z_AXIS 旋转的角度。
- **focus_distance** ( _float_ _|_ _None_ ) – 相机的 focus_distance。
- **gamma** ( _float_ _|_ _None_ ) – 相机围绕从 ORIGIN 到相机的向量的旋转。
- **Zoom** ( _float_ _|_ _None_ ) – 场景的缩放系数。
- **frame_center** ( [_Mobject_]() _|_ _Sequence_ _\[_ _float_ _\]_ _|_ _None_ ) – 笛卡尔坐标中相机框架的新中心。

set_to_default_angled_camera*orientation ( *\\*\* kwargs\_ )

此方法将 default_angle_camera_orientation 设置为传递的关键字参数，并将相机设置为该方向。

参数

\***\*kwargs** – 一些公认的 kwargs 是 phi、theta、focal_distance、gamma，它们与 set_camera_orientation 中的参数含义相同。

stop_3dillusion_camera_rotation ( )

此方法停止所有幻觉相机旋转。

stop_ambient_camera*rotation ( \_about = 'theta'* )

此方法停止所有环境相机旋转。
