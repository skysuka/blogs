---
title: 每周分享第2期
date: 2019-02-24 20:00:39
copyright: false
tags: 
    - 每周分享
---
>2019年2月24日第2期
记录这一周的见闻以及值得分享的内容，每周日晚更新。

# 见闻
1、[15亿参数！史上最强通用NLP模型诞生：狂揽7大数据集最佳纪录](https://mp.weixin.qq.com/s?__biz=MzI3MTA0MTk1MA==&mid=2652038485&idx=1&sn=e5623e1df705fca9cd72679a5210f094&chksm=f12191a4c65618b22662101f3c33aacb7ba308dde8041b41599163305e02bae5afd7094ba4b8&mpshare=1&scene=24&srcid=#rd)

<img height=300 src="http://img.linqunshu.cn/nlpopenai.png">

OpenAI在[官博](https://blog.openai.com/better-language-models/#fn1)介绍了他们训练的一个大规模无监督NLP模型，可以生成连贯的文本段落，刷新了7大数据集基准，并且能在无预训练的情况下，完成阅读理解、问答、机器翻译等多项不同的语言建模任务。OpenAI的这个NLP模型基于Transformer，拥有15亿参数，使用含有800万网页内容的数据集训练。

OpenAI并没有公布GPT-2模型及代码，只公布了一个仅含117M参数的样本模型及[代码](https://github.com/openai/gpt-2)，供有兴趣的研究人员学习和参考。不开源的这一举动也引起了圈内人士的剧烈讨论。

2、[创建知识图谱的成本有多高？](https://mp.weixin.qq.com/s?__biz=MzU2NjAxNDYwMg==&mid=2247485581&idx=1&sn=109f853b5e8aafb73ef6528da05c8eda&chksm=fcb3af68cbc4267efcbef4b32650e5f0be2709579b3b7473eb353b3511cff6687fa4127d2a36&mpshare=1&scene=24&srcid=#rd)

<img width=300 src="http://img.linqunshu.cn/triple.png">
<div>不同知识图谱的每个三元组成本与错误率之间的关系</div>

我们知道强大的深度模型需要很多计算力，那你知道创建一个知识图谱的成本到底是多少吗？德国 Mannheim 大学的研究者（[论文地址](http://ceur-ws.org/Vol-2180/ISWC_2018_Outrageous_Ideas_paper_10.pdf)）最近仔细估算了各种知识图谱每创建一条记录所需要的成本，他们表示对于大型知识图谱，手动创建一个三元组（即一条记录）的成本在 2 到 6 美元之间，总成本在数百万到数十亿美元之间。而自动创建知识图谱的成本要降低 15 到 250 倍（即一个三元组 1 美分到 15 美分），注意其中 15 美分每条的「自动化」知识图谱还是需要大量人力进行数据的验证。

3、[动车组中的“变形金刚”来了](https://mp.weixin.qq.com/s?__biz=MTI0MDU3NDYwMQ==&mid=2656742575&idx=1&sn=455726a21c7b7d5b5beb8ef0806a736d&chksm=7a6051494d17d85f8fe1cdf380dd519548139e2dc662b2dbc7606906ff9a00faeb93d2c3f9cf&mpshare=1&scene=1&srcid=&key=dbd73e96dc6e3e5ca311e35be8746311e50f1b08883375a536996bd7884e68d00c04d1520a6cd9c2d1603e0fe175b5ab08eec6a4a95478bee53d63e3f60941641d4b9eb69385abc4caecca5e901faccb&ascene=1&uin=MTk4OTE4ODkzNQ%3D%3D&devicetype=Windows+10&version=62060728&lang=zh_CN&pass_ticket=NTEglDWqr9d7Bz8pHwPTlJXd1Tp%2BH9Mn0sm0oPtEq41rs02UgoYf%2BIe5mztJ3scC)

<img width=300 src="http://img.linqunshu.cn/train2.png">

高速动车组诞生半个多世纪以来，普遍采用相对固定的编组方式。但铁路运输有客流淡旺季之分，春运期间和日常差别巨大。固定编组动车组不可拆编，不能增加车厢应付客流高峰，也不能减少车厢以减少支出或避免运力浪费，客流和运能常常形成瓶颈。

<img width=300 src="http://img.linqunshu.cn/train3.png">

<img width=300 src="http://img.linqunshu.cn/train1.png">

而现在亮相的可变编组动车组，被车迷们赞誉为动车组中的“变形金刚”。在可变编组动车组新车型中，双层二等座车、双层VIP车、双层餐货和客货合造车等均为双层结构。

可变编动车组将对多行业产生深远影响。大定员纵向卧铺车、双层座车和商务座车在载运能力上，比常规高速动车组分别增加50%、33%和70%，可在淡季增加票价浮动空间，在旺季大幅提升运力应对客流高峰。

# 教程

1、[在团队中使用GitLab中的Merge Request工作模式](http://blog.fwhyy.com/2018/06/Use-the-Merge-Request-working-mode-in-GitLab-in-the-team/)

2、[滴滴开源的跨端整体解决方案 chameleon](https://cmljs.org/doc/example/main.html)

<img src="http://img.linqunshu.cn/chameleon.png">

CML特点是“一端所见即多端所见”，你只需开发一次就能跑所有端。 跟随这个教程，开启你的chameleon跨端开发。

# 工具
1、[Uppy - 文件上传工具](https://github.com/transloadit/uppy)

<img src="https://github.com/transloadit/uppy/raw/master/assets/uppy-demo-oct-2018.gif">

一个基于 JavaScript 的文件上传工具，可无缝集成到任何应用。支持从本地磁盘、远程 urls、Google Drive、Dropbox、Instagram、snap 等位置上传文件，并在线预览编辑等功能。

2、[frontendDaily](https://github.com/kujian/frontendDaily)

<img src="http://img.linqunshu.cn/fedaily.png">

前端日报栏目数据来自码农头条，每日分享前端、移动开发、设计、资源和资讯等，为开发者提供动力。

3、[gotop](https://github.com/cjbassi/gotop)

<img width=600 src="https://github.com/cjbassi/gotop/raw/master/assets/demo.gif">

基于 Go 语言编写命令行活动监视器，挺酷炫的。


# 其他推荐阅读
1、[Siteinspire](https://www.siteinspire.com/)

<img src="http://img.linqunshu.cn/siteinspire.png">

收录了很多设计优秀的网站，可以汲取一下灵感。

2、[Designing in VR](https://www.cnet.com/roadshow/news/ford-virtual-reality-design-gravity-sketch/)

<img width=300 src="https://www.wangbase.com/blogimg/asset/201902/bg2019022207.jpg">

<img width=300 src="https://www.wangbase.com/blogimg/asset/201902/bg2019022208.jpg">

以前设计汽车，都是使用 CAD 软件。现在，福特汽车公司的工程师，开始使用 VR 软件，在虚拟空间里面设计汽车。这种方法的主要优点是，可以直接看到渲染后的内饰和外观。(摘自[阮一峰的每周分享](http://www.ruanyifeng.com/blog/2019/02/weekly-issue-44.html))

3、[HelloGitHub](https://github.com/521xueweihan/HelloGitHub)

分享 GitHub 上有趣、入门级的开源项目，帮你找到编程的乐趣。(摘自[阮一峰的每周分享](http://www.ruanyifeng.com/blog/2019/02/weekly-issue-44.html))

4、[知识图谱与深度学习优势互补，破解更多金融科技难题](https://mp.weixin.qq.com/s?__biz=MzIwMDAwNzAyOA==&mid=2651196519&idx=1&sn=512bc2867ea7ac74fba25adde2aa65ab&key=0c5bd8d37f17829390c7d0b1429c6232f155817eeab20b8a386f7b4a97674bc2f0b58172f4989019a459e77b8a283c1d5f9a860ac0c2d01b95e3d53fc01abd55d1c8925fa110ba12eae28bdf7cf56113&ascene=1&uin=MTk4OTE4ODkzNQ%3D%3D&devicetype=Windows+10&version=62060728&lang=zh_CN&pass_ticket=NTEglDWqr9d7Bz8pHwPTlJXd1Tp%2BH9Mn0sm0oPtEq41rs02UgoYf%2BIe5mztJ3scC)

知识图谱的早期理念来自于Web之父Tim Berners Lee于1998年提出的Semantic Web，最初理想是把基于文本链接的万维网转化成基于实体链接的语义网。深度学习的好处是用非监督式或半监督式的特征学习和分层特征提取高效算法来替代手工获取特征。将深度学习的方法融入知识图谱的应用中，是当下的研究热点之一。

陈华钧老师在该文中从`深度学习与知识图谱获取`，`表示学习与知识图谱推理`，`图神经网络与知识图谱`，`如何赋能金融`等四个方面展开了介绍，提供了一个比较全面的认识。在如何赋能金融方面，以量化投资为例，目前预测股票趋势的深度神经网络模型，虽然效果不错，但大多数具有两个共同的缺点：（1）当前方法对于股票趋势的突变不够敏感，（2）预测结果不能被人类解释。

为了解决这两个问题，“Knowledge-Driven Stock Trend Prediction and Explanation via Temporal Convolution Network”一文提出了一种新的知识驱动的时间卷积网络（KDTCN）模型，用于股票趋势预测和解释。首先，从财经新闻中提取结构化事件，并利用知识图谱引入外部知识来获取事件的向量表示。然后，将事件的向量表示和价格的数值向量表示结合起来预测股票趋势。通过评估预测准确性，来显示知识驱动的事件如何对股票趋势突变起作用。

实验证明，在股票趋势预测中加入知识驱动的事件，（1）可以提升整体的预测效果，对股票数据集当中的突变做出更快的反应，效果优于目前的最优方法；（2）基于知识图谱，将事件和事件之间的联系可视化，有助于对预测结果进行解释，特别是针对突变数据，这些解释以两种渐进的方式完成：一是可视化知识驱动的事件对突变预测结果的影响，二是将事件链接到外部的知识图谱来检索知识驱动的事件的背景知识。
