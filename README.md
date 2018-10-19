# HUDthesis
###### The LaTeX template of thesis of HDU 

## 杭州电子科技大学计算机学院硕士研究生学位论文LaTeX模板
模板上游1：[ZJU-Awesome](https://github.com/ZJU-Awesome/write_with_LaTeX)<br>
模板上游2: [HDU](https://github.com/hduffddybz/HDU-thesis)<br>
模板改造者：  Chaoping Ding&&Mingying Huang
## 联系
如有问题请联系：dcp632013350+contact@gmail.com

---

## 1、简介

为了方便学位论文的排版，让作者专心于内容，
根据[《杭州电子科技大学研究生学位论文格式统一要求（杭电研[2012]311号）》](http://grs.hdu.edu.cn/2013/0507/c1730a51754/page.htm)，并结合实际，改造设计了相应的LaTeX模版。


[**本模板建议杭电计算机学院同学使用**]
---
# window系统下环境配置
---

# 前言：
利用TeX Live+WinEdt+SumatraPDF编写大论文，支持中文编码。
# 需下载软件：
- [TeX Live](https://mirrors.shu.edu.cn/CTAN/systems/texlive/Images/?C=M&O=A)
- [SumatraPDF](https://www.sumatrapdfreader.org/downloadafter.html)
- [WinEdt](http://www.ctex.org/CTeXDownload/)
---

[WinEdt和SumatraPDF安装配置详情](https://blog.csdn.net/qq_25073545/article/details/79265461)

----

# TeX Live环境配置

若要安装 TeXLive ，推荐下载 TeXLive 的 ISO 镜像，因为在线安装下载过程会很慢。如果网速快也可以在线安装。下载地址：http://mirror.ctan.org/systems/texlive/Images/ （该地址会自动分配速度最快的镜像）。

下载完成后，挂载镜像，执行 install-tl-windows.bat 或者 install-tl-advanced.bat 开始安装。
按照自己的需求进行设置，完成后点“安装 TeXLive”
等待安装结束即可。
[TeX Live安装文档](https://github.com/dcpnonstop/blogpic/blob/master/texlive-zh-cn.pdf)

最后还需要手动配置环境变量，在高级系统设置的环境变量页面中，系统变量里面找到 PATH，并在末尾添加“;C:\texlive\bin\win32”（在本例中路径为 C:\texlive\ ，请根据实际情况自行更换路径。效果以打开命令提示符，能正常执行latex命令为准。
# 为WinEdt配置TeX Live环境

1. 下载完成之后就是更改WinEdt的配置了。先配置编译引擎为TeX Live。选择Options->Execution Modes->Tex System，把TeX Root更改为TeX Live 的安装路径，把TeX Bin中的路径更改为TeX Live子文件夹”\bin\win32”，后面的两个选择Auto-detect就可以了，点击应用后会自动刷新编译器。 
![win](https://raw.githubusercontent.com/dcpnonstop/blogpic/master/winedt.jpg)
---

2. 然后更新PDF预览器。在Options->Execution Modes->PDF Viewer 中把包含SumatraPDF.exe的路径替换原来路径，这样就行了。选择SumatraPDF是因为这个阅读器非常轻量，而且能够支持反向搜索，点击PDF中的文字可以快速定位到相应的代码位置，非常方便。

![pdf](https://raw.githubusercontent.com/dcpnonstop/blogpic/master/sumaPDF.jpg)

---
3. 打开相应的.tex文件，按照下图选择**XeLaTex**，然后运行即可
![run](https://raw.githubusercontent.com/dcpnonstop/blogpic/master/run.jpg)

### 现在可以开始尽情的写论文啦~

----
# 杭州电子科技大学硕士论文模板
[杭州电子科技大学硕士论文latex论文模板](https://github.com/dcpnonstop/HDUthesis)

---
mac下环境配置
---
## 2、编译方法

### 2.1 使用mac的用户请看下面（windows用户直接略过）

使用mac或者linux的用户可以通过下面的途径下载Adobe字体，解压放到～/Library/Fonts目录下(如果不知道怎么放入————第一步：打开访达；第二步：按住shift+command+g,这时候就出现了～/Library目录，再进入Fonts目录，把字体放入即可）
第三步：把解压的字体包直接放入到Fonts目录，保存即可)，即可解决编译时出现的字体找不到错误。

- [字体包下载-百度盘](https://pan.baidu.com/s/16enRqhqjpeSvxiaKkQ07jg)


### 2.2、 __OS X__ （[MacTeX2016](https://tug.org/mactex/) 不低于 OS X Yosemite 通过）

拷贝 .latexmkrc 到家目录

    $ cp latexmkrc_mac ~/.latexmkrc

使用latexmk 命令进行编译。
如果您遇到编译错误，请检查是否正确安装mactex和以上字体包。

	$ latexmk main


### 2.3、 __windows__ （仅在[TexLive2016](http://mirrors.ustc.edu.cn/CTAN/systems/texlive/Images/texlive2016.iso) on windows10 测试）:

首先在环境变量里设置```$HOME```，一般是```C:\Users\<username>```

添加或修改 .latexmkrc前，请做好备份。

    \> copy latexmkrc_win %HOME%\.latexmkrc

一样使用 latexmk 命令进行编译。
如果您遇到编译错误，请检查是否正确安装texlive和以上字体包。

### 2.4、__Linux__ (TeXLive2016):

首先添加或修改 .latexmkrc，请做好备份。

    $ cp latexmkrc_linux ~/.latexmkrc

然后使用 latexmk 命令进行编译。
如果您遇到编译错误，请检查是否正确安装texlive以上字体包。

windows和Linxu 皆使用 TeXLive 2016 安装
[TeXLive 2016 中文文档](https://www.tug.org/texlive/doc/texlive-zh-cn/texlive-zh-cn.pdf)

### 2.5、 开启实时编译(OS X)

论文编译时间通常在20秒以上，
为减少论文修改时的查错成本，
强烈建议设置**实时编译**。
方案如下：

由于 OS X 默认的 Preview 不支持自动刷新，
所以不得不安装 [skim](https://sourceforge.net/projects/skim-app/) pdf 阅读器，
若不信任此应用，请参照之后方法自行解决。
安装完成后，在 Sync(同步) 设置处打开 Check for file Changes。
同时修改家目录的 `latexmkrc` 文件。（如果您使用的是 OS X 默认 sed 请执行）

    $ sed -i '' -e '$ d' ~/.latexmkrc
    $ echo "\$pdf_previewer = 'open -a /Applications/Skim.app %O %S';" >> ~/.latexmkrc

现在修改论文源码前，可以在 main.tex 的路径下输入命令

    $ latexmk -pdf -pvc -xelatex main

为简化需要在终端输入的命令，可以在日常设定的 rc 文件中自行加入一个 alias

如果仅仅编译一次论文，则在论文根目录下输入命令

    $ latexmk main

若出现连续几次编译错误并且确信论文源码并无语法错误，则可以尝试清空临时文件的命令再编译

    $ latexmk -c && latexmk main

有洁癖的极端处女座，可以输入以下内容保证每次实时编译都清理临时文件：

    $ echo "\$clean_ext = 'synctex.gz synctex.gz(busy) acn acr alg aux bbl bcf blg brf dvi fdb_latexmk glg glo gls idx ilg ind ist lof log lot lox out paux pdfsync run.xml toc';">>~/.latexmkrc


## 3、相关资源文件说明
```tex
├── clean.bat % windows的清理批处理
├── contents  % 被引用的内容 不可嵌套引用
│   ├── abstract_chinese.tex
│   ├── abstract_english.tex
│   ├── intro.tex
│   ├── whyla.tex
│   ├── elem.tex
│   ├── sum.tex
│   └── thanks.tex
├── main.tex % 论文主源码（通过 include 以上文件来组成论文内容）
├── figures  % 引用图片目录
│   ├── ...
│   ├── ...
│   └── ...
├── gbt7714-2005.bst   % 参考文献样式（南京大学胡海星）
├── logo
│   ├
│   └── HDUlogo.pdf
├── references % 论文引文数据库 自行维护
│   └── test.bib
├── hduthesis.cls       % 论文全书样式 小心查看和修改 避免手残
└── ...
```

通过 `latexmk main` 将论文编译出来后，请检视内容尝试理解本论文模板。

## 4、注意事项

建议使用TeXLive 2016及以上发行版，并采用XeLaTeX进行编译。
论文模板属于学习交流性质，
暂无任何官方机构为本模板合法性背书。
另请**妥善维护**自己的论文资料，
对论文排版过程中造成的不可预见的意外本人概不负责。

目前已知的一个难解问题在于生僻字的排印问题：
如果在论文段落以外的区域排版生僻字，将高于当前行基线一个微小的单位。
本人提供一个不得已为之的解法：为此生僻字预留一个em框（可能涉及更动论文模板，请参照修改），
在论文输出后利用OS X 的 Preview 提供的编辑功能补上该生僻字的文本框。

## 5、许可权和贡献

**MIT** 

欢迎 issue 和 PR，方便大家一起探讨
