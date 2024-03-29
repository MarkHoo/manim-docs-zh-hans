# \_config

设置全局配置和记录器。

Functions

```py
tempconfig(temp)
```

临时修改全局`config`对象的上下文管理器。

在语句内部`with`，将使用修改后的配置。上下文管理器退出后，配置将恢复到原始状态。

参数

**temp** ( [_ManimConfig_]() _|_ _dict_ ) – 其键将用于临时更新全局的对象 `config`。

返回类型

\_GeneratorContextManager

例子

用于临时更改某些配置选项的默认值。`with tempconfig({...})`

```sh
>>> config["frame_height"]
8.0
>>> with tempconfig({"frame_height": 100.0}):
···     print(config["frame_height"])
···
100.0
>>> config["frame_height"]
8.0
```
