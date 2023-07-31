# 弯头[#](#elbow "此标题的固定链接")

合格名称：`manim.mobject.geometry.line.Elbow`

弯头*类*（_宽度= 0.2_，_角度= 0_， _\*\* kwargs_）[\[来源\]](../_modules/manim/mobject/geometry/line.html#Elbow)[#](#manim.mobject.geometry.line.Elbow "此定义的固定链接")

基地：[`VMobject`](manim.mobject.types.vectorized_mobject.VMobject.html#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject")

两条线相互成直角：L 形。

参数

- **width** ( _float_ ) – 肘部两侧的长度。
- **angle** ( _float_ ) – 肘部的旋转。
- **kwargs** – 要传递给的附加参数[`VMobject`](manim.mobject.types.vectorized_mobject.VMobject.html#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject")
- **另请参阅::** ( _.._ ) –[`RightAngle`](manim.mobject.geometry.line.RightAngle.html#manim.mobject.geometry.line.RightAngle "manim.mobject.geometry.line.RightAngle")

例子

示例：Elbow 示例[¶](#elbowexample)

![../_images/ElbowExample-1.png](../_images/ElbowExample-1.png)

from manim import \*

class ElbowExample(Scene):
def construct(self):
elbow_1 = Elbow()
elbow_2 = Elbow(width=2.0)
elbow_3 = Elbow(width=2.0, angle=5\*PI/4)

        elbow_group = Group(elbow_1, elbow_2, elbow_3).arrange(buff=1)
        self.add(elbow_group)

Copy to clipboard

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
