# Windows

--------------------------

## 所需依赖项

- Windows系统版本要求为 `Windows10+`
- Python版本要求： `Python3.8+`
- `FFmpeg`

### 安装 Python

1. 官网下载 [Python]()
2. 双击安装包，勾选 `Add To Path` ，安装时会自动为你配置好Python环境变量
3. 安装路径，删除掉中间的路径，直接安装到C盘根目录，比如Python3.9： `C:\Python39`

--------------------------

> 提示：使用 `pip` 安装时，最好使用镜像，否则可能会因为网络安装失败，因为安装依赖较多且依赖包较大。
> 提示：提前升级 `pip` 到最新版本，否则会在本地安装依赖包时会报错提示因版本问题要求更新 `pip` ，命令如下：

```sh
python -m pip install --upgrade pip -i https://pypi.douban.com/simple
```

### 安装 Manim

```sh
pip install manim -i https://pypi.douban.com/simple
```

运行以下命令，检查是否安装完成

```sh
manim
```

--------------------------

### 安装 `FFmpeg`

1. 官网下载 [FFmpeg](https://ffmpeg.org/download.html#build-windows)，或者这里 [点击下载FFmpeg](https://www.gyan.dev/ffmpeg/builds/ffmpeg-release-essentials.7z) (推荐)
2. 将下载好的FFmpeg压缩包解压出来，把文件夹名称改为 `ffmpeg` ,然后将文件夹剪切或复制到C盘根目录
3. 配置环境变量。依次打开 `Windows设置 -> 系统 -> 关于 -> 高级系统设置 -> 高级 -> 环境变量` ，然后根据需求在user或者系统变量里的 `Path` 中增加一条FFmpeg的bin路径，如： `C:\ffmpeg\bin` ，然后依次点击确定关闭所有窗口。
4. 用快捷键 `Windows键 + r` 打开cmd，输入 `ffmpeg` 命令看能否正常运行，也可通过 `ffmpeg -version` 查看FFmpeg版本信息。

> 提示：Windows键也就是Windows系统图标的那个键，一般在 `Ctrl` 旁边

--------------------------

## 可选依赖项

`MiKTeX`: 如果需要渲染方程或公式等等，需要安装。

### 安装 `MiKTeX`

1. 官网下载 [MiKTeX](https://miktex.org/download)
2. 将下载好的 `MiKTeX` 的exe文件右键管理员打开，一直下一步即可，中间有选择为user安装或者为所有用户安装，可根据自身需要选择。

## 安装完成

恭喜！安装完成，开始愉快的学习吧！
