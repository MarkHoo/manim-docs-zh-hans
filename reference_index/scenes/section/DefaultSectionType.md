# 默认部分类型[#](#defaultsectiontype "此标题的固定链接")

合格名称：`manim.scene.section.DefaultSectionType`

_类_ DefaultSectionType (_值_)[\[来源\]](../_modules/manim/scene/section.html#DefaultSectionType)[#](#manim.scene.section.DefaultSectionType "此定义的固定链接")

基地：`str`,`Enum`

节的类型可用于第三方应用程序。例如，演示系统可以使用这些类型来创建循环。

例子

可以为更多类型重新实现此类：

class PresentationSectionType(str, Enum):
\# start, end, wait for continuation by user
NORMAL = "presentation.normal"
\# start, end, immediately continue to next section
SKIP = "presentation.skip"
\# start, end, restart, immediately continue to next section when continued by user
LOOP = "presentation.loop"
\# start, end, restart, finish animation first when user continues
COMPLETE_LOOP = "presentation.complete_loop"

Copy to clipboard

属性

`NORMAL`
