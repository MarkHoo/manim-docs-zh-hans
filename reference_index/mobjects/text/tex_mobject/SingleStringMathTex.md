# SingleStringMathTex 

合格名称：`manim.mobject.text.tex\_mobject.SingleStringMathTex`


```py
class SingleStringMathTex(tex_string, stroke_width=0, should_center=True, height=None, organize_left_to_right=False, tex_environment='align*', tex_template=None, font_size=48, **kwargs)
```

Bases: `SVGMobject`

使用 LaTeX 渲染文本的基本构建块。

测试

检查创建[`SingleStringMathTex`]()对象是否有效：

```py
>>> SingleStringMathTex('Test') 
SingleStringMathTex('Test')
```


方法

|||
|-|-|
`get_tex_string`|
[`init_colors`]()|初始化颜色。


属性

|||
|-|-|
`animate`|用于对 的任何方法的应用程序进行动画处理`self`。
`animation_overrides`|
`color`|
`depth`|对象的深度。
`fill_color`|如果有多种颜色（对于渐变），则返回第一个颜色
[`font_size`]()|tex mobject 的字体大小。
`hash_seed`|表示生成的对象点结果的唯一哈希值。
`height`|mobject 的高度。
`n_points_per_curve`|
`sheen_factor`|
`stroke_color`|
`width`|mobject 的宽度。


参数

- **tex_string** ( _str_ ) –
- **stroke_width**（_float_）-
- **should_center** (_bool_) –
- **height**（_float**|**None_）-
- **organize_left_to_right**( _bool_ ) –
- **tex_environment** ( _str_ ) –
- **tex_template** ( [_TexTemplate_]() _|\_\_None_) –
- **font_size**（_float_）–


_属性_ font_size 

tex mobject 的字体大小。


`init_colors(propagate_colors=True)`

初始化颜色。

被创造召唤。这是一个空方法，可以由子类实现。
