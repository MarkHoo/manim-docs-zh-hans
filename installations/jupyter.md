# Jupyter Notebooks

## Binder

[Binder](https://mybinder.readthedocs.io/en/latest/)是一个在线平台，以 Jupyter 笔记本的形式托管可共享和可定制的计算环境。Manim 附带内置的`%%manim` Jupyter magic 命令，这使得它可以在这些笔记本中轻松使用。

要查看此类环境的示例，请访问我们的交互式教程：[https://try.manim.community/](https://try.manim.community/)。

以允许通过 Binder 交互共享的方式准备自己的笔记本相对简单：

1.  首先，准备一个目录，其中包含您想要在交互式环境中共享的一个或多个笔记本。您可以通过使用本地安装的 Manim 的 Jupyter 笔记本来创建这些笔记本，也可以在我们预先存在的 [交互式教程环境](https://try.manim.community/)中工作。
2.  在包含笔记本的同一目录中，添加一个名为`Dockerfile`以下内 ​​ 容的文件：

```py
FROM docker.io/manimcommunity/manim:v0.9.0

COPY --chown=manimuser:manimuser . /manim
```

    创建笔记本时，不要忘记将版本标记更改`v0.9.0`为您在本地使用的版本。

3.  使包含您的工作表的目录并向`Dockerfile` 公众开放（特别是：Binder！）。有 [几种不同的选择可以做到这一点](https://mybinder.readthedocs.io/en/latest/introduction.html#how-can-i-prepare-a-repository-for-binder)，在社区中我们通常使用 GitHub 存储库或要点。
4.  您的材料公开后，请访问 [https://mybinder.org](https://mybinder.org)并按照其中的说明为您的工作表生成交互式环境。

暗示

[包含我们的交互式教程的](https://try.manim.community)存储库可以在[https://github.com/ManimCommunity/jupyter_examples](https://github.com/ManimCommunity/jupyter_examples)找到 。

## 谷歌合作实验室

也可以在 [Google Colaboratory](https://colab.research.google.com/)环境中安装 Manim。与 Binder 不同，您可以预先自定义和准备环境（例如 Manim 已安装并可以使用），而每次在 Google Colab 中启动新笔记本时，您都必须注意这一点。幸运的是，这并不是特别困难。

创建新笔记本后，将以下代码块粘贴到单元格中，然后执行它。

```sh
!sudo apt update
!sudo apt install libcairo2-dev ffmpeg \
    texlive texlive-latex-extra texlive-fonts-extra \
    texlive-latex-recommended texlive-science \
    tipa libpango1.0-dev
!pip install manim
!pip install IPython --upgrade
```

您应该开始看到 Colab 安装这些命令中指定的所有依赖项。执行完成后，会提示您重新启动运行时。单击单元输出底部的“重新启动运行时”按钮。您现在可以在 Colab 中使用 Manim 了！

要检查一切是否按预期工作，首先通过运行导入 Manim

```py
from manim import *
```

在新的代码单元中。然后创建另一个包含以下代码的单元格：

```py
%%manim -qm -v WARNING SquareToCircle

class SquareToCircle(Scene):
   def construct(self):
      square = Square()
      circle = Circle()
      circle.set_fill(PINK, opacity=0.5)
      self.play(Create(square))
      self.play(Transform(square, circle))
      self.wait()
```

运行此单元格后，应渲染并显示一个将正方形转换为圆形的短动画。
