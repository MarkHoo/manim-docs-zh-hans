# 渲染器类型

合格名称：`manim.constants.RendererType`


```py
class RendererType(value)
```

Bases: `Enum`

可分配给该属性的所有渲染器类型的枚举`config.renderer`。

Manim 的配置允许将字符串值分配给渲染器设置，然后将这些值替换为相应的枚举对象。换句话说，您可以运行：

```py
config.renderer = "opengl"
```

然后检查渲染器发现该属性已采用该值：

```py
<RendererType.OPENGL: 'opengl'>
```


属性

|||
|-|-|
[`CAIRO`]()|基于 cairo 后端的渲染器。
[`OPENGL`]()|基于 OpenGL 的渲染器。



`CAIRO = 'cairo'`

基于 cairo 后端的渲染器。



`OPENGL = 'opengl'`

基于 OpenGL 的渲染器。
