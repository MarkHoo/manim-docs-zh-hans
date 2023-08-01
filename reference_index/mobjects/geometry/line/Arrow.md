# 箭头

合格名称：`manim.mobject.geometry.line.Arrow`

_类_ 箭头（_\* args_，_笔画宽度= 6_，_缓冲= 0.25_，_最大笔尖长度到长度比= 0.25_，_最大笔划宽度到长度比= 5_， _\*\* kwargs_）[\[来源\]](../_modules/manim/mobject/geometry/line.html#Arrow)[#](#manim.mobject.geometry.line.Arrow "此定义的固定链接")

基地：[`Line`](manim.mobject.geometry.line.Line.html#manim.mobject.geometry.line.Line "manim.mobject.geometry.line.Line")

一个箭头。

参数

- **args** ( _Any_ ) – 要传递给 的参数[`Line`](manim.mobject.geometry.line.Line.html#manim.mobject.geometry.line.Line "manim.mobject.geometry.line.Line")。
- **stroke_width** ( _float_ ) – 箭头的粗细。受 影响`max_stroke_width_to_length_ratio`。
- **buff** ( _float_ ) – 箭头距起点和终点的距离。
- **max_tip_length_to_length_ratio** ( _float_ ) –`tip_length`随着箭头的长度缩放。增加该比率会提高 的最大值`tip_length`。
- **max_lines_width_to_length_ratio** ( _float_ ) –`stroke_width`随着箭头的长度缩放。增加该比率会与 的最大值成比例`stroke_width`。
- **kwargs** – 要传递给 的附加参数[`Line`](manim.mobject.geometry.line.Line.html#manim.mobject.geometry.line.Line "manim.mobject.geometry.line.Line")。

也可以看看

`ArrowTip` `CurvedArrow`

例子

示例：箭头示例[¶](#arrowexample)

![../_images/ArrowExample-1.png](../_images/ArrowExample-1.png)


```py

```


示例：箭头示例[¶](#arrowexample)

![../_images/ArrowExample-2.png](../_images/ArrowExample-2.png)


```py

```


方法

[`get_default_tip_length`](#manim.mobject.geometry.line.Arrow.get_default_tip_length "manim.mobject.geometry.line.Arrow.get_default_tip_length")

返回箭头的默认 tip_length。

[`get_normal_vector`](#manim.mobject.geometry.line.Arrow.get_normal_vector "manim.mobject.geometry.line.Arrow.get_normal_vector")

返回向量的法线。

[`reset_normal_vector`](#manim.mobject.geometry.line.Arrow.reset_normal_vector "manim.mobject.geometry.line.Arrow.reset_normal_vector")

重置向量的法线

[`scale`](#manim.mobject.geometry.line.Arrow.scale "manim.mobject.geometry.line.Arrow.scale")

缩放箭头，但保持笔划宽度和箭头尖端大小固定。

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

获取默认提示长度( )[\[来源\]](../_modules/manim/mobject/geometry/line.html#Arrow.get_default_tip_length)[#](#manim.mobject.geometry.line.Arrow.get_default_tip_length "此定义的固定链接")

返回箭头的默认 tip_length。

例子


```py

```


返回类型

漂浮

获取法线向量( )[\[来源\]](../_modules/manim/mobject/geometry/line.html#Arrow.get_normal_vector)[#](#manim.mobject.geometry.line.Arrow.get_normal_vector "此定义的固定链接")

返回向量的法线。

例子

```py

```


返回类型

_ndarray_

重置正常向量( )[\[来源\]](../_modules/manim/mobject/geometry/line.html#Arrow.reset_normal_vector)[#](#manim.mobject.geometry.line.Arrow.reset_normal_vector "此定义的固定链接")

重置向量的法线

比例（_因子_， _scale_tips = False_， _\*\* kwargs_）[\[来源\]](../_modules/manim/mobject/geometry/line.html#Arrow.scale)[#](#manim.mobject.geometry.line.Arrow.scale "此定义的固定链接")

缩放箭头，但保持笔划宽度和箭头尖端大小固定。

也可以看看

[`scale()`](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject.scale "manim.mobject.mobject.Mobject.scale")

例子


```py

```


使用默认方法手动缩放对象 [`scale()`](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject.scale "manim.mobject.mobject.Mobject.scale")不具有相同的属性：


```py

```

