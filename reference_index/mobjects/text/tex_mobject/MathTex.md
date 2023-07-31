# 数学文本[#](#mathtex "此标题的固定链接")

合格名称：`manim.mobject.text.tex\_mobject.MathTex`

_类_ MathTex ( _\* tex_strings_ , _arg_separator = ' '_ , _substrings_to_isolate = None_ , _tex_to_color_map = None_ , _tex_environment = 'align\*'_ , _\*\* kwargs_ )[\[来源\]](../_modules/manim/mobject/text/tex_mobject.html#MathTex)[#](#manim.mobject.text.tex_mobject.MathTex "此定义的固定链接")

基地：[`SingleStringMathTex`](manim.mobject.text.tex_mobject.SingleStringMathTex.html#manim.mobject.text.tex_mobject.SingleStringMathTex "manim.mobject.text.tex_mobject.SingleStringMathTex")

在数学模式下用 LaTeX 编译的字符串。

例子

示例：公式[¶](#formula)

![../_images/Formula-1.png](../_images/Formula-1.png)

from manim import \*

class Formula(Scene):
def construct(self):
t = MathTex(r"\\int_a^b f'(x) dx = f(b)- f(a)")
self.add(t)

Copy to clipboard

测试

检查是否创建[`MathTex`](#manim.mobject.text.tex_mobject.MathTex "manim.mobject.text.tex_mobject.MathTex")作品：

> > \> MathTex('a^2 + b^2 = c^2')
> > MathTex('a^2 + b^2 = c^2')

Copy to clipboard

检查双括号组分割是否正确：

> > \> t1 = MathTex('{{ a }} + {{ b }} = {{ c }}')
> > \> len(t1.submobjects)
> > 5
> > \> t2 = MathTex(r"\\frac{1}{a+b\\sqrt{2}}")
> > \> len(t2.submobjects)
> > 1

Copy to clipboard

方法

`get_part_by_tex`

`get_parts_by_tex`

`index_of_part`

`index_of_part_by_tex`

`set_color_by_tex`

`set_color_by_tex_to_color_map`

[`set_opacity_by_tex`](#manim.mobject.text.tex_mobject.MathTex.set_opacity_by_tex "manim.mobject.text.tex_mobject.MathTex.set_opacity_by_tex")

设置指定 tex 的不透明度。

`sort_alphabetically`

属性

`animate`

用于对 的任何方法的应用程序进行动画处理`self`。

`animation_overrides`

`color`

`depth`

对象的深度。

`fill_color`

如果有多种颜色（对于渐变），则返回第一个颜色

`font_size`

tex mobject 的字体大小。

`hash_seed`

表示生成的对象点结果的唯一哈希值。

`height`

mobject 的高度。

`n_points_per_curve`

`sheen_factor`

`stroke_color`

`width`

mobject 的宽度。

参数

- **arg_separator** ( _str_ ) –
- **substrings_to_isolate** ( _Iterable_ _\[_ _str_ _\]_ _|_ _None_ ) –
- **tex_to_color_map** (_字典\_\_\[_ _str_ _,_ _Color_ _\]_ ) –
- **tex_environment** ( _str_ ) –

set*opacity_by*tex ( \_tex* ,*不透明度= 0.5* ,*剩余不透明度=无*, *\*\* kwargs\_ )[\[来源\]](../_modules/manim/mobject/text/tex_mobject.html#MathTex.set_opacity_by_tex)[#](#manim.mobject.text.tex_mobject.MathTex.set_opacity_by_tex "此定义的固定链接")

设置指定 tex 的不透明度。如果指定了“remaining_opacity”，则剩余的 tex 将设置为该不透明度。

参数

- **tex** ( _str_ ) – 要设置不透明度的 tex。
- **不透明度**( _float_ ) – 默认 0.5。设置 tex 的不透明度
- **剩余不透明度**（_可选\_\_\[_ _float_ _\]_）-默认无。设置剩余纹理的不透明度。如果 None，那么剩余的 tex 不会被改变
