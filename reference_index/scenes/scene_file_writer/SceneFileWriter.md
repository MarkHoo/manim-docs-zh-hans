# 场景文件编写器

合格名称：`manim.scene.scene\_file\_writer.SceneFileWriter`

```py
class SceneFileWriter(renderer, scene_name, **kwargs)
```

Bases: object

SceneFileWriter 是使用 FFMPEG 将播放的动画实际写入视频文件的对象。这主要供 Manim 内部使用。你很少（如果有的话）必须使用此类的方法，除非修改 Manim 现实的结构。

部分

用于分割场景

类型

列表[`Section`]()

sections_output_dir 

部分视频存储在哪里

类型

`pathlib.Path`

输出名称

不带扩展名的电影名称和部分视频名称的基础

类型

斯特

一些有用的属性是：

“写入电影”（布尔=假）

是否将动画写入视频文件。

“电影文件扩展名”（str =“.mp4”）

输出视频的文件类型扩展名。

“部分电影文件”

所有部分电影文件的列表。

方法

[`add_audio_segment`]()

此方法从 AudioSegment 类型对象添加音频片段和合适的参数。

[`add_partial_movie_file`]()

将新的部分影片文件路径添加到 scene.partial_movie_files 和哈希中的当前部分。

[`add_sound`]()

此方法添加声音文件中的音频片段。

[`begin_animation`]()

由 manim 在内部使用，将动画流式传输到 FFMPEG 以显示或写入文件。

[`clean_cache`]()

将通过删除最旧的 partial_movie_files 来清理缓存。

[`close_movie_pipe`]()

由 Manim 在内部使用以正常停止写入 FFMPEG 的输入缓冲区

`combine_files`

[`combine_to_movie`]()

由 Manim 在内部使用，将构成场景的单独的部分影片文件组合成该场景的单个视频文件。

[`combine_to_section_videos`]()

连接每个部分的部分电影文件。

[`create_audio_segment`](")

创建一个空的、无声的音频段。

[`end_animation`]()

Manim 在内部使用它来优雅地停止流式传输到 FFMPEG。

[`finish`](")

完成对 FFMPEG 缓冲区的写入或将图像写入输出目录。

[`finish_last_section`]()

如果当前节为空，则删除它。

[`flush_cache_directory`]()

删除所有缓存的部分电影文件

[`get_resolution_directory`]()

获取直接包含视频文件的分辨率目录的名称。

[`init_audio`]()

帮助编剧为电影添加音频做好准备。

[`init_output_directories`]()

初始化输出目录。

[`is_already_cached`]()

将检查是否存在以 hash_inplication 命名的文件。

[`next_section`]()

在此创建分段剪切。

[`open_movie_pipe`]()

由 Manim 在内部使用来初始化 FFMPEG 并开始写入 FFMPEG 的输入缓冲区。

`output_image`

`output_image_from_array`

[`print_file_ready_message`]()

将“文件就绪”消息打印到 STDOUT。

[`save_final_image`]()

这个名字用词不当。

[`write_frame`]()

Manim 在内部使用它来将帧写入 FFMPEG 输入缓冲区。

`write_opengl_frame`

[`write_subcaption_file`]()

写入子字幕文件。

属性

`force_output_as_scene_name`

add*audio_segment（\_new_segment*，_时间=无_， _gain_to_background =无_）

此方法从 AudioSegment 类型对象添加音频片段和合适的参数。

参数

- **new_segment** ( _AudioSegment_ ) – 要添加的音频片段
- **time** ( _float_ _|_ _None_ ) – 应添加声音的时间戳。
- **Gain_to_background** ( _float_ _|_ _None_ ) – 片段相对于背景的增益。

添加部分电影文件（_哈希动画_）

将新的部分影片文件路径添加到 scene.partial_movie_files 和哈希中的当前部分。此方法将从哈希计算路径。除此之外，它还会将新动画添加到当前部分。

参数

**hash_animation** ( _str_ ) – 动画的哈希值。

add*sound ( \_sound_file* ,_时间= None_ ,_增益= None_ , _\*\* kwargs_ )

此方法添加声音文件中的音频片段。

参数

- **sound_file** ( _str_ ) – 声音文件的路径。
- **time** ( _float_ _|_ _None_ ) – 应添加音频的时间戳。
- **Gain** ( _float_ _|_ _None_ ) – 给定音频片段的增益。
- \***\*kwargs** – 此方法使用 add_audio_segment，因此可以在此处引用其中使用的任何关键字参数。

开始动画（_allow_write = False_， _file_path = None_）

由 manim 在内部使用，将动画流式传输到 FFMPEG 以显示或写入文件。

参数

**allowed_write** ( _bool_ ) – 是否写入视频文件。

清理缓存( )

将通过删除最旧的 partial_movie_files 来清理缓存。

关闭电影管道( )

由 Manim 在内部使用以正常停止写入 FFMPEG 的输入缓冲区

组合到电影( )

由 Manim 在内部使用，将构成场景的单独的部分影片文件组合成该场景的单个视频文件。

合并到部分视频( )

连接每个部分的部分电影文件。

返回类型

没有任何

创建音频段（）

创建一个空的、无声的音频段。

动画结束（_allow_write = False_）

Manim 在内部使用它来优雅地停止流式传输到 FFMPEG。

参数

**allowed_write** ( _bool_ ) – 是否写入视频文件。

完成( )

完成对 FFMPEG 缓冲区的写入或将图像写入输出目录。将部分电影文件合并到整个场景中。如果 save_last_frame 为 True，则将最后一帧保存在默认图像目录中。

完成最后一个部分( )

如果当前节为空，则删除它。

返回类型

没有任何

刷新缓存目录( )

删除所有缓存的部分电影文件

获取分辨率目录( )

获取直接包含视频文件的分辨率目录的名称。

此方法获取直接包含视频文件的目录的名称。这个名字是`<height_in_pixels_of_video>p<frame_rate>`。例如，如果您以 15fps 渲染 854x480 像素的动画，则直接包含视频文件的目录名称将为`480p15`.

文件结构应该类似于：

```sh
MEDIA_DIR
    |--Tex
    |--texts
    |--videos
    |--<name_of_file_containing_scene>
        |--<height_in_pixels_of_video>p<frame_rate>
            |--<scene_name>.mp4
```

返回

目录的名称。

返回类型

`str`

初始化音频（）

帮助编剧为电影添加音频做好准备。

init*output_directories (*场景名称\_)

初始化输出目录。

笔记

`config`例如， 可以读取目录`config['media_dir']`。如果目标目录尚不存在，则会创建它们。

is*already_cached（*哈希调用\_）

将检查是否存在以 hash_inplication 命名的文件。

参数

**hash_inspiration** ( \_str ) – 与\_scene.play 或 scene.wait 调用相对应的哈希值。

返回

文件是否存在。

返回类型

`bool`

next*section（*名称*，*类型*， \_skip_animations*）

在此创建分段剪切。

参数

- **名称**( _str_ ) –
- **类型**( _str_ ) –
- **跳过动画**( _bool_ ) –

返回类型

没有任何

open*movie_pipe（*文件路径=无\_）

由 Manim 在内部使用来初始化 FFMPEG 并开始写入 FFMPEG 的输入缓冲区。

print_file_ready*message (*文件路径\_)

将“文件就绪”消息打印到 STDOUT。

保存最终图像（_图像_）

这个名字用词不当。此方法将传递给它的图像保存在默认图像目录中。

参数

**image** ( _ndarray_ ) – 要保存的图像的像素数组。

write*frame ( \_frame_or_renderer* )

Manim 在内部使用它来将帧写入 FFMPEG 输入缓冲区。

参数

**frame_or_renderer** ( _np.ndarray_ _|_ _OpenGLRenderer_ ) – 帧的像素数组。

write_subcaption_file ( )

写入子字幕文件。
