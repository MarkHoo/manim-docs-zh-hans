# 文本字体模板[#](#texfonttemplates "此标题的固定链接")

合格名称：`manim.utils.tex\_templates.TexFontTemplates`

_类_ TexFontTemplates[\[来源\]](../_modules/manim/utils/tex_templates.html#TexFontTemplates)[#](#manim.utils.tex_templates.TexFontTemplates "此定义的固定链接")

基地：`object`

[http://jf.burnol.free.fr/showcase.html](http://jf.burnol.free.fr/showcase.html)中描述的字体的 TeX 模板集合[](http://jf.burnol.free.fr/showcase.html)

这些模板经过专门设计，允许您使用不同的字体排版公式和数学。它们基于 mathastext LaTeX 包。

例子

正常用作 Tex() 和 MathTex() mobject 的关键字参数 tex_template 的值：

\`\`Tex("My TeX code", tex_template=TexFontTemplates.comic_sans)\`\`

Copy to clipboard

笔记

其中许多模板要求在本地计算机上安装特定字体。例如，如果未安装 Comic Sans Microsoft 字体，则选择模板 TexFontTemplates.comic_sans 将无法编译。

要进行实验，请尝试渲染 TexFontTemplateLibrary 示例场景：

`manim path/to/manim/example_scenes/advanced_tex_fonts.py TexFontTemplateLibrary -p -ql`

方法

属性

[`american_typewriter`](#manim.utils.tex_templates.TexFontTemplates.american_typewriter "manim.utils.tex_templates.TexFontTemplates.american_typewriter")

美国打字机

[`antykwa`](#manim.utils.tex_templates.TexFontTemplates.antykwa "manim.utils.tex_templates.TexFontTemplates.antykwa")

Antykwa Półtawskiego（希腊语和数学符号的 TX 字体）

[`apple_chancery`](#manim.utils.tex_templates.TexFontTemplates.apple_chancery "manim.utils.tex_templates.TexFontTemplates.apple_chancery")

苹果办公厅

[`auriocus_kalligraphicus`](#manim.utils.tex_templates.TexFontTemplates.auriocus_kalligraphicus "manim.utils.tex_templates.TexFontTemplates.auriocus_kalligraphicus")

Auriocus Kalligraphicus（希腊符号）

[`baskervald_adf_fourier`](#manim.utils.tex_templates.TexFontTemplates.baskervald_adf_fourier "manim.utils.tex_templates.TexFontTemplates.baskervald_adf_fourier")

带傅里叶的 Baskervald ADF

[`baskerville_it`](#manim.utils.tex_templates.TexFontTemplates.baskerville_it "manim.utils.tex_templates.TexFontTemplates.baskerville_it")

巴斯克维尔（斜体）

[`biolinum`](#manim.utils.tex_templates.TexFontTemplates.biolinum "manim.utils.tex_templates.TexFontTemplates.biolinum")

比奥林

[`brushscriptx`](#manim.utils.tex_templates.TexFontTemplates.brushscriptx "manim.utils.tex_templates.TexFontTemplates.brushscriptx")

BrushScriptX-斜体（PX 数学和希腊语）

[`chalkboard_se`](#manim.utils.tex_templates.TexFontTemplates.chalkboard_se "manim.utils.tex_templates.TexFontTemplates.chalkboard_se")

黑板 SE

[`chalkduster`](#manim.utils.tex_templates.TexFontTemplates.chalkduster "manim.utils.tex_templates.TexFontTemplates.chalkduster")

粉笔末

[`comfortaa`](#manim.utils.tex_templates.TexFontTemplates.comfortaa "manim.utils.tex_templates.TexFontTemplates.comfortaa")

康福塔

[`comic_sans`](#manim.utils.tex_templates.TexFontTemplates.comic_sans "manim.utils.tex_templates.TexFontTemplates.comic_sans")

漫画无 MS

[`droid_sans`](#manim.utils.tex_templates.TexFontTemplates.droid_sans "manim.utils.tex_templates.TexFontTemplates.droid_sans")

机器人 Sans

[`droid_sans_it`](#manim.utils.tex_templates.TexFontTemplates.droid_sans_it "manim.utils.tex_templates.TexFontTemplates.droid_sans_it")

Droid Sans（斜体）

[`droid_serif`](#manim.utils.tex_templates.TexFontTemplates.droid_serif "manim.utils.tex_templates.TexFontTemplates.droid_serif")

机器人衬线

[`droid_serif_px_it`](#manim.utils.tex_templates.TexFontTemplates.droid_serif_px_it "manim.utils.tex_templates.TexFontTemplates.droid_serif_px_it")

Droid Serif（PX 数学符号）（斜体）

[`ecf_augie`](#manim.utils.tex_templates.TexFontTemplates.ecf_augie "manim.utils.tex_templates.TexFontTemplates.ecf_augie")

ECF Augie（欧拉希腊语）

[`ecf_jd`](#manim.utils.tex_templates.TexFontTemplates.ecf_jd "manim.utils.tex_templates.TexFontTemplates.ecf_jd")

ECF JD（带 TX 字体）

[`ecf_skeetch`](#manim.utils.tex_templates.TexFontTemplates.ecf_skeetch "manim.utils.tex_templates.TexFontTemplates.ecf_skeetch")

ECF 草图（CM 希腊语）

[`ecf_tall_paul`](#manim.utils.tex_templates.TexFontTemplates.ecf_tall_paul "manim.utils.tex_templates.TexFontTemplates.ecf_tall_paul")

ECF Tall Paul（带 Symbol 字体）

[`ecf_webster`](#manim.utils.tex_templates.TexFontTemplates.ecf_webster "manim.utils.tex_templates.TexFontTemplates.ecf_webster")

ECF Webster（带有 TX 字体）

[`electrum_adf`](#manim.utils.tex_templates.TexFontTemplates.electrum_adf "manim.utils.tex_templates.TexFontTemplates.electrum_adf")

金金银 ADF（CM 希腊语）

[`epigrafica`](#manim.utils.tex_templates.TexFontTemplates.epigrafica "manim.utils.tex_templates.TexFontTemplates.epigrafica")

警句

[`fourier_utopia`](#manim.utils.tex_templates.TexFontTemplates.fourier_utopia "manim.utils.tex_templates.TexFontTemplates.fourier_utopia")

傅立叶乌托邦（傅立叶立式希腊语）

[`french_cursive`](#manim.utils.tex_templates.TexFontTemplates.french_cursive "manim.utils.tex_templates.TexFontTemplates.french_cursive")

法语草书（欧拉希腊语）

[`gfs_bodoni`](#manim.utils.tex_templates.TexFontTemplates.gfs_bodoni "manim.utils.tex_templates.TexFontTemplates.gfs_bodoni")

GFS 博多尼

[`gfs_didot`](#manim.utils.tex_templates.TexFontTemplates.gfs_didot "manim.utils.tex_templates.TexFontTemplates.gfs_didot")

GFS Didot（斜体）

[`gfs_neoHellenic`](#manim.utils.tex_templates.TexFontTemplates.gfs_neoHellenic "manim.utils.tex_templates.TexFontTemplates.gfs_neoHellenic")

GFS 新希腊语

[`gnu_freesans_tx`](#manim.utils.tex_templates.TexFontTemplates.gnu_freesans_tx "manim.utils.tex_templates.TexFontTemplates.gnu_freesans_tx")

GNU FreeSerif（和 TX 字体符号）

[`gnu_freeserif_freesans`](#manim.utils.tex_templates.TexFontTemplates.gnu_freeserif_freesans "manim.utils.tex_templates.TexFontTemplates.gnu_freeserif_freesans")

GNU FreeSerif 和 FreeSans

[`helvetica_fourier_it`](#manim.utils.tex_templates.TexFontTemplates.helvetica_fourier_it "manim.utils.tex_templates.TexFontTemplates.helvetica_fourier_it")

带傅里叶的 Helvetica（斜体）

[`latin_modern_tw`](#manim.utils.tex_templates.TexFontTemplates.latin_modern_tw "manim.utils.tex_templates.TexFontTemplates.latin_modern_tw")

拉丁现代打字机比例

[`latin_modern_tw_it`](#manim.utils.tex_templates.TexFontTemplates.latin_modern_tw_it "manim.utils.tex_templates.TexFontTemplates.latin_modern_tw_it")

拉丁现代打字机比例（CM 希腊语）（斜体）

[`libertine`](#manim.utils.tex_templates.TexFontTemplates.libertine "manim.utils.tex_templates.TexFontTemplates.libertine")

浪荡子

[`libris_adf_fourier`](#manim.utils.tex_templates.TexFontTemplates.libris_adf_fourier "manim.utils.tex_templates.TexFontTemplates.libris_adf_fourier")

Libris ADF 与傅里叶

[`minion_pro_myriad_pro`](#manim.utils.tex_templates.TexFontTemplates.minion_pro_myriad_pro "manim.utils.tex_templates.TexFontTemplates.minion_pro_myriad_pro")

Minion Pro 和 Myriad Pro（以及 TX 字体符号）

[`minion_pro_tx`](#manim.utils.tex_templates.TexFontTemplates.minion_pro_tx "manim.utils.tex_templates.TexFontTemplates.minion_pro_tx")

Minion Pro（和 TX 字体符号）

[`new_century_schoolbook`](#manim.utils.tex_templates.TexFontTemplates.new_century_schoolbook "manim.utils.tex_templates.TexFontTemplates.new_ century_schoolbook")

新世纪教科书（符号希腊语）

[`new_century_schoolbook_px`](#manim.utils.tex_templates.TexFontTemplates.new_century_schoolbook_px "manim.utils.tex_templates.TexFontTemplates.new_ century_schoolbook_px")

新世纪教科书（符号希腊语、PX 数学符号）

[`noteworthy_light`](#manim.utils.tex_templates.TexFontTemplates.noteworthy_light "manim.utils.tex_templates.TexFontTemplates.noteworthy_light")

值得注意的光

[`palatino`](#manim.utils.tex_templates.TexFontTemplates.palatino "manim.utils.tex_templates.TexFontTemplates.palatino")

Palatino（希腊符号）

[`papyrus`](#manim.utils.tex_templates.TexFontTemplates.papyrus "manim.utils.tex_templates.TexFontTemplates.papyrus")

纸莎草纸

[`romande_adf_fourier_it`](#manim.utils.tex_templates.TexFontTemplates.romande_adf_fourier_it "manim.utils.tex_templates.TexFontTemplates.romande_adf_fourier_it")

带傅里叶的 Romande ADF（斜体）

[`slitex`](#manim.utils.tex_templates.TexFontTemplates.slitex "manim.utils.tex_templates.TexFontTemplates.slitex")

SliTeX（欧拉希腊语）

[`times_fourier_it`](#manim.utils.tex_templates.TexFontTemplates.times_fourier_it "manim.utils.tex_templates.TexFontTemplates.times_fourier_it")

傅里叶时代（斜体）

[`urw_avant_garde`](#manim.utils.tex_templates.TexFontTemplates.urw_avant_garde "manim.utils.tex_templates.TexFontTemplates.urw_avant_garde")

URW 前卫（希腊符号）

[`urw_zapf_chancery`](#manim.utils.tex_templates.TexFontTemplates.urw_zapf_chancery "manim.utils.tex_templates.TexFontTemplates.urw_zapf_chancery")

URW Zapf 办公厅（CM 希腊语）

[`venturis_adf_fourier_it`](#manim.utils.tex_templates.TexFontTemplates.venturis_adf_fourier_it "manim.utils.tex_templates.TexFontTemplates.venturis_adf_fourier_it")

带傅里叶的文丘里 ADF（斜体）

[`verdana_it`](#manim.utils.tex_templates.TexFontTemplates.verdana_it "manim.utils.tex_templates.TexFontTemplates.verdana_it")

Verdana（斜体）

[`vollkorn`](#manim.utils.tex_templates.TexFontTemplates.vollkorn "manim.utils.tex_templates.TexFontTemplates.vollkorn")

Vollkorn（希腊语和数学符号的 TX 字体）

[`vollkorn_fourier_it`](#manim.utils.tex_templates.TexFontTemplates.vollkorn_fourier_it "manim.utils.tex_templates.TexFontTemplates.vollkorn_fourier_it")

Vollkorn 与 Fourier（斜体）

[`zapf_chancery`](#manim.utils.tex_templates.TexFontTemplates.zapf_chancery "manim.utils.tex_templates.TexFontTemplates.zapf_chancery")

扎普夫办公厅

american*typewriter *=\_ _<manim.utils.tex.TexTemplate\_\_对象>_ [#](#manim.utils.tex_templates.TexFontTemplates.american_typewriter "Permalink to this definition")[](#manim.utils.tex_templates.TexFontTemplates.american_typewriter "此定义的固定链接")

美国打字机

antykwa _=_ _<manim.utils.tex.TexTemplate\_\_对象>_ [#](#manim.utils.tex_templates.TexFontTemplates.antykwa "Permalink to this definition")[](#manim.utils.tex_templates.TexFontTemplates.antykwa "此定义的固定链接")

Antykwa Półtawskiego（希腊语和数学符号的 TX 字体）

apple*chancery *=\_ _<manim.utils.tex.TexTemplate\_\_对象>_ [#](#manim.utils.tex_templates.TexFontTemplates.apple_chancery "Permalink to this definition")[](#manim.utils.tex_templates.TexFontTemplates.apple_chancery "此定义的固定链接")

苹果办公厅

auriocus*kalligraphicus *=\_ _<manim.utils.tex.TexTemplate\_\_对象>_ [#](#manim.utils.tex_templates.TexFontTemplates.auriocus_kalligraphicus "Permalink to this definition")[](#manim.utils.tex_templates.TexFontTemplates.auriocus_kalligraphicus "此定义的固定链接")

Auriocus Kalligraphicus（希腊符号）

baskervald*adf_fourier *=\_ _<manim.utils.tex.TexTemplate\_\_对象>_ [#](#manim.utils.tex_templates.TexFontTemplates.baskervald_adf_fourier "此定义的固定链接")[](#manim.utils.tex_templates.TexFontTemplates.baskervald_adf_fourier "此定义的固定链接")

带傅里叶的 Baskervald ADF

baskerville*it *=\_ _<manim.utils.tex.TexTemplate\_\_对象>_ [#](#manim.utils.tex_templates.TexFontTemplates.baskerville_it "此定义的固定链接")[](#manim.utils.tex_templates.TexFontTemplates.baskerville_it "此定义的固定链接")

巴斯克维尔（斜体）

biolinum _=_ _<manim.utils.tex.TexTemplate\_\_对象>_ [#](#manim.utils.tex_templates.TexFontTemplates.biolinum "此定义的固定链接")[](#manim.utils.tex_templates.TexFontTemplates.biolinum "此定义的固定链接")

比奥林

Brushscriptx _=_ _<manim.utils.tex.TexTemplate\_\_对象>_ [#](#manim.utils.tex_templates.TexFontTemplates.brushscriptx "此定义的固定链接")[](#manim.utils.tex_templates.TexFontTemplates.brushscriptx "此定义的固定链接")

BrushScriptX-斜体（PX 数学和希腊语）

chalkboard*se *=\_ _<manim.utils.tex.TexTemplate\_\_对象>_ [#](#manim.utils.tex_templates.TexFontTemplates.chalkboard_se "此定义的固定链接")[](#manim.utils.tex_templates.TexFontTemplates.chalkboard_se "此定义的固定链接")

黑板 SE

chalkduster _=_ _<manim.utils.tex.TexTemplate\_\_对象>_ [#](#manim.utils.tex_templates.TexFontTemplates.chalkduster "此定义的固定链接")[](#manim.utils.tex_templates.TexFontTemplates.chalkduster "此定义的固定链接")

粉笔末

Comfortaa _=_ _<manim.utils.tex.TexTemplate\_\_对象>_ [#](#manim.utils.tex_templates.TexFontTemplates.comfortaa "此定义的固定链接")[](#manim.utils.tex_templates.TexFontTemplates.comfortaa "此定义的固定链接")

康福塔

Comic*sans *=\_ _<manim.utils.tex.TexTemplate\_\_对象>_ [#](#manim.utils.tex_templates.TexFontTemplates.comic_sans "此定义的固定链接")[](#manim.utils.tex_templates.TexFontTemplates.comic_sans "此定义的固定链接")

漫画无 MS

droid*sans *=\_ _<manim.utils.tex.TexTemplate\_\_对象>_ [#](#manim.utils.tex_templates.TexFontTemplates.droid_sans "此定义的固定链接")[](#manim.utils.tex_templates.TexFontTemplates.droid_sans "此定义的固定链接")

机器人 Sans

droid*sans_it *=\_ _<manim.utils.tex.TexTemplate\_\_对象>_ [#](#manim.utils.tex_templates.TexFontTemplates.droid_sans_it "此定义的固定链接")[](#manim.utils.tex_templates.TexFontTemplates.droid_sans_it "此定义的固定链接")

Droid Sans（斜体）

droid*serif *=\_ _<manim.utils.tex.TexTemplate\_\_对象>_ [#](#manim.utils.tex_templates.TexFontTemplates.droid_serif "此定义的固定链接")[](#manim.utils.tex_templates.TexFontTemplates.droid_serif "此定义的固定链接")

机器人衬线

droid*serif_px*it _=\_ _<manim.utils.tex.TexTemplate\_\_对象>\_ [#](#manim.utils.tex_templates.TexFontTemplates.droid_serif_px_it "此定义的固定链接")[](#manim.utils.tex_templates.TexFontTemplates.droid_serif_px_it "此定义的固定链接")

Droid Serif（PX 数学符号）（斜体）

ecf*augie *=\_ _<manim.utils.tex.TexTemplate\_\_对象>_ [#](#manim.utils.tex_templates.TexFontTemplates.ecf_augie "此定义的固定链接")[](#manim.utils.tex_templates.TexFontTemplates.ecf_augie "此定义的固定链接")

ECF Augie（欧拉希腊语）

ecf*jd *=\_ _<manim.utils.tex.TexTemplate\_\_对象>_ [#](#manim.utils.tex_templates.TexFontTemplates.ecf_jd "此定义的固定链接")[](#manim.utils.tex_templates.TexFontTemplates.ecf_jd "此定义的固定链接")

ECF JD（带 TX 字体）

ecf*skeetch *=\_ _<manim.utils.tex.TexTemplate\_\_对象>_ [#](#manim.utils.tex_templates.TexFontTemplates.ecf_skeetch "此定义的固定链接")[](#manim.utils.tex_templates.TexFontTemplates.ecf_skeetch "此定义的固定链接")

ECF 草图（CM 希腊语）

ecf*tall_paul *=\_ _<manim.utils.tex.TexTemplate\_\_对象>_ [#](#manim.utils.tex_templates.TexFontTemplates.ecf_tall_paul "此定义的固定链接")[](#manim.utils.tex_templates.TexFontTemplates.ecf_tall_paul "此定义的固定链接")

ECF Tall Paul（带 Symbol 字体）

ecf*webster *=\_ _<manim.utils.tex.TexTemplate\_\_对象>_ [#](#manim.utils.tex_templates.TexFontTemplates.ecf_webster "此定义的固定链接")[](#manim.utils.tex_templates.TexFontTemplates.ecf_webster "此定义的固定链接")

ECF Webster（带有 TX 字体）

electrum*adf *=\_ _<manim.utils.tex.TexTemplate\_\_对象>_ [#](#manim.utils.tex_templates.TexFontTemplates.electrum_adf "此定义的固定链接")[](#manim.utils.tex_templates.TexFontTemplates.electrum_adf "此定义的固定链接")

金金银 ADF（CM 希腊语）

epigrafica _=_ _<manim.utils.tex.TexTemplate\_\_对象>_ [#](#manim.utils.tex_templates.TexFontTemplates.epigrafica "此定义的固定链接")[](#manim.utils.tex_templates.TexFontTemplates.epigrafica "此定义的固定链接")

警句

fourier*utopia *=\_ _<manim.utils.tex.TexTemplate\_\_对象>_ [#](#manim.utils.tex_templates.TexFontTemplates.fourier_utopia "此定义的固定链接")[](#manim.utils.tex_templates.TexFontTemplates.fourier_utopia "此定义的固定链接")

傅立叶乌托邦（傅立叶立式希腊语）

french*cursive *=\_ _<manim.utils.tex.TexTemplate\_\_对象>_ [#](#manim.utils.tex_templates.TexFontTemplates.french_cursive "此定义的固定链接")[](#manim.utils.tex_templates.TexFontTemplates.french_cursive "此定义的固定链接")

法语草书（欧拉希腊语）

gfs*bodoni *=\_ _<manim.utils.tex.TexTemplate\_\_对象>_ [#](#manim.utils.tex_templates.TexFontTemplates.gfs_bodoni "此定义的固定链接")[](#manim.utils.tex_templates.TexFontTemplates.gfs_bodoni "此定义的固定链接")

GFS 博多尼

gfs*didot *=\_ _<manim.utils.tex.TexTemplate\_\_对象>_ [#](#manim.utils.tex_templates.TexFontTemplates.gfs_didot "此定义的固定链接")[](#manim.utils.tex_templates.TexFontTemplates.gfs_didot "此定义的固定链接")

GFS Didot（斜体）

gfs*neoHellenic *=\_ _<manim.utils.tex.TexTemplate\_\_对象>_ [#](#manim.utils.tex_templates.TexFontTemplates.gfs_neoHellenic "此定义的固定链接")[](#manim.utils.tex_templates.TexFontTemplates.gfs_neoHellenic "此定义的固定链接")

GFS 新希腊语

gnu*freesans_tx *=\_ _<manim.utils.tex.TexTemplate\_\_对象>_ [#](#manim.utils.tex_templates.TexFontTemplates.gnu_freesans_tx "此定义的固定链接")[](#manim.utils.tex_templates.TexFontTemplates.gnu_freesans_tx "此定义的固定链接")

GNU FreeSerif（和 TX 字体符号）

gnu*freeserif_freesans *=\_ _<manim.utils.tex.TexTemplate\_\_对象>_ [#](#manim.utils.tex_templates.TexFontTemplates.gnu_freeserif_freesans "此定义的固定链接")[](#manim.utils.tex_templates.TexFontTemplates.gnu_freeserif_freesans "此定义的固定链接")

GNU FreeSerif 和 FreeSans

helvetica*fourier_it *=\_ _<manim.utils.tex.TexTemplate\_\_对象>_ [#](#manim.utils.tex_templates.TexFontTemplates.helvetica_fourier_it "此定义的固定链接")[](#manim.utils.tex_templates.TexFontTemplates.helvetica_fourier_it "此定义的固定链接")

带傅里叶的 Helvetica（斜体）

latin*modern_tw *=\_ _<manim.utils.tex.TexTemplate\_\_对象>_ [#](#manim.utils.tex_templates.TexFontTemplates.latin_modern_tw "此定义的固定链接")[](#manim.utils.tex_templates.TexFontTemplates.latin_modern_tw "此定义的固定链接")

拉丁现代打字机比例

latin*modern_tw*it _=\_ _<manim.utils.tex.TexTemplate\_\_对象>\_ [#](#manim.utils.tex_templates.TexFontTemplates.latin_modern_tw_it "此定义的固定链接")[](#manim.utils.tex_templates.TexFontTemplates.latin_modern_tw_it "此定义的固定链接")

拉丁现代打字机比例（CM 希腊语）（斜体）

libertine _=_ _<manim.utils.tex.TexTemplate\_\_对象>_ [#](#manim.utils.tex_templates.TexFontTemplates.libertine "此定义的固定链接")[](#manim.utils.tex_templates.TexFontTemplates.libertine "此定义的固定链接")

浪荡子

libris*adf_fourier *=\_ _<manim.utils.tex.TexTemplate\_\_对象>_ [#](#manim.utils.tex_templates.TexFontTemplates.libris_adf_fourier "此定义的固定链接")[](#manim.utils.tex_templates.TexFontTemplates.libris_adf_fourier "此定义的固定链接")

Libris ADF 与傅里叶

minion*pro_myriad*pro _=\_ _<manim.utils.tex.TexTemplate\_\_对象>\_ [#](#manim.utils.tex_templates.TexFontTemplates.minion_pro_myriad_pro "此定义的固定链接")[](#manim.utils.tex_templates.TexFontTemplates.minion_pro_myriad_pro "此定义的固定链接")

Minion Pro 和 Myriad Pro（以及 TX 字体符号）

minion*pro_tx *=\_ _<manim.utils.tex.TexTemplate\_\_对象>_ [#](#manim.utils.tex_templates.TexFontTemplates.minion_pro_tx "此定义的固定链接")[](#manim.utils.tex_templates.TexFontTemplates.minion_pro_tx "此定义的固定链接")

Minion Pro（和 TX 字体符号）

new* century_schoolbook *=\_ _<manim.utils.tex.TexTemplate\_\_对象>_ [#](#manim.utils.tex_templates.TexFontTemplates.new_century_schoolbook "此定义的固定链接")[](#manim.utils.tex_templates.TexFontTemplates.new_century_schoolbook "此定义的固定链接")

新世纪教科书（符号希腊语）

new* century_schoolbook_px *=\_ _<manim.utils.tex.TexTemplate\_\_对象>_ [#](#manim.utils.tex_templates.TexFontTemplates.new_century_schoolbook_px "此定义的固定链接")[](#manim.utils.tex_templates.TexFontTemplates.new_century_schoolbook_px "此定义的固定链接")

新世纪教科书（符号希腊语、PX 数学符号）

noteworthy*light *=\_ _<manim.utils.tex.TexTemplate\_\_对象>_ [#](#manim.utils.tex_templates.TexFontTemplates.noteworthy_light "此定义的固定链接")[](#manim.utils.tex_templates.TexFontTemplates.noteworthy_light "此定义的固定链接")

值得注意的光

palatino _=_ _<manim.utils.tex.TexTemplate\_\_对象>_ [#](#manim.utils.tex_templates.TexFontTemplates.palatino "此定义的固定链接")[](#manim.utils.tex_templates.TexFontTemplates.palatino "此定义的固定链接")

Palatino（希腊符号）

纸莎草*=* _<manim.utils.tex.TexTemplate\_\_对象>_ [#](#manim.utils.tex_templates.TexFontTemplates.papyrus "此定义的固定链接")[](#manim.utils.tex_templates.TexFontTemplates.papyrus "此定义的固定链接")

纸莎草纸

romande*adf_fourier*it _=\_ _<manim.utils.tex.TexTemplate\_\_对象>\_ [#](#manim.utils.tex_templates.TexFontTemplates.romande_adf_fourier_it "此定义的固定链接")[](#manim.utils.tex_templates.TexFontTemplates.romande_adf_fourier_it "此定义的固定链接")

带傅里叶的 Romande ADF（斜体）

slimex _=_ _<manim.utils.tex.TexTemplate\_\_对象>_ [#](#manim.utils.tex_templates.TexFontTemplates.slitex "此定义的固定链接")[](#manim.utils.tex_templates.TexFontTemplates.slitex "此定义的固定链接")

SliTeX（欧拉希腊语）

times*fourier_it *=\_ _<manim.utils.tex.TexTemplate\_\_对象>_ [#](#manim.utils.tex_templates.TexFontTemplates.times_fourier_it "此定义的固定链接")[](#manim.utils.tex_templates.TexFontTemplates.times_fourier_it "此定义的固定链接")

傅里叶时代（斜体）

urw*avant_garde *=\_ _<manim.utils.tex.TexTemplate\_\_对象>_ [#](#manim.utils.tex_templates.TexFontTemplates.urw_avant_garde "此定义的固定链接")[](#manim.utils.tex_templates.TexFontTemplates.urw_avant_garde "此定义的固定链接")

URW 前卫（希腊符号）

urw*zapf_chancery *=\_ _<manim.utils.tex.TexTemplate\_\_对象>_ [#](#manim.utils.tex_templates.TexFontTemplates.urw_zapf_chancery "此定义的固定链接")[](#manim.utils.tex_templates.TexFontTemplates.urw_zapf_chancery "此定义的固定链接")

URW Zapf 办公厅（CM 希腊语）

venturis*adf_fourier*it _=\_ _<manim.utils.tex.TexTemplate\_\_对象>\_ [#](#manim.utils.tex_templates.TexFontTemplates.venturis_adf_fourier_it "此定义的固定链接")[](#manim.utils.tex_templates.TexFontTemplates.venturis_adf_fourier_it "此定义的固定链接")

带傅里叶的文丘里 ADF（斜体）

verdana*it *=\_ _<manim.utils.tex.TexTemplate\_\_对象>_ [#](#manim.utils.tex_templates.TexFontTemplates.verdana_it "此定义的固定链接")[](#manim.utils.tex_templates.TexFontTemplates.verdana_it "此定义的固定链接")

Verdana（斜体）

vollkorn _=_ _<manim.utils.tex.TexTemplate\_\_对象>_ [#](#manim.utils.tex_templates.TexFontTemplates.vollkorn "此定义的固定链接")[](#manim.utils.tex_templates.TexFontTemplates.vollkorn "此定义的固定链接")

Vollkorn（希腊语和数学符号的 TX 字体）

vollkorn*fourier_it *=\_ _<manim.utils.tex.TexTemplate\_\_对象>_ [#](#manim.utils.tex_templates.TexFontTemplates.vollkorn_fourier_it "此定义的固定链接")[](#manim.utils.tex_templates.TexFontTemplates.vollkorn_fourier_it "此定义的固定链接")

Vollkorn 与 Fourier（斜体）

zapf*chancery *=\_ _<manim.utils.tex.TexTemplate\_\_对象>_ [#](#manim.utils.tex_templates.TexFontTemplates.zapf_chancery "Permalink to this definition")[](#manim.utils.tex_templates.TexFontTemplates.zapf_chancery "此定义的固定链接")

扎普夫办公厅
