# 点 3D 

合格名称：`manim.mobject.three\_d.three\_dimensions.Dot3D`


```py
class Dot3D(point=array([0., 0., 0.]), radius=0.08, color='#FFFFFF', resolution=(8, 8), **kwargs)
```

Bases: `Sphere`

一个球形点。

参数

- **point** ( _list_ _|_ _np.ndarray_ ) – 点的位置。
- **radius** ( _float_ ) – 点的半径。
- **颜色**( _Color_ ) – 的颜色[`Dot3D`]()。
- **分辨率**( _Sequence_ _\[_ _int_ _\]_ ) – 所采集的样本数[`Dot3D`]()。元组可用于分别定义`u`和的不同分辨率`v`。

例子

示例：Dot3D 示例

![Dot3DExample-1.png](../../static/Dot3DExample-1.png)


```py
from manim import *

class Dot3DExample(ThreeDScene):
    def construct(self):
        self.set_camera_orientation(phi=75*DEGREES, theta=-45*DEGREES)

        axes = ThreeDAxes()
        dot_1 = Dot3D(point=axes.coords_to_point(0, 0, 1), color=RED)
        dot_2 = Dot3D(point=axes.coords_to_point(2, 0, 0), radius=0.1, color=BLUE)
        dot_3 = Dot3D(point=[0, 0, 0], radius=0.1, color=ORANGE)
        self.add(axes, dot_1, dot_2,dot_3)
```


方法



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
