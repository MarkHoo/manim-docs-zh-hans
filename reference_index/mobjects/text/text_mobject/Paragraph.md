# 段落[#](#paragraph "此标题的固定链接")

合格名称：`manim.mobject.text.text\_mobject.Paragraph`

_类_ 段落（_\*文本_， _line_spacing = \- 1_，_对齐=无_， _\*\* kwargs_）[\[来源\]](../_modules/manim/mobject/text/text_mobject.html#Paragraph)[#](#manim.mobject.text.text_mobject.Paragraph "此定义的固定链接")

基地：[`VGroup`](manim.mobject.types.vectorized_mobject.VGroup.html#manim.mobject.types.vectorized_mobject.VGroup "manim.mobject.types.vectorized_mobject.VGroup")

显示一段文本。

对于给定的，属性是 包含所有行的。在这种情况下，每一行都被构造为该行中包含的字符。[`Paragraph`](#manim.mobject.text.text_mobject.Paragraph "manim.mobject.text.text_mobject.Paragraph") ` par``par.chars `[`VGroup`](manim.mobject.types.vectorized_mobject.VGroup.html#manim.mobject.types.vectorized_mobject.VGroup "manim.mobject.types.vectorized_mobject.VGroup")[`VGroup`](manim.mobject.types.vectorized_mobject.VGroup.html#manim.mobject.types.vectorized_mobject.VGroup "manim.mobject.types.vectorized_mobject.VGroup")

参数

- **line_spacing** ( _float_ ) – 表示行之间的间距。默认为-1，表示自动。
- **alignment** (_可选\_\_\[_ _str_ _\]_ ) – 定义段落的对齐方式。默认为无。可能的值为“左”、“右”或“中心”。
- **文本**(_序列\_\_\[_ _str_ _\]_ ) –

例子

正常使用：

paragraph = Paragraph('this is a awesome', 'paragraph',
'With \\nNewlines', '\\tWith Tabs',
' With Spaces', 'With Alignments',
'center', 'left', 'right')

Copy to clipboard

删除不需要的不可见字符：

self.play(Transform(remove_invisible_chars(paragraph.chars\[0:2\]),
remove_invisible_chars(paragraph.chars\[3\]\[0:3\]))

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
