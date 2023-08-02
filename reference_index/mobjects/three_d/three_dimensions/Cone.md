# 锥

合格名称：`manim.mobject.three\_d.three\_dimensions.Cone`


```py

```

一个圆锥体。可以使用 2 个参数来定义：高度和底半径。极角 theta 可以使用 arctan(base_radius / height) 计算。球半径 r 使用毕达哥拉斯定理计算。

参数

- **base_radius** ( _float_ ) – 圆锥体逐渐变细的底半径。
- **height** ( _float_ ) – 从底半径形成的平面到圆锥体顶点测量的高度。
- **Direction** ( _np.ndarray_ ) – 顶点的方向。
- **show_base** ( _bool_ ) – 是否显示基准平面。
- **v_range** ( _Sequence_ _\[_ _float_ _\]_ ) – 开始和结束的方位角。
- **u_min** ( _float_ ) – 顶点处的半径。
- **checkerboard_colors** ( _bool_ ) – 在锥体上显示棋盘网格纹理。

例子

示例：ExampleCone [¶](#examplecone)

![../_images/ExampleCone-1.png](../_images/ExampleCone-1.png)


```py

```


方法

[`func`](#manim.mobject.three_d.three_dimensions.Cone.func "manim.mobject. Three_d. Three_dimensions.Cone.func")

从球坐标转换为笛卡尔坐标。

[`get_direction`](#manim.mobject.three_d.three_dimensions.Cone.get_direction "manim.mobject. Three_d. Three_dimensions.Cone.get_direction")

返回 顶点的当前方向[`Cone`](#manim.mobject.three_d.three_dimensions.Cone "manim.mobject. Three_d. Three_dimensions.Cone")。

[`set_direction`](#manim.mobject.three_d.three_dimensions.Cone.set_direction "manim.mobject. Three_d. Three_dimensions.Cone.set_direction")

更改 顶点的方向[`Cone`](#manim.mobject.three_d.three_dimensions.Cone "manim.mobject. Three_d. Three_dimensions.Cone")。

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

函数（_u_， _v_）[\[来源\]](../_modules/manim/mobject/three_d/three_dimensions.html#Cone.func)[#](#manim.mobject.three_d.three_dimensions.Cone.func "此定义的固定链接")

从球坐标转换为笛卡尔坐标。

参数

- **u** ( _float_ ) – 半径。
- **v** ( _float_ ) – 方位角。

退货

定义 的点[`Cone`](#manim.mobject.three_d.three_dimensions.Cone "manim.mobject. Three_d. Three_dimensions.Cone")。

返回类型

`numpy.array`

获取方向( )[\[来源\]](../_modules/manim/mobject/three_d/three_dimensions.html#Cone.get_direction)[#](#manim.mobject.three_d.three_dimensions.Cone.get_direction "此定义的固定链接")

返回 顶点的当前方向[`Cone`](#manim.mobject.three_d.three_dimensions.Cone "manim.mobject. Three_d. Three_dimensions.Cone")。

退货

**方向**– 顶点的方向。

返回类型

`numpy.array`

设置方向（_方向_）[\[来源\]](../_modules/manim/mobject/three_d/three_dimensions.html#Cone.set_direction)[#](#manim.mobject.three_d.three_dimensions.Cone.set_direction "此定义的固定链接")

更改 顶点的方向[`Cone`](#manim.mobject.three_d.three_dimensions.Cone "manim.mobject. Three_d. Three_dimensions.Cone")。

参数

**Direction** ( _ndarray_ ) – 顶点的方向。

返回类型

没有任何
