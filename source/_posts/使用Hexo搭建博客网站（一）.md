---
title: 使用Hexo搭建博客网站（一）
date: 2016-07-27 14:51:53
tags:
- Hexo
- Markdown
- 博客网站
categories:
- 其他
---

*本文的主要目的是熟悉Markdown语法，原文：[Hexo](https://hexo.io/zh-cn/docs/index.html "https://hexo.io/zh-cn/docs/index.html")*

## 什么是 Hexo?
Hexo 是一个快速、简洁且高效的博客框架。Hexo 使用 Markdown（或其他渲染引擎）解析文章，在几秒内，即可利用靓丽的主题生成静态网页。

## 安装
安装 Hexo 相当简单。然而在安装前，您必须检查电脑中是否已安装下列应用程序：
- [Node.js](https://nodejs.org/en/)
- [Git](https://git-scm.com/)

如果您的电脑中已经安装上述必备程序，那么恭喜您！接下来只需要使用 npm 即可完成 Hexo 的安装。
```
$ npm install -g hexo-cli
```
*Node.js、Git安装略*
- - -

## 建站
安装 Hexo 完成后，请执行下列命令，Hexo 将会在指定文件夹中新建所需要的文件。
```
$ hexo init <folder>
$ cd <folder>
$ npm install
```
新建完成后，指定文件夹的目录如下：
![](/blog/images/2016-7-27/2016-7-27-1.png)

### _config.yml
网站的 配置 信息，您可以在此配置大部分的参数。

### package.json
```
//package.json
{
  "name": "hexo-site",
  "version": "0.0.0",
  "private": true,
  "hexo": {
    "version": ""
  },
  "dependencies": {
    "hexo": "^3.0.0",
    "hexo-generator-archive": "^0.1.0",
    "hexo-generator-category": "^0.1.0",
    "hexo-generator-index": "^0.1.0",
    "hexo-generator-tag": "^0.1.0",
    "hexo-renderer-ejs": "^0.1.0",
    "hexo-renderer-stylus": "^0.2.0",
    "hexo-renderer-marked": "^0.2.4",
    "hexo-server": "^0.1.2"
  }
}
```
### scaffolds
**模版**文件夹。当您新建文章时，Hexo 会根据 scaffold 来建立文件。
### source
资源文件夹是存放用户资源的地方。除`_posts `文件夹之外，开头命名为`_`(下划线)的文件 / 文件夹和隐藏的文件将会被忽略。Markdown 和 HTML 文件会被解析并放到`public`文件夹，而其他文件会被拷贝过去。
### themes
[主题](https://hexo.io/themes/) 文件夹。Hexo 会根据主题来生成静态页面。

## 配置

您可以在 _config.yml 中修改大部份的配置。

### 网站
|参数|描述|
|-|-|
|title|网站标题|
|subtitle|网站副标题|
|description|网站描述|
|language|网站使用的语言|
|timezone|网站时区。Hexo 默认使用您电脑的时区。时区列表。比如说：America/New_York, Japan, 和 UTC 。|

### 网址
|参数|描述|默认值|
|-|-|-|
|url|网址||
|root|网站根目录||
|permalink|文章的永久链接格式|:year/:month/:day/:title/|
|permalink_default|永久链接中各部分的默认值||

>网站存放在子目录:
 如果您的网站存放在子目录中，例如 `http://yoursite.com/blog`，则请将您的 `url` 设为 `http://yoursite.com/blog` 并把 `root` 设为 `/blog/`。
 
 
### 目录
|参数|描述|默认值|
|-|-|-|
|source_dir|资源文件夹，这个文件夹用来存放内容。|source|
|public_dir|公共文件夹，这个文件夹用于存放生成的站点文件。|public|
|tag_dir|标签文件夹|tags|
|archive_dir|归档文件夹|archives|
|category_dir|分类文件夹|categories|
|code_dir|Include code 文件夹|downloads/code|
|i18n_dir|国际化（i18n）文件夹|:lang|
|skip_render|跳过指定文件的渲染，您可使用 glob 表达式来匹配路径。	||


### 文章
|参数	|描述	|默认值|
|-|-|-|
|new_post_name|新文章的文件名称|:title.md|
|default_layout|预设布局|post|
|auto_spacing|在中文和英文之间加入空格	|false|
|titlecase|把标题转换为 title case|false|
|external_link|在新标签中打开链接|true|
|filename_case|把文件名称转换为 (1) 小写或 (2) 大写	|0|
|render_drafts|显示草稿|false|
|post_asset_folder|启动 Asset 文件夹|false|
|relative_link|把链接改为与根目录的相对位址|false|
|future|显示未来的文章|true|
|highlight|代码块的设置||




### 分类 & 标签
|参数|描述|默认值|
|-|-|-|
|default_category|默认分类|uncategorized|
|category_map|分类别名||	
|tag_map|标签别名||

### 日期 / 时间格式
Hexo 使用 Moment.js 来解析和显示时间。

|参数|描述|默认值|
|-|-|-|
|date_format|日期格式|MMM D YYYY|
|time_format|时间格式|H:mm:ss|

### 分页
|参数|描述|默认值|
|-|-|-|
|per_page|每页显示的文章量 (0 = 关闭分页功能)|10|
|pagination_dir|分页目录|page|

### 扩展
|参数|描述|
|-|-|
|theme|当前主题名称。值为`false`时禁用主题|
|deploy|部署部分的设置|


## Markdown代码
````
*本文的主要目的是熟悉Markdown语法，原文：[Hexo](https://hexo.io/zh-cn/docs/index.html "https://hexo.io/zh-cn/docs/index.html")*

## 什么是 Hexo?
Hexo 是一个快速、简洁且高效的博客框架。Hexo 使用 Markdown（或其他渲染引擎）解析文章，在几秒内，即可利用靓丽的主题生成静态网页。

## 安装
安装 Hexo 相当简单。然而在安装前，您必须检查电脑中是否已安装下列应用程序：
- [Node.js](https://nodejs.org/en/)
- [Git](https://git-scm.com/)

如果您的电脑中已经安装上述必备程序，那么恭喜您！接下来只需要使用 npm 即可完成 Hexo 的安装。
```
$ npm install -g hexo-cli
```
*Node.js、Git安装略*
- - -

## 建站
安装 Hexo 完成后，请执行下列命令，Hexo 将会在指定文件夹中新建所需要的文件。
```
$ hexo init <folder>
$ cd <folder>
$ npm install
```
新建完成后，指定文件夹的目录如下：
![](/blog/images/2016-7-27/2016-7-27-1.png)

### _config.yml
网站的 配置 信息，您可以在此配置大部分的参数。

### package.json
```
//package.json
{
  "name": "hexo-site",
  "version": "0.0.0",
  "private": true,
  "hexo": {
    "version": ""
  },
  "dependencies": {
    "hexo": "^3.0.0",
    "hexo-generator-archive": "^0.1.0",
    "hexo-generator-category": "^0.1.0",
    "hexo-generator-index": "^0.1.0",
    "hexo-generator-tag": "^0.1.0",
    "hexo-renderer-ejs": "^0.1.0",
    "hexo-renderer-stylus": "^0.2.0",
    "hexo-renderer-marked": "^0.2.4",
    "hexo-server": "^0.1.2"
  }
}
```
### scaffolds
**模版**文件夹。当您新建文章时，Hexo 会根据 scaffold 来建立文件。
### source
资源文件夹是存放用户资源的地方。除`_posts `文件夹之外，开头命名为`_`(下划线)的文件 / 文件夹和隐藏的文件将会被忽略。Markdown 和 HTML 文件会被解析并放到`public`文件夹，而其他文件会被拷贝过去。
### themes
[主题](https://hexo.io/themes/) 文件夹。Hexo 会根据主题来生成静态页面。

## 配置

您可以在 _config.yml 中修改大部份的配置。

### 网站
|参数|描述|
|-|-|
|title|网站标题|
|subtitle|网站副标题|
|description|网站描述|
|language|网站使用的语言|
|timezone|网站时区。Hexo 默认使用您电脑的时区。时区列表。比如说：America/New_York, Japan, 和 UTC 。|

### 网址
|参数|描述|默认值|
|-|-|-|
|url|网址||
|root|网站根目录||
|permalink|文章的永久链接格式|:year/:month/:day/:title/|
|permalink_default|永久链接中各部分的默认值||

>网站存放在子目录:
 如果您的网站存放在子目录中，例如 `http://yoursite.com/blog`，则请将您的 `url` 设为 `http://yoursite.com/blog` 并把 `root` 设为 `/blog/`。
 
 
### 目录
|参数|描述|默认值|
|-|-|-|
|source_dir|资源文件夹，这个文件夹用来存放内容。|source|
|public_dir|公共文件夹，这个文件夹用于存放生成的站点文件。|public|
|tag_dir|标签文件夹|tags|
|archive_dir|归档文件夹|archives|
|category_dir|分类文件夹|categories|
|code_dir|Include code 文件夹|downloads/code|
|i18n_dir|国际化（i18n）文件夹|:lang|
|skip_render|跳过指定文件的渲染，您可使用 glob 表达式来匹配路径。	||


### 文章
|参数	|描述	|默认值|
|-|-|-|
|new_post_name|新文章的文件名称|:title.md|
|default_layout|预设布局|post|
|auto_spacing|在中文和英文之间加入空格	|false|
|titlecase|把标题转换为 title case|false|
|external_link|在新标签中打开链接|true|
|filename_case|把文件名称转换为 (1) 小写或 (2) 大写	|0|
|render_drafts|显示草稿|false|
|post_asset_folder|启动 Asset 文件夹|false|
|relative_link|把链接改为与根目录的相对位址|false|
|future|显示未来的文章|true|
|highlight|代码块的设置||




### 分类 & 标签
|参数|描述|默认值|
|-|-|-|
|default_category|默认分类|uncategorized|
|category_map|分类别名||	
|tag_map|标签别名||

### 日期 / 时间格式
Hexo 使用 Moment.js 来解析和显示时间。

|参数|描述|默认值|
|-|-|-|
|date_format|日期格式|MMM D YYYY|
|time_format|时间格式|H:mm:ss|

### 分页
|参数|描述|默认值|
|-|-|-|
|per_page|每页显示的文章量 (0 = 关闭分页功能)|10|
|pagination_dir|分页目录|page|

### 扩展
|参数|描述|
|-|-|
|theme|当前主题名称。值为`false`时禁用主题|
|deploy|部署部分的设置|
````
 