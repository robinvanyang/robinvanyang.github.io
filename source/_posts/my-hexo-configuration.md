---
title: 我的Hexo配置过程 
date: 2016-07-15 01:07:18
tags: hexo
---

## 搭博初衷
很久没写博客了，包括csdn和之前的blog，都很久没有维护， 最近工作变动，关于技术及生活规划也有了很多思考，所以想把blog重新开起来，主要是记录个人对技术的感悟，偶尔可能也会在blog上瞎扯扯淡.

## 搭建hexo及基础配置
额，首先还是说一下啥是hexo吧，省的有乱入的朋友没有听说过这玩意，导致一头雾水， hexo是一个静态的个人博客系统， 就我的了解是基于nodeJS来写的. 类似的静态博客系统有很多， 例如还有OctoPress Jekyll等等，这些都是静态博客生成系统.关于个人博客，我个人最早用的是WordPress，wordpress基于php，是一套动态博客系统，现在貌似越来越少人用了，因为配置相对麻烦， 而且要花钱买空间域名. 当时在09年，还没有Github Pages这种东西， 花钱买域名、空间， 对于无收入着来说也挺难下决心来弄的， 自从有了Github Pages， 我们就可以使用github给我们提供的免费空间来做个人博客了， 个人感觉没Github Pages的话各种各样的静态博客生成系统种类也不会如此繁多， 好稀稀拉拉扯了一大堆, 说正题.

首先，hexo环境在我们电脑里的安装，参照hexo文档中的[概述](https://hexo.io/zh-cn/docs/)页面, 这个步骤执行完之后的效果是我们在终端敲 hexo 命令的时候会有反馈，而不是command not found之类的东西
其次, 安装完hexo之后，我们就可以初始化我们自己博客的编辑、发布的环境了， 参见hexo文档中的[建站](https://hexo.io/zh-cn/docs/setup.html)环节. 这步完成之后，我们就可以预览最初版的博客了，执行hexo server 命令, 在浏览器中打开[localhost:4000](localhost:4000), 就可以看到没有经过任何改动的博客效果
博客初始化好之后，我们可以通过修改配置文件, 即博客配置文件夹中的_config.yml文件来达到自定义博客的目的， 最简单的，如博客的标题， 副标题， 还有作者等等, 参见hexo文档中的[配置](https://hexo.io/zh-cn/docs/configuration.html).
最后， 如何将博客发布到网上，让其他人可以看到， 这里只说如何将我们的blog托管到github页面， 首先， 你需要一个github的账号， 之后在你的github中选择新建一个repository,  也就是github主页中的 New repository按钮了， 点击这个按钮进入新建页面，重点来了， 第一， 保证owner要是你的Github用户名，其次, Repository name 一定是如下格式:  yourgithubname.github.io, 都没问题的话就点击Create repository建立你的博客仓库， github这一块弄好之后，就可以通过修改我们博客根目录下的_config.yml文件，来达到发布的目的， 具体操作参见[部署](https://hexo.io/zh-cn/docs/deployment.html)中的Git节点， 配好之后终端执行hexo deploy就可以将你的博客发布到网上了，别忘记先依次执行hexo clean. hexo generate来重新生成一下静态文件。这步可能出现的问题是没有配ssh-key导致无法上传， 具体解决办法，请google关键字: github ssh-key来解决。


### 更多
上面讲了搭建hexo的大概操作，也是给我自己做个备忘，这些都弄好之后， 我们就可以做更多我们自定义博客的操作， 如换个主题等， 可以参考这个[博文](https://www.haomwei.com/technology/maupassant-hexo.html)
一个小tip， 如何添加网站图标, 把你制作好的favicon.ico文件扔到网站根目录下的source文件夹下就好，再走一次hexo clean. hexo generate, hexo deploy的流程。

好，大概就这些， 这两天我也是在学习如何用Hexo，之后关于如何配一个完美的hexo博客，以及markdown的使用， 有什么收获我都会在这篇文章下面继续添加.

## Added
### 如何保存我们的文稿
即如何保存我们的搭建系统，这样我们即使换了电脑, 可以保存我们最重要的markdown文件， 蛇有蛇道，鼠有鼠道，我们可以通过网盘， evernote等保存，或者干脆在github的博客仓库中新建一个branch， 我的做法是将它放到bitbucket中， bitbucket有免费的私密仓库功能， 这是github没有的。


## TODO LIST
1. 关于我页面编辑
2. 发现订阅还有问题
3. 评论模块添加
4. 当然，有技术上的收获时，放到blog里
