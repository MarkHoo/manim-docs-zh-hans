# 环面

合格名称：`manim.mobject.three\_d.three\_dimensions.Torus`


```py
class Torus(major_radius=3, minor_radius=1, u_range=(0, 6.283185307179586), v_range=(0, 6.283185307179586), resolution=None, **kwargs)
```

Bases: `Surface`

一个环面。

参数

- **Major_radius** ( _float_ ) – 从管中心到圆环中心的距离。
- **secondary_radius** ( _float_ ) – 管的半径。
- **u_range** ( _Sequence_ _\[_ _float_ _\]_ ) – 变量的范围`u`：。`(u_min, u_max)`
- **v_range** ( _Sequence_ _\[_ _float_ _\]_ ) – 变量的范围`v`：。`(v_min, v_max)`
- **resolution**( _Sequence_ _\[_ _int_ _\]_ ) – 所采集的样本数[`Torus`]()。元组可用于分别定义`u`和的不同分辨率`v`。


例子

示例：ExampleTorus

![ExampleTorus-1.png](../_images/ExampleTorus-1.png)


```py
from manim import *

class ExampleTorus(ThreeDScene):
    def construct(self):
        axes = ThreeDAxes()
        torus = Torus()
        self.set_camera_orientation(phi=75 * DEGREES, theta=30 * DEGREES)
        self.add(axes, torus)
```


方法

|||
|-|-|
[`func`]()|定义所绘制的 z 值[`Torus`]()。


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



`func(u, v)`

定义所绘制的 z 值[`Torus`]()。

返回

定义 的 z 值[`Torus`]()。

返回类型

`numpy.ndarray`

参数

- **u**（_float_）–
- **v**（_float_）–
