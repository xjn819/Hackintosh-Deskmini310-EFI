# Hackintosh-Deskmini310-EFI

# 购物指南：

- CPU:i3-i9都可以，请务必不要购买ES QS版本CPU（可能会碰到各种各样的问题），其中i7及以上存在功耗墙，不适合购买。
- 内存：随便
- 网卡：拆机卡（BCM943602CS）+转接卡
- 硬盘：请不要购买pm981,pm981a.自主查询合适的SSD 比如SN750等,如果搭配的是白果的wifi转接卡，那尽可能买单面颗粒的SSD，不然叠在一起可能会压弯了。
- 散热器：随便
- 请在购买后先使用WIN，并使用AIDA等压力测试软件测试并确保硬件没有问题！！




# 我的配置/Configurations

- Motherboard/主板: ASROCK 310-com
- External Hard Drive/硬盘: Asgard AN 512 M.2 NVMe SSD
- CPU: I5-8400  
- Wireless Card/网卡: BCM943602CS+转接卡
- RAM/内存: ADATA 16G DDR4 2400MHz X2


# Functions/功能
- Sleep&Wake/睡眠唤醒: OK/正常
- Bluetooth/蓝牙: OK/免驱，正常
- WIFI: OK/免驱，正常
- Wired Internet有线网卡: OK/正常
- Audio声卡:OK/ 正常
- CPU Frequency/变频: OK/正常
- Hand Off: OK/正常







# BIOS设置/BIOS settings


  - CPU Configuration, CPU C states Support, Enabled,
  - CPU Configuration, CPU C states Support, CFG Lock Disabled (必须）
  - Chipset Configuration, Vt-d, Disabled,
  - Chipset Configuration, Onboard HD Audio: Enabled,
  - USB Configuration, XHCI Hand-off, Enabled  （关键）
  - Super IO Configuration, Serial Port, Disabled（必须）
  - Security Secure Boot, Disabled(by default)
  - Boot, CSM, disabled
  - BIOS版本必须在4.0及以上！并且强烈建议使用4.0，没时间看新的acpi。



- 系统完成后睡眠修复, 打开终端执行:

  ```bash
  sudo pmset standby 0
  sudo pmset autopoweroff 0
  sudo pmset hibernatemode 0
  sudo pmset proximitywake 0
  ```
> 或者使用 Hackintool 电源部分修复.

- 系统偏好设置: 节能

   - 取消勾选: 唤醒以供以太网络访问


# 其它注意事项
   - 开机跑码: EFI默认开启了开机跑码方便排错，在正常安装并没发现问题后，请自行修改config.plist里boot-args这项，把-v这个值删除。
   - 不支持hidpi的显示器开机的苹果logo可能不正常，自己修改config.plist中关于UIScale的设置。
   
   - 请务必修改三码！！！！



# 其它无线网卡
- 如果使用dw1820a网卡，请参考https://blog.daliansky.net/DW1820A_BCM94350ZAE-driver-inserts-the-correct-posture.html
- 如果使用dw1560/dw1830网卡，请参考https://blog.daliansky.net/Broadcom-BCM94352z-DW1560-drive-new-posture.html
- 如果使用intel的无线网卡，请参考https://github.com/OpenIntelWireless/itlwm
