# 函数图[#](#functiongraph "此标题的固定链接")

合格名称：`manim.mobject.graphing.functions.FunctionGraph`

_类_ FunctionGraph (_函数_, _x_range = None_ , _color = '#FFFF00'_ , _\*\* kwargs_ )[\[来源\]](../_modules/manim/mobject/graphing/functions.html#FunctionGraph)[#](#manim.mobject.graphing.functions.FunctionGraph "此定义的固定链接")

基地：[`ParametricFunction`](manim.mobject.graphing.functions.ParametricFunction.html#manim.mobject.graphing.functions.ParametricFunction "manim.mobject.graphing.functions.ParametricFunction")

[`ParametricFunction`](manim.mobject.graphing.functions.ParametricFunction.html#manim.mobject.graphing.functions.ParametricFunction "manim.mobject.graphing.functions.ParametricFunction")默认情况下跨越场景长度的 A。

例子

示例：ExampleFunctionGraph [¶](#examplefunctiongraph)

![../_images/ExampleFunctionGraph-1.png](../_images/ExampleFunctionGraph-1.png)

from manim import \*

class ExampleFunctionGraph(Scene):
def construct(self):
cos*func = FunctionGraph(
lambda t: np.cos(t) + 0.5 * np.cos(7 _ t) + (1 / 7) _ np.cos(14 \_ t),
color=RED,
)

        sin\_func\_1 = FunctionGraph(
            lambda t: np.sin(t) + 0.5 * np.sin(7 * t) + (1 / 7) * np.sin(14 * t),
            color=BLUE,
        )

        sin\_func\_2 = FunctionGraph(
            lambda t: np.sin(t) + 0.5 * np.sin(7 * t) + (1 / 7) * np.sin(14 * t),
            x_range=\[-4, 4\],
            color=GREEN,
        ).move_to(\[0, 1, 0\])

        self.add(cos_func, sin\_func\_1, sin\_func\_2)

Copy to clipboard

方法

`get_function`

`get_point_from_function`

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
