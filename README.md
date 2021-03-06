
# EFI
OpenCore: 0.6.4
macOS version: Big sur 11.1

## 硬件配置

| 配件   | 型号 | 说明 |
|------|----|----|
| 主板   |  昂达H410D4 IPC  |  USB3 * 1, USB2 * 2, Tpye-C * 1 |
| CPU  |  i5-10400  |  6c12t, L3 12M  |
| 内存   |  酷兽ddr4 2666（笔记本）  |  16G * 2  |
| 显卡   |  Intel UHD Graphics 630  |  DP * 1, HDMI * 1  |
| SSD  |  西数SN550 500G  |  NVME  |
| 声卡   |  ALC662  |  alcid=5  |
| 有线网卡 |  RTL8111  |  千兆网卡  |
| 无线网卡 |  BCM94360CS2  |  免驱  |
| 电源 |  DC电源  |  150w  |
| 机箱 |  酷鱼MG PLUS DC-ITX  |    |


## 说明

* 已做USB定制: TypeC, USB3正常

## 关于英特尔网卡问题 (2020-12-21已移除英特尔网卡驱动)

*相关内核 [AirportItlwm](https://github.com/OpenIntelWireless/itlwm/releases)*

* AirportItlwm.kext
* IntelBluetoothFirmware.kext
* IntelBluetoothInjector.kext

##### 2020-11-24

测试v1.2.0-alpha，目测网速提升20%-50%。十分看好这个项目。建议长期关注


##### 2020-12-15

* 热心网友反馈，10.15.7可以正常使用新EFI，所以删除了原EFI。如遇到10.15.7英特尔网卡无法使用的情况。请自行替换AirportItlwm。
* 由于条件限制，如遇到蓝牙或者usb口无法使用的情况，请取消勾选 USBPorts.kext。 同时勾选 USBInjectAll.kext 开机后自行定制USB。

##### 2020-12-19

* 更新到OC 0.6.4
* 更新plist修复引导版本识别错误的问题

##### 2020-12-21

* 终于选择弃暗投明，放弃了英特尔网卡。换了 BCM94360CS2 ，重新定制了USB。
* 继续使用英特尔网卡的前往 [AirportItlwm发行版](https://github.com/OpenIntelWireless/itlwm/releases) 下载驱动


## 赞赏

*如果觉得对你有帮助，可以请作者喝杯咖啡*

<img src="https://liebian-ios.oss-cn-shenzhen.aliyuncs.com/wechat_pay_alangmeiyoui.jpeg" style="zoom:30%" />