+++
title = 'Vim操作手册'
date = 2024-09-09T18:35:25+08:00

categories = ["vim"]
tags = ["vim" ,"命令"]

+++





# 1. 关于Vim

## 1.1 Vim的几种模式

- 正常模式：可以使用快捷键命令，或按:输入命令行。
- 插入模式：可以输入文本，在正常模式下，按i、a、o等都可以进入插入模式。
- 可视模式：正常模式下按v可以进入可视模式， 在可视模式下，移动光标可以选择文本。按V进入可视行模式， 总是整行整行的选中。ctrl+v进入可视块模式。
- 替换模式：正常模式下，按R进入。



# 2. 启动Vim

- vim -c cmd file: 在打开文件前，先执行指定的命令；
- vim -r file: 恢复上次异常退出的文件；
- vim -R file: 以只读的方式打开文件，但可以强制保存；
- vim -M file: 以只读的方式打开文件，不可以强制保存；
- vim -y num file: 将编辑窗口的大小设为num行；
- vim + file: 从文件的末尾开始；
- vim +num file: 从第num行开始；
- vim +/string file: 打开file，并将光标停留在第一个找到的string上。
- vim --remote file: 用已有的vim进程打开指定的文件。 如果你不想启用多个vim会话，这个很有用。但要注意， 如果你用vim，会寻找名叫VIM的服务器；如果你已经有一个gvim在运行了， 你可以用gvim --remote file在已有的gvim中打开文件。





# 3. 文档操作

- :e file --关闭当前编辑的文件，并开启新的文件。 如果对当前文件的修改未保存，vi会警告。
- :e! file --放弃对当前文件的修改，编辑新的文件。
- :e+file -- 开始新的文件，并从文件尾开始编辑。
- :e+n file -- 开始新的文件，并从第n行开始编辑。
- :enew --编译一个未命名的新文档。(CTRL-W n)
- :e -- 重新加载当前文档。
- :e! -- 重新加载当前文档，并丢弃已做的改动。
- :e#或ctrl+^ -- 回到刚才编辑的文件，很实用。
- :f或ctrl+g -- 显示文档名，是否修改，和光标位置。
- :f filename -- 改变编辑的文件名，这时再保存相当于另存为。
- gf -- 打开以光标所在字符串为文件名的文件。
- :w -- 保存修改。
- :n1,n2w filename -- 选择性保存从某n1行到另n2行的内容。
- :wq -- 保存并退出。
- ZZ -- 保存并退出。
- :x -- 保存并退出。
- :q[uit] ——退出当前窗口。(CTRL-W q或CTRL-W CTRL-Q)
- :saveas newfilename -- 另存为
- :browse e -- 会打开一个文件浏览器让你选择要编辑的文件。 如果是终端中，则会打开netrw的文件浏览窗口； 如果是gvim，则会打开一个图形界面的浏览窗口。 实际上:browse后可以跟任何编辑文档的命令，如sp等。 用browse打开的起始目录可以由browsedir来设置：
  - :set browsedir=last -- 用上次访问过的目录（默认）；
  - :set browsedir=buffer -- 用当前文件所在目录；
  - :set browsedir=current -- 用当前工作目录；
- :Sex -- 水平分割一个窗口，浏览文件系统；
- :Vex -- 垂直分割一个窗口，浏览文件系统；











\> 在这篇博客中，我引用了作者详细介绍的 Vim 的使用技巧。更多内容请查看原文：[Vim 笔记](https://www.cnblogs.com/jiqingwu/archive/2012/06/14/vim_notes.html)。





