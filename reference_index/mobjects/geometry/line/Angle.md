# 角度

合格名称：`manim.mobject.geometry.line.Angle`

_角度_ 类（_line1_、 _line2_、 _radius = None_、_象限= (1, 1)_、 _other_angle = False_、 _dot = False_、 _dot_radius = None_、 _dot_distance = 0.55_、 _dot_color = '#FFFFFF'_、_肘部= False_、 _\*\* kwargs_）[\[来源\]](../_modules/manim/mobject/geometry/line.html#Angle)[#](#manim.mobject.geometry.line.Angle "此定义的固定链接")

基地：[`VMobject`](manim.mobject.types.vectorized_mobject.VMobject.html#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject")

表示两条线的角度的圆弧或肘型对象。

参数

- **line1** ( [_Line_]() ) – 第一行。
- **line2** ( [_Line_]() ) – 第二行。
- **radius** ( _float_ ) – 的半径`Arc`。
- **Quadrant** ( _Sequence_ _\[_ _int_ _\]_ ) – 由两个数字组成的序列，`int`确定应使用 4 个象限中的哪一个。第一个值指示是否将弧锚定在第一条线上靠近终点 (1) 或起点 (-1) 的位置，第二个值的作用与第二条线上的终点 (1) 或起点 (-1) 类似。线。可能性：(1,1)、(-1,1)、(1,-1)、(-1,-1)。
- **other_angle** ( _bool_ ) – 在由两点和圆弧中心定义的两个可能的角度之间切换。如果设置为 False（默认），圆弧将始终从 line1 上的点逆时针移动，直到到达 line2 上的点。如果设置为 True，角度将从 line1 到 line2 顺时针旋转。
- **dot** ( _bool_ ) – 允许`Dot`弧内有 a。主要用作表示直角的约定。该点可以在接下来的三个参数中自定义。
- **dot_radius** ( _float_ _|_ _None_ ) – 的半径`Dot`。如果没有另外指定，该半径将为圆弧半径的 1/10。
- **dot_distance** ( _float_ ) – 从中心到弧的相对距离：0 将点置于中心，1 将点置于弧本身。
- **dot_color** ( [_Colors_]() ) – 的颜色`Dot`。
- **肘**( _bool_ ) – 生成一个肘型 mobject 来指示直角，请参阅[`RightAngle`]()参考资料 来了解更多信息和简写。
- \***\*kwargs** – 传递给`Arc`or 的构造函数的更多关键字参数[`Elbow`]()。

例子

第一个示例显示了一些中间有一个点的直角，而第二个示例显示了由两条线定义的所有 8 个可能的角度。

示例：RightArcAngle 示例

![RightArcAngleExample-1.png](../static/RightArcAngleExample-1.png)


```py

```


示例：角度示例[¶](#angleexample)

![AngleExample-1.png](../static/AngleExample-1.png)


```py

```


示例：填充角度

![FilledAngle-1.png](../static/FilledAngle-1.png)


```py

```


方法

[`from_three_points`](")

线 AB 和 BC 之间的角度。

[`get_lines`]()

获取形成班级角度的线[`Angle`]()。

[`get_value`]()

获取类的角度值[`Angle`](")。



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

_静态_ from*two_points ( \_A* , _B_ , _C_ , _\*\* kwargs_ )

线 AB 和 BC 之间的角度。

这构造了角度 ∠ABC。

参数

- **A** ( _ndarray_ ) – 第一个角腿的端点
- **B** ( _ndarray_ ) – 角度的顶点
- **C** ( _ndarray_ ) – 第二条角腿的端点
- \***\*kwargs** – 更多关键字参数被传递给[`Angle`](")

退货

角度（线 1，线 2，半径= 0.5，象限=（-1,1），描边宽度= 8），角度（线 1，线 2，半径= 0.7，象限=（-1，-1），颜色=红色，其他角度=真的），

返回类型

由三点计算出的角度

例子

示例：AngleFromThreePoints 示例

![AngleFromThreePointsExample-1.png](../static/AngleFromThreePointsExample-1.png)


```py

```


获取行数( )[\[来源\]](../_modules/manim/mobject/geometry/line.html#Angle.get_lines)[#](#manim.mobject.geometry.line.Angle.get_lines "此定义的固定链接")

获取形成班级角度的线[`Angle`](#manim.mobject.geometry.line.Angle "manim.mobject.geometry.line.Angle")。

退货

包含[`VGroup`](manim.mobject.types.vectorized_mobject.VGroup.html#manim.mobject.types.vectorized_mobject.VGroup "manim.mobject.types.vectorized_mobject.VGroup")形成类角度的线[`Angle`](#manim.mobject.geometry.line.Angle "manim.mobject.geometry.line.Angle")。

返回类型

[`VGroup`](manim.mobject.types.vectorized_mobject.VGroup.html#manim.mobject.types.vectorized_mobject.VGroup "manim.mobject.types.vectorized_mobject.VGroup")

例子


```py

```


get*value（*度= False\_）[\[来源\]](../_modules/manim/mobject/geometry/line.html#Angle.get_value)[#](#manim.mobject.geometry.line.Angle.get_value "此定义的固定链接")

获取类的角度值[`Angle`](#manim.mobject.geometry.line.Angle "manim.mobject.geometry.line.Angle")。

参数

**Degrees** ( _bool_ ) – 一个布尔值，用于决定返回角度值的单位 (deg/rad)。

退货

类角度的度/弧度值[`Angle`](#manim.mobject.geometry.line.Angle "manim.mobject.geometry.line.Angle")。

返回类型

`float`

例子

示例：获取值示例[¶](#getvalueexample)

![GetValueExample-1.png](../static/GetValueExample-1.png)

```py

```

