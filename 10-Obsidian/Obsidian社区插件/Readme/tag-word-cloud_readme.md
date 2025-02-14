---
uid: 2023120719440688
title: Obsidian 插件：【Readme】Tag, Word & Link Cloud
tags: ['obsidian插件', 'readme']
description: 展示你的标签/词/链接的云图
author: AI
type: readme
draft: false
editable: false
modified: 20230101000000
---

# Obsidian 插件：【Readme】Tag, Word & Link Cloud

> [!Note] 插件名片
> - 插件名称：Tag, Word & Link Cloud
> - 插件作者：Johannes Theiner
> - 插件说明：展示你的标签/词/链接的云图
> - 插件分类：['obsidian 插件 ', 'readme']
> - 项目地址：[点我访问](https://github.com/joethei/obsidian-tagcloud)
> - 国内下载地址：[下载安装](https://pkmer.cn/products/plugin/pluginMarket/?tag-word-cloud)

## 概述

展示你的标签/词/链接的云图

![Tag, Word & Link Cloud](https://cdn.pkmer.cn/covers/tag-word-cloud.png!pkmer)

> [!tip] 原文出处
>
>下面自述文件的来源于 [Readme](https://ghproxy.net/https://raw.githubusercontent.com/joethei/obsidian-tagcloud/master/README.md)
>

---

## Readme(翻译）

下面是 [[tag-word-cloud]] 插件的自述翻译

## 标签、词语和链接云

[Obsidian](https://obsidian.md) 插件

![GitHub package.json version](https://img.shields.io/github/package-json/v/joethei/obsidian-tagcloud)
![GitHub manifest.json dynamic (path)](https://img.shields.io/github/manifest-json/minAppVersion/joethei/obsidian-tagcloud?label=lowest%20supported%20app%20version)
![GitHub](https://img.shields.io/github/license/joethei/obsidian-tagcloud)
[![libera manifesto](https://img.shields.io/badge/libera-manifesto-lightgrey.svg)](https://liberamanifesto.com)
---

使用此插件，您可以在笔记中创建标签、链接或词语云。

要实现这一点，请创建一个语言设置为 `tagcloud`、`wordcloud` 或 `linkcloud` 的 [代码块](https://help.obsidian.md/How+to/Format+your+notes#Code+blocks)。

您可以使用 [YAML](https://learnxinyminutes.com/docs/yaml/) 语法来配置您的云。

## 标签云

![](https://cdn.pkmer.cn/covers/tag-word-cloud_1_4.png!pkmer)

显示符合您选择的所有标签。

### 示例

#### 显示整个保险库中的所有标签

~~~markdown
```tagcloud
```

#### 显示当前文件中的所有标签

~~~markdown
```tagcloud
source: file
```
~~~

#### 显示文件夹/文件的所有标签

> ⚠️ 需要 Dataview

~~~markdown
```tagcloud
source: query
query: Folder/File
```
~~~

#### 显示与我们的标签一起出现的所有标签

> ⚠️ 需要 Dataview

~~~markdown
```tagcloud
source: query
query: '#yourTag'
```
~~~

#### 显示所有链接到笔记的标签

> ⚠️ 需要 Dataview

~~~markdown
```tagcloud
source: query
query: '[[其他笔记]]'
```
~~~

### 选项

| **名称** | **描述**                                                                                                 | **可能的值**                                                                                   |
|----------|---------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| query    | 需要 [Dataview](https://github.com/blacksmithgu/obsidian-dataview)，需要将 `source` 设置为 `query` | 有效的 [Dataview Source](https://blacksmithgu.github.io/obsidian-dataview/query/sources/) |

所有其他选项仍然适用于 [这里](#general-options)。

## 词云

![](https://cdn.pkmer.cn/covers/tag-word-cloud_1_5.png!pkmer)

词云显示了您的保险库/笔记中的所有单词。

> ⚠ 仅在加载保险库和运行“重新计算词分布”命令时才会计算词分布。
>
> 这是因为计算过程需要大量的计算资源和时间。[^performance]

### 示例

#### 显示整个保险库中的所有单词

~~~markdown
```词云
```

#### 显示当前文件中的所有单词

~~~markdown
```wordcloud
source: file
```
~~~

### 选项

| **名称**   | **描述**                                                                                                 | **可能的值** | **默认值** |
|-----------|-----------------------------------------------------------------------------------------------------------------|---------------------|-------------|
| stopwords | 从结果中删除所有 [停用词](https://www.opinosis-analytics.com/knowledge-base/stop-words-explained/) | `true`/ `false`     | `true`      |

其他所有选项仍然适用于 [这里](#general-options)

## 链接云

![](https://cdn.pkmer.cn/covers/tag-word-cloud_1_6.png!pkmer)

链接云显示了您的存储库中的所有链接。

此云只能在整个存储库范围内生成。

### 示例

#### 显示所有链接

~~~markdown
```linkcloud
```

#### 显示所有链接到现有文件的链接

~~~markdown
```linkcloud
type: resolved
```

#### 显示所有指向不存在文件的链接

~~~markdown
```linkcloud
type: unresolved
```

### 选项

| **名称** | **描述**             | **可能的值**              | **默认值** |
|----------|-----------------------------|----------------------------------|-------------|
| type     | 要显示的链接类型 | `resolved`, `unresolved`, `both` | `resolved`  |

以下选项也适用。

## 通用选项
以下选项适用于所有云。

| **名称**    | **描述**                                                                                                  | **可能的值**                                                                                                         | **默认值**                            |
|-------------|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| shape       | 绘制的形状                                                                                               | `circle`, `cardioid`, `diamond`, `square`, `triangle-forward`, `triangle`, `pentagon`, `star`                               | `circle`                               |
| source      | 标签/单词来自哪里？                                                                            | `file`, `vault`, `query`(仅在标签云中支持)                                                                        | `vault`                                |
| weight      | 单词大小的乘数因子                                                                  | 任何正整数                                                                                                        | `2`                                    |
| shrinkToFit | 调整单词权重以适应                                                                                   | `true`/`false`                                                                                                              | `true`                                 |
| minCount    | 最小出现次数                                                                                     | 任何正整数                                                                                                        | `0`                                    |
| maxDepth    | 仅显示X个最常用的元素（如果两个元素具有相同的出现次数，则只计算一个） | 任何正整数（增加此数字可能导致云不显示，因为只能渲染这么多元素） | `25`                                   |
| background  | 背景颜色                                                                                                 | 十六进制RGB值                                                                                                     | 选择的主题的背景颜色 |
| width       | 画布宽度                                                                                                  | 以像素为单位（省略了`px`）                                                                                             | 线宽                             |
| height      | 画布高度                                                                                                 | 以像素为单位（省略了`px`）                                                                                             | `width / 2`                            |
| fontFamily  | 用于显示的字体                                                                                             | 任何有效的[font-family](https://developer.mozilla.org/docs/Web/CSS/font-family)                                             |                                        |
| fontWeight  | 字体粗细                                                                                                      | `normal`, `bold`, 或数字                                                                                               | `normal`                               |
| minFontSize | 最小字体大小                                                                                                | 任何数字                                                                                                                  | `0`                                    |
| minRotation | 文本应旋转的最小角度                                                                      | 数字（以弧度为单位）                                                                                                             | `- pi / 2`                             |
| maxRotation | 文本应旋转的最大角度                                                                      | 数字（以弧度为单位）                                                                                                             | `pi / 2`                               |
| ellipticity | '扁平度'程度                                                                                             | 数字                                                                                                                      | `0.65`                                 |
| shuffle     | 每次生成不同的结果？                                                                    | `true`/`false`                                                                                                              | `true`                                 |
| rotateRatio | 旋转概率                                                                                             | 数字作为百分比（因此1.0为100%）                                                                                       | `0.1`                                  |

## 已知问题

- 在某些特定情况下，使用的`canvas`元素的计算宽度为0。
	插件将回退到500的值，这取决于您的Obsidian窗口的大小，可能会看起来很奇怪。

# 鸣谢

- 使用[wordcloud2.js](https://github.com/timdream/wordcloud2.js)构建
- 以及[stopword](https://github.com/fergiemcdowall/stopword)
- 还有[Dataview](https://github.com/blacksmithgu/obsidian-dataview) API
- 在[Tag Wrangler](https://github.com/pjeby/tag-wrangler)的代码帮助下
- 一些代码来自于[Word Count Dashboard for Dataview](https://gist.github.com/chrisgrieser/ac16a80cdd9e8e0e84606cc24e35ad99)


[^performance]: 在一台高性能计算机上，包含约12,000个文件的Vault需要15分钟。



