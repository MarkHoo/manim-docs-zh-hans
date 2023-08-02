# tex_file_writing 

用于编写、编译和转换`.tex`文件的接口。

也可以看看

`mobject.svg.tex_mobject`

Functions

编译*tex ( \_tex_file* , _tex_compiler_ ,_输出格式_)

将 tex_file 编译为 .dvi 或 .xdv 或 .pdf

参数

- **tex_file** ( _Path_ ) – 要排版的 TeX 文件的文件名。
- **tex_compiler** ( _str_ ) – 包含要使用的编译器的字符串，例如`pdflatex`或`lualatex`
- **output_format** ( _str_ ) – 包含编译器生成的输出格式的字符串，例如`.dvi`或`.pdf`

退货

以所需格式（DVI、XDV 或 PDF）生成的输出文件的路径。

返回类型

`Path`

Convert*to_svg ( \_dvi_file* ,_扩展名_,_页= 1_ )

使用 dvisvgm 将 .dvi、.xdv 或 .pdf 文件转换为 svg。

参数

- **dvi_file** ( _Path_ ) – 要转换的输入文件的文件名。
- **扩展名**( _str_ ) – 包含文件扩展名的字符串，从而指示文件类型，例如`.dvi`或`.pdf`
- **page** ( _int_ ) – 如果输入文件是多页，则要转换的页面。

退货

生成的 SVG 文件的路径。

返回类型

`Path`

generate*tex_file（*表达式*，*环境=无*， \_tex_template =无*）

接受一个 tex 表达式（和一个可选的 tex 环境），并返回一个完整的 tex 文件以供编译。

参数

- **expression** ( _str_ ) – 包含要渲染的 TeX 表达式的字符串，例如`\sqrt{2}`or`foo`
- **环境**( _str_ _|_ _None_ ) – 包含应在其中排版表达式的环境的字符串，例如`align*`
- **tex_template** ( [_TexTemplate_]() _|_ _None_ ) – 用于排版的模板类。如果未设置，则使用通过 config\[“tex_template”\]设置的默认模板

退货

生成的 TeX 文件的路径

返回类型

`Path`

Insight*inputenc_error（*匹配\_）

Insight*package_not_found_error（*匹配\_）

print*all_tex*errors ( \_log_file* , \_tex_compiler* , _tex_file_ )

参数

- **日志文件**（_路径_）–
- **tex_compiler** ( _str_ ) –
- **tex_file**（_路径_）–

返回类型

没有任何

print*tex_error ( \_tex_compilation_log* , _error_start_index_ , _tex_source_ )

tex*compilation_command（\_tex_compiler*， _output_format_， _tex_file_， _tex_dir_）

使用所有必要的 cli 标志准备 tex 编译命令

参数

- **tex_compiler** ( _str_ ) – 包含要使用的编译器的字符串，例如`pdflatex`或`lualatex`
- **output_format** ( _str_ ) – 包含编译器生成的输出格式的字符串，例如`.dvi`或`.pdf`
- **tex_file** ( _Path_ ) – 要排版的 TeX 文件的文件名。
- **tex_dir** ( _Path_ ) – 存储编译器输出的目录路径。

退货

根据给定参数编译命令

返回类型

`str`

tex*hash（*表达式\_）

tex_to_svg*file（*表达式*，*环境=无*， \_tex_template =无*）

获取 tex 表达式并返回编译后的 tex 的 svg 版本

参数

- **expression** ( _str_ ) – 包含要渲染的 TeX 表达式的字符串，例如`\sqrt{2}`or`foo`
- **环境**( _str_ _|_ _None_ ) – 包含应在其中排版表达式的环境的字符串，例如`align*`
- **tex_template** ( [_TexTemplate_]() _|_ _None_ ) – 用于排版的模板类。如果未设置，则使用通过 config\[“tex_template”\]设置的默认模板

退货

生成的 SVG 文件的路径。

返回类型

`Path`
