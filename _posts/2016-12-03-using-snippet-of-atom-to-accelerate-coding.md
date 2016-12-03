---
layout: post
title: 使用Atom的Snippet加速编码
---

![一个使用Snippet加速编码的动图示例]({% if site.cdnurl %}{{ site.cdnurl }}{% else %}{{ site.baseurl }}assets{% endif %}/fast-programming-snippet.gif)

<span name="simple code"></span>

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

如果你是程序员，那么你理应厌烦：又一次重复得输入`for`,`[]`,`{}`……而且一个不小心，还很容易输入错误。浪费时间寻找哪里少了一个分号可不是你该做的事情。

<aside name="simple code">
老实说，这种遍历你应该考虑foreach或者是enumerate之类的东西，或者使用迭代器。
不过这里只是做个说明，为此我们保持精简。
</aside>

那么不如来试试Snippet，一小段预先定义好格式的代码块。下次使用时，只需填入变化的部分。是的，就像填表一样。

## 在Atom中设置你的Snippet

为了在Atom中使用Snippet，你需要首先定义好你的代码块格式。

Linux环境下，进入Edit->Snippets...，相对应的，在Windows下是File->Snippets...。

这实际上是一个cson文件，格式如下：

    '.source.python':                         # 在何种文件中使用这个Snippet
      'python coding':                        # 对Snippet的简短说明
        'prefix': 'coding'                    # 输入什么前缀可以触发这个Snippet
        'body': '# -*- coding:utf8 -*-\n'     # Snippet的内容

第一行指定在何种文件中使用Snippet，你可以在设置的Packages中的Installed Package里搜索你要用的编程语言。
点击对应的包，通常名字是：language-编程语言。在打开的包里看看Scope是什么。
常用的几种如下：

| 文件后缀     | Scope     |
| :------------- | :------------- |
| .c .h  | .source.c |
| .py | .source.python |
| .java   | .source.java |
| .js | .source.js |
| .css | .source.css |
| .md | .source.gfm |


## 第一个示例：指定Python文件的编码

我们都知道，如果你在python2中使用中文，在Python文件开头，你需要添加这么一段代码，指定这个文件的编码格式：

    # -*- coding:utf8 -*-

每次都要输入，重复！那就把它变成一段Snippet吧：

    '.source.python':
      'python coding':
        'prefix': 'coding'
        'body': '# -*- coding:utf8 -*-\n'

这样，在打开.py文件后，只需输入`coding`，然后按下Tab键，这段遍布着`*`的代码行就一下子输入成功了。

## 第二个示例：划分你的代码

还是在Python中，如果你想要添加一段像下面这样的代码，将你的.py文件划分成多块的话：

    #=====================
    # 数据爬取结束，开始匹配
    #=====================

这时候，中间的文字是你每次都需要更改的部分，当然可以在输入其他部分后再移到中间部分进行编辑，但我们有更好的东西：

<span name="same code"></span>

    '.source.python':
      'python coding':
        'prefix': 'coding'
        'body': '# -*- coding:utf8 -*-\n'
      'section':
        'prefix': 'section'
        'body': '#=====================\n# $1\n#=====================\n$2'

<aside name = "same code">

注意，对同一后缀文件的Snippet，都得写在一起。

</aside>

$1表示光标第一次所处的位置，按一下Tab后光标会移到$2所处的位置。

在这个例子中，输入section然后按Tab，光标就自动出现在这段代码的中间，输入完中间部分，再按Tab，光标就会移动到这段文字的最后。你可以继续编码，而无需浪费时间在移动光标上。

## 第三个示例：同时编辑多处

在上面，我们使用`\n`划分多行，但是行数一多，这样看起来就眼花缭乱了，我们可以使用`"""`来编写多行的Snippet：

    '.source.java':
      'iterate two dimension array':
        'prefix' : 'for2'
        'body' : """
          for(int $1 = 0; $1 < $2; $1++){
            for(int $3 = 0; $3 < $4; $3++){
              $5[$1][$3]$6
            }
          }
          $7
        """

Atom的一个优势就是可以同时修改文件的不同位置，Snippet自然支持这一点。
你会注意到，$1出现三次，这意味着一次键入，三处输入。这样不但快捷，还能保证命名一致。（错也会错成一样的）。

## 要注意的

- Snippet很方便，但只有你用起来的时候才能加速你的编码。要记得使用，直到肌肉有了记忆，自然而然地使用Snippet。
- Snippet的介绍似乎不是很重要，但安装了其他人的Snippet后，你需要这些介绍来进行区分，所以还是要认真编写的。
- 保持开心，如果Snippet用起来感觉不是爽而是痛苦，那就不要使用它。也许你会发现，这些重复的编码可以用其他的东西来解决，比如`map`函数。
