---
title: "docker报`permission deny`的解决办法"
date: "2022-09-29"
description: "docker error resolve"
tags: [
    "docker",
	"error",
]
---

问题描述：![](https://github.com/forest2code/blog/raw/master/img/dockererror.jpg)

原因：当前用户没有docker权限

解决办法1: 使用`sudo`命令

解决方法2: 将当前用户添加到docker组中

```
sudo groupadd docker			#添加docker用户组，这个用户组应该是已存在了
sudo gpasswd -a $USER docker	#将当前用户加入到docker用户组中
newgrp docker					#更新用户组docker

```
