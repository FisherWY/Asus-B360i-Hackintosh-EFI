# Hackintosh EFI

Click here to [README_EN](./README_EN.md)

### 我安装的MacOS版本：

+ macOS High Sierra 10.13.6(17G65)

### 我的电脑配置：

+ 主板：Asus Rog Strix B360i
+ CPU：Intel Core i5-8500
+ 显卡：Nvidia GeForce GTX 1060 3GB
+ 内存：Crucial By Micron DDR4 2666 8GB + US Corsair DDR4 3000 8GB (Bios设置运行在2666MHz)
+ 硬盘：Asgard AN2 Nvme 250GB



### 关于"OpenCore_EFI_202104"(2021-04)

从这一版本开始，EFI由原先的Clover更换为OpenCore。这一版本的EFI去除了许多已经弃用的驱动，更新了必要的驱动，添加了Intel AC9560的Wi-Fi和蓝牙驱动，使得黑苹果更接近于完美。目前尚存在的一个问题就是：睡眠后一段时间会自动唤醒，初步怀疑是无线网卡导致的唤醒，这个问题产生的原因仍有待确认。如果你找到了这个问题的解决方法，请告诉我。关于这一次迁移的过程，我也记录在了我的博客中，如果你也想从Clover迁移到OpenCore，可以参考一下我的迁移过程，点击[这里](https://fisher.lazybone.xyz/%E4%BB%8Eclover%E8%BF%81%E7%A7%BB%E5%88%B0opencore.html)查看我的博客。

注意：这个EFI并没有去除我的机型配置，请根据自己的机型更换这一部分的配置。



### 关于"完美EFI_202104"(2021-04)

这一版本的EFI基于2019-11版本的EFI，更新了部分驱动，添加了Intel AC 9560无线网卡和蓝牙的驱动(itlwn和IntelBluetoothFirmware)，但该驱动在Clover下需要强制加载，出于对系统最少注入的原则，我已将Clover Bootloader更换为更新的OpenCore。因此本EFI将会是Clover的最后一个EFI，以后不会再更新。



### 关于"完美EFI_201911"(2019-11)

"完美EFI_201911"是我在研究了一个星期后自己尝试配置的，根据自己的硬件添加相应的驱动。没想到一次配置就完美成功了，感谢驱动的开发者和教程的作者！许多驱动跟2019年3月份相比，都精简、稳定了很多。这一次的黑苹果安装配置过程记录在了我的博客中 -> [标签：Hackintosh | Fisher's Blog](http://fisher.lazybone.xyz/tags/hackintosh/)

1. 我在第一次安装的时候遇到了一次卡在了`PTIsensors:started`，但是重启之后就没有问题了，可能是我太急了😂
2. 接下来的系统安装遇到了`应用程序副本已损坏，不能用来安装macOS`的问题，这个问题通过断网和修改系统时间解决
3. 剩下的安装显卡驱动都没有遇到过任何的问题，我记得之前2019年3月份装驱动的时候会报错

##### 测试情况：

- 显卡 -> 正常工作
- 板载有线网卡 -> 正常工作
- 声卡 -> 正常工作
- 睡眠唤醒 -> 正常
- CPU睿频 -> 正常
- 关机 -> 正常
- USB3.0 & USB3.1 -> 正常

##### 可解决的问题：

+ 无线网卡 -> Intel AC 9560无线网卡无相关驱动，这个问题已有itlwm作为解决方法，但在Clover下需要强制驱动



### 关于"基本完美EFI_201903"(2019-03)

"基本完美EFI_201903"是2019年3月份的时候用机械硬盘装Hackintosh使用的EFI，在安装使用过程中没有任何问题

##### 测试情况：

- 显卡 -> 正常工作
- 板载有线网卡 -> 正常工作
- 声卡 -> 正常工作
- 睡眠唤醒 -> 未测试过，不清楚是否正常工作
- CPU睿频 -> 未测试过，不清楚是否正常工作

##### 可解决的问题：

+ 无线网卡 -> Intel AC 9560无线网卡无相关驱动，这个问题已有itlwm作为解决方法，但在Clover下需要强制驱动



### 关于"GitHub_CLOVER(i5-8500_B360_1060)"(2019-03)

"GitHub_CLOVER(i5-8500_B360_1060)"是2019年3月在 https://github.com/sqlsec/clover 这个仓库中提供的，目前该仓库中已经没有这份EFI了。

我在使用的过程中能够正常引导开机，但是安装过程中貌似会卡在啰嗦模式

##### 可解决的问题：

+ 无法关机 -> 后来查到是`config.plist`的配置问题，需要勾选**修复关机**
+ 声卡无法正常工作 -> 怀疑是config.plist配置或驱动问题，最后通过这个帖子解决了问题:  https://hackintosher.com/guides/fix-asus-supremefx-s1220a-hackintosh-audio/
+ 板载网卡无法正常工作 -> 应该是内置的网卡驱动不是最新版本，更换驱动后问题解决
+ 无线网卡 -> Intel AC 9560无线网卡无相关驱动，这个问题已有itlwm作为解决方法，但在Clover下需要强制驱动
