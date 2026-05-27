---
title: CentOS7安装宝塔面板的最新教程
published: 2026-05-28
pinned: true
description: CentOS7安装宝塔面板的最新教程
tags: [Linux,Docker]
category: 技术文章
draft: false
image: ./images/firefly2.avif
---

# CentOS7安装宝塔面板的最新教程
由于宝塔官方不支持旧版的centos7了，所以我们按照下面的步骤来操作，依次输入下面的代码
```linux
sudo cp -r /etc/yum.repos.d /etc/yum.repos.d.backup
sudo rm -rf /etc/yum.repos.d/*
sudo curl -o /etc/yum.repos.d/CentOS-Base.repo http://mirrors.aliyun.com/repo/Centos-7.repo
sudo yum clean all
sudo yum makecache
sudo yum repolist
url=https://download.bt.cn/install/install_panel.sh;if [ -f /usr/bin/curl ];then curl -sSO $url;else wget -O install_panel.sh $url;fi;bash install_panel.sh ed8484bec
```

如无意外执行到最后的代码就会进入到安装的步骤界面了。
