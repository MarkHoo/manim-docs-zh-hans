# 重新运行场景处理程序

合格名称：`manim.scene.scene.RerunSceneHandler`

```py
class RerunSceneHandler(queue)
```

Bases: `FileSystemEventHandler`

一个类，用于在输入文件修改后处理重新运行场景。


方法

|||
|-|-|
[`on_modified`]()|当文件或目录被修改时调用。


on_modified（_事件_）

当文件或目录被修改时调用。

参数

**event** (`DirModifiedEvent`或`FileModifiedEvent`) – 表示文件/目录修改的事件。