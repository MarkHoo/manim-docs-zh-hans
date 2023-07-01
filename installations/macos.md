# macOS

为了简单起见，以下说明假设您已安装流行的[包管理器 Homebrew](https://brew.sh)。虽然您当然也可以在没有它的情况下安装所有依赖项，但使用 Homebrew 使该过程变得更加容易。

如果您想使用 Homebrew 但尚未安装，请按照[Homebrew 的安装说明](https://docs.brew.sh/Installation)进行操作。

笔记

在 Apple 发布其新的基于 ARM 的处理器（Apple Silicon 芯片，如*“M1 芯片”*）后的一段时间内，推荐的 Manim 安装方式依赖于*Rosetta*，Apple 在 Intel 和 ARM 架构之间的兼容层。这不再是必要的，Manim 可以（并且建议）本地安装。

## 所需的依赖项

要安装安装 Manim 所需的所有依赖项（即：ffmpeg、Python 和一些必需的 Python 包），请运行：

brew install py3cairo ffmpeg

Copy to clipboard

在基于*Apple Silicon*的机器上（即具有 M1 芯片或类似芯片的设备；如果您不确定要检查哪个处理器，请打开 Apple 菜单，选择“ *关于本机”并检查\_\_“芯片”*旁边的条目），需要一些额外的依赖项，即：

brew install pango scipy

Copy to clipboard

安装所有必需的依赖项后，只需运行：

pip3 install manim

Copy to clipboard

安装马尼姆。

笔记

安装问题的一个常见原因是`pip3` 系统上没有指向正确的 Python 安装。要检查这一点，请运行：对于 macOS Intel，路径应以 开头，对于 Apple Silicon， 路径应以 开头。如果不是这种情况，则您要么在安装 Homebrew 期间忘记修改 shell 配置文件 ( )，要么在执行此操作后没有重新加载 shell（例如，通过打开新终端）。也有可能其他一些软件（如 Pycharm）更改了该变量 \- 要解决此问题，请确保与 Homebrew 相关的行位于文件的最末尾。` pip3 -V``/usr/local``/opt/homebrew``.zprofile``PATH``.zprofile `

## 可选依赖项

In order to make use of Manim’s interface to LaTeX for, e.g., rendering equations, LaTeX has to be installed as well. Note that this is an optional dependency: if you don’t intend to use LaTeX, you don’t have to install it.

For macOS, the recommended LaTeX distribution is [MacTeX](http://www.tug.org/mactex/). You can install it by following the instructions from the link, or alternatively also via Homebrew by running:

brew install --cask mactex-no-gui

Copy to clipboard

Warning

MacTeX is a _full_ LaTeX distribution and will require more than 4GB of disk space. If this is an issue for you, consider installing a smaller distribution like [BasicTeX](http://www.tug.org/mactex/morepackages.html).

Should you choose to work with some partial TeX distribution, the full list of LaTeX packages which Manim interacts with in some way (a subset might be sufficient for your particular application) is:

amsmath babel-english cbfonts-fd cm-super ctex doublestroke dvisvgm everysel
fontspec frcursive fundus-calligra gnu-freefont jknapltx latex-bin
mathastext microtype ms physics preview ragged2e relsize rsfs
setspace standalone tipa wasy wasysym xcolor xetex xkeyval

Copy to clipboard

## 与Manim一起工作

此时，您应该已经安装了可以正常工作的 Manim。前往我们的[快速入门教程，](../tutorials/quickstart.html)了解如何制作自己的*动画*！
