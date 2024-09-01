# 移动摄像机场景

合格名称：`manim.scene.moving\_camera\_scene.MovingCameraScene`

```py
class MovingCameraScene(camera_class=<class 'manim.camera.moving_camera.MovingCamera'>, **kwargs)
```

Bases: `Scene`

这是一个场景，具有特殊的配置和属性，使其适合相机必须四处移动的情况。

> 也可以看看

> [`MovingCamera`]()


方法

|||
|-|-|
[`get_moving_mobjects`]()|此方法返回场景中正在移动的所有 Mobject 的列表，这些 Mobject 也在传递的动画中。


属性

`camera`


`get_moving_mobjects(*animations)`

此方法返回场景中正在移动的所有 Mobject 的列表，这些 Mobject 也在传递的动画中。

参数

**\*animations** ( [_Animation_]() ) – 将检查其 mobject 的动画。
