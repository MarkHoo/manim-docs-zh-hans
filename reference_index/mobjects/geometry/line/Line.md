# 行[#](#line "此标题的固定链接")

合格名称：`manim.mobject.geometry.line.Line`

_类_ Line ( _start = array(\[- 1., 0., 0.\])_ , _end = array(\[1., 0., 0.\])_ , _buff = 0_ , _path_arc = None_ , _\*\* kwargs_ )[\[来源\]](../_modules/manim/mobject/geometry/line.html#Line)[#](#manim.mobject.geometry.line.Line "此定义的固定链接")

基地：[`TipableVMobject`](manim.mobject.geometry.arc.TipableVMobject.html#manim.mobject.geometry.arc.TipableVMobject "manim.mobject.geometry.arc.TipableVMobject")

方法

[`generate_points`](#manim.mobject.geometry.line.Line.generate_points "manim.mobject.geometry.line.Line.generate_points")

初始化`points`并因此初始化形状。

`get_angle`

[`get_projection`](#manim.mobject.geometry.line.Line.get_projection "manim.mobject.geometry.line.Line.get_projection")

返回点到直线上的投影。

`get_slope`

`get_unit_vector`

`get_vector`

[`init_points`](#manim.mobject.geometry.line.Line.init_points "manim.mobject.geometry.line.Line.init_points")

初始化`points`并因此初始化形状。

[`put_start_and_end_on`](#manim.mobject.geometry.line.Line.put_start_and_end_on "manim.mobject.geometry.line.Line.put_start_and_end_on")

设置直线的起点和终点坐标。

`set_angle`

`set_length`

`set_path_arc`

`set_points_by_ends`

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

生成点( )[\[来源\]](../_modules/manim/mobject/geometry/line.html#Line.generate_points)[#](#manim.mobject.geometry.line.Line.generate_points "此定义的固定链接")

初始化`points`并因此初始化形状。

被创造召唤。这是一个空方法，可以由子类实现。

获取投影（_点_）[\[来源\]](../_modules/manim/mobject/geometry/line.html#Line.get_projection)[#](#manim.mobject.geometry.line.Line.get_projection "此定义的固定链接")

返回点到直线上的投影。

参数

**point** ( _Sequence_ _\[_ _float_ _\]_ ) – 线投影到的点。

返回类型

_序列_\[浮动\]

初始化点（）[#](#manim.mobject.geometry.line.Line.init_points "此定义的固定链接")

初始化`points`并因此初始化形状。

被创造召唤。这是一个空方法，可以由子类实现。

put*start_and_end_on（*开始*，*结束\_）[\[来源\]](../_modules/manim/mobject/geometry/line.html#Line.put_start_and_end_on)[#](#manim.mobject.geometry.line.Line.put_start_and_end_on "此定义的固定链接")

设置直线的起点和终点坐标。

例子

示例：线示例[¶](#lineexample)

from manim import \*

class LineExample(Scene):
def construct(self):
d = VGroup()
for i in range(0,10):
d.add(Dot())
d.arrange_in_grid(buff=1)
self.add(d)
l= Line(d\[0\], d\[1\])
self.add(l)
self.wait()
l.put_start_and_end_on(d\[1\].get_center(), d\[2\].get_center())
self.wait()
l.put_start_and_end_on(d\[4\].get_center(), d\[7\].get_center())
self.wait()

Copy to clipboard

参数

- **开始**（_序列**\[**浮动\_\_\]_）–
- **结束**（_序列**\[**浮动\_\_\]_）–
