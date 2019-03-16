# Hackintosh EFI

#### 我安装的MacOS版本：
+ macOS High Sierra 10.13.6(17G65)

#### 我的电脑配置：
+ 主板：Asus Rog Strix B360i
+ CPU：i5-8500
+ 显卡：Nvidia GeForce GTX 1060 3GB
+ 内存：Crucial By Micron DDR4 2666 8GB
+ 硬盘：一个很老的来自惠普的希捷120g拆机硬盘
    
#### 使用“基本完美EFI”中的EFI在安装使用过程中没有任何问题，显卡正常工作，板载有线网卡正常工作，声卡正常工作。

#### 存在的问题：
+ 无线网卡无驱动 --> Intel AC 9560无线网卡无相关驱动，这个问题目前无解

## -----------------------------------------分割线-----------------------------------------

### 关于"GitHub_CLOVER(i5-8500_B360_1060).zip" --> 这个EFI是在 https://github.com/sqlsec/clover 这个仓库中找的，我在使用的过程中能够正常引导开机

#### 存在的问题：
+ 无法关机，因此不能用于安装系统。
+ 声卡无法正常工作 --> 怀疑是config.plist配置问题，我通过这个帖子解决了问题 https://hackintosher.com/guides/fix-asus-supremefx-s1220a-hackintosh-audio/
+ 网卡无法正常工作 --> 应该是内置的网卡驱动不是最新的V2.4版本，不支持Intel AC 9560。

## -----------------------------------------English-----------------------------------------

#### MacOS version I install:
+ macOS High Sierra 10.13.6(17G65)

#### My PC configuration:
+ MotherBoard: Asus Rog Strix B360i
+ CPU: i5-8500
+ Graphics card: Nvidia GeForce GTX 1060 3GB
+ RAM: Crucial By Micron DDR4 2666 8GB
+ Hard Disk: an old disassemble Seagate hard disk from my HP laptop

#### Use EFI in "基本完美EFI" without any problems during the installation and use, the graphics card, onboard wired network card, sound card is good

#### Problems using EFI "基本完美EFI":
+ Wireless network card didn't work --> Intel AC 9560 no relevant driver, this problem can't be sloved until now

## ------------------------------------Dividing line-----------------------------------

#### About "GitHub_CLOVER(i5-8500_B360_1060).zip" --> This EFI was found in https://github.com/sqlsec/clover repository, I can boot normally during the process of using it.

#### Problems using EFI "GitHub_CLOVER(i5-8500_B360_1060).zip":
+ Unable to shotdown, so that EFI can't use to install system
+ Sound card is not working properly --> Suspected to be a config.plist configuration issue, I solve it via https://hackintosher.com/guides/fix-asus-supremefx-s1220a-hackintosh-audio/
+ NIC is not working properly --> Should be built-in NIC driver is not the latest V2.4 version, does not support Intel AC 9560

