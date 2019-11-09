---
title: "主题功能及Markdown特性测试"
date: 2019-11-08T23:41:48+08:00
lastmod: 2019-11-08T23:41:48+08:00
draft: false
keywords: []
description: ""
tags: [Markdown]
categories: [杂文]
author: ""

# You can also close(false) or open(true) something for this content.
# P.S. comment can only be closed
comment: false
toc: false
autoCollapseToc: false
# You can also define another contentCopyright. e.g. contentCopyright: "This is another copyright."
contentCopyright: false
reward: false
mathjax: true
---


标题
------------------------------------------------------

# H1

## H2

### H3

#### H4

##### H5

###### H6


段落
------------------------------------------------------

使用星号`*`或者单下划线`_`标记*斜体强调*或者_斜体强调_

使用两个星号`**`或者两个下划线`__`标记**加粗强调**或者__加粗强调__

星号和下划线可以叠加使用->**只是加粗 _斜体并加粗_**

使用两个波浪线`~~`标记~~已删除文字~~

插入文字暂无`Markdown`标记，直接使用`HTML`标签`<ins>`标记 <ins>插入文字</ins>

行内代码使用反引号标记->`print("hello world")`

上标X<sup>2</sup> / 下标X<sub>2</sub>

用Latex生成的上标$X^2$ / 下标$X_2$

按键<kbd>Ctrl</kbd>

参考资料<sup>[[1]](#ref01)</sup><sup>[[2]](#ref02)</sup>


链接
------------------------------------------------------

外链[Google](https://www.google.com)

注脚[^1]


列表
------------------------------------------------------
以下的无序、有序和任务列表均支持二级嵌套，不建议使用二级以上的嵌套。


### 无序列表

- 无序列表
    * 嵌套的无序列表
    * 嵌套的无序列表
* 无序列表
    + 嵌套的无序列表
    + 嵌套的无序列表


### 有序列表

1. 有序列表
    1. 嵌套的有序列表
    2. 嵌套的有序列表
2. 有序列表
    - 嵌套的无序列表
    - 嵌套的无序列表
3. 有序列表


### 任务列表

[语法参考](https://github.blog/2013-01-09-task-lists-in-gfm-issues-pulls-comments/)

- [ ] Cmd Markdown 开发
    - [ ] 改进Cmd渲染算法
    - [ ] 支持以PDF导出文稿
    - [x] 新增Todo列表功能
- [ ] 七月旅行准备
    - [ ] 准备需要携带的物品
    - [x] 准备船票


引用
------------------------------------------------------

> 野火烧不尽，春风吹又生。
>
> —— 白居易《赋得古草原送别》


代码
------------------------------------------------------

以一段`python`代码演示

```python
def Hello():
    print("Hello, World!")
```

以一段`JavaScript`代码做演示。

```javascript
// Initialize video.js player
if (document.getElementById('my-player') !== null) {
  /* eslint-disable no-undef */
  videojs('#my-player', {
    aspectRatio: '16:9',
    fluid: true,
  });
}
```


分割线
-----------------------------------------------------

---

中间能写字的分割线，如果修改了分割线的中字内容，需要配合修改`css`的样式


图片
-----------------------------------------------------

![even主题预览](https://raw.githubusercontent.com/olOwOlo/hugo-theme-even/master/images/showcase.png)


表格
-----------------------------------------------------

使用`Markdown`画的表格，如下表:

|   TAbles   | Are| Cool     |
| ---- | ---- | ---- |
|  col 3 is|  right-aligned    |  $1600    |
|  col 2 is|  centered    |  $1231    |
|  zebra stripes| are neat     |  $923    |


Latex公式
------------------------------------------------------

主题使用[MathJax](https://www.mathjax.org/)开源库来实现对数学公式的支持，使用`$$`标记
$$
E = mc^2
$$

但是并不支持行内公式$E = mc^2$


Shortcodes
-----------------------------------------------------

### 网易云音乐

主题文章中可以轻松插入[网易云音乐](https://music.163.com/)的指定音乐，你可以根据需要将音乐设置为自动播放，在主题目录`layouts/shortcodes`文件夹下的`music.html`对该标签进行定义。

{{% music "29719651" %}}


### YouTube

由于不明原因可能无法播放

{{% youtube "s6krMrTeRKs" %}}


### blockquote

Normal quote:
{{< blockquote >}}
  This is a sample quote.
{{< /blockquote >}}

Quote with author:
{{< blockquote author="鲁迅" >}}
  这话我没说过。
{{< /blockquote >}}

Quote with author and source:
{{< blockquote author="鲁迅" source="秋夜" >}}
  我家门前有两棵树，一个是枣树，另一棵也是枣树。
{{< /blockquote >}}

Quote with author and link:
{{< blockquote author="鲁迅" link="https://www.zhihu.com/question/28948637" >}}
  这话还真是我说的。
{{< /blockquote >}}

Quote with author, link and title:
{{< blockquote author="鲁迅" title="啥都是我说的" link="https://www.zhihu.com/question/28948637" >}}
  别找了，算我说过行不。
{{< /blockquote >}}

Quote with author and a link longer than 32 characters, string is first cut at 32 characters then everything after the last forward slash is removed
{{< blockquote author="鲁迅" link="https://www.fabiaoqing.com/search/search/keyword/%E9%B2%81%E8%BF%85%20%E8%BF%99%E5%8F%A5%E8%AF%9D%E6%98%AF%E6%88%91%E8%AF%B4%E7%9A%84" >}}
  什么都是我说的，你们整天烦不烦。
{{< /blockquote >}}

Test from the Octopress blockquote page at: http://octopress.org/docs/plugins/blockquote/
{{< blockquote author="@allanbranch" link="https://twitter.com/allanbranch/status/90766146063712256" >}}
  Over the past 24 hours I've been reflecting on my life & I've realized only one thing. I need a medieval battle axe.
{{< /blockquote >}}


### Wikipedia Link Generator

- {{< wp tag="鲁迅" >}}
- {{< wp tag="鲁迅" lang="fr" >}}
- {{< wp tag="鲁迅" lang="fr" title="">}}
- {{< wp tag="鲁迅" title="鲁 迅" >}}
- {{< wp tag="鲁迅" lange="en" title="鲁 迅">}}


### Image Caption

{{< imgcap title="Simple Caption" src="https://raw.githubusercontent.com/olOwOlo/hugo-theme-even/master/images/showcase.png" >}}


### Youku Video

{{< youku "id_XMjA0MDAwNjU5Mg==" >}}


参考资料
------------------------------------------------------

1. <a id="ref01">[Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)</a>
2. <a id="ref02">[Markdown 语法手册](https://www.zybuluo.com/EncyKe/note/120103)</a>


[^1]: 这是一个注脚
