### Wulian MT7621 开发记录
---
**Data:** 07/23/2015 

1. 已经实现的功能: LED, GPIO, udisk;
2. 还未实现的功能: I2C RTC, SD, SATA, Button, ESATA, ETH, 2.4G/5G

**基本情况说明**

目前MT7621开发的基础代码来自MTK提供的 mtksdk-openwrt-3.10.14-20150311-d021c937.tar.bz2, 该SDK未使用DTS, 所以在配置方面不能按照标准OpenWrt的架构, 目前主要修改内核部分,编写SDK中未支持到的设备驱动.

07/23/2015 保存工作空间,开始其他工作,将未完成的功能以补丁的方式上传到git.

**补丁文件说明:**

> **0503-save-workspace-and-i2c-driver-is-still-WIP.patch** 内核中i2c总线及RTC的驱动补丁,目前测试i2c总线还有问题,故未放到 target/linux/ramips/patches/
> 
> **07-23-2015-save-workspace.patch** target/linux/ramips/mt7621/config-3.10的补丁,主要是配置了I2C及RTC.
---