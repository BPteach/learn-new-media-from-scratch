---
title: 如何用Supermetrics自动更新数据？
date: 2017-08-29
permalink: supermetrics-tutorial
tags: [Google Analysitcs,数据,Supermetrics,Google Spreedsheet]
---

做新媒体营销是为了什么？为了转化。那么我们需要评估我们的每一个行为所带来的效果，而数据是最好的评估工具。数据直观地反映效果，就好像减肥一样，记录每天的体重，观察一段时间的体重曲线，你才能知道自己为了减肥节的食、运的动都是不是有效果。比如，半撇私塾主要通过内容营销的方式来获取流量，那么我们就需要每天记录官网的 PV，来判断我们的文章是否起到了拉新的作用。

但是每天手动更新数据，其实是件很浪费时间的事。就像你要减肥，需要每天记录体重，但手动记录不仅麻烦，而且容易忘，要是有那么一个电子秤可以自动帮你记录每天的体重，还自动更新到对应的 App 里，那简直太方便了。对于我来说，每天手动更新网页的 PV 也是一件很麻烦的事。半撇私塾在搭建数据体系的时候，搭配使用了 **Google Analystics 和 Google Spreedsheet 这两个工具**，每次记录时，我得先看 Google Analystics 的后台，再一步步操作找到我要的数据，再手动填到表格里去……一来二去这就是十几分钟啊，赶上网不好的时候还能更久。

![](http://cdn.bpteach.com/17-8-29/51535974.jpg)

为了省这么十几分钟，我用上了 **Supermetrics** 这个神器，可以帮助我自动更新每天的数据。**Supermetrics 是 Google Docs 里的一个插件**——没错 Google Spreedsheet 里也能用插件。安装了这个插件，我只需要**设置好日期、指标等基本参数，然后每天打开表格、运行插件，点一下鼠标就可以自动更新数据了**，省时又省心。

![](http://cdn.bpteach.com/17-8-29/94030476.jpg)

这个操作可以说是非常快了，下面我就用自动更新 PV 数据这个例子，来分享一下这个神器的使用步骤。

## 第一步：在 Google Spreedsheet 中运行 Supermetrics  插件

先要说明的是，由于这个插件搭配的是 Google Analystics 和 Google Spreedsheet 这两个工具，所以以下的每一个步骤都需要用到代理服务器。这里推荐一个简单又好用的工具：蓝灯（Latern），官方的 GitHub 链接在这里：https://github.com/getlantern/lantern

好的，搞定了翻墙，就正式开始操作了。首先你需要**有一个谷歌账号**，然后按照以下步骤**下载 Supermetrics 插件**：

- 打开 Google Spreedsheet 表格
- 点击 `插件`-`获取插件`
- 输入「Supermetrics 」并搜索
- 点击 `+` 号，添加插件

![](http://cdn.bpteach.com/17-8-29/9345754.jpg)

在添加插件的过程中，会弹出一个小框，提示你登录谷歌账号，所以我说需要有一个谷歌账号啦。

安装好插件，就可以直接点击运行了。

![](http://cdn.bpteach.com/17-8-29/10820335.jpg)

## 第二步：选择 Data Source

运行插件之后，我们要来设置基本的参数了。

首先要设置的是 Data Source，顾名思义，就是**数据来源**。你用什么网站统计数据，就选哪个网站。

比如我用 Google Analystics 进行统计，那么我可以直接在下拉列表里选择 Google Analystics，同样的，Google Analystics 也需要用你的谷歌账号登录。

![](http://cdn.bpteach.com/17-8-29/51638223.jpg)




## 第三步：Select Views

下一个要设置的是 Views，也就是**你要监测的网页**。需要注意的是，**你的谷歌账号必须对这个网页有权限监测**，比如半撇私塾的数据都是用 Google Analystics 来统计的，我用我的谷歌账号登录 Google Analystics 时，有权限看到后台的所有数据。

所以，如果你对你想监测的网页有监测权限，那么你就选择它，当然，下拉列表里会自动出现你有监测权限的网页。比如我可以监测半撇私塾这个网页的数据，那么我就选择 `Master View of BPteach`。

![](http://cdn.bpteach.com/17-8-29/68688760.jpg)

## 第四步：Select dates

这一步是选择**进行数据监测的时间段**，比如监测昨天、过去 7 天、过去 30 天、过去一年的每一天……

**你想监测什么时段，就选什么时段**，比如我想监测从今年年初到现在每天的 PV，以观察变化，我就选 `Year to date`。

![](http://cdn.bpteach.com/17-8-29/58608815.jpg)


## 第五步：Select metrics

这是最关键的一步，也就是选择**你要监测的数据指标**。什么是数据指标呢？也就是网站的 PV、UV、DAU 等数据。

**你的数据体系中哪些指标重要，就记录哪些指标**。比如对我来说最重要的是每天浏览半撇私塾官网的人数，因为这些都是我创作的文章所带来的流量，那么我需要记录每天的 PV，我就选 `Pageviews`。

![](http://cdn.bpteach.com/17-8-29/80883295.jpg)


## 第六步：一键抓取数据

接下来还有两个小操作，一个是设置 Split to rows 的选项，一个是设置 Segment。

- **Split to rows/columns**：意思是你的横行和纵列要显示什么。横行可以设置为日期，纵列可以按照你的需要进行选择，比如我可以选 `New Users` 和 `Returning Users`，这样可以对比新用户和老用户对 PV 的贡献值，看看是哪一部分比较多。不过我只拿每天的 PV 举例，不需要进行额外的对比，那么我可以只选 `Date`。  
- **Segment**：是指你的受众范围，比如我想监测的是所有 PV 而不仅仅是新用户的访问量，那么我就选择 `All Users`。

![](http://cdn.bpteach.com/17-8-29/66157874.jpg)

其他的设置保留默认设置就好，因为你会用到的参数也就上面那么几个，接下来只需要点击 `Get Data to Table`，就可以抓取数据啦。

![](http://cdn.bpteach.com/17-8-29/29824125.jpg)

如果我需要每天记录 PV，那么我只需要每天打开表格和插件，点一次 `Refresh`，就可以抓取每天的数据了。


![](http://cdn.bpteach.com/17-8-29/90238980.jpg)


做新媒体工作时，我们常常会做很多重复的数据分析工作，比如我举的这个每天记录 PV 的例子，就真的很浪费时间。但作为新媒体人，又不可能不结合数据开展工作，那么 Supermetrics 这个小工具就可以派上用场了。

你可以把这个小工具应用到别的场景里，例如统计不同新媒体渠道的引流情况，只需要改变几个简单的设置，比如把 metrics 改一改，就可以抓数据了。简单的操作就能让我们迅速获取数据，这类小工具简直就是帮助新媒体人提升工作效率的福音。
如果想要更系统地学习新媒体营销，请立即免费申请加入「[新媒体自习室](http://learn.bpteach.com/course/100?utm_source=zhihu.com&utm_medium=referral&utm_campaign=mkg102-lx&utm_term=supermetrics-tutorial&utm_content=textlink)」课程。
