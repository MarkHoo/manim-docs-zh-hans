# 文本

合格名称：`manim.mobject.text.text\_mobject.Text`


```py

```

[显示使用 Pango](https://pango.gnome.org/)渲染的（非 LaTeX）文本。

文本对象的行为类似于[`VGroup`](manim.mobject.types.vectorized_mobject.VGroup.html#manim.mobject.types.vectorized_mobject.VGroup "manim.mobject.types.vectorized_mobject.VGroup")给定文本中所有字符的类似迭代。特别地，切片是可能的。

参数

- **text** ( _str_ ) – 需要创建为 mobject 的文本。
- **font** ( _str_ ) – 用于呈现文本的字体系列。这可以是系统字体，也可以是使用 register_font()加载的字体。请注意，不同操作系统的字体系列名称可能有所不同。
- **warn_missing_font** ( \_bool ) – 如果为 True （默认），如果从\_manimpango.list_fonts()返回的字体（区分大小写）列表中不存在该字体，Manim 将发出警告。
- **fill_opacity** (_浮动_) –
- **笔画宽度**（_浮动_）-
- **颜色**(_颜色\_\_|_ _str_ _|\_\_无_) –
- **字体大小**（_浮动_）–
- **line_spacing** (_浮动_) –
- **倾斜**( _str_ ) –
- **重量**( _str_ ) –
- **t2c** (_字典\_\_\[_ _str_ _,_ _str_ _\]_ ) –
- **t2f** (_字典\_\_\[_ _str_ _,_ _str_ _\]_ ) –
- **t2g** (_字典\_\_\[_ _str_ _,**元组**\]_ ) –
- **t2s** (_字典\_\_\[_ _str_ _,_ _str_ _\]_ ) –
- **t2w** (_字典\_\_\[_ _str_ _,_ _str_ _\]_ ) –
- **梯度**（_元组_）–
- **tab_width** ( _int_ ) –
- **高度**（_浮动_）–
- **宽度**（_浮动_）–
- **should_center** (_布尔_) –
- **禁用\_连字**( _bool_ ) –

退货

类似 mobject 的[`VGroup`](manim.mobject.types.vectorized_mobject.VGroup.html#manim.mobject.types.vectorized_mobject.VGroup "manim.mobject.types.vectorized_mobject.VGroup").

返回类型

[`Text`](#manim.mobject.text.text_mobject.Text "manim.mobject.text.text_mobject.Text")

例子

示例：Example1Text

![../_images/Example1Text-1.png](../_images/Example1Text-1.png)

```py

```


示例：文本颜色示例

![../_images/TextColorExample-1.png](../_images/TextColorExample-1.png)


```py

```


示例：TextItalicAndBoldExample 

![../_images/TextItalicAndBoldExample-1.png](../_images/TextItalicAndBoldExample-1.png)


```py

```


示例：文本更多自定义

![../_images/TextMoreCustomization-1.png](../_images/TextMoreCustomization-1.png)


```py

```


由于[`Text`](#manim.mobject.text.text_mobject.Text "manim.mobject.text.text_mobject.Text")使用 Pango 渲染文本，渲染非英文字符是很容易的：

示例：多种字体[¶](#multiplefonts)

![../_images/MultipleFonts-1.png](../_images/MultipleFonts-1.png)

```py

```


示例：PangoRender 


```py

```


测试

检查作品创作情况[`Text`](#manim.mobject.text.text_mobject.Text "manim.mobject.text.text_mobject.Text")：


```py

```


方法

[`init_colors`]()

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

init*colors ( \_propagate_colors = True* )

初始化颜色。

被创造召唤。这是一个空方法，可以由子类实现。
