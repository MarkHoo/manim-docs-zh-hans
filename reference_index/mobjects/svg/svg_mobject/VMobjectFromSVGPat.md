# VMobjectFromSVGPath 

合格名称：`manim.mobject.svg.svg\_mobject.VMobjectFromSVGPath`

_类_ VMobjectFromSVGPath（_path_obj_， _long_lines = False_， _should_subdivide_sharp_curves = False_， _should_remove_null_curves = False_， _\*\* kwargs_）[\[来源\]](../_modules/manim/mobject/svg/svg_mobject.html#VMobjectFromSVGPath)[#](#manim.mobject.svg.svg_mobject.VMobjectFromSVGPath "此定义的固定链接")

基地：[`VMobject`](manim.mobject.types.vectorized_mobject.VMobject.html#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject")

表示 SVG 路径的矢量化 mobject。

笔记

、和关键字参数仅适用于 OpenGL 渲染器`long_lines`。` should_subdivide_sharp_curves``should_remove_null_curves `

参数

- **path_obj** ( _se.Path_ ) – 已解析的 SVG 路径对象。
- **long_lines** ( _bool_ ) – 矢量化对象中的直线是否以一段或两段绘制。
- **should_subdivide_sharp_curves** ( _bool_ ) – 如果两条线段以比给定阈值更尖锐的角度相交，是否进一步细分子曲线。
- **should_remove_null_curves** ( _bool_ ) – 是否删除长度为 0 的子曲线。
- **kwargs** – 更多关键字参数传递给父类。

方法

[`generate_points`](#manim.mobject.svg.svg_mobject.VMobjectFromSVGPath.generate_points "manim.mobject.svg.svg_mobject.VMobjectFromSVGPath.generate_points")

初始化`points`并因此初始化形状。

`handle_commands`

`init_points`

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

生成点（）[#](#manim.mobject.svg.svg_mobject.VMobjectFromSVGPath.generate_points "此定义的固定链接")

初始化`points`并因此初始化形状。

被创造召唤。这是一个空方法，可以由子类实现。

返回类型

没有任何
