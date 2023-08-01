# 正则 Polygram 

合格名称：`manim.mobject.geometry.polygram.RegularPolygram`

_类_ RegularPolygram ( _num_vertices_ , _\*_ ,_密度= 2_ ,_半径= 1_ , _start_angle = None_ , _\*\* kwargs_ )[\[来源\]](../_modules/manim/mobject/geometry/polygram.html#RegularPolygram)[#](#manim.mobject.geometry.polygram.RegularPolygram "此定义的固定链接")

基地：[`Polygram`](manim.mobject.geometry.polygram.Polygram.html#manim.mobject.geometry.polygram.Polygram "manim.mobject.geometry.polygram.Polygram")

A[`Polygram`]()具有规则间隔的顶点。

参数

- **num_vertices** ( _int_ ) – 顶点数。
- **密度**( _int_ ) –

  的密度[`RegularPolygram`]()。

  可以认为是要跳跃多少个顶点才能在它们之间画一条线。每个`density`第 \- 个顶点都是相连的。

- **radius** ( _float_ ) – 顶点所在圆的半径。
- **start_angle** ( _float_ _|_ _None_ ) – 顶点开始的角度；的旋转[`RegularPolygram`]()。
- **kwargs** – 转发到父构造函数。

例子

示例：RegularPolygram 示例

![RegularPolygramExample-1.png](../static/RegularPolygramExample-1.png)


```py

```


方法


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
