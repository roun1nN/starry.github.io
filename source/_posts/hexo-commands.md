---
title: Hexo commands
date: 2022/6/21 hh:mm:ss # 时间
categories:
- Diary
tags:
- green hand
---

Some basic commands of hexo.

## hexo s



```undefined
hexo s
```

启动本地服务器，用于预览主题。默认地址： [http://localhost:4000/](https://link.jianshu.com?t=http://localhost:4000/)

- `hexo s` 是 `hexo server` 的缩写，命令效果一致；
- 预览的同时可以修改文章内容或主题代码，保存后刷新页面即可；
- 对 Hexo 根目录 `_config.yml` 的修改，需要重启本地服务器后才能预览效果。

## hexo n



```bash
hexo n "学习笔记  一"
```

新建一篇标题为 `学习笔记 一` 的文章，因为标题里有空格，所以加上了引号。

- 文章标题可以在对应 md 文件里改，新建时标题可以写的简单些；
- `hexo n` 是 `hexo new` 的缩写，命令效果一致。

### 文章可以拥有如下属性：

|  -   | Setting    | Description  | Default        |
| :--: | ---------- | ------------ | -------------- |
|  1   | layout     | Layout       | post或page     |
|  2   | title      | 文章的标题   |                |
|  3   | date       | 创建日期     | 文件的创建日期 |
|  4   | updated    | 修改日期     | 文件的修改日期 |
|  5   | comments   | 是否开启评论 | true           |
|  6   | tags       | 标签         |                |
|  7   | categories | 分类         |                |
|  8   | permalink  | url中的名字  | 文件名         |

动态博客中通过发布文章页面设置的各种属性，在hexo里要这样设置。

## hexo d



```undefined
hexo d
```

自动生成网站静态文件，并部署到设定的仓库。

- `hexo d` 是 `hexo deploy` 的缩写，命令效果一致。

## hexo clean



```undefined
hexo clean
```

清除缓存文件 `db.json` 和已生成的静态文件 `public`。

- 网站显示异常时可以执行这条命令试试。

## hexo g



```undefined
hexo g
```

生成网站静态文件到默认设置的 `public` 文件夹。

- 便于查看网站生成的静态文件或者手动部署网站；
- 如果使用自动部署，不需要先执行该命令；
- `hexo g` 是 `hexo generate` 的缩写，命令效果一致。

## hexo n page



```undefined
hexo n page aboutme
```

新建一个标题为 `aboutme` 的页面，默认链接地址为 `主页地址/aboutme/`

- 标题可以为中文，但一般习惯用英文；
- 页面标题和文章一样可以随意修改；
- 页面不会出现在首页文章列表和归档中，也不支持设置分类和标签。

## 常用组合



```undefined
hexo clean && hexo s
hexo clean && hexo d
```

可以用输入法等软件为这些命令设置快捷键，方便调用。

## 草稿

草稿相当于很多博客都有的“私密文章”功能。



```cpp
$ hexo new draft "new draft"
```

会在source/_drafts目录下生成一个new-draft.md文件。但是这个文件不被显示在页面上，链接也访问不到。也就是说如果你想把某一篇文章移除显示，又不舍得删除，可以把它移动到_drafts目录之中。

- 如果你希望强行预览草稿，更改配置文件：



```bash
render_drafts: true
```

- 或者，如下方式启动server：



```ruby
$ hexo server --drafts
```

- 下面这条命令可以把草稿变成文章，或者页面：



```ruby
$ hexo publish [layout] <filename>
```



作者：指尖的跳跃
链接：https://www.jianshu.com/p/a2d298e26dcd
来源：简书
著作权归作者所有。商业转载请联系作者获得授权，非商业转载请注明出处。
