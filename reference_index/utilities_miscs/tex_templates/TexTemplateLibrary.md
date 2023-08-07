# TexTemplateLibrary

合格名称：`manim.utils.tex\_templates.TexTemplateLibrary`


```py
class TexTemplateLibrary
```

Bases: `object`

基本 TeX 模板对象的集合


例子

正常用作 Tex() 和 MathTex() mobject 的关键字参数 tex_template 的值：

```py
``Tex("My TeX code", tex_template=TexTemplateLibrary.ctex)``
```


方法



属性

|||
|-|-|
[`ctex`]()|使用 use_ctex 标志时 3b1b 使用的 TeX 模板的实例
[`default`]()|manim 中默认 TeX 模板的实例
[`simple`]()|仅加载基本 AMS 包的简单 TeX 模板实例
[`threeb1b`]()|3b1b 使用的默认 TeX 模板的实例



`ctex = <manim.utils.tex.TexTemplate object>`

使用 use_ctex 标志时 3b1b 使用的 TeX 模板的实例



`default = <manim.utils.tex.TexTemplate object>`

manim 中默认 TeX 模板的实例



`simple = <manim.utils.tex.TexTemplate object>`

仅加载基本 AMS 包的简单 TeX 模板实例



`threeb1b = <manim.utils.tex.TexTemplate object>`

3b1b 使用的默认 TeX 模板的实例
