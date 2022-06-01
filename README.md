# y9000x-
拯救者Y9000X 2020黑苹果OpenCore引导配置
1. 硬件配置 硬件	型号
CPU	Intel i5-9300H
显示器	fHD 1080p
WiFi/蓝牙	Intel AX200
黑苹果支持不完美，屏蔽前三后二总共五个引脚
硬盘	三星PM981A
黑苹果大量读写数据时异常，基本无解，已更换为金士顿512 ssd
EFI测试环境
类型	配置
操作系统	macOS 11.6
显示器分辨率	fhd 1080p
固态硬盘	第一磁盘位金士顿 512 ssd，并且屏蔽第二个磁盘位的PM981A
WiFi/蓝牙	Intel ax200
BIOS	CTEC21WW

2. 功能支持详情
✅ 内置显示器
✅ 电池管理、电池电量显示
✅ 开/合盖唤醒/休眠
✅电源键短按休眠/唤醒
✅开启深度休眠，以更加省电，电源键/开盖唤醒
⚠️ CPU温度传感器
⚠️扬声器节点注册
✅ 3.5mm耳机
✅ 内置麦克风
✅ 摄像头
⚠️ 核显1.2G满频支持
⚠️ 显示器亮度调节（映射到Fn+F11、Fn+F12）
✅ 音量调节（映射到Fn+F2、Fn+F3）
✅ 静音（映射到Fn+F1）
✅ 暂停/播放（映射到Fn+Home）
✅ 触控板（GPIO中断方式、支持多指手势）
✅ WiFi（支持所有信道、解除速率限制）
✅ 蓝牙
⚠️AirDrop
⚠️ AirPlay随航
✅ Type-C PD充电
✅ Type-A USB3.1接口*2
✅ Type-C USB接口*1
✅ Type-C扩展坞（USB、以太网、HDMI2.0、DP）
✅ Type-C雷电接口
✅ 电源按钮环灯及logo灯开关控制（BIOS自带快捷键Fn+L）
✅ 键盘背光灯亮度调节（BIOS自带快捷键Fn+Space）
🔴 指纹识别（因macOS系统安全性限制不可实现）
🔴 除上述已声明可用之外的Fn组合快捷键均不可用
🔴 内置扬声器
🔴 SD卡读卡器


BIOS设置
✅ 磁盘模式设置为AHCI模式Configuration -> Storage -> Controller Mode -> AHCI mode

❗ 从RST(RAID0)模式切换为AHCI模式，磁盘上的所有数据会被清除，所以请提前备份好磁盘重要数据！

✅ 关闭安全启动Security -> Secure Boot -> Disabled

✅ 安装完成后将黑苹果所在的磁盘调节为第一启动顺序，如此每次开机默认进入黑苹果系统
