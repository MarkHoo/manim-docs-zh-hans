# 标记文本

合格名称：`manim.mobject.text.text\_mobject.MarkupText`


```py

```

[显示使用 Pango](https://pango.gnome.org/)渲染的（非 LaTeX）文本。

文本对象的行为类似于[`VGroup`]()给定文本中所有字符的类似迭代。特别地，切片是可能的。

**什么是 PangoMarkup？**

PangoMarkup 是一种类似于 html 的小型标记语言，它可以帮助您在对文本片段进行着色或设计样式时避免使用“字符范围”。您可以将这种语言与[`MarkupText`]().

标记字符串的一个简单示例可能是：


```py

```


它可以与[`MarkupText`]()as 一起使用

示例：标记示例

![MarkupExample-1.png](../_images/MarkupExample-1.png)

```py

```


一个更详细的例子是：

示例：MarkupElaborateExample

![MarkupElaborateExample-1.png](../_images/MarkupElaborateExample-1.png)

```py

```


PangoMarkup 还可以包含 XML 功能，例如数字字符实体，例如`&#169;`也可以使用 for ©。

最通用的标记是`<span>`，然后还有一些便利标记。

以下是支持的标签列表：

- `<b>bold</b>`,`<i>italic</i>`和`<b><i>bold+italic</i></b>`
- `<ul>underline</ul>`和`<s>strike through</s>`
- `<tt>typewriter font</tt>`
- `<big>bigger font</big>`和`<small>smaller font</small>`
- `<sup>superscript</sup>`和`<sub>subscript</sub>`
- `<span underline="double" underline_color="green">double underline</span>`
- `<span underline="error">error underline</span>`
- `<span overline="single" overline_color="green">overline</span>`
- `<span strikethrough="true" strikethrough_color="red">strikethrough</span>`
- `<span font_family="sans">temporary change of font</span>`
- `<span foreground="red">temporary change of color</span>`
- `<span fgcolor="red">temporary change of color</span>`
- `<gradient from="YELLOW" to="RED">temporary gradient</gradient>`

对于`<span>`标记，颜色可以指定为十六进制三元组，如`#aabbcc`或命名为 CSS 颜色，如 `AliceBlue`. 该`<gradient>`标签由 Manim 而不是 Pango 处理，并支持十六进制三元组或 Manim 常量，例如 `RED`或`RED_A`。`RED_A`如果你想像 with 一样使用 Manim 常量`<span>`，则需要使用 Python 的 f-String 语法，如下所示：

```py

```


如果您的文本包含连字，则[`MarkupText`](#manim.mobject.text.text_mobject.MarkupText "manim.mobject.text.text_mobject.MarkupText")班级在创建渐变时可能会错误地确定第一个和最后一个字母。这是因为它们`fl`是两个单独的字符，但可以设置为一个字形 \- 连字。如果您的语言不依赖于连字，请考虑设置`disable_ligatures` 为`True`。如果必须使用连字，则`gradient`标记支持可选属性`offset`，可用于补偿该错误。

例如：

- `<gradient from="RED" to="YELLOW" offset="1">example</gradient>`*提前*一个字母开始渐变
- `<gradient from="RED" to="YELLOW" offset=",1">example</gradient>`*提前*一个字母结束渐变
- `<gradient from="RED" to="YELLOW" offset="2,1">example</gradient>`*提前两个字母开始*渐变并提前一个字母*结束*

如果要着色的文本本身包含连字，则可能需要指定第二个偏移量。当使用 HTML 实体表示特殊字符时，也会发生同样的情况。

当使用`underline`,`overline`或`strikethrough`与 `<gradient>`标签一起使用时，您还需要使用偏移量，因为下划线是最终`SVGMobject`. 查看以下示例。

特殊字符的转义：`>` **应**写为`&gt;` while`<`且`&` *必须*写为`&lt;`and `&amp;`。

您可以在相应的文档页面找到有关 Pango 标记格式的更多信息： [Pango Markup](https://docs.gtk.org/Pango/pango_markup.html)。请注意，并非该类支持所有功能，并且`<gradient>`Pango 不支持上述标签。

参数

- **text** ( _str_ ) – 需要创建为 mobject 的文本。
- **fill_opacity** ( _float_ ) – 填充不透明度，1 表示不透明，0 表示透明。
- **描边宽度**( _float_ ) – 描边宽度。
- **font_size** ( _float_ ) – 字体大小。
- **line_spacing** ( _int_ ) – 行间距。
- **font** ( _str_ ) – 整个文本的全局字体设置。本地覆盖是可能的。
- **slant** ( _str_ ) – 全局倾斜设置，例如 NORMAL 或 ITALIC。本地覆盖是可能的。
- **权重**( _str_ ) – 全局权重设置，例如 NORMAL 或 BOLD。本地覆盖是可能的。
- **梯度**( _tuple_ ) – 全局梯度设置。本地覆盖是可能的。
- **warn_missing_font** ( \_bool ) – 如果为 True （默认），如果从\_manimpango.list_fonts()返回的字体（区分大小写）列表中不存在该字体，Manim 将发出警告。
- **颜色**（_颜色**|**无_）–
- **证明**( _bool_ ) –
- **tab_width** ( _int_ ) –
- **高度**( _int_ ) –
- **宽度**( _int_ ) –
- **should_center** (_布尔_) –
- **禁用\_连字**( _bool_ ) –

退货

文本以[`VGroup`](manim.mobject.types.vectorized_mobject.VGroup.html#manim.mobject.types.vectorized_mobject.VGroup "manim.mobject.types.vectorized_mobject.VGroup")类似 mobject 的形式显示。

返回类型

[`MarkupText`](#manim.mobject.text.text_mobject.MarkupText "manim.mobject.text.text_mobject.MarkupText")

例子

示例：BasicMarkupExample

![BasicMarkupExample-1.png](../_images/BasicMarkupExample-1.png)

```py

```


示例：颜色示例

![ColorExample-1.png](../_images/ColorExample-1.png)

```py

```

示例：下划线示例

![UnderlineExample-1.png](../_images/UnderlineExample-1.png)

```py

```


示例：字体示例

![FontExample-1.png](../_images/FontExample-1.png)

```py

```


示例：换行示例

![NewlineExample-1.png](../_images/NewlineExample-1.png)

```py

```


示例：NoLigaturesExample 

![NoLigaturesExample-1.png](../_images/NoLigaturesExample-1.png)

```py

```


由于[`MarkupText`](#manim.mobject.text.text_mobject.MarkupText "manim.mobject.text.text_mobject.MarkupText")使用 Pango 渲染文本，渲染非英文字符是很容易的：

示例：多语言

![MultiLanguage-1.png](../_images/MultiLanguage-1.png)

```py

```


您可以通过传递参数来调整文本`justify`。

示例：对齐文本

```py

```


测试

检查作品创作情况[`MarkupText`](#manim.mobject.text.text_mobject.MarkupText "manim.mobject.text.text_mobject.MarkupText")：

```py

```


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

`font_size`

`hash_seed`

表示生成的对象点结果的唯一哈希值。

`height`

mobject 的高度。

`n_points_per_curve`

`sheen_factor`

`stroke_color`

`width`

mobject 的宽度。
