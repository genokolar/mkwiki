更新日志
==========

2021年8月17日更新内容
--------
!!! note "此版本为稳定版，推荐更新"

1、添加底灯控制按键（配置工具上💡按键使用）

2、修复：去掉容易误触丢失绑定信息的E键，避免误清空蓝牙绑定信息

3、bootcheck增强：加大检测按键范围，避免误开机

4、bootcheck增强：调整bootcheck整个流程，减少循环操作

5、预期解决偶发的配置丢失问题

6、恢复默认的蓝牙MTU

7、键盘名称中带版本标识，如Omega45D、Omega45E

🔴 轴灯版PCB提供基于nRF SDK17.0.2的版本，请至产品页面下载

当前固件名称命令规则：

型号-子型号-固件类型-编译日期-固件版本.文件类型

如：Omega50-b-nrf52_kbd_sign-20210817-e35fd41.hex

型号为Omega84，子型号为B版本，固件类型为nrf_kbd_sign(蓝牙核心固件，已签名），编译日期为20210817，固件版本为e35fd41，文件类型为hex二进制文件

2021年7月3日更新内容
--------
1、键盘采用actionmap，突破31个高级按键的限制（不包括64、84）

2、添加新的宏指令：循环

3、更新RGB Light驱动：休眠、开机时闪烁白光提示

4、修复智选键导致灯效更改问题

5、提升宏存储区域最大容量到原本4倍

6、其他更改

2021年4月24日更新内容
--------
1、修复USB识别出错问题（Farad69 Rev.C | Omega50 Rev.B）

2、修复三灯指示灯驱动：FN控制蓝牙通道时指示灯错误

3、修复20210116后智选按键长按错误

已知问题：使用部分智选键时会导致RGB灯光被更改

2021年3月28日更新内容
--------

1、更新RGB Light驱动：去掉慢速扫描时关闭指示灯

2、提高蓝牙MTU

3、旋钮按键支持开机

4、调整键盘矩阵扫描，增加硬件兼容性

5、轴灯版键盘配置调整：默认支持OLED屏幕

2021年1月16日更新内容
--------

更新RGB Light驱动：修正指示灯处于省电模式时切换出错

2021年1月2日更新内容
--------
1、修正power button重置逻辑

2、修正TRICKY_L与Command L键冲突的问题

3、修正重启后广播对应指示灯不正确的问题

4、command功能：禁用Nkro切换的，添加RGB 指示灯与轴灯功能切换

5、加入并完善RGB Light功能（仅轴灯版PCB）

6、FN键：增加RGB控制功能

7、其他代码整理调整

2020年11月26日更新内容
--------

1、修正睡眠或关机时自动输出按键问题

2、修正硬件版本号的显示



2020年11月24日更新内容
--------
1、更改双shift+数字切换层的逻辑（1代表第一层）

2、添加 启动按键 功能开关（双Shift+I切换）

3、所有键盘启用 启动按键 功能

4、优化睡眠关机流程，解决睡眠关机时造成的偶发BUG





2020年10月15日更新内容
--------
1、调整FDS初始化，避免无限重启

2、加入多个智选按键

3、取消双SHIFT+I清配置功能，避免误操作（请使用后背按钮或配置工具进行清空）

4、调整电量输出：F = Full n = Null

5、调整按键矩阵扫描，应该可以小幅度降低耗电



2020年10月2日更新内容
--------
1、调整FDS初始化，减少出错可能

2、多功能按钮重置键盘后自动重启生效

3、重新采用调度模式

2020年9月4日更新内容
--------
1、修正FDS初始化出错导致的问题

2、添加亮度调节按键功能

3、调整及修复bootcheck功能

4、3灯驱动增强：添加开关机闪烁指示

5、添加电量输出功能

6、添加关闭指示灯功能

7、其他代码调整

2020年7月13日更新内容
--------
1、修正了USB设备在主机关机后无法正确处理关机事件导致USB锁死的问题

2、尝试修正跨版本升级时FDS存在脏数据导致无法使用的问题

3、修正宏延时计算不正确导致的播放速度下降的问题

4、降低耗电~50ua，提升续航

2020年4月14日更新内容
-----
1、添加鼠标键功能

2、修正NKRO和6KRO不能同时启用的问题

3、修改电量曲线

4、修正宏播放造成死机的问题

5、添加Bootcheck以替代bootmagic

6、添加切换NKRO的FN功能

7、修正蓝牙HID空间分配不足的问题

8、新的事件传递系统

9、新的存储模块和存储系统

10、新的配置协议

11、支持动态写入宏

12、支持动态配置休眠时间

13、添加DAPLink功能

14、改进按键扫描策略，降低电量消耗

15、其他代码优化重整

2020年2月16日更新内容
-------------
1、新增支持自定义宏功能

2、新增支持鼠标按键

3、修改电量曲线，修正充电无法充满问题

4、增加按键稳定时间间隔，解决按键连按问题

5、仅使用1MB通讯速率，更新高发射功率实现

2019年12月10日更新内容
-----------

1、添加切换设备后闪烁对应状态灯功能 及 其他状态灯修改

2、去掉Buttonless DFU功能

3、增加Power按钮长按10秒清空键盘功能

4、修正仅充电状态时无法输入的问题

5、调整代码结构；适配Omega50；采用无调度模式等大量更改

2019年11月26日更新内容
-------------
1、 续航增强

2、 修正WS2812的部分BUG

3、修正GUI键无法正常锁定的BUG

4、其他代码更新

2019年10月24日更新内容
--------------

1、 Power按钮加入短按关机、长按进入DFU功能

2、 去除bootmagic功能，整理代码，开机唤醒更快

3、 添加键盘重置功能 ，双Shift+I重置键盘

4、 修正关机休眠导致的按键长按问题 ；修正开机闪烁灯太短不易查看问题

2019年10月21日更新内容
--------------

1、新的多设备切换逻辑，更稳定易用

2、修正休眠、关机重启后无法初始化到休眠关机前设备问题

3、修正windows系统设备关机后无法切换设备的问题

4、关机/休眠/唤醒时闪烁系统状态灯进行提示

5、修正键盘状态灯（如Caps灯）在关机/休眠时无法正常关闭问题

6、支持数字电量文本输出（MacOS等无法显示电量的系统也能用文本输出的方式显示电量）

7、修正清空全部绑定后重置到首个设备存在的问题。

2019年9月13日更新内容
--------------

1、调整代码，更新tmk core代码，修正拼写错误；

2、设定清空所有绑定时自动回到首个设备，避免整个绑定过程混乱；

3、设定重复切换到当前设备时，按键无效（如当前为Q设备，再次按下Q切换将不进行任何操作）

总体来说，都是稳定性方面的更新。

2019年9月5日前更新内容
--------------

1、修正WS2812在休眠、关机时无法关闭的问题

2、修改RGB的默认设置，默认关闭RGB

3、修正重启后当前连接设备重置为第一个的问题

4、添加WS2812驱动，现在你们可以接灯带了

5、功能键更新：更改清空设备键，添加WS2812 RGB灯光控制按键

6、使用新的多设备切换方法，杜绝各设备抢连的问题

7、更新蓝牙服务，以期更稳定；

8、更新eeconfig