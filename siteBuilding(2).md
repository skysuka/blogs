---
title: '搭建个人主站教程（下）'
date: 2018-10-13 12:10:08
tags:
    - 教程
    - 个人主站
---

这是建站的第二篇教程博客，主要介绍一些让主站建设更加`professional`的方法或工具。

# 建站框架
## 使用Hexo搭建个人主站
Hexo是一个快速简单强大的博客框架，基于Node.js。这节将介绍在一台CentOS云服务器上部署基于Hexo的博客站点。
先来对Hexo如何实现静态博客的访问有个大概的了解：
>本地通过`hexo g`渲染博客的静态文件（将Sources文件夹内的markdown文件渲染为静态的HTML文件，存储在Public文件夹中，然后通过`hexo d`把静态文件push到服务器上创建的git仓库，服务器上的git仓库通过git-hooks自动将仓库内的文件checkout到网站所在的根目录，通过设置Nginx的配置可以使得用户访问网站。
### 本地环境搭建
#### 安装`Nodejs`, `hexo-cli`
#### 初始化Hexo博客

```
npm install hexo-cli -g // 安装hexo-cli
hexo init // 初始化hexo文件夹
npm install // 安装Hexo的扩展插件
npm install hexo-deployer-git --save // 用于Git自动部署
npm install hexo-server --save // 用于本地服务器
```

#### 新建第一篇博客

```
hexo new "my first blog"
hexo g && hexo s // 本地起服务
```
打开http://localhost:4000，可以看到如下界面：
<div align=center><img src="http://img.linqunshu.cn/blog2_2.jpg"></div>
<center>图1.Hexo博客界面</center>

#### 更换博客主题（可选操作）

Hexo官网上提供了非常多的用户提交的theme，以使用NexT主题为例，打开terminal，cd到hexo目录的theme文件夹下，下载NexT主题，再将_config.yml中的theme改为`hexo-theme-next`即可。

```
git clone https://github.com/theme-next/hexo-theme-next.git
```
<div align=center><img src="http://img.linqunshu.cn/blog2_3.png"></div>
<center>图2.Hexo博客界面更换为NexT主题</center>

### 服务器端环境搭建

#### 安装Nginx Node.js

```
yum -y update // 首先进行服务端的系统更新
yum install -y nginx nodejs
nginx // 启动nginx服务器
```
<div align=center><img src="http://img.linqunshu.cn/blog2_4.png"></div>
<center>图3.Nginx测试页面</center>

**注意：**浏览器输入服务器的ip地址可能不一定会出现图3的测试页面，这种无法打开的现象可能是因为云主机的安全组没有设置80端口（Nginx的默认监听端口为80），也有可能是云主机的防火墙的原因，其中关闭防火墙的指令如下：

```
systemctl stop firewalld.service // 关闭防火墙
```
虽然这样可以解决问题，但是安全风险比较大，我们可以通过以下方式进行设置：

```
systemctl restart firewalld.service // 打开刚才关闭的防火墙
firewall-cmd --zone=public --add-port=80/tcp --permanent // 添加80端口
systemctl restart firewalld.service // 重启防火墙使设置生效
```
#### 创建仓库
在云服务器上创建git仓库，注意`--bare`参数，之所以要使用bare，可以[参考这篇回答](https://segmentfault.com/q/1010000004683286)。
```
cd /home/linqunshu.cn
mkdir blog.git && cd blog.git
git init --bare
```
#### 修改本地Hexo配置
修改本地Hexo目录下的`_config.yml`文件，其中`xxx.xxx.xxx.xxx`是云主机的地址，`/home/linqunshu.cn/blog.git`是上一步创建的云主机上的git仓库，`master`是分支
```
deploy:
  type: git
  repo: root@xxx.xxx.xxx.xxx:/home/linqunshu.cn/blog.git
  branch: master
```

#### 自动部署
在本地执行`hexo g -d`命令之后，还只是将本地的HTML等静态文件提交到云主机的git仓库中，我们还需要将云主机git仓库中的文件自动拷贝到网站所在的根目录中，我们可以设置git仓库中`git hooks`来实现这一自动化的部署。
```
cd /home/linqunshu.cn/blog.git/hooks
touch post-receive
vim post-receive
```
然后输入以下脚本即可：
```
#!/bin/sh
git --work-tree=/home/linqunshu.cn/www --git-dir=/home/linqunshu.cn/blog.git checkout -f 
```
更改目录权限：
```
chmod +x post-receive // 执行权限
```

#### 配置Nginx服务器

```
vim /etc/nginx/nginx.conf
// 按图4修改nginx配置
nginx -s reload // 修改配置后重新加载生效
```
打开nginx.conf后，按照个人需求修改下面的设置，server_name为网址，root为网站所在的根目录。
<div align=center><img src="http://img.linqunshu.cn/blog2_1.jpg"></div>
<center>图4.编辑Nginx配置</center>

### 部署博客
```
hexo clean && hexo g -d
```

# 页面美化
## 页面插入BGM
两种用于插入BGM的HTML Music Codes

```
<audio src="./music/falicity.mp3" controls>	
<p>Fallback content goes here.</p>
</audio>
```
或者

```
<embed name="" src="./music/falicity.mp3" loop="false" hidden="true" autostart="true">
```
需要在不同的浏览器上测试。