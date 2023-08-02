# 大括号

合格名称：`manim.mobject.svg.brace.Brace`


```py

```

获取一个 mobject 并在其旁边绘制一个大括号。

传递方向向量确定绘制支撑的方向。默认情况下，它是从下面绘制的。

参数

- **mobject** ( [_Mobject_]() ) – 与大括号相邻的 mobject。
- **Direction** ( _Sequence_ _\[_ _float_ _\]_ _|_ _None_ ) – 支撑面向 mobject 的方向。

也可以看看

[`BraceBetweenPoints`]()

例子

示例：大括号示例

![BraceExample-1.png](../_images/BraceExample-1.png)

```py

```


方法

[`get_direction`]()

用于[`shoelace_direction()`]()计算方向。

`get_tex`

`get_text`

`get_tip`

`put_at_tip`

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

获取方向( )

用于[`shoelace_direction()`]()计算方向。点的方向决定了绘制对象的方向，顺时针还是逆时针。

例子

a 的默认方向[`Circle`]()是逆时针：

```py

```


退货

要么`"CW"`要么`"CCW"`.

返回类型

`str`
