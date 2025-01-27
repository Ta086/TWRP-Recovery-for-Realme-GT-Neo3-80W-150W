# TWRP Recovery for 真我GT Neo3 80W/150W
设备树：color597
编译：color597
适用版本：realme UI 5.0 | Android 14，将发布适用于多个内核版本的 TWRP，刷入之前请先确认当前版本的内核版本，避免刷错

注意事项：
1. 请严格按照“适用版本”的要求刷入
2. 该机型的 recovery ramdisk 位于 vendor_boot 中，故需要将此文件刷入 vendor_boot 分区，命令：fastboot flash vendor_boot xxx.img
3. 请勿使 vendor_dlkm 分区无法挂载，否则可能无法正常进入 recovery 模式
4. 刷入完成后，可通过长按音量 + 与电源键强制重启系统，若能正常开机，即能正常进入 recovery 模式，此操作有助于降低变砖几率。

正常工作的功能：
1. data 分区解密
2. MTP
3. OTG
4. Fastbootd
5. 振动调节

未经测试/不正常的功能：
1. 官方 OTA 固件刷入（官方提供的降级固件除外）

已知且非 TWRP 本身问题：
1. Magisk 安装包无法刷入（Magisk 安装程序误判未启用的 init_boot 分区，导致报错 Unsupported/Unknown image format，静等 Magisk 作者修复）

文件介绍：
1. 若当前系统版本的内核版本为 5.10.168，请刷入带有 5.10.168 文件名的 vendor_boot 镜像，以此类推。
2. 文件名中带 F.xx，表示此 vendor_boot 镜像在 F.xx 版本中刷入最为合适。比如 F.37 版本应该刷入 F.37 版本的 vendor_boot 镜像
