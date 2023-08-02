# 十字

合格名称：`manim.mobject.geometry.shape\_matchers.Cross`

```py
class Cross(mobject=None, stroke_color='#FC6255', stroke_width=6, scale_factor=1, **kwargs)
```

Bases: `VGroup`

创建一个十字架。

参数

- **mobject** ( [_Mobject_]() _|_ _None_ ) – 链接到此实例的 mobject。当指定时它适合 mobject。默认为无。
- **stroke_color** ( _Color_ ) – 指定十字线的颜色。默认为红色。
- **stroke_width** ( _float_ ) – 指定交叉线的宽度。默认为 6。
- **scale_factor** ( _float_ ) – 将交叉缩放到提供的单位。默认为 1。

例子

示例：ExampleCross

![ExampleCross-1.png](../static/ExampleCross-1.png)

```py
from manim import *

class ExampleCross(Scene):
    def construct(self):
        cross = Cross()
        self.add(cross)
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
