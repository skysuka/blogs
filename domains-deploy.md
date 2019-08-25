---
title: 如何使用一台服务器支持多个域名和站点
date: 2019-06-11 14:15:46
tags:
    - 技术向
    - 教程
---

# 背景

我在腾讯云有一台服务器，有两个域名和各自的网站：`linqunshu.cn`以及`molardata.com`，我想把这两个网站都部署在这一台云服务器上（节约前期成本）。

虽然可以使用`Tomcat`在不同的端口上部署网站，但是这种方式在访问时，还需要在网址的最后添加端口，非常不美观。当然也有不添加端口的方法，这篇博客就记录了实现的过程，通过`Nginx`的端口转发实现。

# 操作过程

- 在域名服务商对域名进行解析

添加`@`和`www`记录字段，记录值为服务器的ip地址。

- 设置`Nginx`的conf配置

在nginx.conf文件中（一般情况下是在/usr/sbin/nginx文件路径下，不确定Nginx位置的同学，可以命令行输入`whereis nginx`进行查询）的配置添加的信息如下（做配置改动前，建议复制一份作为备份）
```
// 添加以下内容
upstream linqunshu {
    server 127.0.0.1:3009;
}
upstream molardata {
    server 127.0.0.1:4000;
}
server {
    listen       80 default_server;
    listen       [::]:80 default_server;
    server_name  www.linqunshu.cn;
    root         /home/linqunshu.cn/www;
    location / {
    }
    error_page 404 /404.html;
        location = /40x.html {
    }
    error_page 500 502 503 504 /50x.html;
        location = /50x.html {
    }
}
server {
    listen       80;
    server_name  www.molardata.com molardata.com;
    root         /home/molardata.com;
    location / {
    }
    error_page 500 502 503 504 /50x.html;
        location = /50x.html {
    }
}
```

- 重启`Nginx`

先检查一下conf文件是否正确，在命令行里输入（Nginx的地址可能有差异）：
```
/usr/sbin/nginx -t
```

如果正常的话可以看到：
```
nginx: the configuration file /etc/nginx/nginx.conf syntax is ok
nginx: configuration file /etc/nginx/nginx.conf test is successful
```

确认配置正确后，可以重启`Nginx`：
```
/usr/sbin/nginx -s reload
```

- 其他细节

测试前可清除一下DNS缓存，如果是Mac系统，使用如下命令：
```
sudo dscacheutil -flushcache
```

# 参考资料

- https://www.jianshu.com/p/fc16f4914c02