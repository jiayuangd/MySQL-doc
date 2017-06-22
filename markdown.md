## MarkDown

Markdown 是一种轻量级标记语言，创始人为約翰·格魯伯（John Gruber）。 它允许人们“使用易读易写的纯文本格式编写文档，然后转换成有效的XHTML(或者HTML)文档”。

Markdown 标记转成HTML的样式每个网站有自己的风格, 但整体的标记格式是统一的. 我们以github来保存相关的文档, 所以我们以github的为样式为标准.

### 标题

使用#，可表示1-6级标题。

# 一级标题
## 二级标题
### 三级标题
#### 四级标题
##### 五级标题
###### 六级标题

### 文字修饰符

看一下粗体字, 斜体字的标记.

*This text will be italic*
_This will also be italic_

**This text will be bold**
__This will also be bold__

~~This text will be delete~~
_You **can** combine them_

### 列表

### 无序列表
主要使用-和*来标记无序列表
```
- George Washington
- John Adams
* Thomas Jefferson
```
### 有序列表
```
1. James Madison
2. James Monroe
3. John Quincy Adams
```
1. James Madison
1. James Monroe
1. John Quincy Adams
```
### 任务列表
```
- [x] Finish my changes
- [ ] Push my commits to GitHub
- [ ] Open a pull request
```
### 段落

段落的前后要有空行，所谓的空行是指没有文字内容。若想在段内强制换行的方式是使用两个以上空格加上回车（引用中换行省略回车）。

### 区块引用

在段落的每行或者只在第一行使用符号>,还可使用多个嵌套引用，如：
```
> 区块引用
>> 嵌套引用
```
### 链接
```
[github](http://github.com)
```
效果:
github

### 图片
```
If you want to embed images, this is how you do it:

![Image of Yaktocat](https://octodex.github.com/images/yaktocat.png)
```
### 代码块
```c
#include <stdio.h>
int main(void){
printf(“hello world!”);
return 0;
}
```
支持Emoji表情

@octocat :+1: This PR looks great - it's ready to merge! :shipit:

表格

标题 | 内容 | 备注
-----|------|-----
今天 | 很热 | 少穿
昨天 | 下雨 | 打伞



