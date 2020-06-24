<h1>Markdown语法</h1>

[TOC]

## 标题

使用 `#` 设置标题。
支持 1-6 级标题，直接使用对应数量的 `#` 即可。

对于第一级和第二级标题，还可以通过 `===` 和 `---` 的方式来实现。

示例：

``` markdown
# 一级标题

一级标题
===

二级标题
---

## 二级标题

...

###### 六级标题
```

效果：

> # 一级标题
>
> 一级标题
> ===
>
> ## 二级标题
>
> 二级标题
> ---
>
> ### 三级标题
>
> #### 四级标题
>
> ##### 五级标题
>
> ###### 六级标题

### 目录

使用 `[TOC]`，markdown会根据标题生成目录，并根据目录级别，自动划分层级。

示例：

``` markdown
[TOC]
```

效果：

[TOC]

<div style="background-color: rgba(255,229,100,.3);border-color: #e7c000;color: #6b5900;padding: .1rem 1.5rem;border-left-width: .5rem;border-left-style: solid;margin: 1rem 0;"><p style="line-height: 1.7;font-weight: 600;margin-bottom: -.4rem;display: block;margin-block-start: 1em;margin-block-end: 1em;margin-inline-start: 0px;margin-inline-end: 0px;color: #b29400;">注意</p><p style="line-height: 1.7;display: block;margin-block-start: 1em;margin-block-end: 1em;margin-inline-start: 0px;margin-inline-end: 0px;color: #6b5900;">有些编辑器或网站是区分大小写的，所以尽量使用大写格式来生成目录。</p></div>

## 字体

### 加粗

使用 `**` 将需要加粗的文字包裹起来即可。

示例：

``` markdown
这段文字，**这里**需要加粗
```

效果：

> 这段文字，**这里**需要加粗

### 斜体

使用 `*` 将需要斜体的文字包裹起来即可。

示例：

``` markdown
这段文字，*这里*需要斜体
```

效果：

> 这段文字，*这里*需要斜体

<div style="background-color: #f3f5f7;border-color: #42b983;padding: .1rem 1.5rem;border-left-width: .5rem;border-left-style: solid;margin: 1rem 0;"><p style="line-height: 1.7;font-weight: 600;margin-bottom: -.4rem;display: block;margin-block-start: 1em;margin-block-end: 1em;margin-inline-start: 0px;margin-inline-end: 0px;">提示</p><p style="line-height: 1.7;display: block;margin-block-start: 1em;margin-block-end: 1em;margin-inline-start: 0px;margin-inline-end: 0px;">如果需要加粗的斜体，可以通过 *** 实现。</p></div>

### 删除线

使用 `~~` 将需要显示删除线的文字包裹起来即可。

示例：

``` markdown
这段文字，~~这里~~需要删除线
```

效果：

> 这段文字，~~这里~~需要删除线

## 链接

### 文字链接

使用 `[描述](地址)` 的方式可以增加链接。

示例：

``` markdown
[这是一个链接](https://www.jeremyjone.com)
```

效果：

> [这是一个链接](https://www.jeremyjone.com)

#### 内链接

有时候，文件内需要跳转到指定目录位置，也可以使用链接进行跳转。

链接部分使用 `#` + 目录名 来实现跳转，不论几级目录，都这样写。所以，目录中的名称不应该有重复，这样会引起不必要的奇异。

示例：

``` markdown
跳转到 [目录](#目录)
```

效果：

跳转到 [目录](#目录)

### 图片链接

使用 `![alt](图片地址)` 的方式可以关联并展示一张图片，这适用于本地和远程。

示例：

``` markdown
![示例图片](https://desktop.jeremyjone.com/test/images/01.jpg)
```

效果：

> ![示例图片](https://desktop.jeremyjone.com/test/images/01.jpg)

## 分割线

使用 `***` 或者 `---` 可以实现分割线。

示例：

``` markdown
***

---
```

效果：

> &nbsp;
>
> ---
>
> ***
>
> &nbsp;

## 注脚

注脚通常用于解释某些内容，类似书本中的注释、详解。

使用 `[^keyword]` 的方式添加注脚名，然后在文本的任意位置（通常在最下方）添加注脚内容。当然，注脚的内容永远显示在最下方。

示例：

``` markdown
这是一段Markdown[^1]文本，它可以直接转为HTML[^2]，可以使用插件[^script]实现更丰富的功能。

[^1]: Markdown是一种文本标记语言。
[^2]: HTML是一种超文本标记语言。
[^script]: 用于markdown的插件。
```

效果：

这是一段Markdown[^1]文本，它可以直接转为HTML[^2]，可以使用插件[^script]实现更丰富的功能。

[^1]: Markdown是一种文本标记语言。
[^2]: HTML是一种超文本标记语言。
[^script]: 用于markdown的插件。

## 引用

使用 `>` 实现引用，多个 `>` 可以实现多级引用。

示例：

``` markdown
> 一级引用
>> 二级引用
>>> 三级引用
...
>>>>>>>>>>>>>>>>>>>> n级引用
```

效果：

> 一级引用
>> 二级引用
>>> 三级引用
>>>>>>>>>>>>>>>>>>>> n级引用

## 代码

代码内容是程序员必备，同时也可以突出一些重点内容。

### 行内代码块

通过 `` ` `` 可以将你希望的代码内容或者重点内容包裹起来，像这样：

示例：

``` markdown
这是一篇 `markdown` 文档。
```

效果：

> 这是一篇 `markdown` 文档。

#### 特殊字符的处理方式

如果你希望的内容中如果包含 `` ` ``，这就比较棘手了，不过这对于markdown很简单。使用 ` `` ` 来包裹包含 `` ` ``的内容即可。同样的，你也可以使用 `` ` `` 来包裹具有 ` `` `的内容。看上去它更像是一段绕口令，如果你对`python`熟悉，那么这样的方式应该并不陌生，它和`python`字符串的使用方式类似。

示例：

``` markdown
如何使用 `markdown` 将 `` ` `` 包裹到行内块？这个问题很简单，使用 ` `` `的方式即可。
```

效果：

> 如何使用 `markdown` 将 `` ` `` 包裹到行内块？这个问题很简单，使用 ` `` `的方式即可。

<div style="background-color: #f3f5f7;border-color: #42b983;padding: .1rem 1.5rem;border-left-width: .5rem;border-left-style: solid;margin: 1rem 0;"><p style="line-height: 1.7;font-weight: 600;margin-bottom: -.4rem;display: block;margin-block-start: 1em;margin-block-end: 1em;margin-inline-start: 0px;margin-inline-end: 0px;">提示</p><p style="line-height: 1.7;display: block;margin-block-start: 1em;margin-block-end: 1em;margin-inline-start: 0px;margin-inline-end: 0px;">`` 和 ` 本身的功能是一样的，它们都可以包裹任意内容，区别是它们可以包含对方。</p></div>

### 代码块

这是一个比较单独的区域，通过 ` ``` `可以定义一个单独的代码区域。同时，在 ` ``` ` 后面跟上语言名称，可以根据对应的代码规则，高亮代码内容。

示例：

``` markdown
 ``` js
     function() {
         /* content */
     }
 ``` // 结束代码块
```

效果：

``` js
function() {
   /* content */
}
```

<div style="background-color: #f3f5f7;border-color: #42b983;padding: .1rem 1.5rem;border-left-width: .5rem;border-left-style: solid;margin: 1rem 0;"><p style="line-height: 1.7;font-weight: 600;margin-bottom: -.4rem;display: block;margin-block-start: 1em;margin-block-end: 1em;margin-inline-start: 0px;margin-inline-end: 0px;">提示</p><p style="line-height: 1.7;display: block;margin-block-start: 1em;margin-block-end: 1em;margin-inline-start: 0px;margin-inline-end: 0px;">markdown支持的语言是通过不同插件实现的，不同编辑器、网站，支持的都不尽相同，可以查看 Prism 完整的语言列表：<a href="https://prismjs.com/#supported-languages" target="_blank">语言列表</a></p></div>


## 列表

列表分为有序和无序，它们的功能是一样的，同时它们也可以混用，这很方便。

### 无序列表

使用 `-` `+` `*` 的任意一种方式都可以实现无序列表，并且支持多级内容，每一级使用至少2个空格缩进。

示例：

``` markdown
- 内容1
+ 内容2
* 内容3
  - 子内容1
  + 子内容2
  * 子内容3
    - 子内容
```

效果：

> - 内容1
> + 内容2
> * 内容3
>   - 子内容1
>   + 子内容2
>   * 子内容3
>     - 子内容

### 有序列表

有序列表需要使用数字 `1.`(数字 + `.`) 的方式来显式的声明。多级内容使用至少3个空格缩进。

示例：

``` markdown
1. 内容1
2. 内容2
3. 内容3
   1. 子内容1
   2. 子内容2
   3. 子内容3
```

效果：

1. 内容1
2. 内容2
3. 内容3
   1. 子内容1
   2. 子内容2
   3. 子内容3

<div style="background-color: #f3f5f7;border-color: #42b983;padding: .1rem 1.5rem;border-left-width: .5rem;border-left-style: solid;margin: 1rem 0;"><p style="line-height: 1.7;font-weight: 600;margin-bottom: -.4rem;display: block;margin-block-start: 1em;margin-block-end: 1em;margin-inline-start: 0px;margin-inline-end: 0px;"><svg t="1592964301338" class="icon" viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg" p-id="2368" data-darkreader-inline-fill="" width="20" height="20"><path d="M612.352 907.776H410.112c-10.752 0-20.48 8.704-20.48 20.48 0 11.264 8.704 20.48 20.48 20.48h202.24c10.752 0 20.48-8.704 20.48-20.48-0.512-11.776-9.216-20.48-20.48-20.48z m-30.72 60.416H440.32c-10.752 0-20.48 8.704-20.48 20.48 0 11.264 8.704 20.48 20.48 20.48h141.824c10.752 0 20.48-8.704 20.48-20.48-0.512-11.776-9.728-20.48-20.992-20.48zM146.944 452.096H66.048c-10.752 0-20.48 8.704-20.48 20.48 0 11.264 8.704 20.48 20.48 20.48h80.896c10.752 0 20.48-8.704 20.48-20.48-0.512-11.264-9.216-20.48-20.48-20.48z m808.96 0h-80.896c-10.752 0-20.48 8.704-20.48 20.48 0 11.264 8.704 20.48 20.48 20.48h80.896c10.752 0 20.48-8.704 20.48-20.48 0-11.264-9.216-20.48-20.48-20.48zM221.696 731.648l-39.424 39.424c-7.68 7.68-7.68 21.504 0 29.184s21.504 7.68 29.184 0l39.424-39.424c7.68-7.68 7.68-21.504 0-29.184-7.168-8.192-19.968-8.192-29.184 0zM809.472 144.896l-39.424 39.424c-7.68 7.68-7.68 21.504 0 29.184s21.504 7.68 29.184 0l39.424-39.424c7.68-7.68 7.68-21.504 0-29.184-8.192-7.68-21.504-7.68-29.184 0zM222.72 214.016c7.68 7.68 21.504 7.68 29.184 0s7.68-21.504 0-29.184l-39.424-39.424c-7.68-7.68-21.504-7.68-29.184 0s-7.68 21.504 0 29.184l39.424 39.424z m576.512 517.632c-7.68-7.68-21.504-7.68-29.184 0s-7.68 21.504 0 29.184l39.424 39.424c7.68 7.68 21.504 7.68 29.184 0s7.68-21.504 0-29.184l-39.424-39.424zM510.976 139.264c10.752 0 20.48-8.704 20.48-20.48V37.888c0-10.752-8.704-20.48-20.48-20.48-11.264 0-20.48 8.704-20.48 20.48v80.896c0 10.752 9.728 20.48 20.48 20.48z m0 39.936C343.04 179.2 207.872 314.368 207.872 482.816c0 108.032 56.32 203.264 141.824 256.512v107.008c0 22.528 18.432 40.448 40.448 40.448h242.688c22.528 0 40.448-18.432 40.448-40.448v-106.496c84.992-53.76 141.824-148.48 141.824-256.512C814.08 314.88 678.912 179.2 510.976 179.2z m140.8 526.336c-11.776 7.168-19.456 20.48-19.456 34.304v107.008h-100.864v-175.104l96.256-95.232c7.168-7.168 7.168-19.456 0-27.136-7.168-7.168-20.48-7.168-27.136 0l-89.088 88.064-89.088-88.064c-7.168-7.168-20.48-7.168-27.136 0-7.168 7.168-7.168 19.456 0 27.136L491.52 671.744v175.104H389.632v-107.008c0-14.336-7.168-26.112-19.456-34.304-76.8-48.64-122.368-131.072-122.368-222.72C247.808 338.432 366.08 220.16 510.976 220.16c144.896 0 263.168 118.272 263.168 263.168 0 90.624-45.568 173.568-122.368 222.208z" fill="#333333" p-id="2369" data-darkreader-inline-fill="" style="--darkreader-inline-fill:#303336;"></path><path d="M774.144 482.816c0-144.896-118.272-263.168-263.168-263.168-144.896 0-263.168 118.272-263.168 263.168 0 91.136 45.568 174.08 122.368 222.72 11.776 7.68 19.456 20.48 19.456 34.304v107.008h100.864v-175.104L394.24 576.512c-7.168-7.68-7.168-20.48 0-27.136 7.168-7.168 20.48-7.168 27.136 0l89.088 88.064 89.088-88.064c7.168-7.168 20.48-7.168 27.136 0 7.168 7.68 7.168 20.48 0 27.136l-96.256 95.232v175.104h100.864v-107.008c0-14.336 7.168-27.136 19.456-34.304 77.824-48.64 123.392-131.584 123.392-222.72zM426.496 324.608C379.904 355.84 346.112 402.944 330.24 455.68a24.576 24.576 0 0 1-23.552 17.92c-2.56 0-4.608-0.512-7.168-1.024-13.312-4.096-20.992-17.408-16.896-30.72 18.944-64.512 59.904-120.832 115.712-158.72 11.264-7.68 26.624-4.608 34.304 6.656 8.192 11.776 5.12 27.136-6.144 34.816z" fill="#FFE600" p-id="2370" data-darkreader-inline-fill="" style="--darkreader-inline-fill:#ccb800;"></path></svg>小技巧</p><p style="line-height: 1.7;display: block;margin-block-start: 1em;margin-block-end: 1em;margin-inline-start: 0px;margin-inline-end: 0px;">其实你可以使用自定义的有序文字来定义内容前的顺序数列，它更像是一个自定义的无序列表。</p></div>

### Todo 列表

Todo列表是常用的一种待办事宜列表，markdown通过使用 `[ ]` 或 `[x]` 来表示 **未完成** 或 **已完成**。

示例：

``` markdown
- [x] 早上吃一个鸡蛋
- [ ] 中午定外卖要健康
- [ ] 晚上去超市买早餐
```

效果：

- [x] 早上吃一个鸡蛋
- [ ] 中午定外卖要健康
- [ ] 晚上去超市买早餐

<div style="background-color: rgba(255,229,100,.3);border-color: #e7c000;color: #6b5900;padding: .1rem 1.5rem;border-left-width: .5rem;border-left-style: solid;margin: 1rem 0;"><p style="line-height: 1.7;font-weight: 600;margin-bottom: -.4rem;display: block;margin-block-start: 1em;margin-block-end: 1em;margin-inline-start: 0px;margin-inline-end: 0px;color: #b29400;">注意</p><p style="line-height: 1.7;display: block;margin-block-start: 1em;margin-block-end: 1em;margin-inline-start: 0px;margin-inline-end: 0px;color: #6b5900;">它本质上是一个列表，所以不要忘记添加列表的 - 符号。</p></div>

## 表格

在markdown上绘制表格是一件很简单的事情，它通过简单的 `-` 、 `|` 和 `:` 组合起来，就可以完成表格的绘制。

具体方式：

- 使用 `|` 分割每一列的内容。*有些编辑器是可以忽略两边的 `|`的。*
- 使用 `-` 分割表头和内容。
- 使用 `:` 控制每一列的对齐方式，默认左对齐。

示例：

``` markdown
| 表头1 | 表头2 | 表头3 |
|-|:-:|-:|
| 第一列的内容 | 第二列的内容 | 第三列的内容 |
| 内容1 | 内容2 | 内容3 |
```

效果：

> | 表头1 | 表头2 | 表头3 |
> |-|:-:|-:|
> | 第一列的内容 | 第二列的内容 | 第三列的内容 |
> | 内容1 | 内容2 | 内容3 |

### 利用 HTML 绘制更为复杂的表格

虽然这样的表格可以满足绝大多数情况，但有时候我们仍然需要更为复杂的合并情况。可以利用 `HTML` 的 `table` 标签来实现。

当然，这需要一点点 `HTML` 的基础，不过没有关系，这很简单，下面代码对完全没有接触的人也很友好：

示例：

``` html
<table>
   <tr>
        <th width=20%>列宽 `width=20%`</th>
        <th width=45% style="text-align:center">表头居中 `style="text-align:center"`</th>
        <th widht=20% style="text-align:right">居右</th>
        <th widht=5%>列3</th>
   </tr>
   <tr>
        <td >设置背景色 </td>
        <td bgcolor=rgb(92, 184, 92)>`bgcolor=rgb(92, 184, 92)`</td>
        <td bgcolor=#eea236>`bgcolor=#eea236`</td>
        <td bgcolor=pink>`bgcolor=pink`</td>
   </tr>
   <tr>
        <td>**合并列**</td>
        <td colspan=3 align=center> `起始列colspan=2` `align=center`</td>
   </tr>
   <tr>
        <td rowspan=3>**合并行** <br>`起始行rowspan=3`</td>
        <td align=center>`align=center`对`th`无效</td>
        <td>cell</td>
        <td>cell</td>
   </tr>
   <tr>
        <td style="text-align:right">`style="text-align:right"`</td>
        <td>cell</td>
        <td rowspan=2>合并行 `rowspan=2`</td>
   </tr>
   <tr>
        <td>cell</td>
        <td>cell</td>
   </tr>
   <tr><td>cell</td><td>cell</td><td>cell</td><td>cell</td></tr>
</table>
```

效果：

<table>
   <tr>
        <th width=20%>列宽 `width=20%`</th>
        <th width=45% style="text-align:center">表头居中 `style="text-align:center"`</th>
        <th widht=20% style="text-align:right">居右</th>
        <th widht=5%>列3</th>
   </tr>
   <tr>
        <td >设置背景色 </td>
        <td bgcolor=rgb(92, 184, 92)>`bgcolor=rgb(92, 184, 92)`</td>
        <td bgcolor=#eea236>`bgcolor=#eea236`</td>
        <td bgcolor=pink>`bgcolor=pink`</td>
   </tr>
   <tr>
        <td>**合并列**</td>
        <td colspan=3 align=center> `起始列colspan=2` `align=center`</td>
   </tr>
   <tr>
        <td rowspan=3>**合并行** <br>`起始行rowspan=3`</td>
        <td align=center>`align=center`对`th`无效</td>
        <td>cell</td>
        <td>cell</td>
   </tr>
   <tr>
        <td style="text-align:right">`style="text-align:right"`</td>
        <td>cell</td>
        <td rowspan=2>合并行 `rowspan=2`</td>
   </tr>
   <tr>
        <td>cell</td>
        <td>cell</td>
   </tr>
   <tr><td>cell</td><td>cell</td><td>cell</td><td>cell</td></tr>
</table>

## 绘图

markdown本身并不可以绘图，但是通过一些插件可以实现，具体内容参看对应的插件文档。

### 流程图

具体的流程图语法，参看：[流程图语法 flowchart](http://adrai.github.io/flowchart.js/)

``` markdown
 ``` flow
st=>start: 开始:>https://www.jeremyjone.com
 op=>operation: My Operation
 cond=>condition: Yes or No?
 e=>end
 st->op->cond
 cond(yes)->e
 cond(no)->op
 ``` // 结束
```

``` flow
st=>start: 开始:>https://www.jeremyjone.com
op=>operation: My Operation
cond=>condition: Yes or No?
e=>end
st->op->cond
cond(yes)->e
cond(no)->op
```

### 序列图

具体的序列图语法，参看：[序列图语法 js-sequence-diagrams](http://bramp.github.io/js-sequence-diagrams/)

## 公式

markdown通过一系列的语法可以轻松绘制出复杂的公式。更多关于公式的语法，参看：[数学公式语法 mathjax](https://math.meta.stackexchange.com/questions/5020/mathjax-basic-tutorial-and-quick-reference)

示例：

``` markdown
$\sqrt[3]{\frac xy}$

$\left(\frac{\sqrt x}{y^3}\right)$

$\sum_{i=0}^n i^2 = \frac{(n^2+n)(2n+1)}{6}$
```

效果：

$\sqrt[3]{\frac xy}$

$\left(\frac{\sqrt x}{y^3}\right)$

$\sum_{i=0}^n i^2 = \frac{(n^2+n)(2n+1)}{6}$

