# 文本对象

用于显示（非 LaTeX）文本的 Mobjects。

笔记

正如您可以使用[`Tex`](manim.mobject.text.tex_mobject.Tex.html#manim.mobject.text.tex_mobject.Tex "manim.mobject.text.tex_mobject.Tex")and [`MathTex`](manim.mobject.text.tex_mobject.MathTex.html#manim.mobject.text.tex_mobject.MathTex "manim.mobject.text.tex_mobject.MathTex")（在模块中[`tex_mobject`](manim.mobject.text.tex_mobject.html#module-manim.mobject.text.tex_mobject "manim.mobject.text.tex_mobject")）将 LaTeX 插入到视频中一样，您可以使用[`Text`](manim.mobject.text.text_mobject.Text.html#manim.mobject.text.text_mobject.Text "manim.mobject.text.text_mobject.Text")to 添加普通文本。

重要的

请参阅相应的教程[Text Without LaTeX](../guides/using_text.html#using-text-objects)，特别是有关字体的信息。

向动画添加文本的最简单方法是使用该类[`Text`](manim.mobject.text.text_mobject.Text.html#manim.mobject.text.text_mobject.Text "manim.mobject.text.text_mobject.Text")。它使用 Pango 库来渲染文本。使用 Pango，您还可以渲染非英语字母，例如你好或 こんにちは或안녕하세요或 Мульябя babæר。

例子

示例：HelloWorld [¶](#helloworld)

![../_images/HelloWorld-2.png](../_images/HelloWorld-2.png)

```py

```


示例：文本对齐[¶](#textalignment)

![../_images/TextAlignment-1.png](../_images/TextAlignment-1.png)

```py

```


课程

[`MarkupText`](manim.mobject.text.text_mobject.MarkupText.html#manim.mobject.text.text_mobject.MarkupText "manim.mobject.text.text_mobject.MarkupText")

[显示使用 Pango](https://pango.gnome.org/)渲染的（非 LaTeX）文本。

[`Paragraph`](manim.mobject.text.text_mobject.Paragraph.html#manim.mobject.text.text_mobject.Paragraph "manim.mobject.text.text_mobject.Paragraph")

显示一段文本。

[`Text`](manim.mobject.text.text_mobject.Text.html#manim.mobject.text.text_mobject.Text "manim.mobject.text.text_mobject.Text")

[显示使用 Pango](https://pango.gnome.org/)渲染的（非 LaTeX）文本。

功能

注册字体（_字体文件_）[\[来源\]](../_modules/manim/mobject/text/text_mobject.html#register_font)[#](#manim.mobject.text.text_mobject.register_font "此定义的固定链接")

暂时将字体文件添加到 Pango 的搜索路径中。

这会在各个位置搜索 font_file。其搜索顺序如下所述。

1.  绝对路径。
2.  在`assets/fonts`文件夹中。
3.  在`font/`文件夹中。
4.  在同一目录中。

参数

**font_file** ( _str_ _|_ _Path_ ) – 要添加的字体文 ​​ 件。

例子

用于将字体文件添加到搜索路径。`with register_font(...)`

```py

```


提高

- **FileNotFoundError：** – 如果字体不存在。
- **AttributeError:** – 如果在 macOS 上使用此方法。
- **.. 重要::** – 此方法适用于 macOS 的`ManimPango>=v0.2.3`. 在以前的版本中使用此方法会在 macOS 上引发问题`AttributeError`。

参数

**font_file** ( _str_ _|\_\_路径_) –

删除*不可见*字符（_mobject_）[\[来源\]](../_modules/manim/mobject/text/text_mobject.html#remove_invisible_chars)[#](#manim.mobject.text.text_mobject.remove_invisible_chars "此定义的固定链接")

从某些对象中删除不需要的不可见字符的函数。

参数

**mobject** ( [_SVGMobject_](manim.mobject.svg.svg_mobject.SVGMobject.html#manim.mobject.svg.svg_mobject.SVGMobject "manim.mobject.svg.svg_mobject.SVGMobject") ) – 我们想要从中删除不需要的不可见字符的任何 SVGMobject。

退货

没有不需要的不可见字符的 SVGM 对象。

返回类型

[`SVGMobject`](manim.mobject.svg.svg_mobject.SVGMobject.html#manim.mobject.svg.svg_mobject.SVGMobject "manim.mobject.svg.svg_mobject.SVGMobject")
