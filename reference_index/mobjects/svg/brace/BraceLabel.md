# 大括号

合格名称：`manim.mobject.svg.brace.BraceLabel`


```py
class BraceLabel(obj, text, brace_direction=array([ 0., -1., 0.]), label_constructor=<class 'manim.mobject.text.tex_mobject.MathTex'>, font_size=48, buff=0.2, brace_config=None, **kwargs)
```

Bases: `VMobject`

创建一个带有标签的支架。

参数

- **obj** ( [_Mobject_]() ) – 与大括号相邻的 mobject。
- **text** ( _str_ ) – 标签文本。
- **brace_direction** ( _np.ndarray_ ) – 大括号的方向。默认情况下`DOWN`。
- **label_constructor** ( _type_ ) – 用于构造表示标签的 mobject 的类或函数。默认情况下[`MathTex`]()。
- **font_size** ( _float_ ) – 标签的字体大小，传递给`label_constructor`.
- **buff** ( _float_ ) – mobject 和大括号之间的缓冲区。
- **brace_config** ( _dict_ _|_ _None_ ) – 要传递给的参数[`Brace`]()。
- **kwargs** – 要传递给 的附加参数[`VMobject`]()。

方法

`change_brace_label`
`change_label`
`creation_anim`
`shift_brace`

属性

|||
|-|-|
`animate`|用于对 的任何方法的应用程序进行动画处理`self`。
`animation_overrides`|
`color`|
`depth`|对象的深度。
`fill_color`|如果有多种颜色（对于渐变），则返回第一个颜色
`height`|mobject 的高度。
`n_points_per_curve`|
`sheen_factor`|
`stroke_color`|
`width`|mobject 的宽度。
