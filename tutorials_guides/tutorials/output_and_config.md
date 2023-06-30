# Manim 的输出设置

本文档将重点了解 manim 的输出文件和一些可用的主要命令行标志。

> 笔记

> 本教程将从[快速入门](./quickstart.md)停止的地方继续，因此请在开始本教程之前阅读该文档。

## Manim 输出文件夹

此时，您刚刚执行了以下命令。

```sh
manim -pql scene.py SquareToCircle
```

让我们一步步剖析刚刚发生的事情。首先，此命令对文件执行 manim `scene.py`，其中包含我们的动画代码。此外，该命令准确地告诉 manim`Scene`要渲染哪个，在本例中是`SquareToCircle`。这是必要的，因为单个场景文件可能包含多个场景。接下来，标志-p 告诉 manim 在渲染场景后播放场景，而-ql 标志告诉 manim 以低质量渲染场景。

视频渲染后，您将看到 manim 生成了一些新文件，项目文件夹如下所示。

```sh
project/
├─scene.py
└─media
  ├─videos
  |  └─scene
  |     └─480p15
  |        ├─SquareToCircle.mp4
  |        └─partial_movie_files
  ├─text
  └─Tex
```

有相当多的新文件。主要输出在 `media/videos/scene/480p15/SquareToCircle.mp4`. 默认情况下，该`media` 文件夹将包含 manim 的所有输出文件。该`media/videos` 子文件夹包含渲染的视频。在其中，您会发现每种不同视频质量都有一个文件夹。在我们的例子中，由于我们使用了该`-l`标志，因此视频是从 `scene.py`文件中以 480 分辨率、每秒 15 帧的速度生成的。因此，输出可以在里面找到 `media/videos/scene/480p15`。其他文件夹 `media/videos/scene/480p15/partial_movie_files`以及`media/text`包含 `media/Tex`manim 内部使用的文件。

您可以通过执行以下命令来查看 manim 如何使用生成的文件夹结构：

```sh
manim -pqh scene.py SquareToCircle
```

标志 `-ql`（低质量）已被`-qh` 标志取代，高品质。Manim 将花费相当长的时间来渲染此文件，并且一旦完成就会播放它，因为我们正在使用该`-p`标志。输出应如下所示：

[![视频缩略图]()](https://docs.manim.community/en/stable/tutorials/SquareToCircle3-1.mp4)

<iframe src="https://docs.manim.community/en/stable/tutorials/SquareToCircle3-1.mp4"></iframe>

文件夹结构应如下所示。

```sh
project/
├─scene.py
└─media
  ├─videos
  | └─scene
  |   ├─480p15
  |   | ├─SquareToCircle.mp4
  |   | └─partial_movie_files
  |   └─1080p60
  |     ├─SquareToCircle.mp4
  |     └─partial_movie_files
  ├─text
  └─Tex
```

Manim 新建了一个文件夹`media/videos/1080p60`，对应高分辨率和每秒 60 帧。在其中，您可以找到新的`SquareToCircle.mp4`以及相应的 `partial_movie_files`.

当处理具有多个场景的项目并尝试多种分辨率时，输出目录的结构将使您的所有视频保持井井有条。

此外，在添加标志时，manim 可以选择输出场景的最后一帧`-s`。这是快速预览场景的最快选项。对应的文件夹结构如下所示：

```sh
project/
├─scene.py
└─media
  ├─images
  | └─scene
  |   ├─SquareToCircle.png
  ├─videos
  | └─scene
  |   ├─480p15
  |   | ├─SquareToCircle.mp4
  |   | └─partial_movie_files
  |   └─1080p60
  |     ├─SquareToCircle.mp4
  |     └─partial_movie_files
  ├─text
  └─Tex
```

保存最后一帧`-s`可以与不同分辨率的标志相结合，例如，` -s -ql``-s -qh `

## 章节

除了电影输出文件之外，还可以使用节。每个部分都会产生自己的输出视频。两个部分之间的剪切可以这样设置：

```py
def construct(self):
    # play the first animations...
    # you don't need a section in the very beginning as it gets created automatically
    self.next_section()
    # play more animations...
    self.next_section("this is an optional name that doesn't have to be unique")
    # play even more animations...
    self.next_section("this is a section without any animations, it will be removed")
```

其中两个剪辑之间的所有动画都会连接到一个输出视频文件中。请注意，每个部分至少需要一个动画。例如，这不会创建输出视频：

```py
def construct(self):
    self.next_section()
    # this section doesn't have any animations and will be removed
    # but no error will be thrown
    # feel free to tend your flock of empty sections if you so desire
    self.add(Circle())
    self.next_section()
```

解决这个问题的一种方法是稍等一下：

```py
def construct(self):
    self.next_section()
    self.add(Circle())
    # now we wait 1sec and have an animation to satisfy the section
    self.wait()
    self.next_section()
```

对于要为每个部分创建的视频，您必须将标志添加`--save_sections`到 Manim 调用中，如下所示：

```sh
manim --save_sections scene.py
```

如果这样做，该`media`文件夹将如下所示：

```sh
media
├── images
│   └── simple_scenes
└── videos
    └── simple_scenes
        └── 480p15
            ├── ElaborateSceneWithSections.mp4
            ├── partial_movie_files
            │   └── ElaborateSceneWithSections
            │       ├── 2201830969_104169243_1331664314.mp4
            │       ├── 2201830969_398514950_125983425.mp4
            │       ├── 2201830969_398514950_3447021159.mp4
            │       ├── 2201830969_398514950_4144009089.mp4
            │       ├── 2201830969_4218360830_1789939690.mp4
            │       ├── 3163782288_524160878_1793580042.mp4
            │       └── partial_movie_file_list.txt
            └── sections
                ├── ElaborateSceneWithSections_0000.mp4
                ├── ElaborateSceneWithSections_0001.mp4
                ├── ElaborateSceneWithSections_0002.mp4
                └── ElaborateSceneWithSections.json
```

正如您所看到的，每个部分都会在目录中接收自己的输出视频`sections`。此处的 JSON 文件包含每个部分的一些有用信息：

```json
[
    {
        "name": "create square",
        "type": "default.normal",
        "video": "ElaborateSceneWithSections_0000.mp4",
        "codec_name": "h264",
        "width": 854,
        "height": 480,
        "avg_frame_rate": "15/1",
        "duration": "2.000000",
        "nb_frames": "30"
    },
    {
        "name": "transform to circle",
        "type": "default.normal",
        "video": "ElaborateSceneWithSections_0001.mp4",
        "codec_name": "h264",
        "width": 854,
        "height": 480,
        "avg_frame_rate": "15/1",
        "duration": "2.000000",
        "nb_frames": "30"
    },
    {
        "name": "fade out",
        "type": "default.normal",
        "video": "ElaborateSceneWithSections_0002.mp4",
        "codec_name": "h264",
        "width": 854,
        "height": 480,
        "avg_frame_rate": "15/1",
        "duration": "2.000000",
        "nb_frames": "30"
    }
]
```

这些数据可供第三方应用程序使用，例如演示系统或自动视频编辑工具。

您还可以跳过渲染属于某个部分的所有动画，如下所示：

```py
def construct(self):
    self.next_section(skip_animations=True)
    # play some animations that shall be skipped...
    self.next_section()
    # play some animations that won't get skipped...
```

## 一些命令行标志

执行命令时

```sh
manim -pql scene.py SquareToCircle
```

有必要指定`Scene`要呈现哪个类。这是因为单个文件可以包含多个`Scene`类。如果您的文件包含多个`Scene`类，并且您想要渲染所有类，则可以使用该 `-a`标志。

如前所述，`-ql`指定了低渲染质量。这看起来不太好，但是对于快速原型设计和测试非常有用。指定渲染质量的其他选项是`-qm`、`-qh`和 ，`-qk`分别表示中、高和 4k 质量。

该`-p`标志在渲染后就会播放动画。如果您想在动画所在位置打开文件浏览器而不是播放它，可以使用该`-f`标志。您也可以省略这两个标志。

最后，默认情况下 manim 将输出 .mp4 文件。如果您希望动画采用 .gif 格式，请使用该`-i`标志。输出文件将与 .mp4 文件位于同一文件夹中，并且具有相同的名称，但文件扩展名不同。

这是对一些最常见的命令行标志的快速回顾。要全面了解所有可用标志，请参阅 [Manim 配置系统的主题指南](../guides/configuration.md)。
