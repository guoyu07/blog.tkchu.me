---
layout: post
title: Unity 使用作业流程规范
category: program
---

使用Unity有一段时间了，需要总结一下工作流程，这样可以按部就班的完成作业，避免之后不知道自己该做些什么的窘境。

整个流程如下，表情用于记录commit时加的标签

1. 使用语音记录的方式记录自己设计的机制
2. 使用AI进行切图并设计界面
3. 根据界面文件将Sprite导入
4. 编写交互逻辑Mono文件
5. 编写内部逻辑
6. 视情况决定是否编写持久化和本地化文件
7. 重构

<span name="cross_fire">程序类型：</span>

1. 交互：继承MonoBehavior；命名为`*Mono.cs`
  - 在这里的所有引用都是Transform
  - 先获取子对象，再是外部对象
2. UI: 命名为`*UI.cs`
  - 对Transform进行变换
3. 内部逻辑：继承Object；命名为`*.cs`
  - 这里所有的引用是Component
4. 持久化：继承IO；命名为`*IO.cs`
  - 负责存储数据
5. 本地化：使用`TextLocal`&&`UITextLocal`&&`ImageLocal`

<aside name="cross_fire">

这种划分有个问题:脚本间无法顺畅通信。这点尚未找到一个优雅的解决方案。

</aside>

变量顺序：

1. 外部组件`Transform`，`Component`等等
2. 内部部组件`Transform`，`Component`等等
3. 公开可供修改参数
4. 内部参数

函数顺序：

1. 内部继承函数`Awake`，`Start`，`Update`，`OnEnable`，`OnDisable`
2. 外部调用函数 `public`
3. 内部辅助函数 `private`
