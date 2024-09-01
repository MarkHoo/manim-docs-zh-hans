# Debug/调试

调试实用程序。

Functions

```py
index_labels(mobject, label_height=0.15, background_stroke_width=5, background_stroke_color='#000000', **kwargs)
```

返回 mobjects[`VGroup`]()的一个[`Integer`]()，显示每个子对象的索引。

对于处理复杂对象的部分很有用。

参数

- **mobject** ( [_Mobject_]() ) – 将为其子对象添加标签的 mobject。
- **label_height** ( _float_ ) – 标签的高度，默认为 0.15。
- **background_lines_width** – 标签轮廓的描边宽度，默认为 5。
- **background_lines_color** – 标签轮廓的描边颜色。
- **kwargs** – 要传递到用于构造标签的 :class`~.Integer` mobject 中的附加参数。

例子

示例：IndexLabelsExample 

![IndexLabelsExample-1.png](../static/IndexLabelsExample-1.png)

```py
from manim import *

class IndexLabelsExample(Scene):
    def construct(self):
        text = MathTex(
            "\\frac{d}{dx}f(x)g(x)=",
            "f(x)\\frac{d}{dx}g(x)",
            "+",
            "g(x)\\frac{d}{dx}f(x)",
        )

        #index the fist term in the MathTex mob
        indices = index_labels(text[0])

        text[0][1].set_color(PURPLE_B)
        text[0][8:12].set_color(DARK_BLUE)

        self.add(text, indices)
```


`print_family(mobject, n_tabs=0)`

用于调试目的
