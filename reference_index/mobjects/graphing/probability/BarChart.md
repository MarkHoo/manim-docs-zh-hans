# 条形图[#](#barchart "此标题的固定链接")

合格名称：`manim.mobject.graphing.probability.BarChart`

_类_ BarChart (_值_, _bar_names = None_ , _y_range = None_ , _x_length = None_ , _y_length = None_ , _bar_colors = \['#003f5c', '#58508d', '#bc5090', '#ff6361', '#ffa600'\]_ , _bar_width = 0.6_ , _bar_fill_opacity = 0.7_ , _bar_lines_width = 3_ , _\*\* kwargs_ )[\[来源\]](../_modules/manim/mobject/graphing/probability.html#BarChart)[#](#manim.mobject.graphing.probability.BarChart "此定义的固定链接")

基地：[`Axes`](manim.mobject.graphing.coordinate_systems.Axes.html#manim.mobject.graphing.coordinate_systems.Axes "manim.mobject.graphing.coordinate_systems.Axes")

创建条形图。继承自[`Axes`](manim.mobject.graphing.coordinate_systems.Axes.html#manim.mobject.graphing.coordinate_systems.Axes "manim.mobject.graphing.coordinate_systems.Axes")，因此它共享其方法和属性。每个轴都继承自[`NumberLine`](manim.mobject.graphing.number_line.NumberLine.html#manim.mobject.graphing.number_line.NumberLine "manim.mobject.graphing.number_line.NumberLine")，因此传入`x_axis_config`/`y_axis_config` 来控制它们的属性。

参数

- **value** ( _MutableSequence_ _\[_ _float_ _\]_ ) – 确定每个条形高度的值序列。接受负值。
- **bar_names** ( _Sequence_ _\[_ _str_ _\]_ _|_ _None_ ) – 每个柱的名称序列。不必匹配 的长度`values`。
- **y_range** ( _Sequence_ _\[_ _float_ _\]_ _|_ _None_ ) – y 轴值范围。如果`None`，则将根据 的最小值/最大值计算范围`values`，并根据 计算步长`y_length`。
- **x_length** ( _float_ _|_ _None_ ) – x 轴的长度。如果`None`，则根据值的数量和屏幕的宽度自动计算。
- **y_length** ( _float_ _|_ _None_ ) – y 轴的长度。
- **bar_colors** ( _Iterable_ _\[_ _str_ _\]_ ) – 条形的颜色。接受一系列颜色（只能包含一个项目）。如果“bar_colors”的长度与 的长度不匹配`values`，则会自动确定中间颜色。
- **bar_width** ( _float_ ) – 条形的长度。必须介于 0 和 1 之间。
- **bar_fill_opacity** ( _float_ ) – 条形的填充不透明度。
- **bar_lines_width** ( _float_ ) – 条形的描边宽度。

例子

示例：条形图示例[¶](#barchartexample)

![../_images/BarChartExample-1.png](../_images/BarChartExample-1.png)

from manim import \*

class BarChartExample(Scene):
def construct(self):
chart = BarChart(
values=\[-5, 40, -10, 20, -3\],
bar_names=\["one", "two", "three", "four", "five"\],
y_range=\[-20, 50, 10\],
y_length=6,
x_length=10,
x_axis_config={"font_size": 36},
)

        c\_bar\_lbls = chart.get\_bar\_labels(font_size=48)

        self.add(chart, c\_bar\_lbls)

Copy to clipboard

方法

[`change_bar_values`](#manim.mobject.graphing.probability.BarChart.change_bar_values "manim.mobject.graphing.probability.BarChart.change_bar_values")

更新图表条形的高度。

[`get_bar_labels`](#manim.mobject.graphing.probability.BarChart.get_bar_labels "manim.mobject.graphing.probability.BarChart.get_bar_labels")

用相应的值注释每个条。

属性

`animate`

用于对 的任何方法的应用程序进行动画处理`self`。

`animation_overrides`

`color`

`depth`

对象的深度。

`fill_color`

如果有多种颜色（对于渐变），则返回第一个颜色

`height`

mobject 的高度。

`n_points_per_curve`

`sheen_factor`

`stroke_color`

`width`

mobject 的宽度。

change*bar_values（*值*， \_update_colors = True*）[\[来源\]](../_modules/manim/mobject/graphing/probability.html#BarChart.change_bar_values)[#](#manim.mobject.graphing.probability.BarChart.change_bar_values "此定义的固定链接")

更新图表条形的高度。

参数

- **value** ( _Iterable_ _\[_ _float_ _\]_ ) – 将用于更新条形高度的值。不必匹配条数。
- **update_colors** ( _bool_ ) – 是否根据 重新初始化条形的颜色`self.bar_colors`。

例子

示例：ChangeBarValuesExample [¶](#changebarvaluesexample)

![../_images/ChangeBarValuesExample-1.png](../_images/ChangeBarValuesExample-1.png)

from manim import \*

class ChangeBarValuesExample(Scene):
def construct(self):
values=\[-10, -8, -6, -4, -2, 0, 2, 4, 6, 8, 10\]

        chart = BarChart(
            values,
            y_range=\[-10, 10, 2\],
            y\_axis\_config={"font_size": 24},
        )
        self.add(chart)

        chart.change\_bar\_values(list(reversed(values)))
        self.add(chart.get\_bar\_labels(font_size=24))

Copy to clipboard

get*bar_labels ( \_color=None* , _font_size=24_ , _buff=0.25_ , _label_constructor=<class 'manim.mobject.text.tex_mobject.Tex'_ \> )[\[来源\]](../_modules/manim/mobject/graphing/probability.html#BarChart.get_bar_labels)[#](#manim.mobject.graphing.probability.BarChart.get_bar_labels "此定义的固定链接")

用相应的值注释每个条。用于`self.bar_labels`在创建后访问标签。

参数

- **color** ( _Color_ _|_ _None_ ) – 每个标签的颜色。默认情况下`None`，基于父级的条形颜色。
- **font_size** ( _float_ ) – 每个标签的字体大小。
- **buff** ( _float_ ) – 每个标签到其条形的距离。默认为 0.4。
- **label_constructor** ( _type_ _\[_ [_VMobject_](manim.mobject.types.vectorized_mobject.VMobject.html#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject") _\]_ ) – 默认情况下，用于构造标签的 Mobject 类[`Tex`](manim.mobject.text.tex_mobject.Tex.html#manim.mobject.text.tex_mobject.Tex "manim.mobject.text.tex_mobject.Tex")。

例子

示例：GetBarLabelsExample [¶](#getbarlabelsexample)

![../_images/GetBarLabelsExample-1.png](../_images/GetBarLabelsExample-1.png)

from manim import \*

class GetBarLabelsExample(Scene):
def construct(self):
chart = BarChart(values=\[10, 9, 8, 7, 6, 5, 4, 3, 2, 1\], y_range=\[0, 10, 1\])

        c\_bar\_lbls = chart.get\_bar\_labels(
            color=WHITE, label_constructor=MathTex, font_size=36
        )

        self.add(chart, c\_bar\_lbls)

Copy to clipboard
