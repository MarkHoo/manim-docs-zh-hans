# \_配置[#](#module-manim._config "此标题的固定链接")

设置全局配置和记录器。

功能

临时配置（_临时_）[\[来源\]](../_modules/manim/_config.html#tempconfig)[#](#manim._config.tempconfig "此定义的固定链接")

临时修改全局`config`对象的上下文管理器。

在语句内部`with`，将使用修改后的配置。上下文管理器退出后，配置将恢复到原始状态。

参数

**temp** ( [_ManimConfig_](manim._config.utils.ManimConfig.html#manim._config.utils.ManimConfig "manim._config.utils.ManimConfig") _|_ _dict_ ) – 其键将用于临时更新全局的对象 `config`。

返回类型

\_GeneratorContextManager

例子

用于临时更改某些配置选项的默认值。`with tempconfig({...})`

> > \> config\["frame_height"\]
> > 8.0
> > \> with tempconfig({"frame_height": 100.0}):
> > ... print(config\["frame_height"\])
> > ...
> > 100.0
> > \> config\["frame_height"\]
> > 8.0

Copy to clipboard
