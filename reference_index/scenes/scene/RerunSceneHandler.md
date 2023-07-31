重新运行场景处理程序[#](#rerunscenehandler "此标题的固定链接")
============================================

合格名称：`manim.scene.scene.RerunSceneHandler`

_类_ RerunSceneHandler (_队列_)[\[来源\]](../_modules/manim/scene/scene.html#RerunSceneHandler)[#](#manim.scene.scene.RerunSceneHandler "此定义的固定链接")

基地：`FileSystemEventHandler`

一个类，用于在输入文件修改后处理重新运行场景。

方法

  

[`on_modified`](#manim.scene.scene.RerunSceneHandler.on_modified "manim.scene.scene.RerunSceneHandler.on_modified")

当文件或目录被修改时调用。

on_modified（_事件_）[\[来源\]](../_modules/manim/scene/scene.html#RerunSceneHandler.on_modified)[#](#manim.scene.scene.RerunSceneHandler.on_modified "此定义的固定链接")

当文件或目录被修改时调用。

参数

**event** (`DirModifiedEvent`或`FileModifiedEvent`) – 表示文件/目录修改的事件。