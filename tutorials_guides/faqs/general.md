# 常见问题：一般用法

## 为什么 Manim 提示：“there are no scenes inside that module”？

出现此错误的主要原因有两个：如果您已编辑包含您的“Scene”类的文件，但忘记保存它，或者如果您不小心将错误的文件名传递给了`manim`，这是一个可能的结果。 检查您是否拼写正确。

否则，您可能会混淆 Manim 版本。 请参阅`此常见问题解答<不同版本>`

有关为什么有不同版本的解释。在下面假设您正在尝试使用终端中的`manim`可执行文件来运行
为社区版本编写的场景（即，有`from manim import *`，或更具体地说是`from manim import Scene`），那么这个错误表明`manim`可执行文件已被`manimgl`提供的可执行文件覆盖（不幸的是，`manim`和`manimgl`都提供“manim”可执行文件）。

您可以通过运行`manim --version`来检查是否是这种情况，社区维护版本的输出以`Manim Community v...`开头。 如果不是这种情况，则您正在运行`manimgl`。

您可以通过以下任一步骤解决此问题：

- 卸载并重新安装`manim`，
- 使用`manimce`可执行文件代替`manim`可执行文件，
- 或者通过`python -m manim`直接调用 Python 模块来替换对可执行文件的调用。

---

## 为什么无论我在文件中放入什么代码，Manim 都只会渲染黑框?

如果您使用通常的模式来编写`Scene`，即:

```python
class MyAwesomeScene(Scene):
    def construct(self):
        ...
        # your animation code
```

然后仔细检查`construct`的拼写是否正确。 如果包含您的代码的方法没有被称为`construct`（或者您没有调用`construct`中不同的自定义方法），Manim 将不会调用您的方法，而只会输出一个黑框。

---

## Manim 场景(scene)的默认尺寸是多少？

The scene measures 8 units in height and has a default ratio of 16:9,
which means that it measures {math}`8 \cdot 16 / 9 = 14 + 2/9` units in width.
The origin is in the center of the scene, which means that, for example, the
upper left corner of the scene has coordinates `[-7-1/9, 4, 0]`.

---

## 创建 `Mobject` 时如何确定可以传递哪些关键字参数？

Let us consider a specific example, like the {class}`.Circle` class. When looking
at its documentation page, only two specific keyword arguments are listed
(`radius`, and `color`). Besides these concrete arguments, there is also a
catchall `**kwargs` argument which captures all other arguments that are passed
to `Circle`, and passes them on to the base class of {class}`.Circle`, {class}`.Arc`.

让我们考虑一个具体的例子，比如 {class}`.Circle` 类。 当寻找时
在其文档页面中，仅列出了两个特定的关键字参数
（“半径”和“颜色”）。 除了这些具体的论点之外，还有一个
包罗万象的“\*\*kwargs”参数捕获传递的所有其他参数
到 `Circle`，并将它们传递给 {class}`.Circle`、{class}`.Arc` 的基类。

The same holds for {class}`.Arc`: some arguments are explicitly documented, and
there is again a catchall `**kwargs` argument that passes unprocessed arguments
to the next base class -- and so on.

这同样适用于 {class}`.Arc`：一些参数被明确记录，并且
又存在一个包罗万象的“\*\*kwargs”参数，它传递未处理的参数
到下一个基类——等等。

The most important keyword arguments relevant to styling your mobjects are the
ones that are documented for the base classes {class}`.VMobject` and
{class}`.Mobject`.

与设置 mobject 样式相关的最重要的关键字参数是为基类 {class}`.VMobject` 和 {class}`.Mobject` 记录的关键字参数。

---

## Manim 能否渲染透明背景的视频？

是的：只需传递 CLI 标志“-t”（或其长形式“--transparent”）。
请注意，默认的视频文件格式不支持透明度，
这就是为什么 Manim 在使用透明背景渲染时会输出“.mov”而不是“.mp4”。 其他支持透明度的电影文件格式可以通过传递`--format=webm`或`--format=gif`来获得。

---

## 我看过一个视频，其中创作者运行命令 X，但它对我不起作用。 为什么？

您正在观看的视频可能已经过时了。 如果您想继续操作，您要么需要使用视频中使用的相同版本，要么相应地修改代码（在许多情况下它只是一个被重命名的方法等）。 检查视频说明，在某些情况下，创作者会指出是否需要对视频中显示的代码进行更改。

---

## 当使用`Tex`或`MathTex`时，一些字母丢失。 我怎样才能解决这个问题？

您可能需要（重新）构建 LaTeX 使用的某些字体。 对于某些发行版，您可以通过运行以下命令来手动执行此操作

```bash
fmtutil -sys --all
```

我们建议您查阅 LaTeX 发行版的文档以获取更多信息。

---

## 我想将一些代码从`manimgl`迁移到`manim`，我该如何使用`CONFIG`字典？

社区维护的版本很早就放弃了`CONFIG`字典的使用，于 2021 年 1 月发布的版本 v0.2.0。可查看版本变更日志。

在此之前，Manim 的类基本上通过模仿继承来处理 `CONFIG` 字典（以正确处理父类设置的 `CONFIG` 字典），然后将字典中的所有键值对分配为相应对象的属性。

在没有太多继承的情况下，或者对于任何自定义设置，您应该自己设置这些属性。 例如，对于具有下面示例自定义属性的旧式`Scene`

```python
class OldStyle(Scene):
    CONFIG = {"a": 1, "b": 2}
```

应该写成

```python
class NewStyle(Scene):
    a = 1
    b = 2
```

在应该正确继承值的情况下，应该将参数添加到类的初始化函数中。 旧式的 mobject `Thing` 可能看起来像

```python
class Thing(VMobject):
    CONFIG = {
        "stroke_color": RED,
        "fill_opacity": 0.7,
        "my_awesome_argument": 42,
    }
```

where `stroke_color` and `fill_opacity` are arguments that concern the
parent class of `Thing`, and `my_awesome_argument` is a custom argument
that only concerns `Thing`. A version without `CONFIG` could look like this:

其中`stroke_color`和`fill_opacity`是涉及`Thing`父类的参数，`my_awesome_argument`是仅涉及`Thing`的自定义参数。 没有`CONFIG`的版本可能如下所示：

```python
class Thing(VMobject):
    def __init__(
        self, stroke_color=RED, fill_opacity=0.7, my_awesome_argument=42, **kwargs
    ):
        self.my_awesome_argument = my_awesome_argument
        super().__init__(stroke_color=stroke_color, fill_opacity=fill_opacity, **kwargs)
```

---

## 我的安装不支持将 PDF 转换为 SVG，有帮助吗？为什么？

这是 `dvisvgm` 的问题，该工具随 LaTeX 一起提供，可将 LaTeX 输出转换为 Manim 可以解析的 `.svg` 文件。

首先，通过检查输出来确保您的 `dvisvgm` 版本至少为 2.4

```bash
dvisvgm --version
```

If you do not know how to update `dvisvgm`, please refer to your
LaTeX distributions documentation (or the documentation of your
operating system, if `dvisvgm` was installed as a system package).

Second, check whether your ``dvisvgm`` supports PostScript specials. This is
needed to convert from PDF to SVG. Run:

```bash
dvisvgm -l
```

If the output to this command does **not** contain `ps  dvips PostScript specials`,
this is a bad sign. In this case, run

```bash
dvisvgm -h
```

If the output does **not** contain `--libgs=filename`, this means your
`dvisvgm` does not currently support PostScript. You must get another binary.

If, however, `--libgs=filename` appears in the help, that means that your
`dvisvgm` needs the Ghostscript library to support PostScript. Search for
`libgs.so` (on Linux, probably in `/usr/local/lib` or `/usr/lib`) or
`gsdll32.dll` (on 32-bit Windows, probably in `C:\windows\system32`) or
`gsdll64.dll` (on 64-bit Windows, also probably in `C:\windows\system32`)
or `libgsl.dylib` (on MacOS, probably in `/usr/local/lib` or
`/opt/local/lib`). Please look carefully, as the file might be located
elsewhere, e.g. in the directory where Ghostscript is installed.

When you have found the library, try (on MacOS or Linux)

```bash
export LIBGS=<path to your library including the file name>
dvisvgm -l
```

or (on Windows)

```bat
set LIBGS=<path to your library including the file name>
dvisvgm -l
```

You should now see `ps    dvips PostScript specials` in the output. Refer to
your operating system's documentation to find out how you can set or export the
environment variable ``LIBGS`` automatically whenever you open a shell.

As a last check, you can run

```bash
dvisvgm -V1
```

(while still having `LIBGS` set to the correct path, of course.) If `dvisvgm`
can find your Ghostscript installation, it will be shown in the output together
with the version number.

If you do not have the necessary library on your system, please refer to your
operating system's documentation to find out where you can get it and how you
have to install it.

If you are unable to solve your problem, check out the
[dvisvgm FAQ](https://dvisvgm.de/FAQ/).

---

## 哪里可以找到更多学习 Manim 的资源？

In our [Discord server](https://manim.community/discord), we have the community-maintained
`#beginner-resources` channel in which links to helpful learning resources are collected.
You are welcome to join our Discord and take a look yourself! If you have found some
guides or tutorials yourself that are not on our list yet, feel free to add them!
