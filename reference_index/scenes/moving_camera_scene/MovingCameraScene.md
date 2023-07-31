# 移动相机场景[#](#movingcamerascene "此标题的固定链接")

合格名称：`manim.scene.moving\_camera\_scene.MovingCameraScene`

_类_ MovingCameraScene ( _camera_class=<class 'manim.camera.movi​​ng_camera.MovingCamera'>_ , _\*\*kwargs_ )[\[来源\]](../_modules/manim/scene/moving_camera_scene.html#MovingCameraScene)[#](#manim.scene.moving_camera_scene.MovingCameraScene "此定义的固定链接")

基地：[`Scene`](manim.scene.scene.Scene.html#manim.scene.scene.Scene "手动场景.场景.场景")

这是一个场景，具有特殊的配置和属性，使其适合相机必须四处移动的情况。

也可以看看

[`MovingCamera`](manim.camera.moving_camera.MovingCamera.html#manim.camera.moving_camera.MovingCamera "manim.camera.movi​​ng_camera.MovingCamera")

方法

[`get_moving_mobjects`](#manim.scene.moving_camera_scene.MovingCameraScene.get_moving_mobjects "manim.scene.movi​​ng_camera_scene.MovingCameraScene.get_moving_mobjects")

此方法返回场景中正在移动的所有 Mobject 的列表，这些 Mobject 也在传递的动画中。

属性

`camera`

get*moving_mobjects ( *\*动画\_)[\[来源\]](../_modules/manim/scene/moving_camera_scene.html#MovingCameraScene.get_moving_mobjects)[#](#manim.scene.moving_camera_scene.MovingCameraScene.get_moving_mobjects "此定义的固定链接")

此方法返回场景中正在移动的所有 Mobject 的列表，这些 Mobject 也在传递的动画中。

参数

**\*animations** ( [_Animation_](manim.animation.animation.Animation.html#manim.animation.animation.Animation "manim.animation.animation.Animation") ) – 将检查其 mobject 的动画。
