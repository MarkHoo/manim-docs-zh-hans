# 文本[#](#text "此标题的固定链接")

合格名称：`manim.mobject.text.text\_mobject.Text`

_类_ Text (_文本_, _fill_opacity = 1.0_ , _border_width = 0_ , _\*_ , _color = '#FFFFFF'_ , _font_size = 48_ , _line_spacing = \- 1_ , _font = ''_ , _slant = 'NORMAL'_ , _Weight = 'NORMAL'_ , _t2c =无_, _t2f =无_, _t2g =无_,_t2s =无_， _t2w =无_，_渐变=无_， _tab_width = 4_， _warn_missing_font = True_，_高度= None_，_宽度= None_， _should_center = True_， _disable_ligatures = False_， _\*\* kwargs_）[\[来源\]](../_modules/manim/mobject/text/text_mobject.html#Text)[#](#manim.mobject.text.text_mobject.Text "此定义的固定链接")

基地：[`SVGMobject`](manim.mobject.svg.svg_mobject.SVGMobject.html#manim.mobject.svg.svg_mobject.SVGMobject "manim.mobject.svg.svg_mobject.SVGMobject")

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

示例：Example1Text [¶](#example1text)

![../_images/Example1Text-1.png](../_images/Example1Text-1.png)

from manim import \*

class Example1Text(Scene):
def construct(self):
text = Text('Hello world').scale(3)
self.add(text)

Copy to clipboard

示例：文本颜色示例[¶](#textcolorexample)

![../_images/TextColorExample-1.png](../_images/TextColorExample-1.png)

from manim import \*

class TextColorExample(Scene):
def construct(self):
text1 = Text('Hello world', color=BLUE).scale(3)
text2 = Text('Hello world', gradient=(BLUE, GREEN)).scale(3).next_to(text1, DOWN)
self.add(text1, text2)

Copy to clipboard

示例：TextItalicAndBoldExample [¶](#textitalicandboldexample)

![../_images/TextItalicAndBoldExample-1.png](../_images/TextItalicAndBoldExample-1.png)

from manim import \*

class TextItalicAndBoldExample(Scene):
def construct(self):
text1 = Text("Hello world", slant=ITALIC)
text2 = Text("Hello world", t2s={'world':ITALIC})
text3 = Text("Hello world", weight=BOLD)
text4 = Text("Hello world", t2w={'world':BOLD})
text5 = Text("Hello world", t2c={'o':YELLOW}, disable_ligatures=True)
text6 = Text(
"Visit us at docs.manim.community",
t2c={"docs.manim.community": YELLOW},
disable_ligatures=True,
)
text6.scale(1.3).shift(DOWN)
self.add(text1, text2, text3, text4, text5 , text6)
Group(\*self.mobjects).arrange(DOWN, buff=.8).set_height(config.frame_height-LARGE_BUFF)

Copy to clipboard

示例：文本更多自定义[¶](#textmorecustomization)

![../_images/TextMoreCustomization-1.png](../_images/TextMoreCustomization-1.png)

from manim import \*

class TextMoreCustomization(Scene):
def construct(self):
text1 = Text(
'Google',
t2c={'\[:1\]': '#3174f0', '\[1:2\]': '#e53125',
'\[2:3\]': '#fbb003', '\[3:4\]': '#3174f0',
'\[4:5\]': '#269a43', '\[5:\]': '#e53125'}, font_size=58).scale(3)
self.add(text1)

Copy to clipboard

由于[`Text`](#manim.mobject.text.text_mobject.Text "manim.mobject.text.text_mobject.Text")使用 Pango 渲染文本，渲染非英文字符是很容易的：

示例：多种字体[¶](#multiplefonts)

![../_images/MultipleFonts-1.png](../_images/MultipleFonts-1.png)

from manim import \*

class MultipleFonts(Scene):
def construct(self):
morning = Text("வணக்கம்", font="sans-serif")
japanese = Text(
"日本へようこそ", t2c={"日本": BLUE}
) \# works same as \`\`Text\`\`.
mess = Text("Multi-Language", weight=BOLD)
russ = Text("Здравствуйте मस नम म ", font="sans-serif")
hin = Text("नमस्ते", font="sans-serif")
arb = Text(
"صباح الخير \\n تشرفت بمقابلتك", font="sans-serif"
) \# don't mix RTL and LTR languages nothing shows up then ;-)
chinese = Text("臂猿「黛比」帶著孩子", font="sans-serif")
self.add(morning, japanese, mess, russ, hin, arb, chinese)
for i,mobj in enumerate(self.mobjects):
mobj.shift(DOWN\*(i-3))

Copy to clipboard

示例：PangoRender [¶](#pangorender)

from manim import \*

class PangoRender(Scene):
def construct(self):
morning = Text("வணக்கம்", font="sans-serif")
self.play(Write(morning))
self.wait(2)

Copy to clipboard

测试

检查作品创作情况[`Text`](#manim.mobject.text.text_mobject.Text "manim.mobject.text.text_mobject.Text")：

> > \> Text('The horse does not eat cucumber salad.')
> > Text('The horse does not eat cucumber salad.')

Copy to clipboard

方法

[`init_colors`](#manim.mobject.text.text_mobject.Text.init_colors "manim.mobject.text.text_mobject.Text.init_colors")

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

init*colors ( \_propagate_colors = True* )[\[来源\]](../_modules/manim/mobject/text/text_mobject.html#Text.init_colors)[#](#manim.mobject.text.text_mobject.Text.init_colors "此定义的固定链接")

初始化颜色。

被创造召唤。这是一个空方法，可以由子类实现。
