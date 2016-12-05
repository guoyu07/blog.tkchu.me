---
layout: post
title: Atom插件推荐
---

你该用什么文本编辑器呢？

<span name="emergency"></span>

使用传统的vi确实是有好处的。
如果能够熟练掌握，它能加速你的编码过程，而且当你ssh到远程服务器时，vi总是在那里等着你！

<aside name="emergency">
一般我会考虑把文件拖回本地处理完再推上去。这样本地至少还有个备份。
</aside>

<span name="force"></span>

但是vi很难学习，更加难以对其进行扩展。它更像是一台专业级车床，而我们日常的编码工作往往只是打磨一些接合处。
因此我的主力文本编辑器是[Atom](https://atom.io/)。除开Atom漂亮，对Github友好的特性以外，它还有很多优秀的Plugin供你使用。下面是几个我认为值得推荐的实用Plugin。

<aside name="force">
同时强迫你使用SSD并加大你的内存。你也可将这点视为优点，如果你把帽子扔过了墙，你就得想办法翻墙过去。笑。
</aside>

Atom支持的所有Plugin可以在[这里](https://atom.io/packages/list)看到。按照下载量对其进行排序，你可以找到很多有趣的Plugin。下面推荐几个没怎么被人提及的，像pigment这样广为人知的就不提了。

## [Sync Setting](https://atom.io/packages/sync-settings)

Sync Setting使用github的gist功能，在不同的电脑间同步Atom的设置，Snippet，KeyMap，甚至你的Plugin列表。
真正的一次配置，到处使用。
如果你知道其他人设置的Gist的ID，你还可以Fork其他人的设置。唯一美中不足的是，第一次使用创建Gist需要翻墙，但是之后同步设置就不需要了。

---

<span name = "file management"></span>
<aside name = "file management">
文件管理
</aside>

## [Tree View Git Status](https://github.com/subesokun/atom-tree-view-git-status)

这个插件能让你在侧边栏里看到Git的情况，表明哪些文件进行了修改，哪些文件是新增的，以及你本地的代码库和远程的代码库差了多少个commit。

在工作中，它的主要作用是提醒你：你的工作还没有commit，是忘了还是真的没有完成一个feature？

## [Git Control](https://atom.io/packages/git-control)

Git Control为Atom提供了一个图形化的Git界面，包含了大多数需要的Git指令。
虽然我们更加崇尚完全的命令行操作，但其实使用图形化界面可以作为一种节奏调节：经历了漫长的击键编码后，用用鼠标进行懒散的提交吧。
而且还内在地支持了[GitFlow](http://danielkummer.github.io/git-flow-cheatsheet/index.zh_CN.html)这种工作流，不用每次在多个branch间来回切换了。

## [Git Time Machine](https://atom.io/packages/git-time-machine)

Git Time Machine可以让你查看某个文件的历史版本，同时标注出它与当前版本的差异之处。
当你不但需要知道修改了哪些地方，还想要知道修改的上下文时，这个工具很有价值。
特别是你修改别人的代码，发现自己搞砸了，想看看别人代码修改前的原貌时，有了这个能让你飞起来。

## [Local History](https://atom.io/packages/local-history)

这个保存了你每一次的修改，算是在commit之前的版本管理。
如果你一不小心进行了太多次撤销，之后手忙脚乱地进行了错误的键入以至于没法使用重做恢复，这玩意能救你于水火之中。
当然，如果你常常使用commit，这种情形对你来说应该不常发生，但是，有备无患。

---
<span name="strengthen"></span>
<aside name="strengthen">
增强显示效果
</aside>

## [File Icons](https://atom.io/packages/file-icons)

在侧边栏显示的文件会根据后缀显示不同的彩色图标。yeap，能让你心情更好一些。

## [Highlight Line](https://atom.io/packages/highlight-line)和[Highlight Selected](https://atom.io/packages/highlight-selected)

分别是高亮光标所在行和高亮当前选中的内容。在盯了一天屏幕后，那个细细小小的光标就像是隐形了，这个插件能让你找到它。
哦，不过你得使用有区分度的配色方案，如果高亮的颜色和背景色几乎一样，那么高亮也没什么意义。

---

<span name="quick input"></span>
<aside name="quick input">
快捷输入
</aside>

## [Color Picker](https://atom.io/packages/color-picker)

用快捷键调出一个调色板，选择颜色按回车输入相应颜色的代码。
因为每一次调用的时候，都会随机出一种新颜色，所以可以可以免去调色的苦恼。支持的颜色代码范围也很广泛，足以应对大部分需求。

## [Markdown Writer](https://atom.io/packages/markdown-writer)

强化Atom的Markdown输入体验。特别适合创建博客时使用。迅速的创建新博文，为博文加上日期，将博文从草稿移到发布。

## [Markdown scroll sync](https://atom.io/packages/markdown-scroll-sync)

在预览Markdown时，保持MarkDown内容和预览内容位置保持一致。
如果你使用Atom预览结果，这能让你有一种实时编辑的感觉。

## [Multi Cursor](https://atom.io/packages/multi-cursor)

使用键盘插入多个光标，不必再用鼠标一个个点了，避免鼠标一次点错前功尽弃的情况。
警告：如果你没有使用SSD，不要尝试一次性输入超过50个光标，否则就会失去响应。
（等上一会能够复原，但失去响应这种糟糕情况应该只发生在面对人类时。）

这就是我推荐的Atom插件，如果想要找更加编程语言相关的插件，去[这里](https://atom.io/packages/list)搜搜看吧。
