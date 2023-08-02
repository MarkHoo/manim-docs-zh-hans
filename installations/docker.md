# Docker

社区维护着一个 docker 镜像，可以 [在 DockerHub 上](https://hub.docker.com/r/manimcommunity/manim)找到。对于我们的图像`manimcommunity/manim`，有以下标签：

- `latest`[：对应主分支](https://github.com/ManimCommunity/manim)的最新版本，
- `stable`：最新发布的版本（根据 [发布页面](https://github.com/ManimCommunity/manim/releases)），
- `vX.Y.Z`：任何特定的发布版本（根据 [发布页面](https://github.com/ManimCommunity/manim/releases)）。

> 笔记

> 在 Docker 容器中使用 Manim 的 CLI 时， 不支持某些标志，例如`-p`（预览文件）和（在文件浏览器中显示输出文件）。`-f`

## Docker 容器的基本用法

假设您可以通过终端（bash / PowerShell）访问系统上的 docker 安装`docker`，则可以 使用以下命令`CircleToSquare`在文件 test_scenes.py 中渲染场景。

```sh
docker run --rm -it -v "/full/path/to/your/directory:/manim" manimcommunity/manim manim -qm test_scenes.py CircleToSquare
```

> 提示

> 对于 Linux 用户，让容器中的用户写入已安装的卷时可能会出现权限问题。添加到 CLI 参数以防止创建不属于您的用户的输出文件。` --user="$(id -u):$(id -g)"``docker `

您还可以创建一个可以根据自己的喜好进行修改的命名容器，而不是使用上面概述的“一次性容器”方法。第一次运行

```sh
docker run -it --name my-manim-container -v "/full/path/to/your/directory:/manim" manimcommunity/manim /bin/bash
```

在容器内获取交互式 shell，允许您安装更多依赖项（例如使用 texlive 包 `tlmgr`）。一旦您满意，请立即退出容器。然后，在使用它之前，通过运行启动容器

```sh
docker start my-manim-container
```

它在后台启动容器。`CircleToSquare`然后，要渲染文件中的场景`test_scenes.py`，请运行

```sh
docker exec -it my-manim-container manim -qm test_scenes.py CircleToSquare
```

## 通过 Docker 运行 JupyterLab 

使用 Docker 映像的另一种替代方法是启动本地 JupyterLab 实例。为此，只需运行

```sh
docker run -it -p 8888:8888 manimcommunity/manim jupyter lab --ip=0.0.0.0
```

然后按照终端中的说明进行操作。
