# 文本模板

合格名称：`manim.utils.tex.TexTemplate`


```py
class TexTemplate(tex_compiler=None, output_format=None, documentclass=None, preamble=None, placeholder_text=None, post_doc_commands=None, **kwargs)
```

Bases: `object`

TeX 模板用于创建 Tex() 和 MathTex() 对象。

参数

- **tex_compiler** ( _str_ _|_ _None_ ) – 要使用的 TeX 编译器，例如`latex`,`pdflatex`或`lualatex`
- **output_format** ( _str_ _|_ _None_ ) – 编译产生的输出格式，例如`.dvi`或`.pdf`
- **documentclass** ( _str_ _|_ _None_ ) – 定义文档类的命令，例如`\documentclass[preview]{standalone}`
- **preamble** ( _str_ _|_ _None_`\documentclass` ) – 文档的序言，即和之间的部分`\begin{document}`
- **placeholder_text** ( _str_ _|_ _None_ ) – 文档中的文本将被要呈现的表达式替换
- **post_doc_commands** ( _str_ _|_ _None_ ) – 要在之后插入的文本（定义、命令）`\begin{document}`，例如`\boldmath`



`tex_compiler`

要使用的 TeX 编译器，例如`latex`,`pdflatex`或`lualatex`

类型

`str`



`output_format`

编译产生的输出格式，例如`.dvi`或`.pdf`

类型

`str`



`documentclass`

定义文档类的命令，例如`\documentclass[preview]{standalone}`

类型

`str`



`preamble`

文件的序言，即`\documentclass`和之间的部分`\begin{document}`

类型

`str`



`placeholder_text`

文档中的文本将被要呈现的表达式替换

类型

`str`



`post_doc_commands`

要在 后面插入的文本（定义、命令）`\begin{document}`，例如`\boldmath`

类型

`str`


方法

|||
|-|-|
[`add_to_document`]()|将 txt 添加到 TeX 模板中紧接 begin{document} 之后，例如
[`add_to_preamble`]()|将内容添加到 TeX 模板的序言中（例如
`copy`|
[`get_texcode_for_expression`]()|将表达式逐字插入 TeX 模板中。
[`get_texcode_for_expression_in_env`]()|将表达式插入到包含在 begin{environment} 和 end{environment} 中的 TeX 模板中


属性

`default_documentclass`

`default_output_format`

`default_placeholder_text`

`default_post_doc_commands`

`default_preamble`

`default_tex_compiler`



`add_to_document(txt)`

将 txt 添加到 TeX 模板中紧接 begin{document} 之后，例如`\boldmath`

参数

**txt** ( _str_ ) – 包含要添加的文本的字符串。



`add_to_preamble(txt, prepend=False)`

将内容添加到 TeX 模板的序言中（例如定义、包）。文本可以插入到序言的开头或结尾。

参数

- **txt** ( _str_ ) – 包含要添加的文本的字符串，例如`\usepackage{hyperref}`
- **prepend** ( _bool_ ) – 文本是否应添加在序言的开头，即紧接其后`\documentclass`。默认是将其添加到前导码的末尾，即之前`\begin{document}`



`get_texcode_for_expression(expression)`

将表达式逐字插入 TeX 模板中。

参数

**expression**( _str_ ) – 包含要排版的表达式的字符串，例如`$\sqrt{2}$`

返回

基于当前模板的 LaTeX 代码，包含给定`expression`并准备排版

返回类型

`str`



`get_texcode_for_expression_in_env(expression, environment)`

将表达式插入到包含在 begin{environment} 和 end{environment} 中的 TeX 模板中

参数

- **expression**( _str_ ) – 包含要排版的表达式的字符串，例如`$\\sqrt{2}$`
- **environment**( _str_ ) – 包含应在其中排版表达式的环境的字符串，例如`align*`

返回

基于模板的 LaTeX 代码，在其环境中包含给定的表达式，准备排版

返回类型

`str`
