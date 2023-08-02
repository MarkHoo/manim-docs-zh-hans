# 命令

Functions

`capture(command, cwd=None, command_input=None)`


`get_dir_layout(dirpath)`

递归获取 dir 和子目录中所有文件相对于 dirpath 的路径列表。

参数

**dirpath**（_Path_）–

返回类型

_Generator_\[str、None、None\]


`get_video_metadata(path_to_video)`

参数

**path_to_video** ( _str_ _|_ _os.PathLike_ ) –

返回类型

dict[str]
