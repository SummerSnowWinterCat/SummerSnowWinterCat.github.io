---
layout: post
title: "RaspberryPiZERO VNC and WIFI Config"
date: 2018-09-18 20:10:10 +0900
categories:
---

# About raspberrypi zero VNC Connection

    1.下载Win32 DiskManager 
    
    2.下载SD CARD Formatter
    
    3.下载RASPBIAN 
    
    ​	raspbian desktop or raspbian lite
    
    ​	命令行版和桌面版(GUI)
    
    4.SD CARD FORMATTER 对TF卡进行格式化后，使用WIN32 DiskManager进行写入
    
    5.写入完成后 打开BOOT 进入根目录

    ​	创建一个空的ssh文件 无后缀
    
    ​	创建 wpa_supplicant.conf 文件 并用记事本编辑.
    
    ​	写入
        
            ```
            country=JP // 地区
                ctrl_interface=DIR=/var/run/wpa_supplicant GROUP=netdev
                update_config=1
            
                network={
                    ssid="wifi的名字"
                    psk="wifi的密码"
                    key_mgmt=WPA-PSK
                    priority=1
                }
            ```

         保存并将TF卡插入RASPBERRY PI ZERO中
    6.接通电源后 即可利用VNC或PuTTY进行连接
    
    ​6.1.raspberry pi zero的初始用户名为 pi 密码为 raspberrypi
    
    7.download putty and advanced ip scanner
    
    8.打开advanced ip scanner 进行wifi段搜索 找到raspberrypi并复制ip地址
    
    9.打开putty HostName 写入 raspberrypi.local 
    
    ​9.1.端口不变（22）
    
    10.连接完毕！

