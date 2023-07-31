# 点[#](#point "此标题的固定链接")

合格名称：`manim.mobject.types.point\_cloud\_mobject.Point`

_类_ Point (_位置= array(\[0., 0., 0.\])_ ,_颜色= '#000000'_ , _\*\* kwargs_ )[\[来源\]](../_modules/manim/mobject/types/point_cloud_mobject.html#Point)[#](#manim.mobject.types.point_cloud_mobject.Point "此定义的固定链接")

基地：[`PMobject`](manim.mobject.types.point_cloud_mobject.PMobject.html#manim.mobject.types.point_cloud_mobject.PMobject "manim.mobject.types.point_cloud_mobject.PMobject")

例子

示例：示例点[¶](#examplepoint)

![../_images/ExamplePoint-1.png](../_images/ExamplePoint-1.png)

from manim import \*

class ExamplePoint(Scene):
def construct(self):
colorList = \[RED, GREEN, BLUE, YELLOW\]
for i in range(200):
point = Point(location=\[0.63 _ np.random.randint(-4, 4), 0.37 _ np.random.randint(-4, 4), 0\], color=np.random.choice(colorList))
self.add(point)
for i in range(200):
point = Point(location=\[0.37 _ np.random.randint(-4, 4), 0.63 _ np.random.randint(-4, 4), 0\], color=np.random.choice(colorList))
self.add(point)
self.add(point)

Copy to clipboard

方法

[`generate_points`](#manim.mobject.types.point_cloud_mobject.Point.generate_points "manim.mobject.types.point_cloud_mobject.Point.generate_points")

初始化`points`并因此初始化形状。

`init_points`

属性

`animate`

用于对 的任何方法的应用程序进行动画处理`self`。

`animation_overrides`

`depth`

对象的深度。

`height`

mobject 的高度。

`width`

mobject 的宽度。

生成点( )[\[来源\]](../_modules/manim/mobject/types/point_cloud_mobject.html#Point.generate_points)[#](#manim.mobject.types.point_cloud_mobject.Point.generate_points "此定义的固定链接")

初始化`points`并因此初始化形状。

被创造召唤。这是一个空方法，可以由子类实现。
