# 标记线

合格名称：`manim.mobject.geometry.labeled.LabeledLine`

```py
class LabeledLine(label, label_position=0.5, font_size=48, label_color=ManimColor('#FFFFFF'), label_frame=True, frame_fill_color=None, frame_fill_opacity=1, *args, **kwargs)
```

Bases：[`Line`]()

构造一条沿其长度某处包含标签框的线。

参数：

- **label** (_str | Tex | MathTex | Text_) – 将显示在该行上的标签。
- **label_position** (_float | optional_)  – \[0-1\] 范围内的比率，指示标签相对于线条长度的位置。默认值为 0.5。
- **font_size** (_float | optional_) – 控制标签的字体大小。仅当label类型为str时才使用此参数。
- **label_color** (_ParsableManimColor | optional_) – 标签文本的颜色。仅当label类型为str时才使用此参数。
- **label_frame** (_Bool | optional_)  – 将SurroundingRectangle框架添加到标签框。
- **frame_fill_color** (_ParsableManimColor | optional_) – 填充标签框的背景颜色。如果未提供值，则将使用画布的背景颜色。
- **frame_fill_opacity** (_float | optional_) – 通过传递 \[0-1\] 范围内的值来确定标签框的不透明度，其中 0 表示完全透明，1 表示完全不透明。
- **seealso::** (..) -[`LabeledArrow`]()

例子

示例：LabeledLineExample

![](../https://docs.manim.community/en/stable/_images/LabeledLineExample-1.png)

```py
from manim import *

class LabeledLineExample(Scene):
    def construct(self):
        line = LabeledLine(
            label          = '0.5',
            label_position = 0.8,
            font_size      = 20,
            label_color    = WHITE,
            label_frame    = True,

            start=LEFT+DOWN,
            end=RIGHT+UP)

        line.set_length(line.get_length() * 2)
        self.add(line)
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


```py
_original__init__(label, label_position=0.5, font_size=48, label_color=ManimColor('#FFFFFF'), label_frame=True, frame_fill_color=None, frame_fill_opacity=1, *args, **kwargs)
```

初始化自身。请参阅 help(type(self)) 以获取准确的签名。

参数：

- **label** (_str | manim.mobject.text.tex_mobject.Tex | manim.mobject.text.tex_mobject.MathTex | manim.mobject.text.text_mobject.Text_) –

- **label_position** (_float_) –

- **font_size** (_float_) –

- **label_color** (_Union[ManimColor, int, str, Tuple[int, int, int], Tuple[float, float, float], Tuple[int, int, int, int], Tuple[float, float, float, float], ndarray[Any, dtype[int64]], ndarray[Any, dtype[float64]]]_) –

- **label_frame** (bool) –

- **frame_fill_color** (_Union[ManimColor, int, str, Tuple[int, int, int], Tuple[float, float, float], Tuple[int, int, int, int], Tuple[float, float, float, float], ndarray[Any, dtype[int64]], ndarray[Any, dtype[float64]]]_) –

- **frame_fill_opacity** (_float_) –


返回类型：
None
