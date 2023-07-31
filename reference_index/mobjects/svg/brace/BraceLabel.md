# 大括号[#](#bracelabel "此标题的固定链接")

合格名称：`manim.mobject.svg.brace.BraceLabel`

_类_ BraceLabel ( _obj_ ,_文本_,_大括号\_direction=array(\[ 0._ , _-1._ , _0.\])_ , _label_constructor=<class 'manim.mobject.text.tex_mobject.MathTex'>_ , _font_size=48_ , _buff=0.2_ ,_大括号\_config =无_， _\*\*kwargs_）[\[来源\]](../_modules/manim/mobject/svg/brace.html#BraceLabel)[#](#manim.mobject.svg.brace.BraceLabel "此定义的固定链接")

基地：[`VMobject`](manim.mobject.types.vectorized_mobject.VMobject.html#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject")

创建一个带有标签的支架。

参数

- **obj** ( [_Mobject_](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject") ) – 与大括号相邻的 mobject。
- **text** ( _str_ ) – 标签文本。
- **brace_direction** ( _np.ndarray_ ) – 大括号的方向。默认情况下`DOWN`。
- **label_constructor** ( _type_ ) – 用于构造表示标签的 mobject 的类或函数。默认情况下[`MathTex`](manim.mobject.text.tex_mobject.MathTex.html#manim.mobject.text.tex_mobject.MathTex "manim.mobject.text.tex_mobject.MathTex")。
- **font_size** ( _float_ ) – 标签的字体大小，传递给`label_constructor`.
- **buff** ( _float_ ) – mobject 和大括号之间的缓冲区。
- **brace_config** ( _dict_ _|_ _None_ ) – 要传递给的参数[`Brace`](manim.mobject.svg.brace.Brace.html#manim.mobject.svg.brace.Brace "manim.mobject.svg.brace.Brace")。
- **kwargs** – 要传递给 的附加参数[`VMobject`](manim.mobject.types.vectorized_mobject.VMobject.html#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject")。

方法

`change_brace_label`

`change_label`

`creation_anim`

`shift_brace`

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