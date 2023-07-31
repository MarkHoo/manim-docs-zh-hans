# TexTemplateFromFile [#](#textemplatefromfile "此标题的固定链接")

合格名称：`manim.utils.tex.TexTemplateFromFile`

_类_ TexTemplateFromFile ( _\*_ , _tex_filename = 'tex_template.tex'_ , _\*\* kwargs_ )[\[来源\]](../_modules/manim/utils/tex.html#TexTemplateFromFile)[#](#manim.utils.tex.TexTemplateFromFile "此定义的固定链接")

基地：[`TexTemplate`](manim.utils.tex.TexTemplate.html#manim.utils.tex.TexTemplate "manim.utils.tex.TexTemplate")

从模板文件创建的 TexTemplate 对象（默认：tex_template.tex）

参数

- **tex_filename** ( _str_ _|_ _os.PathLike_ ) – 有效 TeX 模板文件的路径
- **kwargs** – 的参数[`TexTemplate`](manim.utils.tex.TexTemplate.html#manim.utils.tex.TexTemplate "manim.utils.tex.TexTemplate")。

模板文件[#](#manim.utils.tex.TexTemplateFromFile.template_file "此定义的固定链接")

有效 TeX 模板文件的路径

类型

`str`

身体[#](#manim.utils.tex.TexTemplateFromFile.body "此定义的固定链接")

TeX 模板文件的内容

类型

`str`

tex\_编译器[#](#manim.utils.tex.TexTemplateFromFile.tex_compiler "此定义的固定链接")

要使用的 TeX 编译器，例如`latex`,`pdflatex`或`lualatex`

类型

`str`

输出格式[#](#manim.utils.tex.TexTemplateFromFile.output_format "此定义的固定链接")

编译产生的输出格式，例如`.dvi`或`.pdf`

类型

`str`

方法

[`add_to_document`](#manim.utils.tex.TexTemplateFromFile.add_to_document "manim.utils.tex.TexTemplateFromFile.add_to_document")

将 txt 添加到 TeX 模板中紧接 begin{document} 之后，例如

[`add_to_preamble`](#manim.utils.tex.TexTemplateFromFile.add_to_preamble "manim.utils.tex.TexTemplateFromFile.add_to_preamble")

将内容添加到 TeX 模板的序言中（例如

`file_not_mutable`

属性

`default_documentclass`

`default_output_format`

`default_placeholder_text`

`default_post_doc_commands`

`default_preamble`

`default_tex_compiler`

添加到文档（_txt_）[\[来源\]](../_modules/manim/utils/tex.html#TexTemplateFromFile.add_to_document)[#](#manim.utils.tex.TexTemplateFromFile.add_to_document "此定义的固定链接")

将 txt 添加到 TeX 模板中紧接 begin{document} 之后，例如`\boldmath`

参数

**txt** – 包含要添加的文本的字符串。

add*to_preamble ( \_txt* , _prepend = False_ )[\[来源\]](../_modules/manim/utils/tex.html#TexTemplateFromFile.add_to_preamble)[#](#manim.utils.tex.TexTemplateFromFile.add_to_preamble "此定义的固定链接")

将内容添加到 TeX 模板的序言中（例如定义、包）。文本可以插入到序言的开头或结尾。

参数

- **txt** – 包含要添加的文本的字符串，例如`\usepackage{hyperref}`
- **prepend** – 文本是否应添加在序言的开头，即紧接其后`\documentclass`。默认是将其添加到前导码的末尾，即之前`\begin{document}`
