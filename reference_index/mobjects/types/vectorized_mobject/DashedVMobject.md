# 虚线VMobject

合格名称：`manim.mobject.types.vectorized\_mobject.DashedVMobject`


```py

```

[`VMobject`](manim.mobject.types.vectorized_mobject.VMobject.html#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject")由破折号而不是直线组成。

参数

- **vmobject** – 将被虚线化的对象
- **num_dashes** – 要添加的破折号数量。
- **dashed_ratio** – 虚线与空白区域的比率。
- **dash_offset** – 沿路径移动虚线的起点。值 1 移动一个完整的破折号长度。
- **equal_lengths** – 如果`True`，破折号将（大约）等长。如果`False`，则破折号将在曲线的输入 t 变量中均匀分割（传统行为）。

例子

示例：DashedVMobjectExample [¶](#dashedvmobjectexample)

![../_images/DashedVMobjectExample-1.png](../_images/DashedVMobjectExample-1.png)

```py

```


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
