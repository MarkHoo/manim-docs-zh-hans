# Manim魔法

合格名称：`manim.utils.ipython\_magic.ManimMagic`


```py
class ManimMagic(**kwargs)
```

Bases: `Magics`

创建一个给定配置的可配置配置。

参数

- **config** ( _Config_ ) – 如果为空，则使用默认值。如果 config 是一个 `Config`实例，它将用于配置该实例。
- **Parent** ( _Configurable instance_ _,\_\_optional_) – 该对象的父 Configurable 实例。
- **args**（_Any_）–
- **kwargs**（_Any_）–

返回类型

_Any_

笔记

Configurable 的子类必须在执行任何其他操作 _之前_`__init__()`调用的方法 并使用：`Configurable` `super()`


```py
class MyConfigurable(Configurable):
    def __init__(self, config=None):
        super(MyConfigurable, self).__init__(config=config)
        # Then any other code you need to finish initialization.
```


这可确保实例配置正确。


方法

|||
|-|-|
`add_additional_args`|
[`manim`]()|渲染 IPython 单元中包含的 Manim 场景。


属性

|||
|-|-|
`config`|其值必须是指定类的实例的特征。
`cross_validation_lock`|一个上下文管理器，用于运行一个块，并将交叉验证锁设置为 True。
`magics`|
`options_table`|
`parent`|其值必须是指定类的实例的特征。
`registered`|
`shell`|



`manim(line, cell=None, local_ns=None)`

渲染 IPython 单元中包含的 Manim 场景。起到线条或细胞魔法的作用。

> 示意

> 这种线条和单元魔法在 JupyterLab 环境中使用时效果最佳：虽然所有功能也可用于经典 Jupyter 笔记本，但如果场景名称保持不变，视频有时可能不会在重复执行同一单元时更新相同。

> 使用 JupyterLab 时不会出现此问题。

有关 JupyterLab 和 Jupyter Notebook 的更多信息，请参阅[https://jupyter.org/](https://jupyter.org/)。

线路模式下的用法：

```py
%manim [CLI options] MyAwesomeScene
```


细胞模式下的使用：

```py
%%manim [CLI options] MyAwesomeScene

class MyAweseomeScene(Scene):
    def construct(self):
        ...
```

运行和以获得可能的命令行界面选项。` %manim --help``%manim render --help `

> 笔记

> 笔记本中显示的渲染视频的最大宽度可以通过`media_width`配置选项进行配置。默认设置为`25vw`，即当前视口宽度的 25%。为了使输出尽可能大，请设置。`config.media_width = "100%"`

> 该`media_embed`选项会将图像/视频输出嵌入笔记本中。这通常是不可取的，因为它使笔记本变得非常大，但在某些平台上是必需的（特别是 Google 的 CoLab，除非被 抑制，否则它会自动启用），并且在笔记本（或转换后的 HTML 文件）相对于移动的情况下需要视频位置。用例包括使用 Sphinx 和 JupyterBook 构建文档。另请参阅.` config.embed = False``manim directive for Sphinx `


例子

首先确保将, 或 甚至 放入单元格中并对其进行评估。然后，Manim 的典型 Jupyter 笔记本单元可能如下所示：` import manim``from manim import * `


```py
%%manim -v WARNING --disable_caching -qm BannerExample

config.media_width = "75%"
config.media_embed = True

class BannerExample(Scene):
    def construct(self):
        self.camera.background_color = "#ece6e2"
        banner_large = ManimBanner(dark_theme=False).scale(0.7)
        self.play(banner_large.create())
        self.play(banner_large.expand())
```


计算此单元格将渲染并显示`BannerExample`单元格主体中定义的场景。

> 笔记

> 如果您想隐藏包含输出进度条的红色框，`progress_bar`则应将配置选项设置为`None`。这也可以通过作为 CLI 标志传递来完成。`--progress_bar None`

参数

- **line**( _str_ ) –
- **cell**( _str_ ) –
- **local_ns** (_dict\[str, Any\]_) –

返回类型

None
