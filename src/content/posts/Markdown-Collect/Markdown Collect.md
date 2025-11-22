---
title: Markdown Collect
published: 2024-08-22 18:29:34
description: Markdown写作指南
categories: Writing
tags: [Markdown, Hexo]
draft: false
---

# 结合Markdown和Hexo特性的一篇写作指南
>注意：根据Markdown处理器或编辑器的不同，部分Markdown语法无法生效，但下面的部分仍会进行列举

## 标题Title
```Markdown
# 一级标题
## 二级标题
### 三级标题
#### 四级标题
##### 五级标题
###### 六级标题

一级标题
==========
使用1个以上=号


二级标题
----------
使用1个以上-号
```

# 一级标题
## 二级标题
### 三级标题
#### 四级标题
##### 五级标题
###### 六级标题

一级标题
==========

二级标题
----------
<br>

## 段落Paragrapgh
```Markdown
段落1，下面是空白行，

段落2，用于分隔段落
```

段落1，下面是空白行，

段落2，用于分隔段落
<br>

## 换行Line Break
```Markdown
我使用两个空格  换行

我使用<br>换行
```

我使用两个空格  换行

我使用<br>换行
<br>

## 强调Bold & Italic
```Markdown
__粗体__
**粗体**

需加粗一个单词或短语的中间部分时使用 **
粗**体**

_斜体_
*斜体*
需斜体一个单词或短语的中间部分时使用 *
斜*体*

___同时使用粗体和斜体___
***同时使用粗体和斜体***
同上对于一个单词或短语的中间部分时使用***
粗***体和斜***体
```
__粗体__
**粗体**
粗**体**

_斜体_
*斜体*
斜*体*

___同时使用粗体和斜体___
***同时使用粗体和斜体***
粗***体和斜***体
<br>

## 引用Quote
```Markdown
>这是一段引用
>
>同样使用空行创建段落

>下面是嵌套的引用
>>在嵌套了
>>>在嵌套嵌套了

引用中使用其他Markdown格式元素
> #### The quarterly results look great!
>
> - Revenue was off the chart.
> - Profits were higher than ever.
>
>  *Everything* is going according to **plan**.
```

>这是一段引用
>
>同样使用空行创建段落

>下面是嵌套的引用
>>在嵌套了
>>>在嵌套嵌套了

> #### The quarterly results look great!
>
> - Revenue was off the chart.
> - Profits were higher than ever.
>
>  *Everything* is going according to **plan**.
<br>

## 列表List
```Markdown
有序列表
1. 项目一
2. 项目二
3. 项目三

无序列表，使用 - 或 + 或 *
- 变形太刀
- 折叠太刀

* 充能太刀
* 带盾太刀

+ 演奏太刀
+ 飞天太刀
```
有序列表
1. 项目一
2. 项目二
3. 项目三

无序列表
- 变形太刀
- 折叠太刀

* 充能太刀
* 带盾太刀

+ 演奏太刀
+ 飞天太刀
<br>

## 代码Code
使用 \`
`git clone`

要在代码段中使用\`时,使用 \`\`
``Use `code` in your markdown``

代码块
1. 行缩进四个空格或一个制表符
    System.out.println("hello world");

2. 围栏，使用3个 \` 或 \~，指定使用的语言来添加语法高亮，例如 \`\`\`java
```java
    /**
     * 文件列表
     */
    @GetMapping("/fileList")
    public ResponseVo loadFileList(HttpSession session, @RequestBody FileQueryDto fileQueryDto) {
        UserSessionDto userSessionDto = (UserSessionDto) session.getAttribute(Constants.SESSION_USER_KEY);
        fileQueryDto.setUserId(userSessionDto.getUserId());
        fileQueryDto.setDelFlag(FileDelFlagEnum.CLOUD.getDelFlag());
        return getSuccessResponseVo(userFileService.loadFileListByPage(fileQueryDto));
    }
```
<br>

## 分隔线Horizontal Rule
```Markdown
3个以上的 \* 或 \- 或 \_
为了兼容性，请在分隔线的前后均添加空白行

***

---

___

```
***

---

___
<br>

## 链接Link
```Markdown
#### 超链接

链接title可选
[超链接显示名](超链接地址 "超链接title")

[HigeNeko Blog](http://www.higeneko.site/ "这是本博客地址")

#### 网址或Email地址
<https://mvnrepository.com/>
<fake@example.com>

#### 格式化链接

使用强调语法
This is **[Bold Link !](example.com.bold)**

将链接表示为代码
This is [`code link`](example.com.code)

#### 引用
[hobbit-hole][1]

[1]: https://en.wikipedia.org/wiki/Hobbit#Lifestyle "Hobbit lifestyles"

#### 文内跳转
[跳转到##链接Link](#链接link)
```

#### 超链接

链接title可选
[超链接显示名](超链接地址 "超链接title")

[HigeNeko Blog](http://www.higeneko.site/ "这是本博客地址")

#### 网址或Email地址
<https://mvnrepository.com/>
<fake@example.com>

#### 格式化链接

使用强调语法
This is **[Bold Link !](example.com.bold)**

将链接表示为代码
This is [`code link`](example.com.code)

#### 引用
[hobbit-hole][1]

[1]: https://en.wikipedia.org/wiki/Hobbit#Lifestyle "Hobbit lifestyles"

#### 文内跳转
[跳转到##链接Link](#链接link)
<br>

## 图片Img
```Markdown
类似链接，前面加上!
![图片alt](图片链接 "图片title")

Hexo打开文章资源文件夹功能后，
如果通过使用相对路径的常规 markdown 语法，
它将不会出现在首页上
![图片不存在](<example.jpg> "图片title")

上面的示例中同样展示了文件路径存在空格时，可以使用的解决办法
```

类似链接，前面加上!
![图片alt](图片链接 "图片title")

Hexo打开文章资源文件夹功能后，
如果通过使用相对路径的常规 markdown 语法，
它将不会出现在首页上
![图片不存在](<example.jpg> "图片title")


#### 调整图片的大小
##### 使用HTML
```Html
![图片不存在](example.jpg =300x300 "This is a example image")
<img src="example.jpg" width=70%>
<img src="example.jpg" width=300 height=300>
```

![图片不存在](example.jpg =300x300 "This is a example image")
<img src="example.jpg" width=70%>
<img src="example.jpg" width=300 height=300>

## 转义字符Escape
```Markdown
\- a
- a
```

\- a
- a
<br>

## 内嵌HTML标签
```Html
<font color=orange size=4>注意！！！</font>
<font color=#0000FF size=6>注意！！！</font>
```
<font color=orange size=4>注意！！！</font>
<font color=#0000FF size=6>注意！！！</font>
<br>

## 表格Table
一般使用工具生成Markdown表格
```Markdown
| Syntax      | Description |
| ----------- | ----------- |
| Header      | Title       |
| Paragraph   | Text        |

左、右对齐，居中
| Syntax      | Description | Test Text     |
| :---        |    :----:   |          ---: |
| Header      | Title       | Here's this   |
| Paragraph   | Text        | And more      |
```

| Syntax      | Description |
| ----------- | ----------- |
| Header      | Title       |
| Paragraph   | Text        |

左、右对齐，居中
| Syntax      | Description | Test Text     |
| :---        |    :----:   |          ---: |
| Header      | Title       | Here's this   |
| Paragraph   | Text        | And more      |

<br>

## 折叠内容Fold
```html
<details>
<summary>点击展开</summary>
被折叠的内容
</details>
```
> 注意：在折叠内容里使用markdown需要先空行

<details>
<summary>点击展开</summary>
被折叠的内容
</details>
<br>

## 删除线Delete Line
```Markdown
~~不是删除线~~
```

~~不是删除线~~
<br>

## 任务列表Task
```Markdown
- [x] 添加使用样例
- [ ] 文章概述调整
```

- [x] 添加使用样例
- [ ] 文章概述调整
<br>

## 表情符号Emoji
```Markdown
复制黏贴
😂
使用表情符号简码
:tent:
```
😂
:tent:
<br>

## 数学公式Formula
```Markdown
上标
n^2^

下标
n~2~
```
上标
n^2^

下标
n~2~
<br>

## 该注意的点
#### 使用`hexo generate`报错
```Shell
ERROR Process failed: _posts/DDD框架.md
ValidationError: `null` is not a string!
```

博客文章中存在某些属性没有填写，为空（null）
例如`excerpt:(文章概要)`

解决方法
1. 填写缺失的属性，不需要时则删掉对应的属性

#### 为标题手动编号
例如 
一、标题
二、标题
(1)标题
(2)标题

为标题手动添加编号，而不是只使用markdown语法标识，
可以增加可读性

#### 多个空行
空行在markdown里是用来区分段落的，
连续使用多个空行，**也只是分隔成两个段落**，不能实现多个空行的效果

*markdown*
```markdown
111





222
```
*显示效果*
111





222

要使用多个空行时，用`<br>`
```markdown
例1
111<br><br>
222

例2
111
<br>
222
```
例1
111<br><br>
222

例2
111
<br>
222

> 例1和例2效果一样都空了**2行**
<br>


