# 虚线

合格名称：`manim.mobject.geometry.line.DashedLine`

_类_ DashedLine（_\* args_， _dash_length = 0.05_， _dashed_ratio = 0.5_， _\*\* kwargs_）[\[来源\]](../_modules/manim/mobject/geometry/line.html#DashedLine)[#](#manim.mobject.geometry.line.DashedLine "此定义的固定链接")

基地：[`Line`](manim.mobject.geometry.line.Line.html#manim.mobject.geometry.line.Line "manim.mobject.geometry.line.Line")

一个虚线[`Line`](manim.mobject.geometry.line.Line.html#manim.mobject.geometry.line.Line "manim.mobject.geometry.line.Line")。

参数

- **args** ( _Any_ ) – 要传递给的参数[`Line`](manim.mobject.geometry.line.Line.html#manim.mobject.geometry.line.Line "manim.mobject.geometry.line.Line")
- **dash_length** ( _float_ ) – 线条中每个单独虚线的长度。
- **dashed_ratio** ( _float_ ) – 虚线空间与空白空间的比率。范围为 0-1。
- **kwargs** – 要传递给的附加参数[`Line`](manim.mobject.geometry.line.Line.html#manim.mobject.geometry.line.Line "manim.mobject.geometry.line.Line")

也可以看看

[`DashedVMobject`](manim.mobject.types.vectorized_mobject.DashedVMobject.html#manim.mobject.types.vectorized_mobject.DashedVMobject "manim.mobject.types.vectorized_mobject.DashedVMobject")

例子

示例：虚线示例[¶](#dashedlineexample)

![../_images/DashedLineExample-1.png](../_images/DashedLineExample-1.png)

from manim import \*

class DashedLineExample(Scene):
def construct(self):
\# dash_length increased
dashed_1 = DashedLine(config.left_side, config.right_side, dash_length=2.0).shift(UP*2)
\# normal
dashed_2 = DashedLine(config.left_side, config.right_side)
\# dashed_ratio decreased
dashed_3 = DashedLine(config.left_side, config.right_side, dashed_ratio=0.1).shift(DOWN*2)
self.add(dashed_1, dashed_2, dashed_3)

Copy to clipboard

方法

[`get_end`](#manim.mobject.geometry.line.DashedLine.get_end "manim.mobject.geometry.line.DashedLine.get_end")

返回线的终点。

[`get_first_handle`](#manim.mobject.geometry.line.DashedLine.get_first_handle "manim.mobject.geometry.line.DashedLine.get_first_handle")

返回第一个句柄的点。

[`get_last_handle`](#manim.mobject.geometry.line.DashedLine.get_last_handle "manim.mobject.geometry.line.DashedLine.get_last_handle")

返回最后一个句柄的点。

[`get_start`](#manim.mobject.geometry.line.DashedLine.get_start "manim.mobject.geometry.line.DashedLine.get_start")

返回线的起点。

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

获取结束( )[\[来源\]](../_modules/manim/mobject/geometry/line.html#DashedLine.get_end)[#](#manim.mobject.geometry.line.DashedLine.get_end "此定义的固定链接")

返回线的终点。

例子

> > \> DashedLine().get_end()
> > array(\[1., 0., 0.\])

Copy to clipboard

返回类型

_ndarray_

获取第一个句柄( )[\[来源\]](../_modules/manim/mobject/geometry/line.html#DashedLine.get_first_handle)[#](#manim.mobject.geometry.line.DashedLine.get_first_handle "此定义的固定链接")

返回第一个句柄的点。

例子

> > \> DashedLine().get_first_handle()
> > array(\[-0.98333333, 0. , 0. \])

Copy to clipboard

返回类型

_ndarray_

获取最后一个句柄（）[\[来源\]](../_modules/manim/mobject/geometry/line.html#DashedLine.get_last_handle)[#](#manim.mobject.geometry.line.DashedLine.get_last_handle "此定义的固定链接")

返回最后一个句柄的点。

例子

> > \> DashedLine().get_last_handle()
> > array(\[0.98333333, 0. , 0. \])

Copy to clipboard

返回类型

_ndarray_

获取开始（）[\[来源\]](../_modules/manim/mobject/geometry/line.html#DashedLine.get_start)[#](#manim.mobject.geometry.line.DashedLine.get_start "此定义的固定链接")

返回线的起点。

例子

> > \> DashedLine().get_start()
> > array(\[-1., 0., 0.\])

Copy to clipboard

返回类型

_ndarray_
