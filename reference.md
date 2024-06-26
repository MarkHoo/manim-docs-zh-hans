# 参考手册


本参考手册详细介绍了 Manim 中包含的模块、函数和变量，描述了它们的含义和用途。要了解如何使用 Manim，请参阅[教程](./tutorials_guides/tutorial.md)。有关自上次版本以来的更改列表，请参阅[更改日志](./changelogs/0.17.3-changelog.md)。

> 警告:
> 
> 链接到此处的页面目前正在开发中。

## 继承图

### 动画(Animations)

![](https://docs.manim.community/en/stable/_images/inheritance-1898b66b1682d0e7a6f6433d8d6f94d0094a7d72.svg)

### 相机(Cameras)

![](https://docs.manim.community/en/stable/_images/inheritance-10268a578e8b4136776d007b0b3bd4e30d50f4a0.svg)

### 对象(Mobjects)

![](https://docs.manim.community/en/stable/_images/inheritance-db7d27bd53559c1ae9add343e2649f89b2f14555.svg)

### 场景(Scenes)

![](https://docs.manim.community/en/stable/_images/inheritance-62a7880b4e0b659fb32a2261db4f2e9432426dd4.svg)


## 模块索引

- [动画](./reference_index/animation.md)
  - [动画片](./reference_index/animations/animation.md)
    - [动画片](./reference_index/animations/animation/Animation.md)
    - [等待](./reference_index/animations/animation/Wait.md)
  - [改变](./reference_index/animations/changing.md)
    - [动画边界](./reference_index/animations/changing/AnimatedBoundary.md)
    - [追踪路径](./reference_index/animations/changing/TracedPath.md)
  - [作品](./reference_index/animations/composition.md)
    - [动画集团](./reference_index/animations/composition/AnimationGroup.md)
    - [滞后启动](./reference_index/animations/composition/LaggedStart.md)
    - [滞后起始图](./reference_index/animations/composition/LaggedStartMap.md)
    - [演替](./reference_index/animations/composition/Succession.md)
  - [创建](./reference_index/animations/creation.md)
    - [按字母添加文本](./reference_index/animations/creation/AddTextLetterByLetter.md)
    - [逐字添加文本](./reference_index/animations/creation/AddTextWordByWord.md)
    - [创造](./reference_index/animations/creation/Create.md)
    - [绘制边框然后填充](./reference_index/animations/creation/DrawBorderThenFill.md)
    - [逐个字母删除文本](./reference_index/animations/creation/RemoveTextLetterByLetter.md)
    - [显示增加的子集](./reference_index/animations/creation/ShowIncreasingSubsets.md)
    - [显示部分](./reference_index/animations/creation/ShowPartial.md)
    - [逐一显示子对象](./reference_index/animations/creation/ShowSubmobjectsOneByOne.md)
    - [螺旋式](./reference_index/animations/creation/SpiralIn.md)
    - [取消创建](./reference_index/animations/creation/Uncreate.md)
    - [取消写入](./reference_index/animations/creation/Unwrite.md)
    - [写](./reference_index/animations/creation/Write.md)
  - [衰退](./reference_index/animations/fading.md)
    - [淡入](./reference_index/animations/fading/FadeIn.md)
    - [消退](./reference_index/animations/fading/FadeOut.md)
  - [生长](./reference_index/animations/growing.md)
    - [成长箭](./reference_index/animations/growing/GrowArrow.md)
    - [从中心成长](./reference_index/animations/growing/GrowFromCenter.md)
    - [从边缘成长](./reference_index/animations/growing/GrowFromEdge.md)
    - [从点成长](./reference_index/animations/growing/GrowFromPoint.md)
    - [从无到有](./reference_index/animations/growing/SpinInFromNothing.md)
  - [指示](./reference_index/animations/indication.md)
    - [应用波](./reference_index/animations/indication/ApplyWave.md)
    - [外接](./reference_index/animations/indication/Circumscribe.md)
    - [闪光](./reference_index/animations/indication/Flash.md)
    - [专注于](./reference_index/animations/indication/FocusOn.md)
    - [表明](./reference_index/animations/indication/Indicate.md)
    - [显示创建然后淡出](./reference_index/animations/indication/ShowCreationThenFadeOut.md)
    - [显示传递闪光](./reference_index/animations/indication/ShowPassingFlash.md)
    - [ShowPassingFlashWithThinningStrokeWidth](./reference_index/animations/indication/ShowPassingFlashWithThinningStrokeWidth.md)
    - [摆动](./reference_index/animations/indication/Wiggle.md)
  - [移动](./reference_index/animations/movement.md)
    - [复同伦](./reference_index/animations/movement/ComplexHomotopy.md)
    - [同伦](./reference_index/animations/movement/Homotopy.md)
    - [沿着路径移动](./reference_index/animations/movement/MoveAlongPath.md)
    - [相流](./reference_index/animations/movement/PhaseFlow.md)
    - [平滑向量同伦](./reference_index/animations/movement/SmoothedVectorizedHomotopy.md)
  - [数字](./reference_index/animations/numbers.md)
    - [将小数更改为值](./reference_index/animations/numbers/ChangeDecimalToValue.md)
    - [改变小数](./reference_index/animations/numbers/ChangingDecimal.md)
  - [回转](./reference_index/animations/rotation.md)
    - [旋转](./reference_index/animations/rotation/Rotate.md)
    - [旋转](./reference_index/animations/rotation/Rotating.md)
  - [专门](./reference_index/animations/specialized.md)
    - [播送](./reference_index/animations/specialized/Broadcast.md)
  - [速度调节器](./reference_index/animations/speedmodifier.md)
    - [改变速度](./reference_index/animations/speedmodifier/ChangeSpeed.md)
  - [转换](./reference_index/animations/transform.md)
    - [应用复数函数](./reference_index/animations/transform/ApplyComplexFunction.md)
    - [应用函数](./reference_index/animations/transform/ApplyFunction.md)
    - [应用矩阵](./reference_index/animations/transform/ApplyMatrix.md)
    - [应用方法](./reference_index/animations/transform/ApplyMethod.md)
    - [应用逐点函数](./reference_index/animations/transform/ApplyPointwiseFunction.md)
    - [应用逐点函数到中心](./reference_index/animations/transform/ApplyPointwiseFunctionToCenter.md)
    - [顺时针变换](./reference_index/animations/transform/ClockwiseTransform.md)
    - [逆时针变换](./reference_index/animations/transform/CounterclockwiseTransform.md)
    - [循环替换](./reference_index/animations/transform/CyclicReplace.md)
    - [淡出颜色](./reference_index/animations/transform/FadeToColor.md)
    - [淡入淡出变换](./reference_index/animations/transform/FadeTransform.md)
    - [淡入淡出变换片段](./reference_index/animations/transform/FadeTransformPieces.md)
    - [移动到目标](./reference_index/animations/transform/MoveToTarget.md)
    - [替换变换](./reference_index/animations/transform/ReplacementTransform.md)
    - [恢复](./reference_index/animations/transform/Restore.md)
    - [就地扩展](./reference_index/animations/transform/ScaleInPlace.md)
    - [收缩到中心](./reference_index/animations/transform/ShrinkToCenter.md)
    - [交换](./reference_index/animations/transform/Swap.md)
    - [转换](./reference_index/animations/transform/Transform.md)
    - [变换动画](./reference_index/animations/transform/TransformAnimations.md)
    - [从复制转换](./reference_index/animations/transform/TransformFromCopy.md)
  - [变换匹配部分](./reference_index/animations/transform_matching_parts.md)
    - [变换匹配抽象库](./reference_index/animations/transform_matching_parts/TransformMatchingAbstractBase.md)
    - [变换匹配形状](./reference_index/animations/transform_matching_parts/TransformMatchingShapes.md)
    - [TransformMatchingTex](./reference_index/animations/transform_matching_parts/TransformMatchingTex.md)
  - [更新者](./reference_index/animations/updaters.md)
    - [模块](./reference_index/animations/updaters.md)
- [相机](./reference_index/camera.md)
  - [相机](./reference_index/cameras/camera.md)
    - [背景彩色 VM 对象显示器](./reference_index/cameras/camera/BackgroundColoredVMobjectDisplayer.md)
    - [相机](./reference_index/cameras/camera/Camera.md)
  - [映射\_相机](./reference_index/cameras/mapping_camera.md)
    - [测绘相机](./reference_index/cameras/mapping_camera/MappingCamera.md)
    - [旧多相机](./reference_index/cameras/mapping_camera/OldMultiCamera.md)
    - [分屏摄像头](./reference_index/cameras/mapping_camera/SplitScreenCamera.md)
  - [移动相机](./reference_index/cameras/moving_camera.md)
    - [移动相机](./reference_index/cameras/moving_camera/MovingCamera.md)
  - [多相机](./reference_index/cameras/multi_camera.md)
    - [多机位](./reference_index/cameras/multi_camera/MultiCamera.md)
  - [三维相机](./reference_index/cameras/three_d_camera.md)
    - [三数码相机](./reference_index/cameras/three_d_camera/ThreeDCamera.md)
- [配置](./reference_index/configuration.md)
  - [模块索引](./reference_index/configuration.md)
    - [\_config](./reference_index/configurations/_config.md)
    - [实用程序](./reference_index/configurations/utils.md)
    - [logger_utils](./reference_index/configurations/logger_utils.md)
- [对象](./reference_index/mobject.md)
  - [框架](./reference_index/mobjects/frame.md)
    - [全屏矩形](./reference_index/mobjects/frame/FullScreenRectangle.md)
    - [屏幕矩形](./reference_index/mobjects/frame/ScreenRectangle.md)
  - [几何学](./reference_index/mobjects/geometry.md)
    - [模块](./reference_index/mobjects/geometry.md)
  - [图形](./reference_index/mobjects/graph.md)
    - [有向图](./reference_index/mobjects/graph/DiGraph.md)
    - [通用图](./reference_index/mobjects/graph/GenericGraph.md)
    - [图形](./reference_index/mobjects/graph/Graph.md)
  - [绘图](./reference_index/mobjects/graphing.md)
    - [模块](./reference_index/mobjects/graphing.md)
  - [标识](./reference_index/mobjects/logo.md)
    - [马尼姆旗帜](./reference_index/mobjects/logo/ManimBanner.md)
  - [矩阵](./reference_index/mobjects/matrix.md)
    - [十进制矩阵](./reference_index/mobjects/matrix/DecimalMatrix.md)
    - [整数矩阵](./reference_index/mobjects/matrix/IntegerMatrix.md)
    - [矩阵](./reference_index/mobjects/matrix/Matrix.md)
    - [对象矩阵](./reference_index/mobjects/matrix/MobjectMatrix.md)
  - [对象](./reference_index/mobjects/mobject.md)
    - [团体](./reference_index/mobjects/mobject/Group.md)
    - [对象](./reference_index/mobjects/mobject/Mobject.md)
  - [svg](./reference_index/mobjects/svg.md)
    - [模块](./reference_index/mobjects/svg.md)
  - [桌子](./reference_index/mobjects/table.md)
    - [十进制表](./reference_index/mobjects/table/DecimalTable.md)
    - [整数表](./reference_index/mobjects/table/IntegerTable.md)
    - [数学表](./reference_index/mobjects/table/MathTable.md)
    - [对象表](./reference_index/mobjects/table/MobjectTable.md)
    - [桌子](./reference_index/mobjects/table/Table.md)
  - [文本](./reference_index/mobjects/text.md)
    - [模块](./reference_index/mobjects/text.md)
  - [三个\_d](./reference_index/mobjects/three_d.md)
    - [模块](./reference_index/mobjects/three_d.md)
  - [类型](./reference_index/mobjects/types.md)
    - [模块](./reference_index/mobjects/types.md)
  - [实用程序](./reference_index/mobjects/utils.md)
  - [价值追踪器](./reference_index/mobjects/value_tracker.md)
    - [复杂价值追踪器](./reference_index/mobjects/value_tracker/ComplexValueTracker.md)
    - [价值追踪器](./reference_index/mobjects/value_tracker/ValueTracker.md)
  - [矢量场](./reference_index/mobjects/vector_field.md)
    - [箭头矢量场](./reference_index/mobjects/vector_field/ArrowVectorField.md)
    - [流线型](./reference_index/mobjects/vector_field/StreamLines.md)
    - [矢量场](./reference_index/mobjects/vector_field/VectorField.md)
- [场景](./reference_index/scene.md)
  - [移动相机场景](./reference_index/scenes/moving_camera_scene.md)
    - [移动相机场景](./reference_index/scenes/moving_camera_scene/MovingCameraScene.md)
  - [部分](./reference_index/scenes/section.md)
    - [默认节类型](./reference_index/scenes/section/DefaultSectionType.md)
    - [部分](./reference_index/scenes/section/Section.md)
  - [场景](./reference_index/scenes/scene.md)
    - [重新运行场景处理程序](./reference_index/scenes/scene/RerunSceneHandler.md)
    - [场景](./reference_index/scenes/scene/Scene.md)
  - [场景文件编写器](./reference_index/scenes/scene_file_writer.md)
    - [场景文件编写器](./reference_index/scenes/scene_file_writer/SceneFileWriter.md)
  - [三维场景](./reference_index/scenes/three_d_scene.md)
    - [特别三场景](./reference_index/scenes/three_d_scene/SpecialThreeDScene.md)
    - [三场景](./reference_index/scenes/three_d_scene/ThreeDScene.md)
  - [矢量空间场景](./reference_index/scenes/vector_space_scene.md)
    - [线性变换场景](./reference_index/scenes/vector_space_scene/LinearTransformationScene.md)
    - [矢量场景](./reference_index/scenes/vector_space_scene/VectorScene.md)
  - [缩放场景](./reference_index/scenes/zoomed_scene.md)
    - [缩放场景](./reference_index/scenes/zoomed_scene/ZoomedScene.md)
- [实用程序和其他模块](./reference_index/utilities_misc.md)
  - [模块索引](./reference_index/utilities_misc.md)
    - [常量](./reference_index/utilities_miscs/constants.md)
    - [贝塞尔](./reference_index/utilities_miscs/bezier.md)
    - [颜色](./reference_index/utilities_miscs/color.md)
    - [命令](./reference_index/utilities_miscs/commands.md)
    - [配置操作](./reference_index/utilities_miscs/config_ops.md)
    - [弃用](./reference_index/utilities_miscs/deprecation.md)
    - [调试](./reference_index/utilities_miscs/debug.md)
    - [文档构建](./reference_index/utilities_miscs/docbuild.md)
    - [散列](./reference_index/utilities_miscs/hashing.md)
    - [ipython_magic](./reference_index/utilities_miscs/ipython_magic.md)
    - [图片](./reference_index/utilities_miscs/images.md)
    - [可迭代对象](./reference_index/utilities_miscs/iterables.md)
    - [路径](./reference_index/utilities_miscs/paths.md)
    - [速率函数](./reference_index/utilities_miscs/rate_functions.md)
    - [简单函数](./reference_index/utilities_miscs/simple_functions.md)
    - [声音](./reference_index/utilities_miscs/sounds.md)
    - [空间操作](./reference_index/utilities_miscs/space_ops.md)
    - [特克斯](./reference_index/utilities_miscs/tex.md)
    - [tex_templates](./reference_index/utilities_miscs/tex_templates.md)
    - [tex_file_writing](./reference_index/utilities_miscs/tex_file_writing.md)


