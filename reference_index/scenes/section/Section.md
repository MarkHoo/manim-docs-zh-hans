# 部分


合格名称：`manim.scene.section.Section`

```py
class Section(type, video, name, skip_animations)
```

Bases: `object`

一个[`Scene`]()可以被分割成多个Section。请参阅[文档]()以获取更多信息。它由多个动画组成。

参数

*   **type**( _str_ ) –
    
*   **video**( _str_ _|_\_None_) –
    
*   **name**( _str_ ) –
    
*   **skip_animations**( _bool_ ) –
    

type

第三方应用程序可以使用它来对不同类型的部分进行分类。

video

包含属于相对于节目录的节的动画的视频文件的路径。如果`None`，则该部分将不会被保存。

name

此部分的人类可读的非唯一名称。

skip_animations

当 时，跳过本节中的动画渲染`True`。

partial_movie_files

属于本节的动画。


> 也可以看看

> [`DefaultSectionType`](), `CairoRenderer.update_skipping_status()`,`OpenGLRenderer.update_skipping_status()`


方法

|||
|-|-|
[`get_clean_partial_movie_files`]()|返回所有不属于`None`.
[`get_dict`]()|获取带有输出视频元数据的字典表示。
[`is_empty`](")|检查该部分是否为空。


`get_clean_partial_movie_files()`

返回所有不属于`None`.

返回类型

列表\[字符串\]

`get_dict(sections_dir)`

获取带有输出视频元数据的字典表示。

每个部分都使用此函数的输出来构建部分索引文件。`sections_dir`输出视频必须在执行此方法之前创建。这是分段视频 API 的主要部分。

参数

**sections_dir** (_路径_) –

返回类型

字典\[str，任意\]

`is_empty()`

检查该部分是否为空。

请注意，由 表示的动画`None`也被计算在内。

返回类型

布尔值