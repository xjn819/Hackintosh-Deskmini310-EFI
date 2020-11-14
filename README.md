# Hackintosh-Deskmini310-EFI

# 购物指南：

- CPU:i3-i9都可以，请务必不要购买ES QS版本CPU，其中i7及以上存在功耗墙，不适合购买。
- 内存：随便
- 网卡：拆机卡（BCM943602CS）+转接卡，或者购买dw1820a（请务必购买编号为CN-OVW3T3的1820a，其他版本可能存在不适用)
- 硬盘：请不要购买pm981,pm981a.自主查询合适的SSD 比如SN750/C2000/C2000PRO等等
- 散热器：随便
- 请在购买后先使用WIN，并使用AIDA等压力测试软件测试并确保硬件没有问题！！




# 我的配置/Configurations

- Motherboard/主板: ASROCK 310-com
- External Hard Drive/硬盘: Asgard AN 512 M.2 NVMe SSD
- CPU: I5-8400  
- Wireless Card/网卡: dw1820(CN-OVW3T3)
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
  - BIOS版本必须在4.0及以上！


# 其他

- 除了白果卡以及1820a之外的wifi蓝牙卡若要驱动请自行搜索黑果小兵的博客。

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

