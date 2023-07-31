# 调试[#](#module-manim.utils.debug "此标题的固定链接")

调试实用程序。

功能

index*labels（\_mobject*， _label_height = 0.15_， _background_lines_width = 5_， _background_lines_color = '＃000000'_， _\*\* kwargs_）[\[来源\]](../_modules/manim/utils/debug.html#index_labels)[#](#manim.utils.debug.index_labels "此定义的固定链接")

返回 mobjects[`VGroup`](manim.mobject.types.vectorized_mobject.VGroup.html#manim.mobject.types.vectorized_mobject.VGroup "manim.mobject.types.vectorized_mobject.VGroup")的一个[`Integer`](manim.mobject.text.numbers.Integer.html#manim.mobject.text.numbers.Integer "manim.mobject.text.numbers.Integer")，显示每个子对象的索引。

对于处理复杂对象的部分很有用。

参数

- **mobject** ( [_Mobject_](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject") ) – 将为其子对象添加标签的 mobject。
- **label_height** ( _float_ ) – 标签的高度，默认为 0.15。
- **background_lines_width** – 标签轮廓的描边宽度，默认为 5。
- **background_lines_color** – 标签轮廓的描边颜色。
- **kwargs** – 要传递到用于构造标签的 :class`~.Integer` mobject 中的附加参数。

例子

示例：IndexLabelsExample [¶](#indexlabelsexample)

![../_images/IndexLabelsExample-1.png](../_images/IndexLabelsExample-1.png)

from manim import \*

class IndexLabelsExample(Scene):
def construct(self):
text = MathTex(
"\\\frac{d}{dx}f(x)g(x)=",
"f(x)\\\frac{d}{dx}g(x)",
"+",
"g(x)\\\frac{d}{dx}f(x)",
)

        #index the fist term in the MathTex mob
        indices = index_labels(text\[0\])

        text\[0\]\[1\].set_color(PURPLE_B)
        text\[0\]\[8:12\].set_color(DARK_BLUE)

        self.add(text, indices)

Copy to clipboard

print*family ( \_mobject* , _n_tabs = 0_ )[\[来源\]](../_modules/manim/utils/debug.html#print_family)[#](#manim.utils.debug.print_family "此定义的固定链接")

用于调试目的
