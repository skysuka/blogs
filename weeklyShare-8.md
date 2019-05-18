---
title: 每周分享第8期
date: 2019-04-21 23:36:53
copyright: false
tags: 
    - 每周分享
---
>2019年4月21日第8期
记录这一周的见闻以及值得分享的内容，每周日晚更新。

# 见闻

1、[中国引力波探测「太极计划」正稳步推进](https://readhub.cn/topic/7LZBJSKs13B)

4 月 17 日至 18 日，香山科学会议聚焦中国空间引力波探测及国际协作联盟。据悉，由中国科学家提出的空间引力波探测**「太极计划」**，正按预期目标稳步推进并已取得重要进展。

2、[UC Bekeley发布一个低成本家居机器人](https://mp.weixin.qq.com/s/2fWdyzEvDqyN3Ll3mhz9-A)

<img src="http://img.linqunshu.cn/robot.png">

> 加州大学伯克利分校 Pieter Abbeel 教授今天在推特公开宣布了伯克利机器人学习实验室最新开发的机器人 BLUE。这款机器人的特点是低成本（不到 5000 美元）、基于 AI 控制，而且可以在非结构化的环境中执行人类熟悉的日常活动，比如，叠一条毛巾。点击此处查看[机器人主页](机器人主页见 http://rll.berkeley.edu/blue/)。

3、[能闻出帕金森病的超级嗅觉](https://mp.weixin.qq.com/s/1LDhfB2xZLYWhSU_Lreyyw)

> 2015年，BBC的一篇报道让英国退休女护士乔伊·米恩尔（Joy Milne）家喻户晓。她在丈夫莱斯（Les）诊断出帕金森病疾病数年之前，就闻出了不同往常的味道。乔伊的这项“超能力”已经获得了科学家们的证实，并且有希望在未来开发出一种新型的诊断帕金森疾病的方式。在最近的研究中，英国曼彻斯特大学研究人员珀迪塔·巴伦（Perdita Barran）与库纳特、乔伊一起确定了导致帕金森气味的主要物质。

4、[D.E. Shaw进军中国市场](https://mp.weixin.qq.com/s/nMTd8-2-h9wKDs4iNRMBeA)

> 与很多华尔街的金融巨头不同，Shaw参与资本市场的目的不是为了翻涌市场波涛、做金钱的俘虏。按他自己的说法，他自始至终都将德劭集团看成自己的一个实验室，他更多的是把自己看成是科学家而非投资家。把投资金融市场作为科学实验的一部分，或许才是他最重要的投资理念。

> 其实德劭基金的成长过程也并不容易，1998年的俄罗斯债务危机一度给它带来重创。与其他众多对冲基金一样，德劭当时在固定收益类投资上蒙受巨额亏损，此后几年一直没有缓过来

5、[恢复死亡猪脑的脑循环](https://mp.weixin.qq.com/s/rXPzzVF_u88lRqJb7RLEIQ)

> 耶鲁大学医学院的神经科学家内纳德·塞斯坦（Nenad Sestan）团队研发了一套名为BrainEx的体外灌注系统，能让死亡数小时后的猪脑恢复脑循环和部分脑细胞功能，并维持至少6小时。

# 教程

1、[图解：从单个服务器扩展到百万用户的系统](https://mp.weixin.qq.com/s/wSCeO8QVYniMIGcBFDZyjw)

<img src="https://arcentry.com/blog/scaling-webapps-for-newbs-and-non-techies/lego-title-image.jpg">

> 你开发了一个网站（例如网上商店、社交网站或者其他任何东西），之后你把它发布到了网上，网站运行良好，每天有几百的访问量，能快速地相响应用户的请求。但是有一天，不知道什么原因，你的网站出名了！ 每分每秒都有成千上万的用户蜂拥而至，你的网站变得越来越慢……对你来讲，这是个好消息，但是对你的Web应用来说这是个坏消息。因为现在它需要扩展了，你的应用需要为全球用户提供7*24不宕机服务。 [原文链接](https://arcentry.com/blog/scaling-webapps-for-newbs-and-non-techies/)

2、[了解一点儿Serverless](https://mp.weixin.qq.com/s/XxJtEWtMnbq0sfHS7cEF1Q)

> 一个“函数”真的只做一件事情，并且不保持状态。 这样一来它可以轻松地被扩展到任意多的服务器/虚拟机/docker容器中去。请求多了就扩容，请求少了，就收缩，请求没了，就卸载，实在是太爽了。这种方式现在称为**Serverless**，并不是说没有服务器，而是说服务器对用户来说是透明的。 应用的装载、启动、卸载，路由是需要平台来搞定。

> Serverless的开发模式和运行模式类似这样：
> 1. 程序员编写完成业务的函数代码
> 2. 上传到支持Serverless的平台，设定触发的规则。
> 3. 请求到来，Serverless平台根据触发规则加载函数，创建函数实例，运行
> 4. 如果请求比较多，会进行实例的扩展，如果请求较少，就进行实例的收缩
> 5. 如果无人访问，卸载函数实例

> 但是，Serverless使得所有想持久化的东西必须得保存到外部的系统或者存储中，例如Redis，MySQL等。 很明显，这些东西也应该以“服务”的方式来呈现，即Backend as a Service (BaaS)。Serverless更适合那些无状态的应用，例如图像和视频的加工，转换， 物联网设备状态的信息处理等等。

3、[前端九部 - 入门者手册2019](https://www.yuque.com/fe9/basic)

九部成员合著的web前端开发零基础入门手册。

4、[什么是比特币](https://book.8btc.com/books/6/masterbitcoin2cn/_book/ch01.html)

5、[秒懂Java注解（Annotation）](https://blog.csdn.net/briblue/article/details/73824058)

6、[基于Netty自己动手实现RPC框架](https://zhuanlan.zhihu.com/p/35720383)

> 使用netty作为原料，fastjson序列化工具作为调料，来实现一个极简的多线程RPC服务框架。

7、[每天阅读一个npm模块](https://github.com/parro-it/awesome-micro-npm-packages)

8、[awesome](https://github.com/sindresorhus/awesome)

>  Github repo. Awesome lists about all kinds of interesting topics.

9、[狼叔：如何正确的学习Node.js](https://cnodejs.org/topic/5ab3166be7b166bb7b9eccf7)

10、[Pattern: Service Mesh](http://philcalcado.com/2017/08/03/pattern_service_mesh.html)

11、[如何优雅地合并多个 Commit](https://github.com/Jisuanke/tech-exp/issues/13)

12、[Java Core Sprout](https://crossoverjie.top/JCSprout/#/)

> 处于萌芽阶段的 Java 核心知识库

# 工具
1、[Framework7](https://github.com/framework7io/framework7/)

<img src="http://img.linqunshu.cn/framework7.png">

Full Featured Mobile HTML Framework For Building iOS & Android Apps.

2、[IONIC](https://ionicframework.com/)

Built on standard web technology, teams use Ionic to build beautiful cross-platform hybrid apps in a fraction of the time.


# 推荐阅读

1、[如果把中国422位皇帝放在一个群里，他们会聊些什么？](https://mp.weixin.qq.com/s?__biz=MzA5MjAyNTM3MQ==&mid=2650036374&idx=1&sn=ab3ce2b813fbac368022b7d7f24bf7c3&key=0c5bd8d37f1782936165bcb579c117833b2164d722817869fd4c6d56ccc989b38032ff79fc6a3ffbd35ad1b48769447c3dac3e092b7b8f4b2ba677ce2653a9d94f4c949dae0fedb0f7d9abd1b1663ffb&ascene=1&uin=MTk4OTE4ODkzNQ%3D%3D&devicetype=Windows+10&version=62060739&lang=zh_CN&pass_ticket=2BghQwQimwAzEEpM29oKIaXjAqn%2BCAaYvMKsjFudld%2BFTRGCXJ9cN5e1BV2LD1dY)

> 从秦始皇开始，到清朝最后一任皇帝溥仪，在2000多年的时间里，中国总共出现了422位皇帝。那么，一个脑洞大开的问题来了。如果把422位皇帝全部拉入一个微信群，他们会聊些什么呢？


2、[马云谈996](https://mp.weixin.qq.com/s/oc0NugBjpsn1_mBtbib2Lg)

文章发表之后的几天引起了超强的争议。

3、[通宵发布](https://mp.weixin.qq.com/s/JzAj4kIFu6PFjeQ0Tt2L3g)

蛮有趣的一篇关于程序员通宵发布的小文章，从19:30到5:30，记录了不同岗位上程序员的当晚的职责和心路历程。

4、[哈啰逆袭前夜：蚂蚁入场前的365天](https://mp.weixin.qq.com/s/3Q74XOnzoDXdhnwXyzyyNw)

> 众所周知，共享单车最大的反转是摩拜卖了，小黄黄了，哈啰单车（如今已更名“哈啰出行”）的市场占有率却反升至第一。

> 当所有人都在从产业和外围思考哈啰逆袭这个教科书式小胜局的时候，我们试图从内因去还原这个团队在合伙与组织角度的取胜原因：当你试图以少胜多、后来居上的时候，你背后的兄弟们，到底能不能支撑你赢这一场？

5、[用友研究院院长阿朱:中国企业服务产业洞察](https://mp.weixin.qq.com/s/plvsOcu78qIMwb86lIbq8A)

> Salesforce 有所不同，它既不收取服务费，也不用企业购买服务器、操作系统和数据库等，只需要企业按年度订阅。另外，Salesforce 可以实现**在线试用、支付和续费全打通**，而且因为绑定了**企业信用卡**，Salesforce 的**续费是自动**的。如果中国的 SaaS 平台能做到这样，那就离爆发不远了。我们知道，在中国实现续费是件很困难的事，因为涉及企业报销，而开发票就有一个复杂的审批流程，如果不自动续费，就很容易导致用户流失、续费率低的现象。

6、[聊聊创业初期的技术选择](https://mp.weixin.qq.com/s/XefJmnFnge-L1LvmyNilOA)

> 我公司曾经拓展过一项外包业务，帮助硅谷没有技术能力的创业团队，在1个月内以3万美元不到的价格快速打造Web、移动Web、App以及对应的Web管理平台，使得他们能够从较为困难的天使融资阶段快速进入Pre-A阶段并进一步拿到A轮融资，这项业务的背后其实是小型创业团队在创业初期面临的一个重要问题：如何选择合适的技术来优化、助推创业过程。

> 首选我有一个观点，创业成功有了融资以后，引入更为高级的技术专家，可能会对技术架构进行通盘重构，所以创业初期与后期的技术架构会大相径庭，事实上大部分成功的创业项目都会经历重大重构，因此，在创业初期选择技术架构的时候，更多要考虑的事情是简单便捷、快速开发，而不需要过多的考虑技术长久和技术扩展。

7、[郭台铭：台湾一代人的缩影](https://mp.weixin.qq.com/s/MdMzot12_1Mpw8S8M1As2Q)

8、[15年缠斗，亚马逊如何一步步败给它的中国电商门徒？](https://mp.weixin.qq.com/s/6He5mZnrTAsxFBKNGEY6Uw)

> 2004年，亚马逊年销售额已经达到70亿美元，而同时间段淘宝的年销售额仅有10亿元人民币，当当、京东更分别仅有淘宝的十分之一和百分之一。这个年代，海外互联网巨头们还是中国企业高山仰止的对象，**从大洋彼岸传回的每一个新鲜的创意都能在国内找到多个模仿者**。

> 进入中国市场后，亚马逊反而放慢了进击的脚步，在今天看来，这样的缓慢有些让人难以想象。亚马逊在收购卓越长达一年之后，才开始启用亚马逊的数据库系统替代卓越网以前的系统，这一替换过程又历经三年时间。而直到2007年6月5日，卓越才改名为“卓越亚马逊”，其域名joyo.com改为amazon.cn。

> 亚马逊中国的不同高管在不同场合均多次表示“用户体验”才是他们关注的第一目标，时任亚马逊中国总裁王汉华就曾表示：亚马逊天天平价，不参加价格战。但是，但在一个百废待兴的市场上，生存才是第一动力，“用户体验”？那是活下去之后才去考虑的东西。在中国当时的电商环境中，武器有且只有一个：低价，而且是低到亏本的低价。

> 尽管亚马逊中国的网站设计受到很多用户质疑，但其实在电子商务诞生初期，亚马逊的网站设计几乎是全球所有电商网站的典范。典型的例子如“一键下单”，这是1999年时亚马逊申请的成为公司标志性产品的专利设计，可以让用户绕过非常繁琐的在线购物过程（该专利已于2017年9月到期），几乎所有电商公司都（不得不）从亚马逊购买许可后才能使用类似功能；还有商品购买之后对消费者进行进一步的推荐，即类似“猜你喜欢”模块，最初也来自亚马逊的推荐系统。

9、[What are Cloud Computing Services [IaaS, CaaS, PaaS, FaaS, SaaS]](https://medium.com/@nnilesh7756/what-are-cloud-computing-services-iaas-caas-paas-faas-saas-ac0f6022d36e)

10、[Web 研发模式演变](https://github.com/lifesinger/blog/issues/184)

蛮早的一篇文章，玉伯写于2014年，不过能非常清晰的看懂Web技术演变的历史过程。

> 历史有时候会打转，咋一看以为是回去了，实际上是螺旋转了一圈，站在了一个新的起点。

