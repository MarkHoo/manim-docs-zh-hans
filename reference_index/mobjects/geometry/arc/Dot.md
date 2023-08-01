# 点

合格名称：`manim.mobject.geometry.arc.Dot`

点*类*（_点= array(\[0., 0., 0.\])_，_半径= 0.08_，_描边宽度= 0_，_填充不透明度= 1.0_，_颜色= '#FFFFFF'_， _\*\* kwargs_）[\[来源\]](../_modules/manim/mobject/geometry/arc.html#Dot)[#](#manim.mobject.geometry.arc.Dot "此定义的固定链接")

基地：[`Circle`](manim.mobject.geometry.arc.Circle.html#manim.mobject.geometry.arc.Circle "manim.mobject.geometry.arc.Circle")

一个半径很小的圆。

参数

- **point** ( _list_ _|_ _np.ndarray_ ) – 点的位置。
- **radius** ( _float_ ) – 点的半径。
- **stroke_width** ( _float_ ) – 点轮廓的粗细。
- **fill_opacity** ( _float_ ) – 点的 fill_colour 的不透明度
- **color** ( _Color_ _|_ _str_ ) – 点的颜色。
- **kwargs** – 要传递给的附加参数[`Circle`](manim.mobject.geometry.arc.Circle.html#manim.mobject.geometry.arc.Circle "manim.mobject.geometry.arc.Circle")

例子

示例：点示例[¶](#dotexample)

![../_images/DotExample-1.png](../_images/DotExample-1.png)

from manim import \*

class DotExample(Scene):
def construct(self):
dot1 = Dot(point=LEFT, radius=0.08)
dot2 = Dot(point=ORIGIN)
dot3 = Dot(point=RIGHT)
self.add(dot1,dot2,dot3)

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
