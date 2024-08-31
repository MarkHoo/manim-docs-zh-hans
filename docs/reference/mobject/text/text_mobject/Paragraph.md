# 段落

合格名称：`manim.mobject.text.text\_mobject.Paragraph`


```py
class Paragraph(*text, line_spacing=- 1, alignment=None, **kwargs)
```

Bases: `VGroup`

显示一段文本。

对于给定的，属性是 包含所有行的。在这种情况下，每一行都被构造为该行中包含的字符。[`Paragraph`]() ` par` `par.chars `[`VGroup`]()[`VGroup`]()

参数

- **line_spacing** ( _float_ ) – 表示行之间的间距。默认为-1，表示自动。
- **alignment** (_Optional\_\_\[_ _str_ _\]_ ) – 定义段落的对齐方式。默认为无。可能的值为“左”、“右”或“中心”。
- **text**(_Sequence\_\_\[_ _str_ _\]_ ) –

例子

正常使用：

```py
paragraph = Paragraph('this is a awesome', 'paragraph',
                      'With \nNewlines', '\tWith Tabs',
                      '  With Spaces', 'With Alignments',
                      'center', 'left', 'right')
```


删除不需要的不可见字符：

```py
self.play(Transform(remove_invisible_chars(paragraph.chars[0:2]),
                    remove_invisible_chars(paragraph.chars[3][0:3]))
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
`height`|mobject 的高度。
`n_points_per_curve`|
`sheen_factor`|
`stroke_color`|
`width`|mobject 的宽度。
