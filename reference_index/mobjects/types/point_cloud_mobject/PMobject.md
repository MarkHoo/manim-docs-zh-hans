# PMobject

合格名称：`manim.mobject.types.point\_cloud\_mobject.PMobject`


```py

```

由点云组成的圆盘

例子

示例：PMobjectExample [¶](#pmobjectexample)

![../_images/PMobjectExample-1.png](../_images/PMobjectExample-1.png)


```py

```

方法

[`add_points`](#manim.mobject.types.point_cloud_mobject.PMobject.add_points "manim.mobject.types.point_cloud_mobject.PMobject.add_points")

加分。

`align_points_with_larger`

`fade_to`

`filter_out`

`get_all_rgbas`

`get_array_attrs`

[`get_color`](#manim.mobject.types.point_cloud_mobject.PMobject.get_color "manim.mobject.types.point_cloud_mobject.PMobject.get_color")

返回的颜色[`Mobject`](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject")

[`get_mobject_type_class`](#manim.mobject.types.point_cloud_mobject.PMobject.get_mobject_type_class "manim.mobject.types.point_cloud_mobject.PMobject.get_mobject_type_class")

返回此 mobject 类型的基类。

[`get_point_mobject`](#manim.mobject.types.point_cloud_mobject.PMobject.get_point_mobject "manim.mobject.types.point_cloud_mobject.PMobject.get_point_mobject")

最简单的[`Mobject`](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject")就是转化为自我或转化为自我。

`get_stroke_width`

`ingest_submobjects`

`interpolate_color`

`match_colors`

`point_from_proportion`

`pointwise_become_partial`

[`reset_points`](#manim.mobject.types.point_cloud_mobject.PMobject.reset_points "manim.mobject.types.point_cloud_mobject.PMobject.reset_points")

设置`points`为空数组。

[`set_color`](#manim.mobject.types.point_cloud_mobject.PMobject.set_color "manim.mobject.types.point_cloud_mobject.PMobject.set_color")

条件是接受一个参数 (x, y, z) 的函数。

`set_color_by_gradient`

`set_colors_by_radial_gradient`

`set_stroke_width`

[`sort_points`](#manim.mobject.types.point_cloud_mobject.PMobject.sort_points "manim.mobject.types.point_cloud_mobject.PMobject.sort_points")

函数是从 R^3 到 R 的任何映射

[`thin_out`](#manim.mobject.types.point_cloud_mobject.PMobject.thin_out "manim.mobject.types.point_cloud_mobject.PMobject.thin_out")

删除除每个第 n 个点之外的所有点（n = 因子）

属性

`animate`

用于对 的任何方法的应用程序进行动画处理`self`。

`animation_overrides`

`depth`

对象的深度。

`height`

mobject 的高度。

`width`

mobject 的宽度。

add*points (*点*, \_rgbas =无*,_颜色=无_, _alpha = 1_ )[\[来源\]](../_modules/manim/mobject/types/point_cloud_mobject.html#PMobject.add_points)[#](#manim.mobject.types.point_cloud_mobject.PMobject.add_points "此定义的固定链接")

加分。

点必须是 Nx3 numpy 数组。如果 Rgbas 不是 None，则它必须是 Nx4 numpy 数组。

获取颜色( )[\[来源\]](../_modules/manim/mobject/types/point_cloud_mobject.html#PMobject.get_color)[#](#manim.mobject.types.point_cloud_mobject.PMobject.get_color "此定义的固定链接")

返回的颜色[`Mobject`](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject")

_静态_ get_mobject_type_class ( )[\[来源\]](../_modules/manim/mobject/types/point_cloud_mobject.html#PMobject.get_mobject_type_class)[#](#manim.mobject.types.point_cloud_mobject.PMobject.get_mobject_type_class "此定义的固定链接")

返回此 mobject 类型的基类。

get*point_mobject（*中心=无\_）[\[来源\]](../_modules/manim/mobject/types/point_cloud_mobject.html#PMobject.get_point_mobject)[#](#manim.mobject.types.point_cloud_mobject.PMobject.get_point_mobject "此定义的固定链接")

最简单的[`Mobject`](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject")就是转化为自我或转化为自我。应由适当类型的点

重置点( )[\[来源\]](../_modules/manim/mobject/types/point_cloud_mobject.html#PMobject.reset_points)[#](#manim.mobject.types.point_cloud_mobject.PMobject.reset_points "此定义的固定链接")

设置`points`为空数组。

set*color（*颜色= '#FFFF00'*，*系列= True\_）[\[来源\]](../_modules/manim/mobject/types/point_cloud_mobject.html#PMobject.set_color)[#](#manim.mobject.types.point_cloud_mobject.PMobject.set_color "此定义的固定链接")

条件是接受一个参数 (x, y, z) 的函数。这里它只是递归到子对象，但是在子类中，这应该基于颜色的内部工作原理进一步实现

sort*points ( \_function=<function PMobject.<lambda>>* )[\[来源\]](../_modules/manim/mobject/types/point_cloud_mobject.html#PMobject.sort_points)[#](#manim.mobject.types.point_cloud_mobject.PMobject.sort_points "此定义的固定链接")

函数是从 R^3 到 R 的任何映射

Thin*out（*因子= 5\_）[\[来源\]](../_modules/manim/mobject/types/point_cloud_mobject.html#PMobject.thin_out)[#](#manim.mobject.types.point_cloud_mobject.PMobject.thin_out "此定义的固定链接")

删除除每个第 n 个点之外的所有点（n = 因子）
