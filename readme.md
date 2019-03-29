# thlorenz/doctoc [![translate-svg]][translate-list]

<!-- [![explain]][source] -->

[explain]: http://llever.com/explain.svg
[source]: https://github.com/chinanf-boy/Source-Explain
[translate-svg]: http://llever.com/translate.svg
[translate-list]: https://github.com/chinanf-boy/chinese-translate-list

「 生成，markdown 文件(`*.md`)的超链接目录 」

[中文](./readme.md) | [english](https://github.com/thlorenz/doctoc)

---

## 校对 ✅

<!-- doc-templite START generated -->
<!-- repo = 'thlorenz/doctoc' -->
<!-- commit = '164f78e6452413a9717f58df8cf9dcb200b6c0f7' -->
<!-- time = '2018-11-21' -->
翻译的原文 | 与日期 | 最新更新 | 更多
---|---|---|---
[commit] | ⏰ 2018-11-21 | ![last] | [中文翻译][translate-list]

[last]: https://img.shields.io/github/last-commit/thlorenz/doctoc.svg
[commit]: https://github.com/thlorenz/doctoc/tree/164f78e6452413a9717f58df8cf9dcb200b6c0f7

<!-- doc-templite END generated -->

### 贡献

欢迎 👏 勘误/校对/更新贡献 😊 [具体贡献请看](https://github.com/chinanf-boy/chinese-translate-list#贡献)

## 生活

[If help, **buy** me coffee —— 营养跟不上了，给我来瓶营养快线吧! 💰](https://github.com/chinanf-boy/live-need-money)

---

# DocToc [![build status](https://secure.travis-ci.org/thlorenz/doctoc.svg)](http://travis-ci.org/thlorenz/doctoc)

<a href="https://www.patreon.com/bePatron?u=8663953"><img alt="become a patron" src="https://c5.patreon.com/external/logo/become_a_patron_button.png" height="35px"></a>

生成，markdown 文件(`*.md`)的超链接目录

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->

**Contents**

- [安装](#%E5%AE%89%E8%A3%85)
- [用法](#%E7%94%A8%E6%B3%95)
  - [将 TOC 添加到目录和子目录中的所有文件](#%E5%B0%86-toc-%E6%B7%BB%E5%8A%A0%E5%88%B0%E7%9B%AE%E5%BD%95%E5%92%8C%E5%AD%90%E7%9B%AE%E5%BD%95%E4%B8%AD%E7%9A%84%E6%89%80%E6%9C%89%E6%96%87%E4%BB%B6)
  - [毫不费力地更新现有的 Doctoc TOCs](#%E6%AF%AB%E4%B8%8D%E8%B4%B9%E5%8A%9B%E5%9C%B0%E6%9B%B4%E6%96%B0%E7%8E%B0%E6%9C%89%E7%9A%84-doctoc-tocs)
  - [将 TOC 添加到单个文件中](#%E5%B0%86-toc-%E6%B7%BB%E5%8A%A0%E5%88%B0%E5%8D%95%E4%B8%AA%E6%96%87%E4%BB%B6%E4%B8%AD)
  - [使用 Doctoc 生成与其他站点兼容的超链接](#%E4%BD%BF%E7%94%A8-doctoc-%E7%94%9F%E6%88%90%E4%B8%8E%E5%85%B6%E4%BB%96%E7%AB%99%E7%82%B9%E5%85%BC%E5%AE%B9%E7%9A%84%E8%B6%85%E9%93%BE%E6%8E%A5)
  - [指定 TOC 的位置](#%E6%8C%87%E5%AE%9A-toc-%E7%9A%84%E4%BD%8D%E7%BD%AE)
  - [指定自定义 TOC 标题](#%E6%8C%87%E5%AE%9A%E8%87%AA%E5%AE%9A%E4%B9%89-toc-%E6%A0%87%E9%A2%98)
  - [指定 TOC 条目的最大 heading 级别](#%E6%8C%87%E5%AE%9A-toc-%E6%9D%A1%E7%9B%AE%E7%9A%84%E6%9C%80%E5%A4%A7-heading-%E7%BA%A7%E5%88%AB)
  - [打印到标准输出](#%E6%89%93%E5%8D%B0%E5%88%B0%E6%A0%87%E5%87%86%E8%BE%93%E5%87%BA)
  - [作为一个`git`钩子来使用](#%E4%BD%9C%E4%B8%BA%E4%B8%80%E4%B8%AAgit%E9%92%A9%E5%AD%90%E6%9D%A5%E4%BD%BF%E7%94%A8)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

## 安装

```
npm install -g doctoc
```

## 用法

在最简单的用法中，一个或多个文件，或文件夹使用`doctoc`命令。这会更新每个指定(md)文件的 TOC(超链接目录)。下面是一些例子.

### 将 TOC 添加到目录和子目录中的所有文件

进入目录:

```
doctoc .
```

这将用 md 解析器，生成标点(`#`)超链接的目录表，更新当前目录及其所有子目录中的所有 md 文件。Doctoc 默认使用 Github 解析器,但可以[可以指定其他模式](#using-doctoc-to-generate-links-compatible-with-other-sites).

### 毫不费力地更新现有的 Doctoc TOCs

如果您已经通过 doctoc 插入了 TOC 注释，那么它将通过运行命令(而不是插入重复的 toc)自动更新。Doctoc 通过

- `<!-- START doctoc -->`和
- `<!-- END doctoc -->`注释

定位 TOC，因此您还可以将生成的 TOC 移动到文档的任何其他部分。

### 将 TOC 添加到单个文件中

如果希望只转换特定的文件,请执行:

```
doctoc /path/to/file [...]
```

#### 实例

```
doctoc README.md

doctoc CONTRIBUTING.md LICENSE.md
```

你可以使用这个特性来做更复杂的事情.例如,如果你安装[ack][ack],您可以添加`<!-- Doctoc SKIP -->`到特定文件， 然后使用

```
ack -L 'Doctoc SKIP' | xargs doctoc
```

这命令只会重新编译那些没有`<!-- Doctoc SKIP -->`的文件.

### 使用 Doctoc 生成与其他站点兼容的超链接

为了添加，兼容的超链接目录表,可添加其他站点的适当参数:

可用模式是:

```
--bitbucket bitbucket.org
--nodejs    nodejs.org
--github    github.com
--gitlab    gitlab.com
--ghost     ghost.org
```

#### 例子

```
doctoc README.md --bitbucket
```

### 指定 TOC 的位置

默认情况下,Doctoc 将 TOC 置于文件的顶部。可用以下格式放置在别处:

```
<!-- START doctoc -->
<!-- END doctoc -->
```

将此代码直接放在 `.md`文件中.例如:

```
// my_new_post.md
Here we are, introducing the post. It's going to be great!
But first: a TOC for easy reference.

<!-- START doctoc -->
<!-- END doctoc -->

# Section One

Here we'll discuss...
```

运行 Doctoc 将在注释之间的位置插入 TOC.

### 指定自定义 TOC 标题

使用`--title`选项指定一个(markdown 格式的)自定义 TOC 标题;`doctoc --title '**Contents**' .` 。从此,你可以简单`doctoc <file>`，就让 Doctoc 保留您指定的标题。(正如这个 readme 文件)

或者,你通过使用`--notitle`选项，用换行符将标题省略。简单地从 TOC 中删除标题.

### 指定 TOC 条目的最大 heading 级别

> 如 `#` == **1**, `##` == **2** ...

使用`--maxlevel`将 TOC 项 限制为指定级别;

- `doctoc --maxlevel 3 .` (比如该 readme 的`#### 实例`并没有超链接)
  
默认情况下,

- 没有限制标题,
- 而来自嵌入式 HTML 的标题(heading)限于 第 4 级.

### 打印到标准输出

您可以使用`-s`或`--stdout`选项。

[ack]: http://beyondgrep.com/

### 作为一个`git`钩子来使用

把 Doctoc 作为一个[pre-commit](http://pre-commit.com)钩子来使用，以下配置:

```yaml
repos:
  - repo: https://github.com/thlorenz/doctoc
    sha: ... # substitute a tagged version
    hooks:
      - id: doctoc
```

这将在 git commit 文件时，运行`doctoc`,确保 TOC 保持最新.
