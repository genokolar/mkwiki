Omega50 Rev.B 介绍
=====================
本页面仅描述rev.B版本（轴灯版）相关信息

描述
---------

- 5x12阵列的50%键盘，共58键
- 支持RGB轴灯
- Type-C接口
- 蓝牙主控为nRF52832（陶瓷天线）
- 采用热拔插方式（佳达隆轴座）
- 支持旋转编码器
- 轴灯兼指示灯功能
- 预留WS2812 RGB灯带焊接位
- 支持PCB卫星轴
- PCB尺寸：247.7mm×95.3mm

![](../img/omega50-b.jpg "Omega50 PCB")

## 指示灯说明

轴灯分为轴灯模式和指示灯模式，出厂默认为指示灯模式，可通过<kbd>Lshift</kbd>+<kbd>Rshift</kbd>+<kbd>L</kbd> 在指示灯模式和轴灯模式之间切换。

轴灯在指示灯模式时，通过不同的颜色指示状态：

- 蓝色-蓝牙连接成功、蓝牙输出
- 绿色-USB输出
- 粉色-蓝牙通道1️⃣广播中
- 黄色-蓝牙通道2️⃣广播中
- 红色-蓝牙通道3️⃣广播中
- USB连接状态下，状态灯常亮
- 蓝牙连接状态下，指示灯5秒后自动熄灭（可自定义常亮时长）
- 蓝牙广播30秒后未连接自动熄灭。

### RGB轴灯说明

轴灯分为轴灯模式和指示灯模式，出厂默认为指示灯模式，可通过<kbd>Lshift</kbd>+<kbd>Rshift</kbd>+<kbd>L</kbd> 在指示灯模式和轴灯模式之间切换。

当前轴灯版PCB采用蓝牙主控直接驱动RGB灯，所以无复杂灯效，仅有单色常亮、单色呼吸和彩虹循环，可手动调色，可视为单色轴灯的增强版本。

轴灯模式时，采用<kbd>Lshift</kbd>+<kbd>Rshift</kbd>+<kbd>Z</kbd> <kbd>X</kbd> <kbd>C</kbd> <kbd>V</kbd>等RGB控制功能调整轴灯。

## 如何启用旋钮编码器

只需要将旋钮编码器焊接到ESC位置，然后接入配置工具，找到键盘设置--布局配置--编码器选项，将按键更改成编码器。

顶部出现的两颗按钮就是旋转功能，下面第一颗按键，就是旋钮按键功能。

![](../img/rotary.png "按键示意图")


## 固件下载

注:USB固件无需更新，不提供下载. 
本页面提供的蓝牙固件基于nRF SDK17.0.2 不能与基于nRF SDK15.3的固件混用。

<a href="http://glab.online/down/sdk17/Omega50-b-20210815-nrf52-all.hex" class="button">20210815蓝牙完整固件</a>

<a href="../down/download.md" class="button2">工具等下载</a>
