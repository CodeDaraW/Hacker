# Hacker | [English Docs](/README.md)
[![Open Source Love](https://badges.frapsoft.com/os/v1/open-source.svg?v=103)](https://github.com/ellerbrock/open-source-badge/)  [![GPL Licence](https://badges.frapsoft.com/os/gpl/gpl.svg?v=103)](https://opensource.org/licenses/GPL-2.0)  


__Hacker 是一款专注于写作的简洁博客主题。在如此讲究复杂排版的趋势下，选择回归本源，专注于写作这件事。__  

一开始是 [moyo](http://liuxinyu.me/) 为 Wordpress 所创作的一个主题，由 CodeDaraW 移植到 Hexo 。

## Demo
参考我的博客：[DaraW](http://blog.daraw.cn/)。  
可以使用 TravisCI 实现自动化部署，配置参考 [CodeDaraW/Blog](https://github.com/CodeDaraW/Blog)。

![](https://ooo.0o0.ooo/2016/08/04/57a306f56bee2.png
)

## 安装
获得主题文件， `git clone` 或者 `download zip` 均可；  

在 `themes` 文件夹中创建文件夹 `Hacker` ，将主题文件都复制粘贴至 `Hacker` 文件夹；  

然后在hexo全局配置文件 `_config.yml` 中应用主题：

```yaml
theme: Hacker
```

这样就安装好了，开始享受吧~

__注意：版本更新后建议在hexo生成前执行一次 `hexo clean` ，清除以前的缓存，避免带来的一些莫名其妙的问题。__

## 配置
### 启用评论和谷歌分析
参考 `_config.example.yml` 配置案例，创建主题配置文件 `_config.yml` 并编辑：

```yaml
# gitment
gitment: false
gitment_owner:
gitment_repo:
gitment_client_id:
gitment_client_secret:

# gitalk
gitalk: false
gitalk_owner:
gitalk_admin: []
gitalk_repo:
gitalk_client_id:
gitalk_client_secret:

# valine comment
valine: false
leancloud_id:
leancloud_key:

# disqus comment
disqus: false
disqus_shortname:

# utterances comment
utterances: false
utterances_repo:

# livere city comment
livere: false
livere_data_uid:

# giscus comment
giscus: false
data_repo: 
data_repo_id: 
data_category: 
data_category_id: 
data_mapping: 
#data_term: 
data_strict: 0
data_reactions_enabled: 0
data_emit_metadata: 0
data_input_position: bottom 
data_loading: 
data_lang:

# google analytics
googleTrackId:

# baidu analytics
baiduTrackId:
```

`gitment`: `boolean`，是否开启 Gitment 评论  
`gitment_owner`: `string`，你的 GitHub ID  
`gitment_repo`: `string`，存储评论的 Repo  
`gitment_client_id`: `string`，你的 Client ID  
`gitment_client_secret`: `string`，你的 Client Secret  

`gitalk`: `boolean`，是否开启 Gitalk 评论  
`gitalk_owner`: `string`，你的 GitHub ID  
`gitalk_admin`: `array`，所有管理员 GitHub ID  
`gitalk_repo`: `string`，存储评论的 Repo  
`gitalk_client_id`: `string`，你的 Client ID  
`gitalk_client_secret`: `string`，你的 Client Secret  

`valine`: `boolean`，是否开启 Valine 评论  
`leancloud_id`: `string`，你的 LeanCloud ID  
`leancloud_key`: `string`，你的 LeanCloud Key  

`disqus`: `boolean`，是否开启 Disqus 评论  
`disqus_shortname`: `string`，你的 Disqus Site Shortname。  

`utterances`: `boolean`， 是否开启 utterances 评论  
`utterances_repo`: `string`，存储评论的 Repo

`livere`: `boolean`，是否开启 LiveRe City 评论  
`livere_data_uid`: `string`，可以在这里找到 https://livere.com/insight/myCode

`giscus`: `boolean`，是否开启 giscus 评论  
`data_repo`: `string`，存储评论的 Repo  
`data_repo_id`: `string`，可从 https://giscus.app 轻松获取此 ID   
`data_category`: 当搜索匹配的 discussion 时，giscus 将只搜索该分类  
`data_category_id`: `string`，可从 https://giscus.app 轻松获取此 ID ， 推荐使用公告（announcements）类型的分类   
`data_mapping`: 输入 pathname 或者 URL 或者 title 或者 og:title 或者 specific 或者 number   
`data_term`: 如果在 data_mapping （页面与 Discussion 映射关系）中选择了 specific （特定字符串）或者 number （特定 discussion 号），请打开这个选项然后输入字符或者 discussion 号  
`data_strict`: `boolean`，是否使用严格的标题匹配  
`data_reactions_enabled`: `boolean`，是否启用主帖子上的反应（reaction）   
`data_emit_metadata`: `boolean`，是否输出 discussion 的元数据  
`data_input_position`: 输入 top 或者 bottom 将评论框放在评论上方或下方    
`data_loading`: 输入“lazy”或者保持空白，以开启或关闭懒加载评论    
`data_lang`: giscus 的显示语言

`googleTrackId`: `string`，为谷歌分析的个人ID，留空则为不使用谷歌分析。

`baiduTrackId`: `string`, 为百度统计的个人ID,留空则为不是用谷歌分析。

### 启用分类和标签页面
分类功能：执行 `hexo new page categories` ，然后修改生成的 `source/categories/index.md` ：

``` markdown
title: categories
date: 2017-01-30 19:16:17
layout: "categories"
---  
```

如果你需要关闭该页的评论，可以添加一行 `comments: false`；`title` 对应的则是该页的标题。  

标签功能：同理，执行 `hexo new page tags` ，然后修改生成的 `source/tags/index.md` ：
``` markdown
title: tags
date: 2017-01-30 19:16:17
layout: "tags"
---  
```
配置同分类功能。

在菜单中添加链接：编辑主题的 `_config.yml` ，在 `menu` 中添加 `Categories: /categories` 和 `Tags: /tags`，如下：
``` yml
menu:
  Home: /
  Archives: /archives
  Categories: /categories
  Tags: /tags
```

## 自动化部署

为了避免冲突, 我将`_config.xml` 添加到了`gitignore`中, 所以如果你想通过自动化工具来部署博客, 你可以将`_config.xml`从`gitignore`中移除或添加软链.

## 协议

GNU GPL(General Public License) v2.0
