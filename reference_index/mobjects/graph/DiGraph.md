# 有向图[#](#digraph "此标题的固定链接")

合格名称：`manim.mobject.graph.DiGraph`

_类_ DiGraph (_顶点_,_边_, _labels=False_ , _label_fill_color='#000000'_ , _layout='spring'_ , _layout_scale=2_ , _layout_config=None_ , _vertex_type=<class 'manim.mobject.geometry.arc.Dot'>_ , _vertex_config =无_， _vertex_mobjects =无_， _edge_type = <类 'manim.mobject.geometry.line.Line'>_，_分区=无_， _root_vertex =无_， _edge_config =无_）[\[来源\]](../_modules/manim/mobject/graph.html#DiGraph)[#](#manim.mobject.graph.DiGraph "此定义的固定链接")

基地：[`GenericGraph`](manim.mobject.graph.GenericGraph.html#manim.mobject.graph.GenericGraph "manim.mobject.graph.GenericGraph")

有向图。

笔记

与无向图相比，给定边中的顶点的指定顺序在这里是相关的。

也可以看看

[`GenericGraph`](manim.mobject.graph.GenericGraph.html#manim.mobject.graph.GenericGraph "manim.mobject.graph.GenericGraph")

参数

- **vertices** ( _list_ _\[_ _Hashable_ _\]_ ) – 顶点列表。必须是可散列的元素。
- **Edges** ( _list_ _\[_ _tuple_ _\[_ _Hashable_ _,_ _Hashable_ _\]_ _\]_ ) – 边列表，指定为元组，其中 和 都是顶点。边的方向是从到。` (u, v)``u``v``u``v `
- **labels** ( _bool_ _|_ _dict_ ) – 控制是否标记顶点。如果`False`（默认），则不标记顶点；如果`True`他们使用其名称（如 中指定`vertices`）通过 进行标记[`MathTex`](manim.mobject.text.tex_mobject.MathTex.html#manim.mobject.text.tex_mobject.MathTex "manim.mobject.text.tex_mobject.MathTex")。或者，可以通过传递一个字典来指定自定义标签，该字典的键是顶点，其值是相应的顶点标签（通过例如 或 呈现[`Text`](manim.mobject.text.text_mobject.Text.html#manim.mobject.text.text_mobject.Text "manim.mobject.text.text_mobject.Text")）[`Tex`](manim.mobject.text.tex_mobject.Tex.html#manim.mobject.text.tex_mobject.Tex "manim.mobject.text.tex_mobject.Tex")。
- **label_fill_color** ( _str_`labels` ) – 设置设置为 时 生成的默认标签的填充颜色`True`。对 的其他值没有影响`labels`。
- **布局**( _str_ _|_ _dict_ ) – `"spring"`（默认）、`"circular"`、`"kamada_kawai"`、 `"planar"`、`"random"`、`"shell"`、`"spectral"`、`"spiral"`、`"tree"`和`"partite"` 用于自动顶点定位`networkx` （有关更多详细信息，请参阅[其文档](https://networkx.org/documentation/stable/reference/drawing.html#module-networkx.drawing.layout) ）或为每个顶点指定坐标（值）的字典之一（键）用于手动定位。
- **layout_config** ( _dict_ _|_ _None_ ) – 仅适用于自动生成的布局。`layout`一个字典，其条目作为关键字参数传递给通过 of 指定的自动布局算法`networkx`。布局还接受 作为字典内的关键字参数传递的`tree`特殊参数。传递一个元组作为此参数会覆盖 的值并确保顶点的排列方式使得同一层中同级的中心在水平方向上至少相距单位，并且相邻层在垂直方向上间隔单位。` vertex_spacing``layout_config``(space_x, space_y)``layout_scale``space_x``space_y `
- **layout_scale** ( _float_ _|_ _tuple_ ) – 自动生成的布局的比例：顶点将被排列，使得坐标位于区间内。某些布局接受一个元组， 导致第一个坐标位于 间隔 中，第二个坐标位于 中。默认值：2。` [-scale, scale]``(scale_x, scale_y)``[-scale_x, scale_x]``[-scale_y, scale_y] `
- **vertex_type** ( _type_ _\[_ [_Mobject_](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject") _\]_ ) – 用于在场景中显示顶点的 mobject 类。
- **vertex_config** ( _dict_ _|_ _None_ ) – 包含要传递给 via 指定的类的关键字参数的字典`vertex_type`，或者其键是顶点的字典，其值是包含与相应顶点相关的 mobject 的关键字参数的字典。
- **vertex_mobjects** ( _dict_ _|_ _None_ ) – 一个字典，其键是顶点，其值是用作顶点的 mobject。在此处传递顶点将覆盖顶点的所有其他配置选项。
- **edge_type** ( _type_ _\[_ [_Mobject_](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject") _\]_ ) – 用于显示场景中边缘的 mobject 类。
- **edge_config** ( _dict_ _|_ _None_ ) – 包含要传递给 via 指定的类的关键字参数的字典`edge_type`，或者其键是边的字典，其值是包含与相应边相关的 mobject 的关键字参数的字典。您可以通过添加`tip_config`全局样式的字典或将字典添加到特定的`edge_config`.
- **分区**( _list_ _\[_ _list_ _\[_ _Hashable_ _\]_ _\]_ _|_ _None_ ) –
- **root_vertex** ( _Hashable_ _|_ _None_ ) –

例子

示例：移动有向图[¶](#movingdigraph)

from manim import \*

class MovingDiGraph(Scene):
def construct(self):
vertices = \[1, 2, 3, 4\]
edges = \[(1, 2), (2, 3), (3, 4), (1, 3), (1, 4)\]

        g = DiGraph(vertices, edges)

        self.add(g)
        self.play(
            g\[1\].animate.move_to(\[1, 1, 1\]),
            g\[2\].animate.move_to(\[-1, 1, 2\]),
            g\[3\].animate.move_to(\[1, -1, -1\]),
            g\[4\].animate.move_to(\[-1, -1, 0\]),
        )
        self.wait()

Copy to clipboard

您可以全局或局部自定义边缘和箭头提示。

示例：自定义有向图[¶](#customdigraph)

from manim import \*

class CustomDiGraph(Scene):
def construct(self):
vertices = \[i for i in range(5)\]
edges = \[
(0, 1),
(1, 2),
(3, 2),
(3, 4),
\]

        edge_config = {
            "stroke_width": 2,
            "tip_config": {
                "tip_shape": ArrowSquareTip,
                "tip_length": 0.15,
            },
            (3, 4): {
                "color": RED,
                "tip_config": {"tip_length": 0.25, "tip_width": 0.25}
            },
        }

        g = DiGraph(
            vertices,
            edges,
            labels=True,
            layout="circular",
            edge_config=edge_config,
        ).scale(1.4)

        self.play(Create(g))
        self.wait()

Copy to clipboard

由于此实现尊重标签边界，因此您也可以将其用于带有标签的无向移动图。

示例：无向移动有向图[¶](#undirectedmovingdigraph)

from manim import \*

class UndirectedMovingDiGraph(Scene):
def construct(self):
vertices = \[i for i in range(5)\]
edges = \[
(0, 1),
(1, 2),
(3, 2),
(3, 4),
\]

        edge_config = {
            "stroke_width": 2,
            "tip_config": {"tip_length": 0, "tip_width": 0},
            (3, 4): {"color": RED},
        }

        g = DiGraph(
            vertices,
            edges,
            labels=True,
            layout="circular",
            edge_config=edge_config,
        ).scale(1.4)

        self.play(Create(g))
        self.wait()

        self.play(
            g\[1\].animate.move_to(\[1, 1, 1\]),
            g\[2\].animate.move_to(\[-1, 1, 2\]),
            g\[3\].animate.move_to(\[-1.5, -1.5, -1\]),
            g\[4\].animate.move_to(\[1, -2, -1\]),
        )
        self.wait()

Copy to clipboard

方法

[`update_edges`](#manim.mobject.graph.DiGraph.update_edges "manim.mobject.graph.DiGraph.update_edges")

更新边以粘在其相应的顶点。

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

update*edges（*图\_）[\[来源\]](../_modules/manim/mobject/graph.html#DiGraph.update_edges)[#](#manim.mobject.graph.DiGraph.update_edges "此定义的固定链接")

更新边以粘在其相应的顶点。

箭头尖端需要重新定位，否则它们可能会变形。
