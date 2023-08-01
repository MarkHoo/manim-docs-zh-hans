# 默认部分类型

合格名称：`manim.scene.section.DefaultSectionType`

```py
class DefaultSectionType(value)
```

Bases: str, Enum

节的类型可用于第三方应用程序。例如，演示系统可以使用这些类型来创建循环。

例子

可以为更多类型重新实现此类：

```py
class PresentationSectionType(str, Enum):
    # start, end, wait for continuation by user
    NORMAL = "presentation.normal"
    # start, end, immediately continue to next section
    SKIP = "presentation.skip"
    # start, end, restart, immediately continue to next section when continued by user
    LOOP = "presentation.loop"
    # start, end, restart, finish animation first when user continues
    COMPLETE_LOOP = "presentation.complete_loop"
```

属性

`NORMAL`
