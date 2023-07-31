# 图[#](#graph "此标题的固定链接")

合格名称：`manim.mobject.graph.Graph`

_类_ Graph (_顶点_,_边_, _labels=False_ , _label_fill_color='#000000'_ , _layout='spring'_ , _layout_scale=2_ , _layout_config=None_ , _vertex_type=<class 'manim.mobject.geometry.arc.Dot'>_ , _vertex_config =无_， _vertex_mobjects =无_， _edge_type = <类 'manim.mobject.geometry.line.Line'>_，_分区=无_， _root_vertex =无_， _edge_config =无_）[\[来源\]](../_modules/manim/mobject/graph.html#Graph)[#](#manim.mobject.graph.Graph "此定义的固定链接")

基地：[`GenericGraph`](manim.mobject.graph.GenericGraph.html#manim.mobject.graph.GenericGraph "manim.mobject.graph.GenericGraph")

无向图（顶点与边相连）。

该图带有一个更新器，可以使边缘在移动时粘在顶点上。请参阅[`DiGraph`](manim.mobject.graph.DiGraph.html#manim.mobject.graph.DiGraph "manim.mobject.graph.有向图")参考资料 以获得具有定向边缘的版本。

也可以看看

[`GenericGraph`](manim.mobject.graph.GenericGraph.html#manim.mobject.graph.GenericGraph "manim.mobject.graph.GenericGraph")

参数

- **vertices** ( _list_ _\[_ _Hashable_ _\]_ ) – 顶点列表。必须是可散列的元素。
- **Edges** ( _list_ _\[_ _tuple_ _\[_ _Hashable_ _,_ _Hashable_ _\]_ _\]_ ) – 边列表，指定为元组，其中 和 都是顶点。顶点顺序无关紧要。` (u, v)``u``v `
- **labels** ( _bool_ _|_ _dict_ ) – 控制是否标记顶点。如果`False`（默认），则不标记顶点；如果`True`他们使用其名称（如 中指定`vertices`）通过 进行标记[`MathTex`](manim.mobject.text.tex_mobject.MathTex.html#manim.mobject.text.tex_mobject.MathTex "manim.mobject.text.tex_mobject.MathTex")。或者，可以通过传递一个字典来指定自定义标签，该字典的键是顶点，其值是相应的顶点标签（通过例如 或 呈现[`Text`](manim.mobject.text.text_mobject.Text.html#manim.mobject.text.text_mobject.Text "manim.mobject.text.text_mobject.Text")）[`Tex`](manim.mobject.text.tex_mobject.Tex.html#manim.mobject.text.tex_mobject.Tex "manim.mobject.text.tex_mobject.Tex")。
- **label_fill_color** ( _str_`labels` ) – 设置设置为 时 生成的默认标签的填充颜色`True`。对 的其他值没有影响`labels`。
- **布局**( _str_ _|_ _dict_ ) – `"spring"`（默认）、`"circular"`、`"kamada_kawai"`、 `"planar"`、`"random"`、`"shell"`、`"spectral"`、`"spiral"`、`"tree"`和`"partite"` 用于自动顶点定位`networkx` （有关更多详细信息，请参阅[其文档](https://networkx.org/documentation/stable/reference/drawing.html#module-networkx.drawing.layout) ）或为每个顶点指定坐标（值）的字典之一（键）用于手动定位。
- **layout_config** ( _dict_ _|_ _None_ ) – 仅适用于自动生成的布局。`layout`一个字典，其条目作为关键字参数传递给通过 of 指定的自动布局算法`networkx`。布局还接受 作为字典内的关键字参数传递的`tree`特殊参数。传递一个元组作为此参数会覆盖 的值并确保顶点的排列方式使得同一层中同级的中心在水平方向上至少相距单位，并且相邻层在垂直方向上间隔单位。` vertex_spacing``layout_config``(space_x, space_y)``layout_scale``space_x``space_y `
- **layout_scale** ( _float_ _|_ _tuple_ ) – 自动生成的布局的比例：顶点将被排列，使得坐标位于区间内。某些布局接受一个元组， 导致第一个坐标位于 间隔 中，第二个坐标位于 中。默认值：2。` [-scale, scale]``(scale_x, scale_y)``[-scale_x, scale_x]``[-scale_y, scale_y] `
- **vertex_type** ( _type_ _\[_ [_Mobject_](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject") _\]_ ) – 用于在场景中显示顶点的 mobject 类。
- **vertex_config** ( _dict_ _|_ _None_ ) – 包含要传递给 via 指定的类的关键字参数的字典`vertex_type`，或者其键是顶点的字典，其值是包含与相应顶点相关的 mobject 的关键字参数的字典。
- **vertex_mobjects** ( _dict_ _|_ _None_ ) – 一个字典，其键是顶点，其值是用作顶点的 mobject。在此处传递顶点将覆盖顶点的所有其他配置选项。
- **edge_type** ( _type_ _\[_ [_Mobject_](manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject") _\]_ ) – 用于显示场景中边缘的 mobject 类。
- **edge_config** ( _dict_ _|_ _None_ ) – 包含要传递给 via 指定的类的关键字参数的字典`edge_type`，或者其键是边的字典，其值是包含与相应边相关的 mobject 的关键字参数的字典。
- **分区**( _list_ _\[_ _list_ _\[_ _Hashable_ _\]_ _\]_ _|_ _None_ ) –
- **root_vertex** ( _Hashable_ _|_ _None_ ) –

例子

首先，我们创建一个小图并演示边与顶点一起移动。

示例：移动顶点[¶](#movingvertices)

from manim import \*

class MovingVertices(Scene):
def construct(self):
vertices = \[1, 2, 3, 4\]
edges = \[(1, 2), (2, 3), (3, 4), (1, 3), (1, 4)\]
g = Graph(vertices, edges)
self.play(Create(g))
self.wait()
self.play(g\[1\].animate.move_to(\[1, 1, 0\]),
g\[2\].animate.move_to(\[-1, 1, 0\]),
g\[3\].animate.move_to(\[1, -1, 0\]),
g\[4\].animate.move_to(\[-1, -1, 0\]))
self.wait()

Copy to clipboard

有多种自动定位算法可供选择：

示例：GraphAutoPosition [¶](#graphautoposition)

![../_images/GraphAutoPosition-1.png](../_images/GraphAutoPosition-1.png)

from manim import \*

class GraphAutoPosition(Scene):
def construct(self):
vertices = \[1, 2, 3, 4, 5, 6, 7, 8\]
edges = \[(1, 7), (1, 8), (2, 3), (2, 4), (2, 5),
(2, 8), (3, 4), (6, 1), (6, 2),
(6, 3), (7, 2), (7, 4)\]
autolayouts = \["spring", "circular", "kamada_kawai",
"planar", "random", "shell",
"spectral", "spiral"\]
graphs = \[Graph(vertices, edges, layout=lt).scale(0.5)
for lt in autolayouts\]
r1 = VGroup(*graphs\[:3\]).arrange()
r2 = VGroup(*graphs\[3:6\]).arrange()
r3 = VGroup(\*graphs\[6:\]).arrange()
self.add(VGroup(r1, r2, r3).arrange(direction=DOWN))

Copy to clipboard

顶点也可以手动定位：

示例：GraphManualPosition [¶](#graphmanualposition)

![../_images/GraphManualPosition-1.png](../_images/GraphManualPosition-1.png)

from manim import \*

class GraphManualPosition(Scene):
def construct(self):
vertices = \[1, 2, 3, 4\]
edges = \[(1, 2), (2, 3), (3, 4), (4, 1)\]
lt = {1: \[0, 0, 0\], 2: \[1, 1, 0\], 3: \[1, -1, 0\], 4: \[-1, 0, 0\]}
G = Graph(vertices, edges, layout=lt)
self.add(G)

Copy to clipboard

可以对图中的顶点进行标记，并且可以默认修改顶点和边的配置以及特定顶点和边的配置。

笔记

在 中`edge_config`，边可以双向传递：如果 是图中的边，则和 都可以用作字典中的键。` (u, v)``(u, v)``(v, u) `

示例：LabeledModifiedGraph [¶](#labeledmodifiedgraph)

![../_images/LabeledModifiedGraph-1.png](../_images/LabeledModifiedGraph-1.png)

from manim import \*

class LabeledModifiedGraph(Scene):
def construct(self):
vertices = \[1, 2, 3, 4, 5, 6, 7, 8\]
edges = \[(1, 7), (1, 8), (2, 3), (2, 4), (2, 5),
(2, 8), (3, 4), (6, 1), (6, 2),
(6, 3), (7, 2), (7, 4)\]
g = Graph(vertices, edges, layout="circular", layout_scale=3,
labels=True, vertex_config={7: {"fill_color": RED}},
edge_config={(1, 7): {"stroke_color": RED},
(2, 7): {"stroke_color": RED},
(4, 7): {"stroke_color": RED}})
self.add(g)

Copy to clipboard

您还可以通过指定每边的顶点列表并选择分片布局，在列上布局分片图。

笔记

图中未在任何分区中列出的所有顶点都将收集在其自己的分区中并呈现在最右侧的列中。

示例：PartiteGraph [¶](#partitegraph)

![../_images/PartiteGraph-1.png](../_images/PartiteGraph-1.png)

from manim import \*

import networkx as nx

class PartiteGraph(Scene):
def construct(self):
G = nx.Graph()
G.add_nodes_from(\[0, 1, 2, 3\])
G.add_edges_from(\[(0, 2), (0,3), (1, 2)\])
graph = Graph(list(G.nodes), list(G.edges), layout="partite", partitions=\[\[0, 1\]\])
self.play(Create(graph))

Copy to clipboard

通过使用分区布局和为每一层定义分区，可以促进线性人工神经网络的表示。

示例：线性神经网络[¶](#linearnn)

![../_images/LinearNN-1.png](../_images/LinearNN-1.png)

from manim import \*

class LinearNN(Scene):
def construct(self):
edges = \[\]
partitions = \[\]
c = 0
layers = \[2, 3, 3, 2\] \# the number of neurons in each layer

        for i in layers:
            partitions.append(list(range(c + 1, c + i + 1)))
            c += i
        for i, v in enumerate(layers\[1:\]):
                last = sum(layers\[:i+1\])
                for j in range(v):
                    for k in range(last - layers\[i\], last):
                        edges.append((k + 1, j + last + 1))

        vertices = np.arange(1, sum(layers) + 1)

        graph = Graph(
            vertices,
            edges,
            layout='partite',
            partitions=partitions,
            layout_scale=3,
            vertex_config={'radius': 0.20},
        )
        self.add(graph)

Copy to clipboard

自定义树布局可用于按距根顶点的距离显示图形。您必须通过树的根顶点。

示例：树[¶](#tree)

from manim import \*

import networkx as nx

class Tree(Scene):
def construct(self):
G = nx.Graph()

        G.add_node("ROOT")

        for i in range(5):
            G.add_node("Child_%i" % i)
            G.add_node("Grandchild_%i" % i)
            G.add_node("Greatgrandchild_%i" % i)

            G.add_edge("ROOT", "Child_%i" % i)
            G.add_edge("Child_%i" % i, "Grandchild_%i" % i)
            G.add_edge("Grandchild_%i" % i, "Greatgrandchild_%i" % i)

        self.play(Create(
            Graph(list(G.nodes), list(G.edges), layout="tree", root_vertex="ROOT")))

Copy to clipboard

以下代码示例说明了`vertex_spacing` 特定于`"tree"`布局的布局参数的使用。如上所述，设置`vertex_spacing`会覆盖 的指定值`layout_scale`，因此更难控制 mobject 的大小。但是，我们可以使用以下命令调整捕获的帧并缩小[`MovingCameraScene`](manim.scene.moving_camera_scene.MovingCameraScene.html#manim.scene.moving_camera_scene.MovingCameraScene "manim.scene.movi​​ng_camera_scene.MovingCameraScene")：

class LargeTreeGeneration(MovingCameraScene):
DEPTH = 4
CHILDREN_PER_VERTEX = 3
LAYOUT_CONFIG = {"vertex_spacing": (0.5, 1)}
VERTEX_CONF = {"radius": 0.25, "color": BLUE_B, "fill_opacity": 1}

    def expand_vertex(self, g, vertex_id: str, depth: int):
        new_vertices = \[f"{vertex_id}/{i}" for i in range(self.CHILDREN\_PER\_VERTEX)\]
        new_edges = \[(vertex_id, child_id) for child_id in new_vertices\]
        g.add_edges(
            *new_edges,
            vertex_config=self.VERTEX_CONF,
            positions={
                k: g.vertices\[vertex_id\].get_center() + 0.1 * DOWN for k in new_vertices
            },
        )
        if depth < self.DEPTH:
            for child_id in new_vertices:
                self.expand_vertex(g, child_id, depth + 1)

        return g

    def construct(self):
        g = Graph(\["ROOT"\], \[\], vertex_config=self.VERTEX_CONF)
        g = self.expand_vertex(g, "ROOT", 1)
        self.add(g)

        self.play(
            g.animate.change_layout(
                "tree",
                root_vertex="ROOT",
                layout_config=self.LAYOUT_CONFIG,
            )
        )
        self.play(self.camera.auto_zoom(g, margin=1), run_time=0.5)

Copy to clipboard

方法

`update_edges`

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
