# Manim配置

合格名称：`manim.\_config.utils.ManimConfig`

```py
class ManimConfig
```

Bases: `MutableMapping`

类似字典的类存储所有配置选项。

全局`config`对象是此类的一个实例，并且充当库的所有可自定义行为的单一事实来源。

全局`config`对象能够消化不同类型的源并将它们转换为统一的接口。这些源是（按优先级升序排列）：配置文件、命令行参数和编程更改。无论用户选择如何设置配置选项，她都可以使用 的 [`ManimConfig`]()属性和属性来访问其当前值。

笔记

每个配置选项都作为此类的属性实现。

每个配置选项都可以使用属性的全名通过配置文件进行设置。如果配置选项具有关联的 CLI 标志，则该标志等于属性的全名。那些承认替代标志或根本没有标志的记录在各个属性的文档字符串中。


例子

为了演示起见，我们在以下示例中使用全局配置对象的副本；`config`如果您确实想修改配置，可以跳过这些行并直接导入：

```py
from manim import config as global_config
config = global_config.copy()
```

每个配置选项都允许使用字典语法和属性语法。例如，以下两行是等效的：

```py
from manim import WHITE
config.background_color = WHITE
config["background_color"] = WHITE
```

前者是优选的；提供后者主要是为了向后兼容。

配置选项旨在保持内部一致性。例如，设置`frame_y_radius`将影响`frame_height`：

```py
config.frame_height
8.0
config.frame_y_radius = 5.0
config.frame_height
10.0
```

与配置选项交互的方式有很多种。以配置选项为例`background_color`。有三种方法可以更改它：通过配置文件、通过 CLI 标志或以编程方式。

要通过配置文件设置背景颜色，请保存 `manim.cfg`包含以下内容的以下文件。

```ini
[CLI]
background_color = WHITE
```
为了使该`.cfg`文件应用于 manim 场景，需要将其放置在与脚本相同的目录中，

```sh
project/
├─scene.py
└─manim.cfg
```
现在，当用户执行

```sh
manim scene.py
```
场景的背景将设置为`WHITE`。无论从何处调用 manim 命令，这都适用。

命令行参数覆盖`.cfg`文件。在前面的示例中，执行

```sh
manim scene.py -c BLUE
```

无论 . 的内容如何，​​ 都会将背景颜色设置为蓝色 `manim.cfg`。

最后，场景脚本本身内所做的任何编程更改都将覆盖命令行参数。例如，如果`scene.py`包含以下内容

```py
from manim import *

config.background_color = RED

class MyScene(Scene):
    ...
```

`manim.cfg`无论调用 manim 时使用的 CLI 参数或内容如何，​​ 背景颜色都将设置为 RED 。


方法

|||
|-|-|
[`copy`]()|深度复制此 ManimConfig 的内容。
[`digest_args`]()|处理 CLI 参数中存在的配置选项。
[`digest_file`]()|处理文件中存在的配置选项`.cfg`。
[`digest_parser`]()|处理对象中存在的配置选项`ConfigParser`。
[`get_dir`]()|解决存储目录的配置选项。
`resolve_movie_file_extension`|
[`update`]()|[`ManimConfig`]()消化在另一个或字典中找到的选项。


属性

|||
|-|-|
[`aspect_ratio`]()|纵横比（宽度/高度），以像素为单位（--分辨率，-r）。
[`assets_dir`]()|用于查找视频资产的目录（无标志）。
[`background_color`]()|场景的背景颜色 (-c)。
[`background_opacity`]()|0.0（完全透明）和 1.0（完全不透明）之间的数字。
[`bottom`]()|坐标位于框架的中心底部。
[`custom_folders`]()|是否使用自定义文件夹输出。
[`disable_caching`]()|是否使用场景缓存。
[`disable_caching_warning`]()|如果要散列的子对象过多，是否发出警告。
[`dry_run`]()|是否启用试运行。
[`enable_gui`]()|启用 GUI 交互。
[`enable_wireframe`]()|在 opengl 中启用线框调试模式。
[`ffmpeg_executable`]()|手动指定 ffmpeg 可执行文件的路径
[`ffmpeg_loglevel`]()|ffmpeg 的详细级别（无标志）。
[`flush_cache`]()|是否删除所有缓存的部分影片文件。
[`force_window`]()|使用 opengl 渲染器时设置为强制窗口
[`format`]()|文件格式; “png”、“gif”、“mp4”、“webm”或“mov”。
[`frame_height`]()|以逻辑单位表示的帧高度（无标志）。
[`frame_rate`]()|帧速率（以每秒帧数为单位）。
[`frame_size`]()|元组（像素宽度，像素高度）（无标志）。
[`frame_width`]()|以逻辑单位表示的帧宽度（无标志）。
[`frame_x_radius`]()|帧宽度的一半（无标志）。
[`frame_y_radius`]()|框架高度的一半（无标志）。
[`from_animation_number`]()|以此数字 (-n) 开始渲染动画。
[`fullscreen`]()|将窗口扩展至其可能的最大尺寸。
[`gui_location`]()|启用 GUI 交互。
[`images_dir`]()|放置图像的目录（无标志）。
[`input_file`]()|输入文件名。
[`left_side`]()|坐标位于框架的中间左侧。
[`log_dir`]()|放置日志的目录。
[`log_to_file`]()|是否将日志保存到文件中。
[`max_files_cached`]()|缓存的最大文件数。
[`media_dir`]()|主输出目录。
[`media_embed`]()|在 Jupyter 笔记本中嵌入视频
[`media_width`]()|Jupyter 笔记本中的媒体宽度
[`movie_file_extension`]()|.mp4、.webm 或 .mov。
[`notify_outdated_version`]()|是否有可用版本更新时通知。
[`output_file`]()|输出文件名 (-o)。
[`partial_movie_dir`]()|放置部分电影文件的目录（无标志）。
[`pixel_height`]()|帧高度以像素为单位（--分辨率，-r）。
[`pixel_width`]()|帧宽度以像素为单位（--分辨率，-r）。
[`plugins`]()|要启用的插件列表。
[`preview`]()|是否播放渲染的影片(-p)。
[`progress_bar`]()|渲染动画时是否显示进度条。
[`quality`]()|视频质量 (-q)。
[`renderer`]()|当前活动的渲染器。
[`right_side`]()|坐标位于框架的右中位置。
[`save_as_gif`]()|是否以 .gif 格式保存渲染场景 (-i)。
[`save_last_frame`]()|是否将场景的最后一帧保存为图像文件（-s）。
[`save_pngs`]()|是否将场景中的所有帧保存为图像文件（-g）。
[`save_sections`]()|除电影文件外，是否保存每个部分的单个视频。
[`scene_names`]()|从文件中播放的场景。
[`sections_dir`]()|放置部分视频的目录（无标志）。
[`show_in_file_browser`]()|是否在文件浏览器中显示输出文件（-f）。
[`tex_dir`]()|放置 tex 的目录（无标志）。
[`tex_template`]()|渲染 Tex 时使用的模板。
[`tex_template_file`]()|从中读取 Tex 模板的文件（无标志）。
[`text_dir`]()|放置文本的目录（无标志）。
[`top`]()|坐标位于框架的中心顶部。
[`transparent`]()|背景不透明度是否为 0.0 (-t)。
[`upto_animation_number`]()|在此编号处停止渲染动画。
[`use_projection_fill_shaders`]()|使用与变换矩阵兼容的着色器进行 OpenGLVM 对象填充。
[`use_projection_stroke_shaders`]()|使用与变换矩阵兼容的 OpenGLVM 对象描边着色器。
[`verbosity`]()|记录器冗长；“调试”、“信息”、“警告”、“错误”或“严重”(-v)。
[`video_dir`]()|放置视频的目录（无标志）。
[`window_monitor`]()|将渲染场景的监视器
[`window_position`]()|设置预览窗口的位置。
[`window_size`]()|opengl 窗口的大小。
[`write_all`]()|是否渲染输入文件中的所有场景 (-a)。
[`write_to_movie`]()|是否将场景渲染为电影文件 (-w)。
[`zero_pad`]()|PNG 零填充。



_属性_ aspect_ratio

以像素为单位的宽高比（宽度/高度）（-分辨率，-r）。

_属性_ asset_dir 

用于查找视频资产的目录（无标志）。

_属性_ background_color

场景的背景颜色 (-c)。

_属性_ background_opacity

0.0（完全透明）和 1.0（完全不透明）之间的数字。

_属性_ bottom
坐标位于框架的中心底部。



`copy()`

深度复制此 ManimConfig 的内容。

返回

该对象的副本不包含共享引用。

返回类型

[`ManimConfig`]()

> 也可以看看

> `tempconfig()`

笔记

这就是背后的主要机制`tempconfig()`。

_属性_ custom_folders

是否使用自定义文件夹输出。



`digest_args(args)`

处理 CLI 参数中存在的配置选项。

参数

**args** (_命名空间_) – 由 . 返回的对象`main_utils.parse_args()`。

返回

**self** – 该对象在处理`parser`.

返回类型

[`ManimConfig`]()

> 也可以看看

> `main_utils.parse_args()`, [`digest_parser()`](), [`digest_file()`]()

笔记

如果`args.config_file`是非空字符串，则在消化任何其他 CLI 参数之前`ManimConfig`尝试消化所述文件的内容。[`digest_file()`]()


`digest_file(filename)`

处理文件中存在的配置选项`.cfg`。

此方法处理单个`.cfg`文件，而 [`digest_parser()`]()可以处理可能从多个`.cfg`文件构建的任意解析器。

参数

**filename** ( _str_ _|_ _os.PathLike_ ) – 文件的路径`.cfg`。

返回

**self** – 该对象在处理`filename`.

返回类型

[`ManimConfig`]()

> 也可以看看

> [`digest_file()`](), [`digest_args()`](),[`make_config_parser()`]()

笔记

如果有多个`.cfg`文件需要处理，首先将它们解析为单个`ConfigParser`对象并通过一次调用来消化它们 [`digest_parser()`]()总是比多次调用此方法更有效。


`digest_parser(parser)`

处理对象中存在的配置选项`ConfigParser`。

此方法可以处理任意解析器，而不仅仅是从单个文件读取的解析器，而且[`digest_file()`]()一次只能处理一个文件。

参数

**parser** ( _ConfigParser_ ) – 反映一个或多个文件内容的对象`.cfg`。特别地，它可以反映已经以级联方式解析的多个文件的内容。

返回

**self** – 该对象在处理`parser`.

返回类型

[`ManimConfig`]()

> 也可以看看

> [`make_config_parser()`](), [`digest_file()`](),[`digest_args()`]()

笔记

如果有多个文件需要处理，首先将它们解析为单个对象，然后调用此函数一次（而不是 多次调用）`.cfg`总是更有效。`ConfigParser`[`digest_file()`]()


例子

要消化两个文件中设置的配置选项，首先创建一个 ConfigParser 并解析这两个文件，然后消化解析器：

```py
parser = configparser.ConfigParser()
parser.read([file1, file2])
config = ManimConfig().digest_parser(parser)
```

事实上，全局`config`对象是这样初始化的：

```py
parser = make_config_parser()
config = ManimConfig().digest_parser(parser)
```

_属性_ disable_caching

是否使用场景缓存。

_属性_ disable_caching_warning 

如果要散列的子对象过多，是否发出警告。

_属性_ dry_run 

是否启用试运行。

_属性_ enable_gui

启用 GUI 交互。

_属性_ enable_wireframe

在 opengl 中启用线框调试模式。

_属性_ ffmpeg_executable

手动指定 ffmpeg 可执行文件的路径

_属性_ ffmpeg_loglevel

ffmpeg 的详细级别（无标志）。

_属性_ flush_cache 

是否删除所有缓存的部分影片文件。

_属性_ force_window 

使用 opengl 渲染器时设置为强制窗口

_属性_ format

文件格式; “png”、“gif”、“mp4”、“webm”或“mov”。

_属性_ frame_height 

以逻辑单位表示的帧高度（无标志）。

_属性_ frame_rate
帧速率（以每秒帧数为单位）。

_属性_ frame_size 

元组（像素宽度，像素高度）（无标志）。

_属性_ frame_width 

以逻辑单位表示的帧宽度（无标志）。

_属性_ frame_x_radius 

帧宽度的一半（无标志）。

_属性_ frame_y_radius 

框架高度的一半（无标志）。

_属性_ from_animation_number

以此数字 (-n) 开始渲染动画。

_属性_ fullscreen

将窗口扩展至其可能的最大尺寸。



`get_dir(key, **kwargs)`

解决存储目录的配置选项。

存储目录的配置选项可能相互依赖。此方法用于向最终用户提供实际目录。

参数

- **key** ( _str_ ) – 要解析的配置选项。必须是以 结尾的选项 `'_dir'`，例如`'media_dir'`或`'video_dir'`。
- **kwargs** ( _str_ ) – 解析目录时要使用的任何字符串。

返回

请求目录的路径。如果路径解析为空字符串，`None`则返回。

返回类型

`pathlib.Path`

提高

**KeyError** – When`key`不是存储目录的配置选项，因此[`get_dir()`]()不合适；或者在 `key`适当的时候但没有足够的信息来解析目录。

笔记

标准`str.format()`语法用于解析路径，因此路径可以包含使用 f 字符串表示法的任意占位符。但是，这些将需要`kwargs`包含所需的值。


例子

的值`config.tex_dir`是`'{media_dir}/Tex'`默认值，即它是所在`config.media_dir`位置的子文件夹。为了获取*实际*目录，请使用[`get_dir()`]().

```sh
>>> from manim import config as globalconfig
>>> config = globalconfig.copy()
>>> config.tex_dir
'{media_dir}/Tex'
>>> config.media_dir
'./media'
>>> config.get_dir("tex_dir").as_posix()
'media/Tex'
```

解析目录是在最后一刻以惰性方式完成的，以反映其他配置选项中的任何更改：

```sh
>>> config.media_dir = "my_media_dir"
>>> config.get_dir("tex_dir").as_posix()
'my_media_dir/Tex'
```

某些目录依赖于 [`ManimConfig`](). 例如，video_dir 的默认值 包括输入文件的名称和视频质量（例如 480p15）。此信息必须通过以下方式提供`kwargs`：

```sh
>>> config.video_dir
'{media_dir}/videos/{module_name}/{quality}'
>>> config.get_dir("video_dir")
Traceback (most recent call last):
KeyError: 'video_dir {media_dir}/videos/{module_name}/{quality} requires the following keyword arguments: module_name'
>>> config.get_dir("video_dir", module_name="myfile").as_posix()
'my_media_dir/videos/myfile/1080p60'
```

请注意，质量不需要作为关键字参数传递，因为 [`ManimConfig`]()它存储有关质量的信息。

目录可以被递归地定义。例如，配置选项 `partial_movie_dir`取决于`video_dir`，而后者又取决于`media_dir`：

```sh
>>> config.partial_movie_dir
'{video_dir}/partial_movie_files/{scene_name}'
>>> config.get_dir("partial_movie_dir")
Traceback (most recent call last):
KeyError: 'partial_movie_dir {video_dir}/partial_movie_files/{scene_name} requires the following keyword arguments: scene_name'
>>> config.get_dir(
    "partial_movie_dir", module_name="myfile", scene_name="myscene"
).as_posix()
'my_media_dir/videos/myfile/1080p60/partial_movie_files/myscene'
```

使用标准 f 字符串语法。定义目录时可以使用任意名称，只要将相应的值传递给 [`ManimConfig.get_dir()`]()via 即可`kwargs`。

```sh
>>> config.media_dir = "{dir1}/{dir2}"
>>> config.get_dir("media_dir")
Traceback (most recent call last):
KeyError: 'media_dir {dir1}/{dir2} requires the following keyword arguments: dir1'
>>> config.get_dir("media_dir", dir1="foo", dir2="bar").as_posix()
'foo/bar'
>>> config.media_dir = "./media"
>>> config.get_dir("media_dir").as_posix()
'media'
```

_属性_ gui_location 

启用 GUI 交互。

_属性_ images_dir 

放置图像的目录（无标志）。见[`ManimConfig.get_dir()`]()。

_属性_ input_file

输入文件名。

_属性_ left_side
坐标位于框架的中间左侧。

_属性_ log_dir 

放置日志的目录。见[`ManimConfig.get_dir()`]()。

_属性_ log_to_file 

是否将日志保存到文件中。

_属性_ max_files_cached 

缓存的最大文件数。使用 -1 表示无穷大（无标志）。

_属性_ media_dir 

主输出目录。见[`ManimConfig.get_dir()`]()。

_属性_ media_embed 

在 Jupyter 笔记本中嵌入视频

_属性_ media_width

Jupyter 笔记本中的媒体宽度

_属性_ movie_file_extension 

.mp4、.webm 或 .mov。

_属性_ notify_outdated_version 

是否有可用版本更新时通知。

_属性_ output_file

输出文件名 (-o)。

_属性_ partial_movie_dir 

放置部分电影文件的目录（无标志）。见[`ManimConfig.get_dir()`]()。

_属性_ pixel_height

帧高度以像素为单位（-分辨率，-r）。

_属性_ pixel_width

帧宽度以像素为单位（–分辨率，-r）。

_属性_ plugins

要启用的插件列表。

_属性_ preview

是否播放渲染的影片(-p)。

_属性_ progress_bar 

渲染动画时是否显示进度条。

_物业_ quality

视频质量 (-q)。

_属性_ renderer

当前活动的渲染器。

填充了 中可用的渲染器之一[`RendererType`]()。

测试：

```sh
>>> test_config = ManimConfig()
>>> test_config.renderer is None  # a new ManimConfig is unpopulated
True
>>> test_config.renderer = 'opengl'
>>> test_config.renderer
<RendererType.OPENGL: 'opengl'>
>>> test_config.renderer = 42
Traceback (most recent call last):
...
ValueError: 42 is not a valid RendererType
```

检查渲染器类型的大小写是否无关紧要：

```sh
>>> test_config.renderer = 'OpenGL'
>>> test_config.renderer = 'cAirO'
```


_属性_ right_side

坐标位于框架的右中位置。

_属性_ save_as_gif 

是否以 .gif 格式保存渲染场景 (-i)。

_属性_ save_last_frame 

是否将场景的最后一帧保存为图像文件（-s）。

_属性_ save_pngs 

是否将场景中的所有帧保存为图像文件（-g）。

_属性_ save_sections 

除电影文件外，是否保存每个部分的单个视频。

_属性_ scene_names

从文件中播放的场景。

_属性_ section_dir 

放置部分视频的目录（无标志）。见[`ManimConfig.get_dir()`]()。

_属性_ show_in_file_browser 

是否在文件浏览器中显示输出文件（-f）。

_属性_ tex_dir 

放置 tex 的目录（无标志）。见[`ManimConfig.get_dir()`]()。

_属性_ tex_template 

渲染 Tex 时使用的模板。请参阅[`TexTemplate`]()。

_属性_ tex_template_file 

从中读取 Tex 模板的文件（无标志）。见[`TexTemplateFromFile`]()。

_属性_ text_dir 

放置文本的目录（无标志）。见[`ManimConfig.get_dir()`]()。

_属性_ top

坐标位于框架的中心顶部。

_属性_ transparent

背景不透明度是否为 0.0 (-t)。



`update(obj)`

[`ManimConfig`]()消化在另一个或字典中找到的选项。

与 类似`dict.update()`，用 的值替换该对象的值`obj`。

参数

**obj** ( [_ManimConfig_]() _|_ _dict_ ) – 要从中复制值的对象。

返回类型

None

提高

**AttributeError** – 如果`obj`是一个字典，但包含不属于任何配置选项的键。

> 也可以看看

> [`digest_file()`](), [`digest_args()`](),[`digest_parser()`]()

_属性_ upto_animation_number

在此编号处停止渲染动画。使用 -1 以避免跳过 (-n)。

_属性_ use_projection_fill_shaders 

使用与变换矩阵兼容的着色器进行 OpenGLVM 对象填充。

_属性_ use_projection_lines_shaders 

使用与变换矩阵兼容的 OpenGLVM 对象描边着色器。

_属性_ verbosity
记录器冗长；“调试”、“信息”、“警告”、“错误”或“严重”(-v)。

_属性_ video_dir 

放置视频的目录（无标志）。见[`ManimConfig.get_dir()`]()。

_属性_ window_monitor 

将渲染场景的监视器

_属性_ window_position

设置预览窗口的位置。您可以使用方向，例如 UL/DR/ORIGIN/LEFT...或窗口左上角的位置（像素），例如“960,540”

_属性_ window_size 

opengl 窗口的大小。“默认”根据显示监视器自动缩放窗口。

_属性_ write_all 

是否渲染输入文件中的所有场景 (-a)。

_属性_ write_to_movie 

是否将场景渲染为电影文件 (-w)。

_属性_ zero_pad

PNG 零填充。0（无零填充）和 9（最少 9 列）之间的数字。
