# 快速入门

> 笔记

> [在继续之前，请按照安装](../installation.html)中的步骤安装 Manim 并确保其正常运行。有关将 Manim 与 Jupyterlab 或 Jupyter Notebook 结合使用的信息，请参阅、 的文档 。[`IPython magic command`](../reference/manim.utils.ipython_magic.ManimMagic.html#manim.utils.ipython_magic.ManimMagic.manim "manim.utils.ipython_magic.ManimMagic.manim")`%%manim`

## 概述

本快速入门指南将引导您使用 Manim 创建示例项目：用于精确编程动画的动画引擎。

首先，您将使用命令行界面创建一个`Scene`Manim 生成视频的类。在 中，`Scene`您将为一个圆圈设置动画。然后，您将添加另一个`Scene`显示正方形转变为圆形的内容。这将向您介绍 Manim 的动画能力。然后，您将定位多个数学对象`Mobject`。最后，您将学习`.animate`语法，这是一个强大的功能，可以动画化您用来修改 s 的方法`Mobject`。

## 开始一个新项目

首先创建一个新文件夹。为了本指南的目的，将该文件夹命名为`project`：

```sh
project/
```

该文件夹是您项目的根文件夹。它包含 Manim 运行所需的所有文件，以及您的项目产生的任何输出。

## 为圆制作动画

1.  打开文本编辑器，例如记事本。将以下代码片段复制到窗口中：

```py
from manim import *


class CreateCircle(Scene):
    def construct(self):
        circle = Circle()  # create a circle
        circle.set_fill(PINK, opacity=0.5)  # set the color and transparency
        self.play(Create(circle))  # show the circle on screen
```

2.  将代码片段保存到您的项目文件夹中，名称为`scene.py`.

```sh
project/
└─scene.py
```

3. 打开命令行，导航到项目文件夹，然后执行以下命令：

```sh
manim -pql scene.py CreateCircle
```

Manim 将输出渲染信息，然后创建 MP4 文件。您的默认电影播放器 ​​ 将播放 MP4 文件，并显示以下动画。

[![视频缩略图]()](https://docs.manim.community/en/stable/tutorials/CreateCircle-1.mp4)

<iframe src="https://docs.manim.community/en/stable/tutorials/CreateCircle-1.mp4"></iframe>


如果您看到绘制粉红色圆圈的动画，那么恭喜您！您刚刚从头开始编写了第一个 Manim 场景。

如果您收到错误消息，看不到视频，或者视频输出看起来不像前面的动画，则很可能 Manim 尚未正确安装。请参阅我们的[常见问题解答部分](../faq/index.html) ，获取有关最常见问题的帮助。

### 解释

让我们逐行查看刚刚执行的脚本，看看 Manim 如何绘制圆圈。

第一行导入库的所有内容：

```py
from manim import *
```

这是使用 Manim 的推荐方式，因为单个脚本通常使用 Manim 命名空间中的多个名称。在您的脚本中，您导入并使用了 `Scene`、`Circle`、`PINK`和`Create`。

现在让我们看看接下来的两行：

```py
class CreateCircle(Scene):
    def construct(self):
        ...
```

大多数时候，编写动画脚本的代码完全包含在类[`construct()`](../reference/manim.scene.scene.Scene.html#manim.scene.scene.Scene.construct "manim.scene.scene.Scene.construct")的方法中[`Scene`](../reference/manim.scene.scene.Scene.html#manim.scene.scene.Scene "手动场景.场景.场景")。在里面[`construct()`](../reference/manim.scene.scene.Scene.html#manim.scene.scene.Scene.construct "manim.scene.scene.Scene.construct")，您可以创建对象，将它们显示在屏幕上，并为它们设置动画。

接下来的两行创建一个圆圈并设置其颜色和不透明度：

```py
circle = Circle()  # create a circle
circle.set_fill(PINK, opacity=0.5)  # set the color and transparency
```

最后，最后一行使用动画[`Create`](../reference/manim.animation.creation.Create.html#manim.animation.creation.Create "manim.animation.creation.Create")在屏幕上显示圆圈：

```py
self.play(Create(circle))  # show the circle on screen
```

> 提示

> 所有动画必须驻留在[`construct()`](../reference/manim.scene.scene.Scene.html#manim.scene.scene.Scene.construct "manim.scene.scene.Scene.construct")派生自 的类的方法中[`Scene`](../reference/manim.scene.scene.Scene.html#manim.scene.scene.Scene "手动场景.场景.场景")。其他代码（例如辅助函数或数学函数）可能驻留在类之外。

## 将正方形变成圆形

圆形动画完成后，让我们继续处理一些更复杂的事情。

1.  打开`scene.py`，并在类下方添加以下代码片段`CreateCircle`：

```py
class SquareToCircle(Scene):
    def construct(self):
        circle = Circle()  # create a circle
        circle.set_fill(PINK, opacity=0.5)  # set color and transparency

        square = Square()  # create a square
        square.rotate(PI / 4)  # rotate a certain amount

        self.play(Create(square))  # animate the creation of the square
        self.play(Transform(square, circle))  # interpolate the square into the circle
        self.play(FadeOut(square))  # fade out animation
```

2.  `SquareToCircle`通过在命令行中运行以下命令进行渲染：

```sh
manim -pql scene.py SquareToCircle
```

将呈现以下动画：

[![视频缩略图]()](https://docs.manim.community/en/stable/tutorials/SquareToCircle2-1.mp4)

<iframe src="https://docs.manim.community/en/stable/tutorials/SquareToCircle2-1.mp4"></iframe>

此示例展示了 Manim 的主要功能之一：只需几行代码即可实现复杂且数学密集型动画（例如在两个几何形状之间干净地插值）的能力。

## 定位`Mobject`s

接下来，让我们回顾一下定位的一些基本技巧`Mobject`。

1.  打开`scene.py`，并在方法下方添加以下代码片段`SquareToCircle`：

```py
class SquareAndCircle(Scene):
    def construct(self):
        circle = Circle()  # create a circle
        circle.set_fill(PINK, opacity=0.5)  # set the color and transparency

        square = Square()  # create a square
        square.set_fill(BLUE, opacity=0.5)  # set the color and transparency

        square.next_to(circle, RIGHT, buff=0.5)  # set the position
        self.play(Create(circle), Create(square))  # show the shapes on screen
```

2.  `SquareAndCircle`通过在命令行中运行以下命令进行渲染：

```sh
manim -pql scene.py SquareAndCircle
```

将呈现以下动画：

[![视频缩略图]()](https://docs.manim.community/en/stable/tutorials/SquareAndCircle2-1.mp4)

<iframe src="https://docs.manim.community/en/stable/tutorials/SquareAndCircle2-1.mp4"></iframe>

`next_to`是一种`Mobject`定位`Mobject`s 的方法。

我们首先通过传递该方法的第一个参数来指定粉红色圆圈作为正方形的参考点`circle`。第二个参数用于指定`Mobject`相对于参考点的放置方向。在本例中，我们将方向设置为`RIGHT`，告诉 Manim 将正方形放置在圆的右侧。最后，`buff=0.5`在两个对象之间应用一个小距离缓冲区。

尝试改为`RIGHT`、`LEFT`、`UP`或`DOWN`，看看它如何改变正方形的位置。

使用定位方法，您可以渲染具有多个 s 的场景`Mobject`，使用坐标设置它们在场景中的位置或相对于彼此定位它们。

有关定位方法和其他定位方法的更多信息，请查看我们的参考手册中的方法`next_to`列表。[`Mobject`](../reference/manim.mobject.mobject.Mobject.html#manim.mobject.mobject.Mobject "manim.mobject.mobject.Mobject")

## 使用`.animate`语法到动画方法

本教程的最后一课是使用`.animate`一种`Mobject`方法，以动画方式对`Mobject`. 当您添加`.animate`到任何修改 a 的方法调用之前时`Mobject`，该方法将变成可以使用 播放的动画`self.play`。让我们回过头来`SquareToCircle`看看创建 时使用方法`Mobject`和使用 来动画这些方法调用之间的区别`.animate`。

1.  打开`scene.py`，并在类下方添加以下代码片段`SquareAndCircle`：

```py
class AnimatedSquareToCircle(Scene):
    def construct(self):
        circle = Circle()  # create a circle
        square = Square()  # create a square

        self.play(Create(square))  # show the square on screen
        self.play(square.animate.rotate(PI / 4))  # rotate the square
        self.play(
            ReplacementTransform(square, circle)
        )  # transform the square into a circle
        self.play(
            circle.animate.set_fill(PINK, opacity=0.5)
        )  # color the circle on screen
```

2. 通过在命令行中运行以下命令来渲染 `AnimatedSquareToCircle`：

```sh
manim -pql scene.py AnimatedSquareToCircle
```

将呈现以下动画：

[![视频缩略图]()](https://docs.manim.community/en/stable/tutorials/AnimatedSquareToCircle2-1.mp4)

<iframe src="https://docs.manim.community/en/stable/tutorials/AnimatedSquareToCircle2-1.mp4"></iframe>

第一个`self.play`创建正方形。第二个动画将其旋转 45 度。第三个将正方形变成圆形，最后一个将圆形涂成粉红色。尽管最终结果与 的结果相同`SquareToCircle`，`.animate`但显示 `rotate`并动态`set_fill`应用于`Mobject`，而不是使用已应用的更改来创建它们。

尝试其他方法，例如`flip`或`shift`，看看会发生什么。

3.  打开`scene.py`，并在类下方添加以下代码片段`AnimatedSquareToCircle`：

```py
class DifferentRotations(Scene):
    def construct(self):
        left_square = Square(color=BLUE, fill_opacity=0.7).shift(2 * LEFT)
        right_square = Square(color=GREEN, fill_opacity=0.7).shift(2 * RIGHT)
        self.play(
            left_square.animate.rotate(PI), Rotate(right_square, angle=PI), run_time=2
        )
        self.wait()
```

4. 通过在命令行中运行以下命令来渲染 `DifferentRotations`：

```sh
manim -pql scene.py DifferentRotations
```

将呈现以下动画：

[![视频缩略图]()](https://docs.manim.community/en/stable/tutorials/DifferentRotations2-1.mp4)

<iframe src="https://docs.manim.community/en/stable/tutorials/DifferentRotations2-1.mp4"></iframe>

这`Scene`说明了 的怪癖`.animate`。使用时`.animate`，Manim 实际上采用 a`Mobject`的起始状态和结束状态并对两者进行插值。在课堂上`AnimatedSquareToCircle`，您可以在正方形旋转时观察到这一点：当正方形的角移动到第一个正方形转变为第二个正方形所需的位置时，它们似乎会稍微收缩。

在 中，旋转的解释和 方法`DifferentRotations`之间的差异更加明显。旋转 360 度的开始和结束状态是相同的，因此尝试对两个相同的对象进行插值，结果是左边的正方形。如果您发现自己的使用导致了类似的不需要的行为，请考虑使用传统的动画方法，例如右方块，它使用.` .animate``Rotate``Mobject``.animate``.animate``Rotate `

### 你完成了！

有了 Manim 的工作安装和这个示例项目，您就可以开始创建自己的动画了。要了解有关 Manim 幕后功能的更多信息，请继续学习下一个教程： [Manim 的输出设置](output_and_config.html)。有关 Manim 功能及其配置和其他设置的概述，请查看其他[教程](index.html)。有关所有可用功能的列表，请参阅 [参考手册](../reference.html)页面。
