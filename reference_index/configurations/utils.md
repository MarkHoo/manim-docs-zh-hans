# 实用程序[#](#module-manim._config.utils "此标题的固定链接")

用于创建和设置配置的实用程序。

该模块导出的主类是[`ManimConfig`](manim._config.utils.ManimConfig.html#manim._config.utils.ManimConfig "manim._config.utils.ManimConfig"). 此类包含所有配置选项，包括帧几何形状（例如帧高度/宽度、帧速率）、输出（例如目录、日志记录）、样式（例如背景颜色、透明度）和一般行为（例如编写电影与编写单个电影）框架）。

有关 Manim 配置系统的介绍，请参阅[配置。](../guides/configuration.html)

课程

[`ManimConfig`](manim._config.utils.ManimConfig.html#manim._config.utils.ManimConfig "manim._config.utils.ManimConfig")

类似字典的类存储所有配置选项。

[`ManimFrame`](manim._config.utils.ManimFrame.html#manim._config.utils.ManimFrame "manim._config.utils.ManimFrame")

功能

配置文件路径( )[\[来源\]](../_modules/manim/_config/utils.html#config_file_paths)[#](#manim._config.utils.config_file_paths "此定义的固定链接")

`.cfg`将搜索文件的路径。

首次导入 manim 时，它会处理`.cfg`它找到的所有文件。此函数返回搜索这些文件的位置。按照优先级升序排列，它们是：库范围的配置文件、用户范围的配置文件和文件夹范围的配置文件。

库范围的配置文件决定 manim 的默认行为。用户范围的配置文件存储在用户的主文件夹中，并确定每当用户从系统中的任何位置调用 manim 时的行为。文件夹范围的配置文件仅影响同一文件夹中的场景。后两个文件是可选的。

这些文件（如果存在）旨在加载到单个 `configparser.ConfigParser`对象中，然后由 [`ManimConfig`](manim._config.utils.ManimConfig.html#manim._config.utils.ManimConfig "manim._config.utils.ManimConfig").

退货

可能包含文件的路径列表`.cfg`，按优先级升序排列。

返回类型

列表\[ `Path`\]

也可以看看

[`make_config_parser()`](#manim._config.utils.make_config_parser "manim._config.utils.make_config_parser"), [`ManimConfig.digest_file()`](manim._config.utils.ManimConfig.html#manim._config.utils.ManimConfig.digest_file "manim._config.utils.ManimConfig.digest_file"),[`ManimConfig.digest_parser()`](manim._config.utils.ManimConfig.html#manim._config.utils.ManimConfig.digest_parser "manim._config.utils.ManimConfig.digest_parser")

笔记

用户范围的配置文件的位置是特定于操作系统的。

make*config_parser（*自定义文件=无\_）[\[来源\]](../_modules/manim/_config/utils.html#make_config_parser)[#](#manim._config.utils.make_config_parser "此定义的固定链接")

创建一个`ConfigParser`对象并加载任何`.cfg`文件。

用户范围文件（如果存在）将覆盖库范围文件。文件夹范围的文件（如果存在）将覆盖其他两个文件。

可以通过传递 来忽略文件夹范围的文件`custom_file`。但是，用户范围和库范围的配置文件不能被忽略。

参数

**custom_file** ( _str_ _|_ _os.PathLike_ _|_ _None_ ) – 自定义配置文件的路径。如果使用，相关目录中的文件夹范围文件将被忽略（如果存在）。如果没有，则将使用文件夹范围的文件（如果存在）。

退货

包含在找到的 .cfg 文件中找到的配置选项的解析器。它保证至少包含在库范围文件中找到的配置选项。

返回类型

`ConfigParser`

也可以看看

[`config_file_paths()`](#manim._config.utils.config_file_paths "manim._config.utils.config_file_paths")
