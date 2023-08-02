# tex_file_writing 

用于编写、编译和转换`.tex`文件的接口。

> 也可以看看

`mobject.svg.tex_mobject`

Functions


`compile_tex(tex_file, tex_compiler, output_format)`

将 tex_file 编译为 .dvi 或 .xdv 或 .pdf

参数

- **tex_file** ( _Path_ ) – 要排版的 TeX 文件的文件名。
- **tex_compiler** ( _str_ ) – 包含要使用的编译器的字符串，例如`pdflatex`或`lualatex`
- **output_format** ( _str_ ) – 包含编译器生成的输出格式的字符串，例如`.dvi`或`.pdf`

返回

以所需格式（DVI、XDV 或 PDF）生成的输出文件的路径。

返回类型

`Path`


`convert_to_svg(dvi_file, extension, page=1)`

使用 dvisvgm 将 .dvi、.xdv 或 .pdf 文件转换为 svg。

参数

- **dvi_file** ( _Path_ ) – 要转换的输入文件的文件名。
- **extension**( _str_ ) – 包含文件扩展名的字符串，从而指示文件类型，例如`.dvi`或`.pdf`
- **page** ( _int_ ) – 如果输入文件是多页，则要转换的页面。

返回

生成的 SVG 文件的路径。

返回类型

`Path`


`generate_tex_file(expression, environment=None, tex_template=None)`

接受一个 tex 表达式（和一个可选的 tex 环境），并返回一个完整的 tex 文件以供编译。

参数

- **expression** ( _str_ ) – 包含要渲染的 TeX 表达式的字符串，例如`\sqrt{2}`or`foo`
- **environment**( _str_ _|_ _None_ ) – 包含应在其中排版表达式的环境的字符串，例如`align*`
- **tex_template** ( [_TexTemplate_]() _|_ _None_ ) – 用于排版的模板类。如果未设置，则使用通过 config\[“tex_template”\]设置的默认模板

返回

生成的 TeX 文件的路径

返回类型

`Path`


`insight_inputenc_error(matching)`

`insight_package_not_found_error(matching)`

`print_all_tex_errors(log_file, tex_compiler, tex_file)`

参数

- **日志文件**（_Path_）–
- **tex_compiler** ( _str_ ) –
- **tex_file**（_Path_）–

返回类型

None

```py
print_tex_error(tex_compilation_log, error_start_index, tex_source)
```

```py
tex_compilation_command(tex_compiler, output_format, tex_file, tex_dir)
```

使用所有必要的 cli 标志准备 tex 编译命令

参数

- **tex_compiler** ( _str_ ) – 包含要使用的编译器的字符串，例如`pdflatex`或`lualatex`
- **output_format** ( _str_ ) – 包含编译器生成的输出格式的字符串，例如`.dvi`或`.pdf`
- **tex_file** ( _Path_ ) – 要排版的 TeX 文件的文件名。
- **tex_dir** ( _Path_ ) – 存储编译器输出的目录路径。

返回

根据给定参数编译命令

返回类型

`str`


`tex_hash(expression)`


```py
tex_to_svg_file(expression, environment=None, tex_template=None)
```

获取 tex 表达式并返回编译后的 tex 的 svg 版本

参数

- **expression** ( _str_ ) – 包含要渲染的 TeX 表达式的字符串，例如`\sqrt{2}`or`foo`
- **环境**( _str_ _|_ _None_ ) – 包含应在其中排版表达式的环境的字符串，例如`align*`
- **tex_template** ( [_TexTemplate_]() _|_ _None_ ) – 用于排版的模板类。如果未设置，则使用通过 config\[“tex_template”\]设置的默认模板

返回

生成的 SVG 文件的路径。

返回类型

`Path`
