# 插件

插件是扩展 Manim 核心功能的特性。由于 Manim 是可扩展的，并不是所有东西都属于它的核心，我们将介绍如何安装、使用和创建您自己的插件。

> 笔记

> 插件的标准命名约定是在插件前加上 `manim-`. 这使用户可以轻松地在 PyPI 等包存储库中找到它们。

> 警告

> 插件功能是新的并且正在积极开发中。期待有关安装、使用和创建插件的最佳实践的更新；以及新的子命令/标志`manim plugins`

> 提示

> 有关可用插件的列表，请参阅https://plugins.manim.community/。

### 安装插件

可以通过以下`pip` 命令轻松安装插件：

```shell
pip install manim-*
```

安装插件后，您可以使用该命令列出可用的插件，请参阅以下帮助输出：`manim plugins`

```shell
manim plugins -h
Usage: manim plugins [OPTIONS]

  Manages Manim plugins.

Options:
-l, --list  List available plugins
-h, --help  Show this message and exit.

Made with <3 by Manim Community developers.
```

您可以这样列出插件：

```shell
manim plugins -l
Plugins:
• manim_plugintemplate
```

### 在项目中使用插件

要启用插件manim.cfg或应使用命令行参数。

> 重点

> 插件应该是插件的模块名称而不是 PyPi 名称。

通过启用插件`manim.cfg`

```shell
[CLI]
plugins = manim_rubikscube
```

要指定多个插件，必须使用逗号分隔值。

```sh
[CLI]
plugins = manim_rubikscube, manim_plugintemplate
```

### 创建插件

插件旨在扩展 Manim 的核心功能。如果您不确定某个功能是否应该包含在 Manim 的核心中，请随时在Discord 服务器上提问。访问 PyPI.org 上的 manim-plugintemplate，它是创建插件的深入教程。

```sh
pip install manim-plugintemplate
```

manim 插件的唯一要求是它们指定一个带有组的入口点，"manim.plugins". 这允许 Manim 发现用户环境中可用的插件。关于插件的目录结构、构建系统和命名的一切都完全取决于您作为作者的决定。前面提到的模板插件只是一个使用 Poetry 的模型，因为这是 Manim 使用的构建系统。插件的入口点可以在 poetry 中指定为：

```sh
[tool.poetry.plugins."manim.plugins"]
"name" = "object_reference"
```

这`name`是插件模块的名称。

此处`object_reference`可以指向模块中的函数或模块本身。例如，

```sh
[tool.poetry.plugins."manim.plugins"]
"manim_plugintemplate" = "manim_plugintemplate"
```

这里使用了一个模块作为`object_reference`，启用该插件后，Manim 将查找`__all__`定义在中的关键字，`manim_plugintemplate`并将所有内容作为全局变量一一查找。

如果`object_reference`是一个函数，Manim 调用该函数并期望该函数返回需要全局定义的模块或函数的列表。

例如

```
[tool.poetry.plugins."manim.plugins"]
"manim_plugintemplate" = "manim_awesomeplugin.imports:setup_things"
```

在这里，Manim 将调用`setup_things`定义 的函数`manim_awesomeplugin.imports`并调用它。它返回将全局导入的函数或模块列表。
