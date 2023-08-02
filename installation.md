# 安装

根据您的使用案例，建议使用不同的安装选项：如果您只是想稍微使用一下 Manim，交互式浏览器内笔记本是探索该库的一种非常简单的方法，因为它们不需要本地安装。前往 [https://try.manim.community](https://try.manim.community)尝试我们的交互式教程。

否则，如果您打算使用 Manim 处理动画项目，我们建议您在本地安装该库（安装到 conda 环境、系统的 Python 或通过 Docker）。

> 警告

> 请注意，Manim 有多个不同版本。本网站上的说明**仅**适用于*社区版*。如果您不确定应该安装哪个版本，请详细了解[Manim 版本之间的差异。](./tutorials_guides/faqs/installation.md)

1.  [将 Manim 安装到 conda 环境]()
2.  [将 Manim 安装到系统的 Python 中]()
3.  [通过 Docker 使用 Manim]()
4.  [通过 Binder / Google Colab 的交互式 Jupyter 笔记本]()

## 在 conda 中安装 Manim

Conda 是 Python 的包管理器，允许创建存储所有依赖项的环境。这样，您的电脑就不会因为不需要的库而变得混乱，并且当您不再需要该环境时，可以将其删除。这是安装 manim 的好方法，因为所有依赖项（如 `ffmpeg`、`pycairo`等）都附带它。此外，无论您使用的是 Windows、Linux、Intel Mac 还是 Apple Silicon，安装步骤都是相同的。

以下页面展示了如何在 conda 环境中安装 Manim：

- [conda]()
  - [所需的依赖项]()
  - [可选依赖项]()
  - [与Manim合作]()

## 在本地安装 Manim

Manim 是一个 Python 库，可以 [通过 pip 安装](https://pypi.org/project/manim/)。但是，为了让 Manim 正常工作，需要首先安装一些额外的系统依赖项。以下页面提供了特定于操作系统的说明供您遵循。

Manim 需要 Python 版本`3.7`或更高版本才能运行。

> 提示

> 根据您的特定设置，安装过程可能会略有不同。确保您已尝试仔细按照以下页面上的步骤进行操作，但如果您遇到困难，我们很乐意提供帮助：[加入我们的 Discord]()，或[直接在 GitHub](https://github.com/ManimCommunity/manim/discussions)上开始新的讨论。

- [Windows]()
  - [所需的依赖项]()
  - [可选依赖项]()
  - [与Manim合作]()
- [苹果系统]()
  - [所需的依赖项]()
  - [可选依赖项]()
  - [与Manim合作]()
- [Linux]()
  - [所需的依赖项]()
  - [可选依赖项]()
  - [与Manim合作]()

在本地安装 Manim 后，您可以继续阅读我们的 [快速入门指南]()

如上所述，如果出现错误或其他问题，请不要担心：请参阅我们的[常见问题解答部分]()

## 通过 Docker 使用 Manim

[Docker](https://www.docker.com)是一种虚拟化工具，允许分发封装的软件环境（容器）。

以下页面包含有关社区维护的 docker 映像的更多信息`manimcommunity/manim`：

- [Docker]()
  - [Docker 容器的基本使用]()
  - [通过 Docker 运行 JupyterLab]()

## 适用于您的浏览器的交互式 Jupyter 笔记本

Manim 附带了一个内置的 IPython magic 命令，专为在[Jupyter 笔记本](https://jupyter.org)`%%manim`中使用而设计。我们位于[https://try.manim.community](https://try.manim.community)的交互式教程演示了如何在 Jupyter Notebook 中使用 Manim。

以下几页解释了如何自己设置这样的交互式环境：

- [Jupyter 笔记本]()
  - [活页夹]()
  - [谷歌合作实验室]()

## 编辑

如果您使用的是 Visual Studio Code，您可以安装一个名为 *Manim Sideview*的扩展，它提供自动渲染和编辑器内动画的集成预览。[该扩展可以通过 VS Code 市场](https://marketplace.visualstudio.com/items?itemName=Rickaym.manim-sideview)安装 。

## 供开发者安装

为了更改库中的代码，建议以不同的方式安装 Manim。如果您对此感兴趣，请按照我们的[贡献指南]()
