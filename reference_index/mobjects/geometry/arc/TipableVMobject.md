# 可提示 VM 对象

合格名称：`manim.mobject.geometry.arc.TipableVMobject`

```py
class TipableVMobject(tip_length=0.35, normal_vector=array([0., 0., 1.]), tip_style={}, **kwargs)
```

Bases: `VMobject`

用于圆弧和直线之间的共享功能。功能可大致分为以下几组：

> - 添加、创建、修改提示
>
>   - add_tip 在推送新提示之前调用 create_tip
>
>     进入 TipableVMobject 的子对象列表
>
>   - 风格和位置配置
>
> - 检查提示
>
>   - 布尔值检查 TipableVM 对象是否有提示
>
>     和一个起始提示
>
> - 吸气剂
>
>   - 简单的访问器，返回相关信息
>
>     TipableVMobject 实例的提示、长度等


方法

|||
|-|-|
[`add_tip`]()|向 TipableVMobject 实例添加提示，认识到如果它是“起始提示”，则可能需要切换端点。
`asign_tip_attr`|
[`create_tip`]()|对提示进行样式化，在空间上定位它，并将新实例化的提示返回给调用者。
`get_default_tip_length`|
[`get_end`]()|返回笔画围绕端点的点[`Mobject`]()。
`get_first_handle`|
`get_last_handle`|
`get_length`|
[`get_start`]()|返回围绕笔划的起始点[`Mobject`]()。
[`get_tip`]()|返回 TipableVMobject 实例的（第一个）提示，否则抛出异常。
[`get_tips`]()|返回包含 TipableVMObject 实例的提示的 VGroup（VMobject 集合）。
[`get_unpositioned_tip`]()|返回已按风格配置但尚未在空间中指定位置的提示。
`has_start_tip`|
`has_tip`|
`pop_tips`|
`position_tip`|
`reset_endpoints_based_on_tip`|



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



`add_tip(tip=None, tip_shape=None, tip_length=None, tip_width=None, at_start=False)`

向 TipableVMobject 实例添加提示，认识到如果它是“起始提示”，则可能需要切换端点。

`create_tip(tip_shape=None, tip_length=None, tip_width=None, at_start=False)`

对提示进行样式化，在空间上定位它，并将新实例化的提示返回给调用者。

`get_end()`

返回笔画围绕端点的点[`Mobject`]()。

`get_start()`

返回围绕笔划的起始点[`Mobject`]()。

`get_tip()`

返回 TipableVMobject 实例的（第一个）提示，否则抛出异常。

`get_tips()`

返回包含 TipableVMObject 实例的提示的 VGroup（VMobject 集合）。

`get_unpositioned_tip(tip_shape=None, tip_length=None, tip_width=None)`

返回已按风格配置但尚未在空间中指定位置的提示。
