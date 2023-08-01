# 多面体

合格名称：`manim.mobject.three\_d.polyhedra.Polyhedron`

多面体*类*（_vertex_coords_、 _faces_list_、 _faces_config = {}_、 _graph_config = {}_）[\[来源\]](../_modules/manim/mobject/three_d/polyhedra.html#Polyhedron)[#](#manim.mobject.three_d.polyhedra.Polyhedron "此定义的固定链接")

基地：[`VGroup`](manim.mobject.types.vectorized_mobject.VGroup.html#manim.mobject.types.vectorized_mobject.VGroup "manim.mobject.types.vectorized_mobject.VGroup")

一个抽象的多面体类。

在此实现中，多面体是通过空间中的顶点坐标列表和面列表来定义的。此实现反映了标准多面体数据格式（OFF，目标文件格式）的实现。

参数

- **vertex_coords** ( _list_ _\[_ _list_ _\[_ _float_ _\]_ _|_ _np.ndarray_ _\]_ ) – 多面体中相应顶点的坐标列表。每个坐标将对应一个顶点。顶点使用 Python 的常用索引进行索引。
- **faces_list** ( _list_ _\[_ _list_ _\[_ _int_ _\]_ _\]_ ) – 面孔列表。每个面都是一个子列表，其中包含形成该面角的顶点的索引。
- **faces_config** ( _dict_ _\[_ _str_ _,_ _str_ _|_ _int_ _|_ _float_ _|_ _bool_ _\]_ ) – 表示多面体面的多边形的配置。
- **graph_config** ( _dict_ _\[_ _str_ _,_ _str_ _|_ _int_ _|_ _float_ _|_ _bool_ _\]_ ) – 包含多面体的顶点和边的图的配置。

例子

为了了解如何创建自定义多面体，让我们使用一个相当简单的例子 \- 方形金字塔。

示例：SquarePyramidScene [¶](#squarepyramidscene)

![../_images/SquarePyramidScene-1.png](../_images/SquarePyramidScene-1.png)

from manim import \*

class SquarePyramidScene(ThreeDScene):
def construct(self):
self.set*camera_orientation(phi=75 * DEGREES, theta=30 \_ DEGREES)
vertex_coords = \[
\[1, 1, 0\],
\[1, -1, 0\],
\[-1, -1, 0\],
\[-1, 1, 0\],
\[0, 0, 2\]
\]
faces_list = \[
\[0, 1, 4\],
\[1, 2, 4\],
\[2, 3, 4\],
\[3, 0, 4\],
\[0, 1, 2, 3\]
\]
pyramid = Polyhedron(vertex_coords, faces_list)
self.add(pyramid)

Copy to clipboard

在定义上面的多面体时，我们首先定义了顶点的坐标。这些是正方形底边的角，以顶点列表中的前四个坐标给出，而顶点是列表中的最后一个坐标。

接下来，我们定义多面体的面。金字塔的三角面是以底边两个相邻顶点和顶点处的顶点为角的多边形。因此，我们在面列表的前四个元素中定义这些面。最后一个元素定义了金字塔的底部。

实例化后，多面体的图形和面也可以直接访问和修改。它们分别存储在 graph 和 faces 属性中。

示例：PolyhedronSubMobjects [¶](#polyhedronsubmobjects)

![../_images/PolyhedronSubMobjects-1.png](../_images/PolyhedronSubMobjects-1.png)

from manim import \*

class PolyhedronSubMobjects(ThreeDScene):
def construct(self):
self.set*camera_orientation(phi=75 * DEGREES, theta=30 \_ DEGREES)
octahedron = Octahedron(edge_length = 3)
octahedron.graph\[0\].set_color(RED)
octahedron.faces\[2\].set_color(YELLOW)
self.add(octahedron)

Copy to clipboard

方法

[`create_faces`](#manim.mobject.three_d.polyhedra.Polyhedron.create_faces "manim.mobject.two_d.polyhedra.Polyhedron.create_faces")

从面坐标列表创建面 VGroup。

[`extract_face_coords`](#manim.mobject.three_d.polyhedra.Polyhedron.extract_face_coords "manim.mobject.two_d.polyhedra.Polyhedron.extract_face_coords")

提取图中顶点的坐标。

[`get_edges`](#manim.mobject.three_d.polyhedra.Polyhedron.get_edges "manim.mobject.two_d.polyhedra.Polyhedron.get_edges")

创建循环成对元组列表。

`update_faces`

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

创建面（_面坐标_）[\[来源\]](../_modules/manim/mobject/three_d/polyhedra.html#Polyhedron.create_faces)[#](#manim.mobject.three_d.polyhedra.Polyhedron.create_faces "此定义的固定链接")

从面坐标列表创建面 VGroup。

参数

**face_coords** (_列表**\[**列表**\[**列表\_\_|_ _np.ndarray_ _\]_ _\]_ ) –

返回类型

[V 组](manim.mobject.types.vectorized_mobject.VGroup.html#manim.mobject.types.vectorized_mobject.VGroup "manim.mobject.types.vectorized_mobject.VGroup")

提取人脸坐标( )[\[来源\]](../_modules/manim/mobject/three_d/polyhedra.html#Polyhedron.extract_face_coords)[#](#manim.mobject.three_d.polyhedra.Polyhedron.extract_face_coords "此定义的固定链接")

提取图中顶点的坐标。用于更新面孔。

返回类型

列表\[列表\[np.ndarray\]\]

获取边（_faces_list_）[\[来源\]](../_modules/manim/mobject/three_d/polyhedra.html#Polyhedron.get_edges)[#](#manim.mobject.three_d.polyhedra.Polyhedron.get_edges "此定义的固定链接")

创建循环成对元组列表。

参数

**faces_list** (_列表**\[**列表\_\_\[_ _int_ _\]_ _\]_ ) –

返回类型

列表\[元组\[int, int\]\]
