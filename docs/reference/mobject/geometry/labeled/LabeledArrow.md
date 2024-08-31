# 标记箭头

限定名称：`manim.mobject.geometry.labeled.LabeledArrow`

`class LabeledArrow(*args, **kwargs)`

Bases:[`LabeledLine`](),[`Arrow`]()

构造一个箭头，其中包含沿其长度某处的标签框。该类从LabeledLine继承其标签属性，因此控制它的主要参数是相同的。

参数：

- **label** (_str | Tex | MathTex | Text_) – 将显示在该行上的标签。
- **label_position** (_float | optional_)  – \[0-1\] 范围内的比率，指示标签相对于线条长度的位置。默认值为 0.5。
- **font_size** (_float | optional_) – 控制标签的字体大小。仅当label类型为str时才使用此参数。
- **label_color** (_ParsableManimColor | optional_)  – 标签文本的颜色。仅当label类型为str时才使用此参数。
- **label_frame** (_Bool | optional_)  – 将SurroundingRectangle框架添加到标签框。
- **frame_fill_color** (_ParsableManimColor | optional_)  – 填充标签框的背景颜色。如果未提供值，则将使用画布的背景颜色。
- **frame_fill_opacity** (_float | optional_) – 通过传递 \[0-1\] 范围内的值来确定标签框的不透明度，其中 0 表示完全透明，1 表示完全不透明。

> 也可以看看
> [`LabeledLine`]()

例子

示例：LabeledArrowExample

![](https://docs.manim.community/en/stable/_images/LabeledArrowExample-1.png)

```py
from manim import *

class LabeledArrowExample(Scene):
    def construct(self):
        l_arrow = LabeledArrow("0.5", start=LEFT*3, end=RIGHT*3 + UP*2, label_position=0.5)

        self.add(l_arrow)
```

方法


属性

|||
|-|-|
`animate`|用于对 的任何方法的应用程序进行动画处理`self`。
`animation_overrides`|
`color`|
`depth`|对象的深度。
`fill_color`|如果有多种颜色（用于渐变），则返回第一个颜色
`height`|mobject 的高度。
`n_points_per_curve`|
`sheen_factor`|
`stroke_color`|
`width`|mobject 的宽度。


`_original__init__(*args, **kwargs)`

初始化自身。请参阅 help(type(self)) 以获取准确的签名。

返回类型：
None

