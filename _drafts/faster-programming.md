---
layout: post
title: Atom插件推荐
---

你该用什么文本编辑器呢？

<span name="emergency"></span>

使用传统的vi之类的编辑器确实是有好处的。
它能加速你的编码过程，即使是ssh到远程服务器，vi总是在那里等着你！

<aside name="emergency">

一般我会考虑把文件拖回本地处理完再推上去。这样本地至少还有个备份。

</aside>

但是vi很难学习，它更像是一台专业级车床，而我们日常的编码工作往往只是打磨一些接合。
我推荐你使用[Atom](https://atom.io/)。

<span name="force"></span>

它看上去很漂亮，支持snippets，帮你快速输入代码，还有很多优秀的plugin。

<aside name="force">
同时强迫你使用SSD并加大你的内存。你也可将这点视为优点，如果你把帽子扔过了墙，你就得想办法翻墙过去。笑。
</aside>

# snippets

首先要推荐snippets，这能让你快速输入固定格式的代码块。

<span name="simple code"></span>

<aside name="simple code">
老实说，这种遍历你应该考虑foreach或者是enumerate之类的东西，或者使用迭代器。
不过这里只是做个说明，因此用了这么一个简陋的例子。
</aside>

我们经常需要对二维数组进行迭代，比如这样：

    for(int x = 0; x < width; x++){
      for(int y = 0; y < height; y++){
        screen[x][y].setColor("black");
      }
    }

过上一段时间，你又要写这么一段代码：

    for(int i = 0; i < rows; i++){
      for(int j = 0; j< columns; j++){
        objects[i][j].update();
      }
    }

如果你是程序员，那么你理应厌烦：又一次重复得输入`for`,`[]`,`{}`……而且一个不小心，还很容易输入错误。

那么不如来试试Snippet。
在菜单的Edit->Snippet...中进入Snippet配置界面。

for(int i = 0; i < columns; i++){
  for(int j = 0; j < rows; j++){
    objects[i][j].update();
  }
}

https://atom.io/packages/list
plugin:


workflow
keymap
snippets
