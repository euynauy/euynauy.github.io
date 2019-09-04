---
title: 没有软路由，Mi Box S照样能看Netflix、Youtube
date: 2019-09-04 10:50:50
tags: 
- Mi Box S
- 电视盒子
categories: 
- 电视盒子
- Mi Box S
---

咸鱼买的Mi Box S到啦！

卖家貌似是从美国沃尔玛海淘的，460包邮，比淘宝便宜。

我本来也想海淘，可它半天不打折，不想等了。

# 为啥选择它？

一、原生AndroidTV、Netflix 4K和Youtube 4K支持

二、配置尚可

三、Nvidia Shield TV贵，游戏功能无用

# 外观

网上照片太多了，我就拍个外包装好了。

<!--more-->

![IMG_0322.JPG](https://i.loli.net/2019/09/04/LVERwplsAuf9ibP.jpg)

# 家里没有实现路由器科学上网，怎么办？

因为家里还没有软路由，所以没法实现路由器科学上网。而且连接wifi后使用代理设置居然保存不了（有知道的大佬说下原因），无奈只能另辟蹊径，使用adb安装了[MiXplorer](https://forum.xda-developers.com/showpost.php?p=23109280&postcount=2)和[Shadowsocks  for Android TV](https://github.com/shadowsocks/shadowsocks-android/releases)实现Mi Box S科学上网。

## 一、adb连接Mi Box S并安装apk

1.前往Android开发[官方网站](https://developer.android.com/studio/releases/platform-tools.html)，下载到最新的Android platform-tools

2.打开Mi Box S开发者选项，并开启usb调试

3.将Mi Box S与要运行 adb 的电脑连接到同一个局域网，比如连到同一个 WiFi。

4.cmd进入Android platform-tools目录

5.`adb connect <miboxs的ip地址>:5555`，在Mi Box S上确认连接，使用`adb devices`确认连接状态

![TIM截图20190904184607.png](https://i.loli.net/2019/09/04/v3fDrB7yX1GoRtV.png)

![IMG_0335.JPG](https://i.loli.net/2019/09/04/usVEMO62pwY98ie.jpg)

7.将要安装的apk文件放在Android platform-tools目录下

![TIM截图20190904184856.png](https://i.loli.net/2019/09/04/eUbFQwc68XMyBij.png)

8.`adb install 文件名.apk`

![IMG_0338.JPG](https://i.loli.net/2019/09/04/1TFhmyvkwXCQH3j.jpg)

<center>打开应用即可看到安装的软件</center>


## 二、Shadowsocks tv设置

1.将PC端Shadowsocks目录中的gui-config.json拷贝到U盘

![TIM截图20190904185813.png](https://i.loli.net/2019/09/04/SNmK6kE3OfoDplZ.png)

2.关闭USB调试，插入U盘

![IMG_0336.JPG](https://i.loli.net/2019/09/04/XKVhFJs9Evati6k.jpg)

3.打开Shadowsocks tv，选择从文件中替换，使用MiXplorer，导入gui-config.json

![IMG_0339.JPG](https://i.loli.net/2019/09/04/QlZ9jKURydprGBN.jpg)

![IMG_0341.JPG](https://i.loli.net/2019/09/04/1QrkjMV3Z5CwRKG.jpg)

![IMG_0342.JPG](https://i.loli.net/2019/09/04/3I749CkPsKdoyBf.jpg)

4.选择节点连接，Mi Box S成功科学上网，然后登陆谷歌账号，更新软件。

![IMG_0343.JPG](https://i.loli.net/2019/09/04/jioqBXtahGS4Jev.jpg)

# 大功告成

![IMG_0344.JPG](https://i.loli.net/2019/09/04/uG267ji8DdPo4YJ.jpg)

![IMG_0346.JPG](https://i.loli.net/2019/09/04/GX2HADxzPdZ8k19.jpg)

![IMG_0347.JPG](https://i.loli.net/2019/09/04/fl4AzOWeY1iRHtJ.jpg)

<center>Netflix</center>


![IMG_0345.JPG](https://i.loli.net/2019/09/04/VD2ezNZQkTF8d5p.jpg)

<center>Youtube 4K</center>


# Enjoy it!

