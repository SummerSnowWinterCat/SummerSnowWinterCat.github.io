---
layout: post
title: "RaspberryPiZERO VNC and WIFI Config「Windows」"
date: 2018-09-18 20:10:10 +0900
categories:
---

# About raspberrypi zero VNC Connection

    1.Download Win32 DiskManager 
    
    2.Download SD CARD Formatter
    
    3.Download RASPBIAN 
        version:
    ​	    <raspbian desktop or raspbian lite>
                    desktop or command line 
    ​	            桌面版(GUI)和命令行
    
    4.SD Card Formatter (Formatter TF Card and Use the DiskManager)
    4.1.SD CARD FORMATTER 对TF卡进行格式化后，使用WIN32 DiskManager进行写入
    
    5.Then find goto Boot File Root
       5.0.写入完成后 打开BOOT 进入根目录
    ​5.1.Create a new ssh file
       5.1.0.创建一个空的ssh文件 无后缀    
    ​	5.2.Create wpa_supplicant.conf file open with text_editor
          5.2.0创建 wpa_supplicant.conf 文件 并用记事本编辑.
        Create...
    ​	>>>写入
        
            ```
            country=JP // Gobal Location
                ctrl_interface=DIR=/var/run/wpa_supplicant GROUP=netdev
                update_config=1
            
                network={
                    ssid="wifi ssid"
                    psk="wifi password"
                    key_mgmt=WPA-PSK
                    priority=1
                }
            ```

         5.3.保存并将TF卡插入RASPBERRY PI ZERO中
    6.接通电源后 即可利用VNC或PuTTY进行连接
    
    ​6.1.raspberry pi zero的初始用户名为 pi 密码为 raspberrypi
    
    7.download putty and advanced ip scanner
    
    8.打开advanced ip scanner 进行wifi段搜索 找到raspberrypi并复制ip地址
    
    9.打开putty HostName 写入 raspberrypi.local 
    
    ​9.1.端口不变（22）
    
    10.连接完毕！

