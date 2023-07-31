# 渲染器类型[#](#renderertype "此标题的固定链接")

合格名称：`manim.constants.RendererType`

渲染器类型*类*（_值_）[\[来源\]](../_modules/manim/constants.html#RendererType)[#](#manim.constants.RendererType "此定义的固定链接")

基地：`Enum`

可分配给该属性的所有渲染器类型的枚举`config.renderer`。

Manim 的配置允许将字符串值分配给渲染器设置，然后将这些值替换为相应的枚举对象。换句话说，您可以运行：

config.renderer = "opengl"

Copy to clipboard

然后检查渲染器发现该属性已采用该值：

<RendererType.OPENGL: 'opengl'>

Copy to clipboard

属性

[`CAIRO`](#manim.constants.RendererType.CAIRO "manim.constants.RendererType.CAIRO")

基于 cairo 后端的渲染器。

[`OPENGL`](#manim.constants.RendererType.OPENGL "manim.constants.RendererType.OPENGL")

基于 OpenGL 的渲染器。

开罗*=* _'开罗'_ [#](#manim.constants.RendererType.CAIRO "此定义的固定链接")[](#manim.constants.RendererType.CAIRO "此定义的固定链接")

基于 cairo 后端的渲染器。

OPENGL _=_ _'opengl'_ [#](#manim.constants.RendererType.OPENGL "此定义的固定链接")[](#manim.constants.RendererType.OPENGL "此定义的固定链接")

基于 OpenGL 的渲染器。
