---
uid: 2023120719261835
title: Obsidian 插件：【Readme】Daily Note Outline
tags: ['obsidian插件', 'readme']
description: 添加一个自定义视图，显示多个日常笔记的大纲，包括标题、链接、标签和列表项。
author: AI
type: readme
draft: false
editable: false
modified: 20230101000000
---

# Obsidian 插件：【Readme】Daily Note Outline

> [!Note] 插件名片
> - 插件名称：Daily Note Outline
> - 插件作者：iiz
> - 插件说明：添加一个自定义视图，显示多个日常笔记的大纲，包括标题、链接、标签和列表项。
> - 插件分类：['obsidian 插件 ', 'readme']
> - 项目地址：[点我访问](https://github.com/iiz00/obsidian-daily-note-outline)
> - 国内下载地址：[下载安装](https://pkmer.cn/products/plugin/pluginMarket/?obsidian-daily-note-outline)

## 概述

添加一个自定义视图，显示多个日常笔记的大纲，包括标题、链接、标签和列表项。

![Daily Note Outline](https://cdn.pkmer.cn/covers/obsidian-daily-note-outline.png!pkmer)

> [!tip] 原文出处
>
>下面自述文件的来源于 [Readme](https://ghproxy.net/https://raw.githubusercontent.com/iiz00/obsidian-daily-note-outline/master/README.md)
>

---

## Readme(翻译）

下面是 [[obsidian-daily-note-outline]] 插件的自述翻译

# Obsidian 每日笔记大纲

Japanese documentation is located on the second half of this page.

## 简介

每日笔记是记录各种小笔记和想法的好地方。然而，有时候很难找到你之后写在哪个每日笔记中。<br>
这个插件创建了一个自定义视图，可以同时显示多个每日笔记的大纲。大纲不仅可以显示标题，还可以显示链接、标签和列表项。

![screenshot](https://cdn.pkmer.cn/covers/obsidian-daily-note-outline_2_0.png!pkmer)

![demo](https://cdn.pkmer.cn/covers/obsidian-daily-note-outline_2_1.gif)

## v1.0.0 的新功能 - 支持 Periodic Notes 插件

Daily Note Outline v1.0.0 添加了对周期性笔记的支持作为新功能。也就是说，支持每周/每月/每季度/每年的笔记和日历集。

（有关周期性笔记的更多信息，请参见<https://github.com/liamcain/obsidian-periodic-notes）<br>>

要在 DNO 中显示周期性笔记，需要执行以下步骤。

- 安装并激活 Periodic Notes 社区插件，并正确配置要使用的粒度和文件夹路径。
- 在 DNO 设置的“Periodic Notes”部分激活“periodic notes”和“calendar sets”。

**注意事项**

- Calendar sets 是在 Periodic Notes v1.0.0-beta 版本中添加的功能，在 v0.0.17 版本中不可用。要使用日历集功能，必须安装 Periodic Notes 的 beta 版本，例如使用 Obsidian BRAT 插件。
	- 另外，由于日历集是 Periodic Notes 的 beta 功能，存在一种可能性，即由于 Periodic Notes 的规范更改，将来可能无法在 DNO 中使用该功能。
- 如果发现任何问题，请在论坛或 GitHub 存储库中告诉我。

### 使用方法

- 激活功能后，当前的粒度（天/周/月/季度/年）和日历集名称将显示在 DNO 的视图上。
- 单击它们将切换粒度或日历集以便按顺序显示。右键单击它们将显示一个列表，允许您选择一个。

![SS2](https://cdn.pkmer.cn/covers/obsidian-daily-note-outline_2_2.png!pkmer)

## 入门指南

从社区插件列表中安装插件。<br>
确保启用了 Daily Note 核心插件或 Periodic Notes 插件。<br>
要显示大纲，请在命令面板中选择“Daily Note Outline: Open Outline”。<br>

如何使用

要更改要显示的日期范围，请单击左右箭头。

要返回初始日期范围，请单击房子图标。

单击刷新图标以重新绘制轮廓。

单击齿轮图标以打开设置（右键单击可打开上下文菜单，您可以快速更改多个设置）。

单击带有加号图标的日历以创建/打开今天的日记（右键单击可以创建/打开明天的日记）。

单击每个轮廓元素以打开其位置。

按下 Ctrl 键进行预览。

我建议您首先在设置中设置每个轮廓元素（标题、链接、标签和列表项）的显示/隐藏设置。

## 特征

### 简单过滤器/包含/排除

为了隐藏不必要的项目并仅显示必要的项目，实现了三种类型的过滤器功能：**简单过滤器**、**包含**和**排除**。

**简单过滤器**只是隐藏与指定的单词或短语匹配的项目。不考虑项目的层次结构。<br>
**包含**只能应用于一种类型的大纲元素。它将从指定类型的大纲元素到下一个相似元素的范围视为一个块，并且只显示与指定的单词或短语匹配且属于该块的项目。<br>
相反，**排除**隐藏匹配的项目及其块。如果在设置的“排除结束于”部分指定了一个元素类型，或者启用了包含功能，则该块被认为在该元素处结束，只有该块的部分被隐藏。

**包含**和**排除**可以同时使用。（但是，对于在包含中指定的元素类型指定排除关键字是没有意义的。）

**简单过滤器**可以与其他过滤器一起使用。例如，如果您指定与包含关键字相同的关键字，您可以仅显示属于与包含关键字匹配的元素的元素，而不是元素本身。

### 提取

您可以提取只包含特定单词的大纲元素。有三种方法可以实现这一点。<br>

1. 点击放大镜按钮，然后输入您想要提取的字符串。<br>
2. 右键单击大纲元素，然后从上下文菜单中选择“提取”。只会提取包含相同名称的元素。<br>
3. 右键单击放大镜按钮，然后选择“提取任务”。只会提取具有复选框的列表项。<br>
被过滤或其他方式隐藏的项目将不会显示。<br>
要取消提取，请点击 X 按钮（放大镜按钮将变为 X 按钮）。<br>

## 设置

一些子项在初始状态下不会显示，只有当父项打开时才会出现。

### 基础知识

#### 初始搜索类型

- 向后（默认）
	- 显示从今天开始的过去若干天的日记。<br>
- 向前
	- 显示从起始日期指定的日期开始的若干天的日记。<br>

#### 包括未来的日记

当使用向后搜索时，还会显示未来指定天数的日记（如果设置得足够长，您还可以将此插件用作即将发生事件的列表！）。

#### 开始日期

对于正向搜索，在启动时指定以 YYYY-MM-DD 格式开始搜索的日期。<br>
单击 UI 按钮下的日期范围可跳转到该日期。

#### 搜索持续时间

指定每页要探索的天数。建议每天使用每日笔记的人设置较短的时间段，而偶尔使用的人则设置较长的时间段。我建议大约 7-56 天。

#### 显示标题/链接/标签/列表项和任务

选择是否在大纲中显示每个元素。

显示所有根列表项

关于列表项，如果此设置关闭，则仅显示连续列表中的第一项。当打开时，它会显示所有根级别的列表项。

显示所有任务/仅任务/隐藏已完成任务

任务的显示设置（包括复选框的列表项）。

显示所有任务将显示所有级别的任务，不考虑上述列表设置；仅任务将隐藏除任务外的所有列表项；隐藏已完成任务将隐藏已完成的任务。

#### 显示文件信息

在每个日记文件名的右侧显示文件信息。<br>
行数：文件中的行数<br>
距离：句号与基准日期的距离（对于向后搜索是今天，对于向前搜索是在开始日期中指定的日期）

#### 插件视图的位置

在重新显示或更新时指定插件视图的显示位置。

（您可以指定除左侧和右侧边栏以外的位置，但行为可能不够复杂。）

### 周期性笔记

除非激活了周期性笔记社区插件，否则本节不会显示。

#### 日历集

如果您想在周期性笔记插件中使用日历集，请打开此选项。（必须安装周期性笔记的 beta 版本）

#### 定期笔记

如果您想使用定期笔记，请打开此选项。

#### 搜索周期性笔记的持续时间

为每个周期性笔记指定每页的搜索持续时间。

将日期范围附加到每周笔记的文件名旁边显示。

### 标题

#### 要显示的标题级别

选择是否在大纲中显示每个级别的标题。

### 预览

#### 内联预览

在每个大纲元素旁边显示几个连续的单词。

#### 工具提示预览

将后续的句子显示为鼠标悬停的工具提示。

#### 工具提示预览方向

指定显示工具提示预览的方向。<br>
（我找不到自动确定适当方向的方法...）

### 简单过滤器

#### 忽略的标题/链接/标签/列表项

如果每个大纲元素包含指定的单词或短语，则该大纲元素将不会显示。

每行指定一个。

### 包括

#### 包含的元素类型

指定要应用包含过滤器的大纲元素类型。

仅显示包含指定单词或短语的大纲元素及其后面的块。每个应该用新行分隔。

指定是否显示在包含的元素类型中指定的大纲元素出现之前的注释的开头部分。

### 排除

排除结束于

如果在此字段中指定了任何大纲元素类型，则由排除过滤器排除的区域将在指定的元素处终止。

如果在包含过滤器中指定了任何类型，则排除将在该类型处终止，并且此字段将被忽略。

#### 要排除的标题/链接/标签/列表项

包含指定单词或短语的大纲元素及其后面的区域将被隐藏。

每个应该用新行分隔。

### 外观

设置每个大纲元素在显示时的外观。

可以为每个元素添加图标和前缀字符串。

如果选择“自定义”图标，则在“自定义图标”字段中输入 Lucide 图标（<https://lucide.dev/）的图标名称。某些图标似乎无法显示。>

除标题外的缩进

当您选择“跟随前面的标题”时，其他元素的缩进根据前面的标题级别进行调整。

标题：重复标题前缀

如果您为标题输入了前缀，打开此选项将会重复前缀的级别数。

#### 标题：添加缩进

根据标题的级别添加缩进。

任务：在前缀中添加复选框文本

在任务前缀的末尾添加一个指示复选框状态的字符串。

### 其他

#### 仅显示.md 文件/完全匹配的文件

如果您正在使用 Periodic Notes 插件的 beta 版本，将识别更多文件名作为周期性笔记。每个选项都会隐藏不是 md 文件或不符合格式的文件。

### 调试

#### 显示调试信息

如果打开，一些调试信息将显示在控制台中。

## 致谢

在开发这个插件时，我参考了 Obsidian 社区中许多优秀的插件。特别是：<br>
[@liamcain的每日笔记界面](https://github.com/liamcain/obsidian-daily-notes-interface) 用于处理每日笔记。<br>
[@st3v3nmw的间隔重复](https://github.com/st3v3nmw/obsidian-spaced-repetition) 和 [@tgrosinger的最近文件](https://github.com/tgrosinger/recent-files-obsidian) 用于创建自定义视图。<br>
创建新周期性笔记的代码部分修改自 [@liamcain的周期性笔记](https://github.com/liamcain/obsidian-periodic-notes)（MIT 许可证）。

我还在 Discord 的 plugin-dev 频道中搜索并参考了许多帖子。

如果你喜欢我的插件，我会很感激如果你能给我买杯咖啡！<br> [!["Buy Me A Coffee"](https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png)](https://www.buymeacoffee.com/iiz00)

## (想要) 做的事情

- 折叠一个笔记
- 笔记重构
- 在每天显示链接的提及/创建/修改的文件（从性能上来说可行吗？）
- 除了每日笔记外的其他衍生插件

### 完成

- 支持定期笔记
- 显示每个笔记的行数
- 如果没有大纲元素存在，则显示第一个部分
- UI 按钮用于更改设置
- 简单的过滤/包含/排除/提取
- 部分完成
	- 更好的预览

## 更新日志

- 1.2.2
	- 修复
		- 将提取函数更改为不区分大小写。
- 1.2.1
	- 修复
		- 修复了在 Obsidian v1.3.1（内部版本）中更改导致的外观错误。
- 1.2.0
	- 改进
		- 如果您正在使用周期性笔记插件的测试版，则将识别更广泛的文件名作为周期性笔记。如果您打开“设置 ->其他 ->仅显示完全匹配的文件”，您将只看到与格式完全匹配的文件。
- 1.1.1
	- 修复
		- 修复了有时会意外显示非 .md 文件的问题（您可以从“设置 ->其他 ->仅显示 .md 文件”重新显示它们）。
- 1.1.0
	- 改进
		- 现在可以从设置按钮的上下文菜单（右键单击齿轮图标）更改多个设置。
		- 当在设置 ->外观中指定时，除标题以外的大纲元素现在可以根据前一个标题进行缩进。
		- 星期几、周数和第一个标签已添加到可以在设置 ->显示文件信息中选择的项目列表中。
		- 现在可以从链接元素的上下文菜单中打开链接的笔记。
	- 修复
		- 修复：当使用周期性笔记插件 v0.0.17 时，如果将一周的第一天设置为星期一，则每周笔记将不会在 DNO 中显示。
		- 添加了一个设置，以在设置底部的控制台中显示调试信息。
			- 此功能旨在缩小使用周期性笔记插件测试版时无法切换到每周笔记的报告原因。
- 1.0.0
	- 测试新功能
		- 支持周期性笔记插件（显示周期性笔记、日历设置）
			- 您必须预先安装并启用周期性笔记社区插件。
	- 改进
		- 插件设置更改现在会自动反映在视图中。
	- 修复
		- 修复了一些大纲解析问题。
- 0.6.0
	- 新功能
		- 现在任务（复选框）与列表项分开处理
			- 您可以通过右键单击提取图标来提取任务。
		- 更改各个元素的外观（设置）
	- 改进
		- 从上下文菜单中，您可以在新标签页、分割窗格或弹出窗口中打开大纲元素。
		- 在设置中，当关闭主要项目时，现在会隐藏相关项目。
		- 提取模态框接受 Enter 键。
	- 修复
		- 修复了在某些情况下提取功能失败的问题。
- 0.5.0
	- 重要修复
		- 修复了在某些情况下移动版本中的过载问题。如果问题仍然存在，请告诉我。
	- 新功能
		- 提取
			- 您可以提取包含特定单词的大纲元素。
				1. 单击放大镜图标按钮并输入要提取的单词。
				2. 右键单击大纲元素，在上下文菜单中选择“提取”。然后只显示具有相同名称的元素。
				3. 要结束提取，请单击取消提取的按钮。
	- 改进
		- 添加了一个用于创建/打开今天的日记的 UI 按钮。
			- 右键单击该按钮会显示上下文菜单，以创建明天的日记。
		- 您可以从设置中选择此插件视图出现的默认位置。
- 0.4.0
	- 新功能
		- 包含/排除
			- 您可以包含或排除一些带有所属元素的大纲元素。
	- 改进
		- 更新后，插件现在会自动打开其视图（无需从命令面板重新打开）。
- 0.3.0
	- 新功能
		- 2 种新的预览方式
			- 1. 内联预览
				- 在每个大纲元素旁边显示几个后续单词。
			- 2. 工具提示预览
				- 鼠标悬停时，以工具提示的形式显示后续句子。
	- 改进
		- 添加了一个打开插件设置的 UI 按钮。
		- 单击日期范围以跳转到设置中的起始日期。
	- 修复
		修复了长名称项目溢出的问题。
- 0.2.0
	- 新功能
		- 按单词或短语筛选大纲元素。
		- 在文件名右侧显示一些文件信息。
		- 如果文件没有大纲元素，则显示文件的第一行。
	- 改进
		- 悬停预览现在显示每个元素的正确位置。
- 0.1.1
	- 初始发布。

# Obsidian Daily Note Outline 日本語ドキュメント

## 概要

Daily Notes 插件非常方便，可以用于记录一些简短的备忘录和杂乱的想法。然而，有时候我们会很难找到我们写在哪里的内容。

该插件可以在侧边栏中批量显示多个 Daily Notes 的大纲，以便更容易地了解所写的内容。它不仅可以显示标题，还可以显示链接、标签、列表项等。

![screenshot](https://cdn.pkmer.cn/covers/obsidian-daily-note-outline_2_0.png!pkmer)

![demo](https://cdn.pkmer.cn/covers/obsidian-daily-note-outline_2_1.gif)

## v1.0.0 新功能 - 支持周期性笔记插件

在 Daily Note Outline v1.0.0 中，我们添加了对周期性笔记的支持作为新功能。这包括对每周/每月/每季度/每年笔记以及日历集的支持。

（有关周期性笔记的详细信息，请参阅 <https://github.com/liamcain/obsidian-periodic-notes）>

要在 DNO 中显示周期性笔记，需要执行以下步骤：

- 安装并启用 Periodic Notes 社区插件，并进行适当的设置，如使用粒度和文件夹路径等。
- 在 DNO 的设置中的 "Periodic Notes" 部分，启用 "periodic notes" 和 "calendar sets"。

**注意事项**

- 日历集是在 periodic notes v1.0.0-beta 版中添加的功能，而不是 v0.0.17 版本。如果不安装周期性笔记的 beta 版，例如使用 obsidian BRAT 插件，将无法使用该功能。此外，由于它是 beta 版功能，因此在将来的规格更改等情况下可能无法使用。
- 如果遇到任何问题，请务必告知论坛或 GitHub 存储库。

### 使用方法

- 当功能被启用时，DNO 视图的顶部将显示当前显示的粒度（day/week/month/quarter/year）和日历集名称。
- 单击它们将逐个切换显示的粒度和日历集。右键单击将显示列表，可以进行选择。

![SS2](https://cdn.pkmer.cn/covers/obsidian-daily-note-outline_2_2.png!pkmer)

开始使用，请从社区插件列表中安装并启用此插件。<br>
请确保已启用 Daily Note 核心插件或 Periodic Notes 插件。<br>
如果大纲未显示，请从命令面板中执行“Daily Note Outline: Open Outline”。<br>

如何使用

当您想要更改显示的日期范围时，请单击左右箭头。

单击家的图标将返回初始设置的范围。

单击更新图标将重新绘制视图。

单击齿轮图标将打开设置。右键单击可打开快速切换上下文菜单以切换一些项目。

单击带有加号的日历图标将创建或打开今天的日记。右键单击可打开明天的日记。

单击每个大纲元素将打开该位置。

按住 Ctrl 键并在每个元素上按下，将显示悬停预览。

在使用之前，建议您首先在设置页面中为每个大纲元素（标题、链接、标签、列表项）设置显示/隐藏。

## 功能

### 简单过滤器/包含/排除过滤器

我们实现了三种过滤器功能：简单过滤器、包含和排除，以便隐藏不必要的项目并仅显示所需的项目。<br>
简单过滤器会简单地隐藏与指定的单词或短语匹配的项目，不考虑项目的层次结构。<br>
包含只能用于一种大纲元素。它将指定类型的大纲元素与下一个相同类型的元素之间的内容作为一个块处理，并仅显示与指定的单词或短语匹配的项目以及属于该块的项目。<br>
相反，排除将隐藏匹配的项目和其块。在设置中指定元素类型的“排除结束于”部分，或者启用了包含功能时，将判断块在该元素处结束，并将其隐藏。<br>
包含和排除可以同时使用。（但是，如果在包含中指定了元素类型并指定了排除关键字，那么没有意义。）<br>
简单过滤器可以与其他过滤器同时使用。例如，如果指定与包含相同的关键字，则不会显示包含的目标元素本身，而只会显示其所属的元素。

### 抽出

可以提取包含特定字符串的大纲元素。有三种方法可以实现。<br>

1. 点击放大镜按钮，输入要提取的字符串。<br>
2. 右键单击大纲元素，从上下文菜单中选择提取。只会提取包含相同名称的大纲元素。<br>
3. 点击放大镜按钮，选择提取任务。只会提取任务（包含复选框的列表项）。<br>

原本由于过滤等原因而隐藏的项目将不会显示。<br>
要取消提取，请点击×按钮（放大镜按钮将变为×按钮）。<br>

## 设置 設定

某些子项目在初始状态下不会显示，只有当父项目打开时才会显示。

### 基础知识

#### 初始搜索类型

- 选择从今天的日期开始向后显示，还是从指定日期开始向前显示指定天数。
- 向后（默认）
  - 显示过去指定天数的每日笔记，以今天为起点。通常情况下，这个选项是合适的。
- 向前
  - 以指定的起始日期为起点，显示指定天数的每日笔记。

#### 包括未来的每日笔记

当搜索类型为向后搜索时，还会显示指定天数的未来每日笔记。如果设置得很长，它还可以用作未来事件的列表！

#### 开始日期

当搜索类型为前向搜索时，以 YYYY-MM-DD 的格式指定搜索开始日期。<br>
此外，单击 UI 按钮下方的日期范围显示，也会跳转到这一天。

#### 搜索持续时间

在每一页上指定以天为单位的每日笔记搜索期限。对于经常使用日记的人来说，可以将其设置为较短的时间，而对于很少使用的人来说，可以将其设置为较长的时间。大约 7 天至 56 天左右。

显示标题/链接/标签/列表项和任务的元素是否作为大纲显示。

显示所有根列表项

显示所有任务/仅显示任务/隐藏已完成任务

这是关于任务（包含复选框的列表项）的显示设置。当打开“显示所有任务”时，无论上面的列表设置如何，都会显示所有层级的任务。当打开“仅显示任务”时，除了任务以外的列表将被隐藏。关闭“隐藏已完成任务”将隐藏已完成的任务。

#### 显示文件信息

在文件名的右侧显示信息

行数：文件的行数

距离：从基准日期开始的天数（在向后搜索中为今天，在向前搜索中为指定的日期）或周数等。

#### 插件视图的位置

在表示或更新时，指定视图显示在哪里。

左右的侧边栏是比较常见的选择。虽然也可以指定其他位置，但可能不够精细。

### 定期的なメモ

このセクションは、Periodic Notes コミュニティプラグインが有効になっていない場合に表示されません。

#### 日历设置

如果要使用 Periodic Notes 插件的日历设置，请将其打开（需要安装 Periodic Notes 的 Beta 版）。

定期的なメモを使用する場合は、オンにしてください。

#### 搜索周期性笔记的持续时间

指定每页的搜索持续时间，针对每个周期性笔记。

#### 将日期范围附加到每周笔记

当显示每周笔记时，在文件名旁边显示相应的日期范围。

### 标题

#### 要显示的标题级别

指定是否将各级标题作为大纲显示。

### 预览

#### 内联预览

在大纲元素的右侧，模糊显示接下来的几个单词。

#### 工具提示预览

将鼠标光标悬停在大纲元素上时，将显示后续文本作为工具提示。

#### 工具提示预览方向

指定工具提示预览的方向（我本来想自动分配的，但是不知道怎么做...）

### 简单过滤器

#### 忽略的标题/链接/标签/列表项

包含指定单词或短语的大纲元素将被隐藏。请使用换行符分隔每个元素。

### 包括

#### 包含的元素类型

指定的大纲元素类型将成为包含过滤器的目标。

指定した単語やフレーズが含まれるアウトライン要素と、それに続くブロックのみが表示対象となります。それぞれ改行で区切って下さい。

#### 包括开始部分

在笔记的开头部分，指定是否显示包含在 Element type for include 中指定的类型的大纲元素之前的部分。

### 排除

排除在这里

如果在此项目中指定了任何一个大纲元素类型，则通过排除过滤器指定的元素将在指定的元素处终止。

如果在包含过滤器中指定了任何一个类型，则排除将在该类型处终止，并且将忽略此项目。

#### 見出し/リンク/タグ/リスト項目を除外する

指定された単語やフレーズが含まれるアウトライン要素と、それに続く領域（同種のアウトライン要素、または Exclusion end at で指定された要素が出現する前までの領域）は非表示になります。

それぞれ改行で区切ってください。

### 外观

设置显示每个大纲元素的外观。

可以为每个元素添加图标和前缀字符串。

如果选择自定义图标，请输入 Lucide（<https://lucide.dev/）的图标名称。似乎无法显示某些图标。>

#### 除标题外的缩进

当设置后，除标题外的大纲元素将缩进与前一个标题相同的程度（或更多一级）。

标题：重复标题前缀

如果输入标题的前缀，启用此选项后，标题的级别数将重复前缀。

#### 标题：添加缩进

任务：在前缀中添加复选框状态的文本。

### 其他

#### 仅显示.md 文件/完全匹配的文件

如果您正在使用 Periodic Notes 插件的 Beta 版，更广泛的文件名将被识别为周期性笔记。这些选项将隐藏除 md 文件以外的任何不符合格式的文件。

### 调试

#### 显示调试信息

当打开时，将在控制台上显示一些用于调试的信息。

## 致谢

在创建此插件时，我参考了许多优秀的 Obsidian 插件。特别感谢以下插件的作者：<br>

- 使用了 @liamcain 的 daily note interface 插件来处理每日笔记的功能。<br>
- 在创建自定义视图时，我大量参考了 st3v3nmw 的 Spaced Repetition 插件和 tgrosinger 的 Recent files 插件。<br>
- 关于创建周期性笔记的新功能，我部分修改了 [Periodic Notes by @liamcain](https://github.com/liamcain/obsidian-periodic-notes) （MIT 许可证）的代码来使用。<br>
此外，我还参考了 Discord 的 plugin-dev 频道中的许多帖子。

## 请我喝杯咖啡

如果你喜欢这个插件，我会很高兴如果你能请我喝杯咖啡！<br>
[!["请我喝杯咖啡"](https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png)](https://www.buymeacoffee.com/iiz00)
