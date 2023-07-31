# logger_utils [#](#module-manim._config.logger_utils "此标题的固定链接")

创建和设置记录器的实用程序。

导入库后，可以通过`manim.logger`或 访问 Manim 的记录器。`logging.getLogger("manim")`Manim 还导出第二个对象 ，`console`该对象应用于在屏幕上打印不需要记录的消息。

两者`logger`都`console`使用该`rich`库来生成富文本格式。

课程

[`JSONFormatter`](manim._config.logger_utils.JSONFormatter.html#manim._config.logger_utils.JSONFormatter "manim._config.logger_utils.JSONFormatter")

以自定义 JSON 格式输出日志的格式化程序。

功能

make*logger（*解析器*，*详细程度\_）[\[来源\]](../_modules/manim/_config/logger_utils.html#make_logger)[#](#manim._config.logger_utils.make_logger "此定义的固定链接")

制作 manim 记录器和控制台。

参数

- **parser** ( _configparser.ConfigParser_ ) – 包含正在使用的任何 .cfg 文件的解析器。
- **verbosity** ( _str_ ) – 记录器的详细级别。

退货

manim 记录器和控制台。第一个控制台输出到 stdout，第二个控制台输出到 stderr。全部使用返回的主题 [`parse_theme()`](#manim._config.logger_utils.parse_theme "manim._config.logger_utils.parse_theme")。

返回类型

`logging.Logger`, `rich.Console`,`rich.Console`

也可以看看

[`make_config_parser()`](manim._config.utils.html#manim._config.utils.make_config_parser "manim._config.utils.make_config_parser"),[`parse_theme()`](#manim._config.logger_utils.parse_theme "manim._config.logger_utils.parse_theme")

笔记

假定`parser`仅包含与在顶层配置记录器相关的选项。

parse*theme（*解析器\_）[\[来源\]](../_modules/manim/_config/logger_utils.html#parse_theme)[#](#manim._config.logger_utils.parse_theme "此定义的固定链接")

配置丰富的记录器和控制台输出样式。

参数

**解析器**( _ConfigParser_ ) – 包含正在使用的任何 .cfg 文件的解析器。

退货

manim 记录器使用的丰富主题。

返回类型

`rich.Theme`

也可以看看

[`make_logger()`](#manim._config.logger_utils.make_logger "manim._config.logger_utils.make_logger")

set*file_logger (*场景名称*,*模块名称*,*日志目录\_)[\[来源\]](../_modules/manim/_config/logger_utils.html#set_file_logger)[#](#manim._config.logger_utils.set_file_logger "此定义的固定链接")

将文件处理程序添加到 manim 记录器。

文件的路径是使用 构建的`config.log_dir`。

参数

- **scene_name** ( _str_ ) – 场景的名称，用于日志文件的名称。
- **module_name** ( _str_ ) – 模块的名称，用于日志文件的名称。
- **log_dir** ( _Path_ ) – 存储日志文件的文件夹的路径。

返回类型

没有任何
