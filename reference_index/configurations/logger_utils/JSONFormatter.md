# JSONFormatter 

合格名称：`manim.\_config.logger\_utils.JSONFormatter`

```py
class JSONFormatter(fmt=None, datefmt=None, style='%', validate=True)
```

Bases: Formatter

以自定义 JSON 格式输出日志的格式化程序。

此类在内部用于测试目的。

使用指定的格式字符串初始化格式化程序。

使用指定的格式字符串或如上所述的默认值初始化格式化程序。允许使用可选的 datefmt 参数进行专门的日期格式设置。如果省略 datefmt，您将获得类似 ISO8601（或类似 RFC 3339）的格式。

使用样式参数“%”、“{”或“$”来指定要在格式字符串中使用 % 格式、 `str.format()`( `{}`) 格式或 格式之一。`string.Template`

3.2 版本更改：添加了`style`参数。

方法

|||
|-|-|
[`format`]()|将记录格式化为自定义 JSON 格式。

属性

`default_msec_format`
`default_time_format`

格式（_记录_）[\[来源\]](../_modules/manim/_config/logger_utils.html#JSONFormatter.format)[#](#manim._config.logger_utils.JSONFormatter.format "此定义的固定链接")

将记录格式化为自定义 JSON 格式。

参数

**记录**（_字典_）–

返回类型

斯特
