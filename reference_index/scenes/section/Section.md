# 部分
==================================================================

合格名称：`manim.scene.section.Section`

_类_ 部分（_类型_，_视频_，_名称_， _skip_animations_）[\[来源\]](../_modules/manim/scene/section.html#Section)[#](#manim.scene.section.Section "此定义的固定链接")

基地：`object`

A[`Scene`](manim.scene.scene.Scene.html#manim.scene.scene.Scene "手动场景.场景.场景")可以被分割成多个Section。请参阅[文档](../tutorials/output_and_config.html)以获取更多信息。它由多个动画组成。

参数

*   **类型**( _str_ ) –
    
*   **视频**( _str_ _|__无_) –
    
*   **名称**( _str_ ) –
    
*   **跳过动画**( _bool_ ) –
    

输入[#](#manim.scene.section.Section.type "此定义的固定链接")

第三方应用程序可以使用它来对不同类型的部分进行分类。

视频[#](#manim.scene.section.Section.video "此定义的固定链接")

包含属于相对于节目录的节的动画的视频文件的路径。如果`None`，则该部分将不会被保存。

名字[#](#manim.scene.section.Section.name "此定义的固定链接")

此部分的人类可读的非唯一名称。

跳过动画[#](#manim.scene.section.Section.skip_animations "此定义的固定链接")

当 时，跳过本节中的动画渲染`True`。

部分电影文件[#](#manim.scene.section.Section.partial_movie_files "此定义的固定链接")

属于本节的动画。

也可以看看

[`DefaultSectionType`](manim.scene.section.DefaultSectionType.html#manim.scene.section.DefaultSectionType "manim.scene.section.DefaultSectionType"), `CairoRenderer.update_skipping_status()`,`OpenGLRenderer.update_skipping_status()`

方法

  

[`get_clean_partial_movie_files`](#manim.scene.section.Section.get_clean_partial_movie_files "manim.scene.section.Section.get_clean_partial_movie_files")

返回所有不属于`None`.

[`get_dict`](#manim.scene.section.Section.get_dict "manim.scene.section.Section.get_dict")

获取带有输出视频元数据的字典表示。

[`is_empty`](#manim.scene.section.Section.is_empty "manim.scene.section.Section.is_empty")

检查该部分是否为空。

获取\_clean\_partial\_movie\_files ( )[\[来源\]](../_modules/manim/scene/section.html#Section.get_clean_partial_movie_files)[#](#manim.scene.section.Section.get_clean_partial_movie_files "此定义的固定链接")

返回所有不属于`None`.

返回类型

列表\[字符串\]

get_dict ( _sections_dir_ )[\[来源\]](../_modules/manim/scene/section.html#Section.get_dict)[#](#manim.scene.section.Section.get_dict "此定义的固定链接")

获取带有输出视频元数据的字典表示。

每个部分都使用此函数的输出来构建部分索引文件。`sections_dir`输出视频必须在执行此方法之前创建。这是分段视频 API 的主要部分。

参数

**sections_dir** (_路径_) –

返回类型

字典\[str，任意\]

为空( )[\[来源\]](../_modules/manim/scene/section.html#Section.is_empty)[#](#manim.scene.section.Section.is_empty "此定义的固定链接")

检查该部分是否为空。

请注意，由 表示的动画`None`也被计算在内。

返回类型

布尔值