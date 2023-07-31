# 通用图[#](#genericgraph "此标题的固定链接")

合格名称：`manim.mobject.graph.GenericGraph`

_类_ GenericGraph (_顶点_,_边_, _labels=False_ , _label_fill_color='#000000'_ ,_布局='spring'_ , _layout_scale=2_ , _layout_config=None_ , _vertex_type=<class 'manim.mobject.geometry.arc.Dot'>_ , _vertex_config =无_， _vertex_mobjects =无_， _edge_type = <类 'manim.mobject.geometry.line.Line'>_，_分区=无_， _root_vertex =无_， _edge_config =无_）[\[来源\]](../_modules/manim/mobject/graph.html#GenericGraph)[#](#manim.mobject.graph.GenericGraph "此定义的固定链接")

基地：[`VMobject`](manim.mobject.types.vectorized_mobject.VMobject.html#manim.mobject.types.vectorized_mobject.VMobject "manim.mobject.types.vectorized_mobject.VMobject")

图的抽象基类（即与边连接的顶点的集合）。

可以通过传递（不同的、可散列的）顶点名称列表和边列表（作为顶点名称的元组）来实例化图。详细信息请参见该类的具体实现示例。

笔记

此实现使用更新器使边随顶点移动。

也可以看看

[`Graph`](manim.mobject.graph.Graph.html#manim.mobject.graph.Graph "manim.mobject.graph.Graph"),[`DiGraph`](manim.mobject.graph.DiGraph.html#manim.mobject.graph.DiGraph "manim.mobject.graph.有向图")

参数

- **vertices** ( _list_ _\[_ _Hashable_ _\]_ ) – 顶点列表。必须是可散列的元素。
- **Edges** ( _list_ _\[_ _tuple_ _\[_ _Hashable_ _,_ _Hashable_ _\]_ _\]_ ) – 边列表，指定为元组，其中 和 都是顶点。` (u, v)``u``v `
- **labels** ( _bool_ _|_ _dict_ ) – 控制是否标记顶点。如果`False`（默认），则不标记顶点；如果`True`他们使用其名称（如 中指定`vertices`）通过 进行标记[`MathTex`](manim.mobject.text.tex_mobject.MathTex.html#manim.mobject.text.tex_mobject.MathTex "manim.mobject.text.tex_mobject.MathTex")。或者，可以通过传递一个字典来指定自定义标签，该字典的键是顶点，其值是相应的顶点标签（通过例如 或 呈现[`Text`](manim.mobject.text.text_mobject.Text.html#manim.mobject.text.text_mobject.Text "manim.mobject.text.text_mobject.Text")）[`Tex`](manim.mobject.text.tex_mobject.Tex.html#manim.mobject.text.tex_mobject.Tex "manim.mobject.text.tex_mobject.Tex")。
- **label_fill_color** ( _str_`labels` ) – 设置设置为 时 生成的默认标签的填充颜色`True`。对 的其他值没有影响`labels`。
- **布局**( _str_ _|_ _dict_ ) – `"spring"`（默认）、`"circular"`、`"kamada_kawai"`、 `"planar"`、`"random"`、`"shell"`、`"spectral"`、`"spiral"`、`"tree"`和`"partite"` 用于自动顶点定位`networkx` （有关更多详细信息，请参阅[其文档](https://networkx.org/documentation/stable/reference/drawing.html#module-networkx.drawing.layout) ）或为每个顶点指定坐标（值）的字典之一（键）用于手动定位。
- **layout_config** ( _dict_ _|_ _None_ ) – 仅适用于自动生成的布局。一个字典，其条目作为关键字参数传递给通过 of\`\`networkx\`\` 指定的自动布局算法`layout`。布局还接受 作为字典内的关键字参数传递的`tree`特殊参数。传递一个元组作为此参数会覆盖 的值并确保顶点的排列方式使得同一层中同级的中心在水平方向上至少相距单位，并且相邻层在垂直方向上间隔单位。` vertex_spacing``layout_config``(space_x, space_y)``layout_scale``space_x``space_y `
- **layout_scale** ( _float_ _|_ _tuple_ ) – 自动生成的布局的比例：顶点将被排列，使得坐标位于区间内。某些布局接受一个元组， 导致第一个坐标位于 间隔 中，第二个坐标位于 中。默认值：2。` [-scale, scale]``(scale_x, scale_y)``[-scale_x, scale_x]``[-scale_y, scale_y] `
- **vertex_type** ( _type_ _\[_ [_Mobject_](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject") _\]_ ) – 用于在场景中显示顶点的 mobject 类。
- **vertex_config** ( _dict_ _|_ _None_ ) – 包含要传递给 via 指定的类的关键字参数的字典`vertex_type`，或者其键是顶点的字典，其值是包含与相应顶点相关的 mobject 的关键字参数的字典。
- **vertex_mobjects** ( _dict_ _|_ _None_ ) – 一个字典，其键是顶点，其值是用作顶点的 mobject。在此处传递顶点将覆盖顶点的所有其他配置选项。
- **edge_type** ( _type_ _\[_ [_Mobject_](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject") _\]_ ) – 用于显示场景中边缘的 mobject 类。
- **edge_config** ( _dict_ _|_ _None_ ) – 包含要传递给 via 指定的类的关键字参数的字典`edge_type`，或者其键是边的字典，其值是包含与相应边相关的 mobject 的关键字参数的字典。
- **分区**( _list_ _\[_ _list_ _\[_ _Hashable_ _\]_ _\]_ _|_ _None_ ) –
- **root_vertex** ( _Hashable_ _|_ _None_ ) –

方法

[`add_edges`](#manim.mobject.graph.GenericGraph.add_edges "manim.mobject.graph.GenericGraph.add_edges")

向图中添加新边。

[`add_vertices`](#manim.mobject.graph.GenericGraph.add_vertices "manim.mobject.graph.GenericGraph.add_vertices")

将顶点列表添加到图形中。

[`change_layout`](#manim.mobject.graph.GenericGraph.change_layout "manim.mobject.graph.GenericGraph.change_layout")

更改此图表的布局。

[`from_networkx`](#manim.mobject.graph.GenericGraph.from_networkx "manim.mobject.graph.GenericGraph.from_networkx")

从给定的图表构建一个[`Graph`](manim.mobject.graph.Graph.html#manim.mobject.graph.Graph "manim.mobject.graph.Graph")或。[`DiGraph`](manim.mobject.graph.DiGraph.html#manim.mobject.graph.DiGraph "manim.mobject.graph.有向图")`networkx`

[`remove_edges`](#manim.mobject.graph.GenericGraph.remove_edges "manim.mobject.graph.GenericGraph.remove_edges")

从图中删除几条边。

[`remove_vertices`](#manim.mobject.graph.GenericGraph.remove_vertices "manim.mobject.graph.GenericGraph.remove_vertices")

从图中删除几个顶点。

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

add*edges（*\*edges*， \_edge_type=< class'manim.mobject.geometry.line.Line'>*， _edge_config=None_， _\*\*kwargs_）[\[来源\]](../_modules/manim/mobject/graph.html#GenericGraph.add_edges)[#](#manim.mobject.graph.GenericGraph.add_edges "此定义的固定链接")

向图中添加新边。

参数

- **Edges** ( _tuple_ _\[_ _Hashable_ _,_ _Hashable_ _\]_ ) – 要添加的边（作为顶点标识符的元组）。如果传递了一个不存在的顶点，则会创建一个具有默认设置的新顶点。事先自己创建新顶点来自定义它们。
- **edge_type** ( _type_ _\[_ [_Mobject_](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject") _\]_ ) – 用于显示场景中边缘的 mobject 类。
- **edge_config** ( _dict_ _|_ _None_ ) – 包含要传递给 via 指定的类的关键字参数的字典`edge_type`，或者其键是边元组的字典，其值是包含要传递用于构造相应边的关键字参数的字典。
- **kwargs** – 任何进一步的关键字参数都会传递给它[`add_vertices()`](#manim.mobject.graph.GenericGraph.add_vertices "manim.mobject.graph.GenericGraph.add_vertices") ，用于在传递的边中创建新顶点。

退货

包含所有新添加的顶点和边的组。

返回类型

[团体](manim.mobject.mobject.Group.html#manim.mobject.mobject.Group "manim.mobject.mobject.Group")

add*vertices ( *\*vertices* , \_Positions=None* , _labels=False_ , _label_fill_color='#000000'_ , _vertex_type=<class 'manim.mobject.geometry.arc.Dot'>_ , _vertex_config=None_ , _vertex_mobjects=None_ )[\[来源\]](../_modules/manim/mobject/graph.html#GenericGraph.add_vertices)[#](#manim.mobject.graph.GenericGraph.add_vertices "此定义的固定链接")

将顶点列表添加到图形中。

参数

- **vertices** ( _Hashable_ ) – 可哈希顶点标识符。
- **Positions** ( _dict_ _|_ _None_ ) – 一个字典，指定应添加新顶点的坐标。如果`None`，则所有顶点都创建在图的中心。
- **labels** ( _bool_ ) – 控制顶点是否被标记。如果`False`（默认），则顶点不被标记；如果`True`使用其名称（如 中指定`vertex`）通过 进行标记[`MathTex`](manim.mobject.text.tex_mobject.MathTex.html#manim.mobject.text.tex_mobject.MathTex "manim.mobject.text.tex_mobject.MathTex")。或者，[`Mobject`](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject")可以传递 any 来用作标签。
- **label_fill_color** ( _str_`labels` ) – 设置设置为 时 生成的默认标签的填充颜色`True`。对 的其他值没有影响`labels`。
- **vertex_type** ( _type_ _\[_ [_Mobject_](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject") _\]_ ) – 用于在场景中显示顶点的 mobject 类。
- **vertex_config** ( _dict_ _|_ _None_ ) – 包含要传递给通过指定的类的关键字参数的字典`vertex_type`。
- **vertex_mobjects** ( _dict_ _|_ _None_ ) – 一个字典，其键是顶点标识符，其值是应用作顶点的 mobject。覆盖所有其他顶点自定义选项。
- **自我**（[_图_](manim.mobject.graph.Graph.html#manim.mobject.graph.Graph "manim.mobject.graph.Graph")）-

change*layout（*布局= 'spring'_， \_layout_scale = 2_， _layout_config = None_，_分区= None_， _root_vertex = None_）[\[来源\]](../_modules/manim/mobject/graph.html#GenericGraph.change_layout)[#](#manim.mobject.graph.GenericGraph.change_layout "此定义的固定链接")

更改此图表的布局。

[`Graph`](manim.mobject.graph.Graph.html#manim.mobject.graph.Graph "manim.mobject.graph.Graph")有关关键字参数的详细信息，请参阅 的文档。

例子

示例：更改 GraphLayout [¶](#changegraphlayout)

from manim import \*

class ChangeGraphLayout(Scene):
def construct(self):
G = Graph(\[1, 2, 3, 4, 5\], \[(1, 2), (2, 3), (3, 4), (4, 5)\],
layout={1: \[-2, 0, 0\], 2: \[-1, 0, 0\], 3: \[0, 0, 0\],
4: \[1, 0, 0\], 5: \[2, 0, 0\]}
)
self.play(Create(G))
self.play(G.animate.change_layout("circular"))
self.wait()

Copy to clipboard

参数

- **布局**( _str_ _|_ _dict_ ) –
- **布局比例**（_浮动_）-
- **布局配置**(_字典**|**无_) –
- **分区**( _list_ _\[_ _list_ _\[_ _Hashable_ _\]_ _\]_ _|_ _None_ ) –
- **root_vertex** ( _Hashable_ _|_ _None_ ) –

返回类型

[图形](manim.mobject.graph.Graph.html#manim.mobject.graph.Graph "manim.mobject.graph.Graph")

_类方法_ from*networkx ( \_nxgraph* , _\*\* kwargs_ )[\[来源\]](../_modules/manim/mobject/graph.html#GenericGraph.from_networkx)[#](#manim.mobject.graph.GenericGraph.from_networkx "此定义的固定链接")

从给定的图表构建一个[`Graph`](manim.mobject.graph.Graph.html#manim.mobject.graph.Graph "manim.mobject.graph.Graph")或。[`DiGraph`](manim.mobject.graph.DiGraph.html#manim.mobject.graph.DiGraph "manim.mobject.graph.有向图")`networkx`

参数

- **nxgraph** ( _nx.classes.graph.Graph_ _|_ _nx.classes.digraph.DiGraph_ ) –`networkx`图或有向图。
- \***\*kwargs** – 要传递给 的构造函数的关键字[`Graph`](manim.mobject.graph.Graph.html#manim.mobject.graph.Graph "manim.mobject.graph.Graph")。

例子

示例：导入网络 xGraph [¶](#importnetworkxgraph)

from manim import \*

import networkx as nx

nxgraph = nx.erdos_renyi_graph(14, 0.5)

class ImportNetworkxGraph(Scene):
def construct(self):
G = Graph.from_networkx(nxgraph, layout="spring", layout_scale=3.5)
self.play(Create(G))
self.play(*\[G\[v\].animate.move_to(5*RIGHT*np.cos(ind/7 * PI) +
3*UP*np.sin(ind/7 \* PI))
for ind, v in enumerate(G.vertices)\])
self.play(Uncreate(G))

Copy to clipboard

删除边缘（_\*边缘_）[\[来源\]](../_modules/manim/mobject/graph.html#GenericGraph.remove_edges)[#](#manim.mobject.graph.GenericGraph.remove_edges "此定义的固定链接")

从图中删除几条边。

参数

**Edges** ( _tuple_ _\[_ _Hashable_ _\]_ ) – 要从图中删除的边。

退货

包含所有已移除边的组。

返回类型

[团体](manim.mobject.mobject.Group.html#manim.mobject.mobject.Group "manim.mobject.mobject.Group")

删除顶点（_\*顶点_）[\[来源\]](../_modules/manim/mobject/graph.html#GenericGraph.remove_vertices)[#](#manim.mobject.graph.GenericGraph.remove_vertices "此定义的固定链接")

从图中删除几个顶点。

参数

**vertices** – 要从图中删除的顶点。

例子

> > \> G = Graph(\[1, 2, 3\], \[(1, 2), (2, 3)\])
> > \> removed = G.remove_vertices(2, 3); removed
> > VGroup(Line, Line, Dot, Dot)
> > \> G
> > Undirected graph on 1 vertices and 0 edges

Copy to clipboard
