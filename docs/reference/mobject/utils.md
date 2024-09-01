# 实用工具

用于处理 mobject 的实用程序。

Functions

`get_mobject_class()`

获取 mobject 基类，具体取决于当前活动的渲染器。

> 笔记

> 此方法旨在用于 Manim 本身的代码库或插件中，其中代码应独立于所选渲染器工作。

例子

该函数必须显式导入。我们测试返回的类的名称是否是已知的 mobject 基类之一：

```sh
>>> from manim.mobject.utils import get_mobject_class
>>> get_mobject_class().__name__ in ['Mobject', 'OpenGLMobject']
True
```

返回类型

type

`get_point_mobject_class()`

获取点云 mobject 类，具体取决于当前活动的渲染器。

> 笔记

> 此方法旨在用于 Manim 本身的代码库或插件中，其中代码应独立于所选渲染器工作。

例子

该函数必须显式导入。我们测试返回的类的名称是否是已知的 mobject 基类之一：

```sh
>>> from manim.mobject.utils import get_point_mobject_class
>>> get_point_mobject_class().__name__ in ['PMobject', 'OpenGLPMobject']
True
```

返回类型

type

`get_vectorized_mobject_class()`

获取矢量化 mobject 类，具体取决于当前活动的渲染器。

> 笔记

> 此方法旨在用于 Manim 本身的代码库或插件中，其中代码应独立于所选渲染器工作。

例子

该函数必须显式导入。我们测试返回的类的名称是否是已知的 mobject 基类之一：

```sh
>>> from manim.mobject.utils import get_vectorized_mobject_class
>>> get_vectorized_mobject_class().__name__ in ['VMobject', 'OpenGLVMobject']
True
```

返回类型

type
