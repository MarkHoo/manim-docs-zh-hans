# 实用程序[#](#module-manim.mobject.utils "此标题的固定链接")

用于处理 mobject 的实用程序。

功能

获取对象类( )[\[来源\]](../_modules/manim/mobject/utils.html#get_mobject_class)[#](#manim.mobject.utils.get_mobject_class "此定义的固定链接")

获取 mobject 基类，具体取决于当前活动的渲染器。

笔记

此方法旨在用于 Manim 本身的代码库或插件中，其中代码应独立于所选渲染器工作。

例子

该函数必须显式导入。我们测试返回的类的名称是否是已知的 mobject 基类之一：

> > \> from manim.mobject.utils import get_mobject_class
> > \> get_mobject_class().\_\_name\_\_ in \['Mobject', 'OpenGLMobject'\]
> > True

Copy to clipboard

返回类型

类型

获取点对象类( )[\[来源\]](../_modules/manim/mobject/utils.html#get_point_mobject_class)[#](#manim.mobject.utils.get_point_mobject_class "此定义的固定链接")

获取点云 mobject 类，具体取决于当前活动的渲染器。

笔记

此方法旨在用于 Manim 本身的代码库或插件中，其中代码应独立于所选渲染器工作。

例子

该函数必须显式导入。我们测试返回的类的名称是否是已知的 mobject 基类之一：

> > \> from manim.mobject.utils import get_point_mobject_class
> > \> get_point_mobject_class().\_\_name\_\_ in \['PMobject', 'OpenGLPMobject'\]
> > True

Copy to clipboard

返回类型

类型

获取向量化对象类( )[\[来源\]](../_modules/manim/mobject/utils.html#get_vectorized_mobject_class)[#](#manim.mobject.utils.get_vectorized_mobject_class "此定义的固定链接")

获取矢量化 mobject 类，具体取决于当前活动的渲染器。

笔记

此方法旨在用于 Manim 本身的代码库或插件中，其中代码应独立于所选渲染器工作。

例子

该函数必须显式导入。我们测试返回的类的名称是否是已知的 mobject 基类之一：

> > \> from manim.mobject.utils import get_vectorized_mobject_class
> > \> get_vectorized_mobject_class().\_\_name\_\_ in \['VMobject', 'OpenGLVMobject'\]
> > True

Copy to clipboard

返回类型

类型
