# 立方体

合格名称：`manim.mobject.three\_d.three\_dimensions.Cube`


```py
class Cube(side_length=2, fill_opacity=0.75, fill_color='#58C4DD', stroke_width=0, **kwargs)
```

Bases: `VGroup`

三维立方体。

参数

- **side_length** ( _float_ ) – 各边的长度[`Cube`]()。
- **fill_opacity** ( _float_ ) – 的不透明度[`Cube`]()，从 0 表示完全透明到 1 表示完全不透明。默认为 0.75。
- **fill_color** ( _Color_ ) – 的颜色[`Cube`]()。
- **stroke_width** ( _float_ ) – 围绕每个面的描边宽度[`Cube`]()。


例子

示例：Cube 示例

![CubeExample-1.png](../_images/CubeExample-1.png)

```py
from manim import *

class CubeExample(ThreeDScene):
    def construct(self):
        self.set_camera_orientation(phi=75*DEGREES, theta=-45*DEGREES)

        axes = ThreeDAxes()
        cube = Cube(side_length=3, fill_opacity=0.7, fill_color=BLUE)
        self.add(cube)
```


方法

|||
|-|-|
[`generate_points`]()|创建 的侧面[`Cube`]()。
[`init_points`]()|创建 的侧面[`Cube`]()。


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



`generate_points()`

创建 的侧面[`Cube`]()。

返回类型

None


`init_points()`

创建 的侧面[`Cube`]()。

返回类型

None
