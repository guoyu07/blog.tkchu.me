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

Atom支持的所有Plugin可以在[这里](https://atom.io/packages/list)看到。按照下载量对其进行排序，你可以找到很多有趣的Plugin。

## [Sync Setting](https://atom.io/packages/sync-settings)

Sync Setting使用github的gist功能，在不同的电脑间同步Atom的设置，Snippet，KeyMap，甚至你的Plugin列表。
真正的一次配置，到处使用。
非常好用，你还可以Fork其他人的设置，唯一美中不足的是，第一次使用需要翻墙。

---

**文件管理：**

## [Tree View Git Status](https://github.com/subesokun/atom-tree-view-git-status)

这个插件能让你能在侧边栏里看到Git的情况，表明哪些文件进行了修改，哪些文件是新增的，以及你本地的代码库和远程的代码库差了多少个commit。

## [Git Control](https://atom.io/packages/git-control)

Git Control为Atom提供了一个图形化的Git界面，包含了大多数需要的Git指令，而且还内在地支持了[GitFlow](http://danielkummer.github.io/git-flow-cheatsheet/index.zh_CN.html)这种工作流程。

## [Git Time Machine](https://atom.io/packages/git-time-machine)

Git Time Machine可以让你查看某个文件的历史版本，同时标注出它与当前版本的差异之处。当你不但需要知道修改了哪些地方，还想要知道修改的上下文时，这个工具很有价值。

## [Local History](https://atom.io/packages/local-history)

这个保存了你每一次的修改，算是在commit之前的版本管理。如果你一不小心进行了太多次撤销，之后手忙脚乱地进行了错误的键入以至于没法使用重做，这玩意能救你于水火之中。

---

**增强显示效果：**

## [File Icons](https://atom.io/packages/file-icons)

在侧边栏显示的文件会根据后缀显示不同的图标。

## [TODO Show](https://atom.io/packages/todo-show)

高亮显示TODO，更容易找到。

## [Highlight Line](https://atom.io/packages/highlight-line)

高亮光标所在行。

## [Highlight Selected](https://atom.io/packages/highlight-selected)

高亮当前选中的内容，在文中其他的出现相同的内容也会高亮。

---

**快捷输入：**

## [Color Picker](https://atom.io/packages/color-picker)

用快捷键在文中选择颜色并插入

## [Markdown Writer](https://atom.io/packages/markdown-writer)

强化Atom的Markdown输入体验。可以迅速的创建新博文，为博文加上日期等等。

## [Markdown scroll sync](https://atom.io/packages/markdown-scroll-sync)

在预览Markdown时，保持MarkDown内容和预览内容位置保持一致。

## [Multi Cursor](https://atom.io/packages/multi-cursor)

使用键盘插入多个光标。
