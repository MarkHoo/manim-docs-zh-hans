# Linux

安装说明取决于您的特定操作系统和包管理器。如果您恰好知道自己在做什么，您还可以简单地确保您的系统具有：

- Python 3 的最新版本 (3.7–3.10)，
- [与 pycairo](https://cairographics.org/pycairo/)形式的有效 Cairo 绑定一起 ，
- FFmpeg 可通过命令行访问`ffmpeg`，
- 和[Pango](https://pango.gnome.org)标头。

然后，安装 Manim 只需要运行：

pip3 install manim

Copy to clipboard

笔记

鉴于当前迁移到通过 OpenGL 进行渲染的努力，此列表可能不完整。如果您在安装时遇到缺少依赖项，请告诉我们 <https://github.com/ManimCommunity/manim/issues/new/choose> 。

无论如何，我们还在下面编译了几种常见的操作系统和包管理器组合的说明。

## 所需的依赖项

### apt – Ubuntu / Mint / Debian 

要首先更新源代码，然后安装 Cairo、Pango 和 FFmpeg，只需运行：

sudo apt update
sudo apt install build-essential python3-dev libcairo2-dev libpango1.0-dev ffmpeg

Copy to clipboard

如果您没有安装 python3-pip，请通过以下方式安装：

sudo apt install python3-pip

Copy to clipboard

然后，要安装 Manim，请运行：

pip3 install manim

Copy to clipboard

继续阅读[可选依赖项](#linux-optional-dependencies) 部分。

### dnf – Fedora / CentOS / RHEL 

安装 Cairo 和 Pango：

sudo dnf install cairo-devel pango-devel

Copy to clipboard

为了成功构建`pycairo`轮子，您还需要 Python 开发标头：

sudo dnf install python3-devel

Copy to clipboard

FFmpeg 只能通过 RPMfusion 存储库使用，您必须先配置该存储库 - 请参阅[https://rpmfusion.org/Configuration/](https://rpmfusion.org/Configuration/)了解说明。然后，安装 FFmpeg：

sudo dnf install ffmpeg

Copy to clipboard

此时，您已拥有所有必需的依赖项，并且可以通过运行以下命令来安装 Manim：

pip3 install manim

Copy to clipboard

继续阅读[可选依赖项](#linux-optional-dependencies) 部分。

### pacman – Arch / Manjaro 

提示

感谢*groctel ，* AUR 上有一个专用的 Manim 包！<https://aur.archlinux.org/packages/manim/>

如果您不想使用 AUR 的打包版本，则需要手动执行以下操作：更新包源，然后安装 Cairo、Pango 和 FFmpeg：

sudo pacman -Syu
sudo pacman -S cairo pango ffmpeg

Copy to clipboard

如果您尚未`python-pip`安装，请运行以下命令来获取它：

sudo pacman -S python-pip

Copy to clipboard

然后只需通过以下方式安装 Manim：

pip3 install manim

Copy to clipboard

继续阅读[可选依赖项](#linux-optional-dependencies) 部分。

## 可选依赖项

为了利用 Manim 的 LaTeX 接口来渲染方程等，还必须安装 LaTeX。请注意，这是一个可选的依赖项：如果您不打算使用 LaTeX，则不必安装它。

您可以使用您喜欢的任何 LaTeX 发行版或最容易通过包管理器安装的发行版。通常， 如果您不太关心磁盘空间，[TeX Live 是一个不错的选择。](https://www.tug.org/texlive/)

对于基于 Debian 的系统（如 Ubuntu），可以通过运行以下命令来安装足够的 LaTeX 依赖项：

sudo apt install texlive texlive-latex-extra

Copy to clipboard

如果您选择使用一些较小的 TeX 发行版（例如 [TinyTeX ）](https://yihui.org/tinytex/)，Manim 以某种方式与之交互的 LaTeX 包的完整列表（一个子集可能足以满足您的特定应用程序）是：

collection-basic amsmath babel-english cbfonts-fd cm-super ctex doublestroke
dvisvgm everysel fontspec frcursive fundus-calligra gnu-freefont jknapltx
latex-bin mathastext microtype ms physics preview ragged2e relsize rsfs
setspace standalone tipa wasy wasysym xcolor xetex xkeyval

Copy to clipboard

## 与马尼姆一起工作

此时，您应该已经安装好了 Manim，请前往我们的[快速入门教程](../tutorials/quickstart.html)，了解如何制作您自己的*动画*！
