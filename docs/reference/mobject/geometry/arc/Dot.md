# 点

合格名称：`manim.mobject.geometry.arc.Dot`

```py
class Dot(point=array([0., 0., 0.]), radius=0.08, stroke_width=0, fill_opacity=1.0, color='#FFFFFF', **kwargs)
```

Bases: `Circle`

一个半径很小的圆。

参数

- **point** ( _list_ _|_ _np.ndarray_ ) – 点的位置。
- **radius** ( _float_ ) – 点的半径。
- **stroke_width** ( _float_ ) – 点轮廓的粗细。
- **fill_opacity** ( _float_ ) – 点的 fill_colour 的不透明度
- **color** ( _Color_ _|_ _str_ ) – 点的颜色。
- **kwargs** – 要传递给的附加参数[`Circle`]()

例子

示例：点示例

![DotExample-1.png](../../static/DotExample-1.png)

```py
from manim import *

class DotExample(Scene):
    def construct(self):
        dot1 = Dot(point=LEFT, radius=0.08)
        dot2 = Dot(point=ORIGIN)
        dot3 = Dot(point=RIGHT)
        self.add(dot1,dot2,dot3)
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
