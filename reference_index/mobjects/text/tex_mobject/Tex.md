# Tex

合格名称：`manim.mobject.text.tex\_mobject.Tex`


```py
class Tex(*tex_strings, arg_separator='', tex_environment='center', **kwargs)
```

Bases: `MathTex`

在正常模式下用 LaTeX 编译的字符串。

测试

检查写入 LaTeX 字符串是否有效：

```py
>>> Tex('The horse does not eat cucumber salad.') 
Tex('The horse does not eat cucumber salad.')
```


方法



属性

|||
|-|-|
`animate`|用于对 的任何方法的应用程序进行动画处理`self`。
`animation_overrides`|
`color`|
`depth`|对象的深度。
`fill_color`|如果有多种颜色（对于渐变），则返回第一个颜色
`font_size`|tex mobject 的字体大小。
`hash_seed`|表示生成的对象点结果的唯一哈希值。
`height`|mobject 的高度。
`n_points_per_curve`|
`sheen_factor`|
`stroke_color`|
`width`|mobject 的宽度。


`_original__init__(*tex_strings, arg_separator='', tex_environment='center', **kwargs)`

初始化自身。请参阅 help(type(self)) 以获取准确的签名。
