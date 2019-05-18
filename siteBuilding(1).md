---
title: '搭建个人主站教程（上）'
date: 2018-10-13 11:10:08
tags:
    - 教程
    - 个人主站
---
本站的第一篇博客的话，就来讲一下是如何建站的吧。教程分为两期，第一期（也就是本篇博客）主要介绍一下如何从购买域名和服务器开始，搭建最简单的个人主站。之后会再出一期教程，介绍如何让自己的主站变得更加professional~


# 域名与主机购买
之前有使用过`github的page服务`来搭建个人主站，应该是最经济实惠搭建主站的方法了，投入成本为0，但是这样的网站对于国内访问者速度太慢了，所以之后尝试coding.net上的page服务，国内用户访问起来速度会更快一些。但是通过page服务建立的主站，访问的地址比如说是这样的`linqunshu.github.io`，但是我希望是这样的url: `linqunshu.cn`，那么就需要自己购买域名和主机了。

购买域名的网站有很多，我在腾讯云上和GoDaddy上都有购买过域名，在国外的网站上（比如GoDaddy）购买域名，相比于在国内的网站上（比如腾讯云）购买，最大的好处在于搭网站不用备案这个域名，会方便很多，但是要注意如果主机买的也是国内的话，也还是要备案的，所以在买主机的时候，也可以考虑买国外的服务器，比如搬瓦工的主机，顺便解决科学上网的需求。



<div align=center><img src="http://img.linqunshu.cn/blog1_1.jpg"/></div>
<center>图1.在购买域名前需要先看看自己心仪的域名是否已经被占用</center>

# 服务器环境搭建
买好域名和主机之后，我们可以开始在主机上搭建http服务器了，这里介绍使用`Tomcat`来搭建服务器，Tomcat服务器是一个免费的开放源代码的Web应用服务器，属于`轻量级应用服务器`，在中小型系统和并发访问用户不是很多的场合下被普遍使用，挺适合我们当前的应用场景。[附上Tomcat的下载链接](https://tomcat.apache.org/download-80.cgi)，因为我的服务器上的系统是centos，所以下载的是core下面的tar.gz包。除了需要下载Tomcat之外，还需要下载JDK，[附上JDK下载链接](https://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)，因为Tomcat服务器在收到请求时，需要调用JDK来编译JAVA程序。(大家在下载JDK的时候可能会发现真的是有好多版本，而且版本的命名之间好像跨度也很大，关于版本的一些概念可以参考这篇文章： [浅谈Java SE新版本发布线路图](https://www.jianshu.com/p/8df06dc8c1e6) )

<div align=center><img src="http://img.linqunshu.cn/blog1_2.jpg"/></div>
<center>图2.将Tomcat和JDK上传至服务器</center>


为了能让Tomcat知道JDK被安装在了什么位置，我们需要对/etc/profile进行配置，这个文件是存储linux上环境变量用的，在/etc/profile文件里的末尾添加上以下内容（具体路径根据实际情况做改变）：
```
export JAVA_HOME=/home/web/jdk1.8 
export JRE_HOME=${JAVA_HOME}/jre
export CLASSPATH=.:${JAVA_HOME}/lib:${JRE_HOME}/lib:$CLASSPATH
export JAVA_PATH=${JAVA_HOME}/bin:${JRE_HOME}/bin
export PATH=$PATH:${JAVA_PATH}
export CATALINA_HOME=/home/web/tomcat8.0.53
```
配置完成后，需要执行：
```
source /etc/profile
```
这样操作可以在不重启计算机的情况下使profile立刻生效，之后启动Tomcat服务即可：
```
cd /home/web/tomcat8.0.53/bin/
sh startup.sh
```
如果需要重启Tomcat服务器：
```
sh shutdown.sh
sh startup.sh
```
这样在浏览器里输入`你的服务器IP地址:8080`就可以看到这样的初始界面了：


<div align=center><img src="http://img.linqunshu.cn/blog1_3.jpg"></div>
<center>图3.初始界面</center>

但是如果总是输入`www.linqunshu.cn:8080`就比较麻烦了，如果要简化成`www.linqunshu.cn`，需要对Tomcat的一些配置进行更改。打开/home/web/tomcat8.0.53/conf/下的server.xml配置文件，将以下内容：
```
<Connector port="8080" protocol="HTTP/1.1"
            connectionTimeout="20000"
            redirectPort="8443" />
```
修改为：
```
<Connector port="80" protocol="HTTP/1.1"
            connectionTimeout="20000"
            redirectPort="8443" />
```
之后重启Tomcat服务器即可。


# 后续内容
将自己写好的个人主站的html文件（比如CV）传到服务器的`/home/web/tomcat8.0.53/webapp`文件夹下，重新启动Tomcat服务器，就可以通过访问`www.linqunshu.com/CV`看到自己的主页啦！如果觉得加上'/CV'不够简短，可以通过在server.xml中在`<host>`与`</host>`之间添加以下内容即可：
```
<Context path="" docBase="/CV" debug="0" reloadable="true"/>
```
但是是不是有更优雅的搭建博客，发布文章的方式呢？的确有很多方法，比如用`Hexo`，这些内容将会在下一篇文章中具体介绍~
