# TexTemplateFromFile 

合格名称：`manim.utils.tex.TexTemplateFromFile`


```py
class TexTemplateFromFile(*, tex_filename='tex_template.tex', **kwargs)
```

Bases: `TexTemplate`

从模板文件创建的 TexTemplate 对象（默认：tex_template.tex）

参数

- **tex_filename** ( _str_ _|_ _os.PathLike_ ) – 有效 TeX 模板文件的路径
- **kwargs** – 的参数[`TexTemplate`]()。



`template_file`

有效 TeX 模板文件的路径

类型

`str`



`body`

TeX 模板文件的内容

类型

`str`



`tex_compiler`

要使用的 TeX 编译器，例如`latex`,`pdflatex`或`lualatex`

类型

`str`



`output_format`

编译产生的输出格式，例如`.dvi`或`.pdf`

类型

`str`



方法

|||
|-|-|
[`add_to_document`]()|将 txt 添加到 TeX 模板中紧接 begin{document} 之后，例如
[`add_to_preamble`]()|将内容添加到 TeX 模板的序言中（例如
`file_not_mutable`|


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

**txt** – 包含要添加的文本的字符串。



`add_to_preamble(txt, prepend=False)`

将内容添加到 TeX 模板的序言中（例如定义、包）。文本可以插入到序言的开头或结尾。

参数

- **txt** – 包含要添加的文本的字符串，例如`\usepackage{hyperref}`
- **prepend** – 文本是否应添加在序言的开头，即紧接其后`\documentclass`。默认是将其添加到前导码的末尾，即之前`\begin{document}`
