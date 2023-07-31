# 切线[#](#tangentline "此标题的固定链接")

合格名称：`manim.mobject.geometry.line.TangentLine`

_类_ TangentLine ( _vmob_ , _alpha_ ,_长度= 1_ , _d_alpha = 1e-06_ , _\*\* kwargs_ )[\[来源\]](../_modules/manim/mobject/geometry/line.html#TangentLine)[#](#manim.mobject.geometry.line.TangentLine "此定义的固定链接")

基地：[`Line`](manim.mobject.geometry.line.Line.html#manim.mobject.geometry.line.Line "manim.mobject.geometry.line.Line")

构造一条[`VMobject`](manim.mobject.types.vectorized_mobject.VMobject.html#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject")在特定点与 a 相切的线。

参数

- **vmob** ( [_VMobject_](manim.mobject.types.vectorized_mobject.VMobject.html#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject") ) – 绘制切线的 VMobject。
- **alpha** ( _float_ ) – 沿着形状构建线的距离。范围：0-1。
- **length** ( _float_ ) – 切线的长度。
- **d_alpha** ( _float_ ) –`dx`值
- **kwargs** – 要传递给的附加参数[`Line`](manim.mobject.geometry.line.Line.html#manim.mobject.geometry.line.Line "manim.mobject.geometry.line.Line")

也可以看看

[`point_from_proportion()`](manim.mobject.types.vectorized_mobject.VMobject.html#manim.mobject.types.vectorized_mobject.VMobject.point_from_proportion "manim.mobject.types.vectorized_mobject.VMobject.point_from_proportion")

例子

示例：TangentLine 示例[¶](#tangentlineexample)

![../_images/TangentLineExample-1.png](../_images/TangentLineExample-1.png)

from manim import \*

class TangentLineExample(Scene):
def construct(self):
circle = Circle(radius=2)
line_1 = TangentLine(circle, alpha=0.0, length=4, color=BLUE_D) \# right
line_2 = TangentLine(circle, alpha=0.4, length=4, color=GREEN) \# top left
self.add(circle, line_1, line_2)

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
