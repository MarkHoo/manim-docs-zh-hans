# 颜色

用于处理颜色和预定义颜色常量的实用程序。

## 颜色数据结构

|||
|-|-|
|[`core`]()||

Manim 的（内部）颜色数据结构和一些用于颜色转换的实用程序。

## 预定义颜色

Manim 中有多种预定义颜色可用：

- 中列出的颜色[`color.manim_colors`]()被加载到 Manim 的全局名称空间中。
- [`color.AS2700`]()、[`color.X11`]()、 和中的颜色[`color.XKCD`]()需要通过其模块（在 Manim 的全局命名空间中可用）访问，或单独导入。例如：

```
>>> from manim import XKCD
>>> XKCD.AVOCADO
ManimColor('#90B134')
```

  或者，另一种选择：

```
>>> from manim.utils.color.XKCD import AVOCADO
>>> AVOCADO
ManimColor('#90B134')
```

以下模块包含预定义的颜色常量：

|||
|-|-|
[`manim_colors`]()|全局名称空间中包含的颜色。
[`AS2700`]()|澳大利亚颜色标准
[`BS381`]()|英国颜色标准
[`XKCD`]()|XKCD 颜色名称调查中的颜色
[`X11`]()|X11 颜色
