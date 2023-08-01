# 矢量

合格名称：`manim.mobject.geometry.line.Vector`

_类_ Vector (_方向= array(\[1., 0., 0.\])_ , _buff = 0_ , _\*\* kwargs_ )[\[来源\]](../_modules/manim/mobject/geometry/line.html#Vector)[#](#manim.mobject.geometry.line.Vector "此定义的固定链接")

基地：[`Arrow`](manim.mobject.geometry.line.Arrow.html#manim.mobject.geometry.line.Arrow "manim.mobject.geometry.line.Arrow")

专门用于图形的向量。

参数

- **Direction** ( _list_ _|_ _np.ndarray_ ) – 箭头的方向。
- **buff** ( _float_ ) – 向量与其端点的距离。
- **kwargs** – 要传递给的附加参数[`Arrow`]()

例子

示例：矢量示例

![VectorExample-1.png](../static/VectorExample-1.png)


```py

```


方法

[`coordinate_label`]()

根据向量的坐标创建标签。


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


坐标标签（_整数标签=真_， _n_dim = 2_，_颜色=无_， _\*\* kwargs_）

根据向量的坐标创建标签。

参数

- **integer_labels** ( _bool_ ) – 是否将坐标舍入为整数。
- **n_dim** ( _int_ ) – 向量的维数。
- **color** ( _Color_ _|_ _None_ ) – 设置标签的颜色，可选。
- **kwargs** – 要传递给 的附加参数[`Matrix`]()。

退货

标签。

返回类型

[`Matrix`]()

例子

示例：矢量坐标标签

![VectorCooperativeLabel-1.png](../static/VectorCoordinateLabel-1.png)


```py

```

