# SingleStringMathTex [#](#singlestringmathtex "此标题的固定链接")

合格名称：`manim.mobject.text.tex\_mobject.SingleStringMathTex`

_类_ SingleStringMathTex ( _tex_string_ , _Stroke_width = 0_ , _Should_center = True_ , _height = None_ , _organize_left_to_right = False_ , _tex_environment = 'align\*'_ , _tex_template = None_ , _font_size = 48_ , _\*\* kwargs_ )[\[来源\]](../_modules/manim/mobject/text/tex_mobject.html#SingleStringMathTex)[#](#manim.mobject.text.tex_mobject.SingleStringMathTex "此定义的固定链接")

基地：[`SVGMobject`](manim.mobject.svg.svg_mobject.SVGMobject.html#manim.mobject.svg.svg_mobject.SVGMobject "manim.mobject.svg.svg_mobject.SVGMobject")

使用 LaTeX 渲染文本的基本构建块。

测试

检查创建[`SingleStringMathTex`](#manim.mobject.text.tex_mobject.SingleStringMathTex "manim.mobject.text.tex_mobject.SingleStringMathTex")对象是否有效：

> > \> SingleStringMathTex('Test')
> > SingleStringMathTex('Test')

Copy to clipboard

方法

`get_tex_string`

[`init_colors`](#manim.mobject.text.tex_mobject.SingleStringMathTex.init_colors "manim.mobject.text.tex_mobject.SingleStringMathTex.init_colors")

初始化颜色。

属性

`animate`

用于对 的任何方法的应用程序进行动画处理`self`。

`animation_overrides`

`color`

`depth`

对象的深度。

`fill_color`

如果有多种颜色（对于渐变），则返回第一个颜色

[`font_size`](#manim.mobject.text.tex_mobject.SingleStringMathTex.font_size "manim.mobject.text.tex_mobject.SingleStringMathTex.font_size")

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

- **tex_string** ( _str_ ) –
- **笔画宽度**（_浮动_）-
- **should_center** (_布尔_) –
- **高度**（_浮动**|**无_）-
- **组织从左到右**( _bool_ ) –
- **tex_environment** ( _str_ ) –
- **tex_template** ( [_TexTemplate_](manim.utils.tex.TexTemplate.html#manim.utils.tex.TexTemplate "manim.utils.tex.TexTemplate") _|\_\_无_) –
- **字体大小**（_浮动_）–

_属性_ 字体大小[#](#manim.mobject.text.tex_mobject.SingleStringMathTex.font_size "此定义的固定链接")

tex mobject 的字体大小。

init*colors ( \_propagate_colors = True* )[\[来源\]](../_modules/manim/mobject/text/tex_mobject.html#SingleStringMathTex.init_colors)[#](#manim.mobject.text.tex_mobject.SingleStringMathTex.init_colors "此定义的固定链接")

初始化颜色。

被创造召唤。这是一个空方法，可以由子类实现。
