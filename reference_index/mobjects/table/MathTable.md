# 数学表

合格名称：`manim.mobject.table.MathTable`

_类_ MathTable (_表_, _element_to_mobject=<class 'manim.mobject.text.tex_mobject.MathTex'>_ , _\*\*kwargs_ )[\[来源\]](../_modules/manim/mobject/table.html#MathTable)[#](#manim.mobject.table.MathTable "此定义的固定链接")

基地：[`Table`](manim.mobject.table.Table.html#manim.mobject.table.Table "manim.mobject.table.Table")

[`Table`](manim.mobject.table.Table.html#manim.mobject.table.Table "manim.mobject.table.Table")与 LaTeX 一起使用的专用对象。

例子

示例：MathTable 示例

![MathTableExample-1.png](../_images/MathTableExample-1.png)

```py

```


element_to_mobject 设置[`Table`](manim.mobject.table.Table.html#manim.mobject.table.Table "manim.mobject.table.Table")为的特殊情况。表中的每个条目都是在 Latex 对齐环境中设置的。[`MathTex`](manim.mobject.text.tex_mobject.MathTex.html#manim.mobject.text.tex_mobject.MathTex "manim.mobject.text.tex_mobject.MathTex")

参数

- **table** ( _Iterable_ _\[_ _Iterable_ _\[_ _float_ _|_ _str_ _\]_ _\]_ ) – 二维数组或列表列表。表的内容必须是 的有效输入[`MathTex`](manim.mobject.text.tex_mobject.MathTex.html#manim.mobject.text.tex_mobject.MathTex "manim.mobject.text.tex_mobject.MathTex")。
- **element_to_mobject** ( _Callable_ _\[_ _\[_ _float_ _|_ _str_ _\]_ _,_ [_VMobject_](manim.mobject.types.vectorized_mobject.VMobject.html#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject") _\]_ ) –[`Mobject`](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject")应用于表条目的类。设置为[`MathTex`](manim.mobject.text.tex_mobject.MathTex.html#manim.mobject.text.tex_mobject.MathTex "manim.mobject.text.tex_mobject.MathTex").
- **kwargs** – 要传递给 的附加参数[`Table`](manim.mobject.table.Table.html#manim.mobject.table.Table "manim.mobject.table.Table")。

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
