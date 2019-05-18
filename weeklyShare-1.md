---
title: 每周分享第1期
date: 2019-02-17 10:16:48
copyright: false
tags: 
    - 每周分享
---

>2019年2月17日第1期
记录这一周的见闻以及值得分享的内容，每周日晚更新。

# CS见闻

1、[谷歌发布全球首个产品级移动端分布式机器学习系统](https://mp.weixin.qq.com/s/S_ggeDKR90tatkxc_35-hg)

<div align=center><img src="http://img.linqunshu.cn/federatedlearning.png"></div>

谷歌近日宣布，他们实现了全球首个产品级的超大规模移动端分布式机器学习系统，目前已经能够在数千万部手机上运行。其中运用的是他们在17年提出的联合学习（Federated Learning），联合学习（FL）是一种分布式机器学习方法，可以对保存在移动电话等设备上的大量分散数据进行训练。

根据谷歌官博介绍，用户的设备会下载一个当前模型，这个模型会从手机数据中学习不断得到改善，然后将变化总结为一个小的关键更新。只有这个关键更新会以加密的方式被传到云端，之后这一更新会在云端迅速被其他用户对共享模型提交的更新平均化（averaged）。

简单说，所有的训练数据都留在用户的设备上，而且上传到云端的个别更新也不会存储到云端。这样只上传关键的加密更新数据，能在一定程度上保证用户的隐私。

2、[神经网络层并非“生而平等”](https://mp.weixin.qq.com/s/6mi2trmQSMeb2bKZRkPm5w)

在[这篇新的论文](https://arxiv.org/pdf/1902.01996.pdf)中，张弛原等人继续探讨深度神经网络的泛化能力，深入到层的级别，并指出在研究深度模型时，仅关注参数或范数（norm）的数量是远远不够的。深层网络中的层在表示预测函数时所起的作用并不均等。某些层对于产生良好的预测结果至关重要，而其他层对于在训练中分配其参数则具备相当高的鲁棒性。

3、[用 Polygon-RNN++ 实现分段数据集的高效交互式标注](http://www.cs.toronto.edu/polyrnn/)

<div align=center><img src="http://img.linqunshu.cn/polygon.jpg"></div>

Polygon-RNN++能够让你在图中每个目标物体的周围大致圈出多边形形状，然后网络会自动生成分割的标注，可以大幅度提高标注的效率。[online demo](http://www.cs.toronto.edu/~amlan/demo/)

4、[NLP Chinese Corpus项目：大规模中文自然语言处理语料](https://github.com/brightmart/nlp_chinese_corpus)

一期目标：10个百万级中文语料 & 3个千万级中文语料(2019年5月1号)

二期目标：30个百万级中文语料 & 10个千万级中文语料 & 1个亿级中文语料（2019年12月31日）

目前提供了`维基百科json版`、`新闻语料json版`、`百科类问答json版`。

# 新闻&创投

1、[强生34亿美元收购外科手术机器人公司Auris](https://readhub.cn/topic/7Kh1AElk62b)

强生周三宣布，该公司将以34亿美元的价格收购Auris Health，支付方式为现金，这项交易可令强生获得后者用于呼吸道手术和肺癌检测的外科手术机器人技术。据预计，医疗机器人市场到2023年时的规模将可达到近120亿美元。

2、[中科大成功研制"智能窗纱"，50秒可净化室内雾霾](https://readhub.cn/topic/7KgOPaB9IYW)

中国科学技术大学俞书宏教授团队通过“浸染自组装”方法，研制出一种制备速度快、成本低廉的“智能窗纱”材料，对室内空气的净化效率最高可达99.65%，能在50秒内将空气中的PM2.5浓度从“严重污染”净化至“优”。


# 教程

1、[The modern JavaScript Tutorial ](https://javascript.info/)

<div align=center><img src="http://img.linqunshu.cn/jsinfo.png"></div>

不仅只是介绍JavaScript的语法，还会介绍JavaScript能做什么，不能做什么，以及是什么原因使得会有这些限制，内容非常丰富。不仅适合初学者学习，也适合重温一下知识。

2、[MIT深度学习基础教程：CNN、RNN等7种深度学习架构范例 概览](https://mp.weixin.qq.com/s?__biz=MzU0NjY0NDIzMA==&mid=2247485002&idx=2&sn=97534e50cb9eeafe189afac03bb4aa5f&chksm=fb5bce23cc2c473589d896c27dc010ef410c43a16c97c55fc8b88f984db2d1488ce20ab572df&mpshare=1&scene=24&srcid=#rd)

3、[数据可视化基础](https://serialmentor.com/dataviz/)

O'Reilly 新书《数据可视化基础》一书的在线预览版。(摘自[阮一峰的每周分享](http://www.ruanyifeng.com/blog/2019/02/weekly-issue-43.html))

# 工具

1、[Git History](https://github.com/pomber/git-history)

<div align=center><img src="https://user-images.githubusercontent.com/1911623/52460615-f3899d80-2b49-11e9-8c21-06af4097a527.gif"></div>

可以快速地以可视化的方式浏览Github上文件的历史版本。

2、[Carbon代码“美颜神器”](https://carbon.now.sh)

<div align=center><img src="http://img.linqunshu.cn/carbon.png"></div>

可以生成各式各样好看的代码图片。

3、[Gource](https://gource.io/)

<div align=center><img src="http://img.linqunshu.cn/gource.png"></div>

`Gource`是一个很好玩的可视化工具，可以针对Git的log进行分析并做可视化处理，将代码仓库的历史变成视频。

4、[FLATICON](https://www.flaticon.com/)

<div align=center><img src="http://img.linqunshu.cn/flaticon.png"></div>

FlatIcon是最大的免费ICON网站，提供了包括PNG, SVG, EPS, PSD以及BASE在内的64种格式。
<div>Icons made by <a href="https://www.flaticon.com/authors/freepik" title="Freepik">Freepik</a> from <a href="https://www.flaticon.com/" 		    title="Flaticon">www.flaticon.com</a> is licensed by <a href="http://creativecommons.org/licenses/by/3.0/" 		    title="Creative Commons BY 3.0" target="_blank">CC 3.0 BY</a></div>

# 其他推荐阅读

1、[阮一峰的个人主站](http://www.ruanyifeng.com/blog/)

<div align=center><img src="http://img.linqunshu.cn/ruanyifeng.png"></div>

比较喜欢看他的每周分享，也是建立本站每周分享的灵感来源。

2、[A股30年，历史的拐点和暗示](https://mp.weixin.qq.com/s/o-h93gAZ1umcrpp5Su8qdA)

<div align=center><img src="http://img.linqunshu.cn/2018aStock(1).png"></div>

从1990年到2018年A股的股价走势与重大事件图，读史使人明智，站在更长的时间跨度上，更能理解一些事件对资本市场的冲击力。

3、[如何破解汇率的密码](https://mp.weixin.qq.com/s/_ycvf_ZmSPvi1g7n--eo3Q)

文章从四个部分：`基础：汇率为什么如此重要`、`历史：中国三次汇率改革战`、`逻辑：管涛的汇率研究方法`、`姿势：普通人如何避开误区`来对人民币的汇率进行了非常有趣的阐述。

4、[商业计划书全攻略](https://mp.weixin.qq.com/s/llYxkXfh6F-K_Hrv9zvrXg)

5、[Amazon Moments：亚马逊通过优惠券等鼓励用户下载第三方应用](https://readhub.cn/topic/7KjDDTMkXTl)

<div align=center><img src="http://img.linqunshu.cn/moments.png"></div>

亚马逊于2月14日正式推出了新的应用奖励工具[Amazon Moments](https://developer.amazon.com/es/moments)，Amazon Moments的模式类似国内的趣头条：用户完成特定的目标，手机应用开发商、发行方会回馈以实体或虚拟商品，包括优惠券等。首批参与测试的公司包括游戏公司 FunPlus、《华盛顿邮报》、TikTok 等。供WeCrowds参考。

6、[宏观对冲交易员的交易体系总结：主流偏见、反身性与宏观交易](https://mp.weixin.qq.com/s/i3FxYAX0Gq7Wn4OAObSsaw)

文中有一些值得思考的观点，记录如下：
- 当个体偏见成为市场很多人共同具备的感知后，无论其是否“真实”，这种偏见就会成为重要的可以影响资产价格的因素之一。我把这些因素称之为“宏观因子”。这些宏观因子，有些可以量化，有些则无法量化。这些宏观因子之间的关系非常复杂，既有相互强化的，也有互相抵消的，有些因子与资产价格有关，有些则无关。辨识宏观因子以及他们之间的关系，是交易中最重要的工作之一。
- 文中建议对历史上的主要资产的价格运动进行复盘，比如浮动汇率体制和大通胀（1971.1~1981.1）、里根第一任期（1981.1~1985.2）等。