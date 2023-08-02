# Conda

## 所需的依赖项

要创建 conda 环境，您必须首先安装 [conda](https://docs.conda.io/projects/conda/en/latest/user-guide/install/download.html) 或[mamba](https://mamba.readthedocs.io/en/latest/installation.html)这两个最流行的 conda 客户端。

安装 conda 后，您可以创建一个新环境并`manim`通过运行在里面安装

```sh
conda create -n my-manim-environment
conda activate my-manim-environment
conda install -c conda-forge manim
```

由于所有依赖项（LaTeX 除外）均由 conda 处理，因此您无需担心需要安装额外的依赖项。

## 可选依赖项

例如，为了利用 Manim 的 LaTeX 接口来渲染方程，还必须安装 LaTeX。请注意，这是一个可选的依赖项：如果您不打算使用 LaTeX，则不必安装它。

您可以按照[Windows]()、 [Linux]()或 [macOS]()的可选依赖项步骤安装 LaTeX 。

## 与Manim一起工作

此时，您应该已经安装好了 Manim，请前往我们的[快速入门教程]()，了解如何制作您自己的*动画*！
