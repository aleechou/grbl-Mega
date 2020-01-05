

* 各项配置： https://github.com/gnea/grbl/wiki/Grbl-v1.1-Configuration
* 错误/警告：https://github.com/gnea/grbl/wiki/Grbl-v1.1-Interface
* 硬件接口： https://github.com/gnea/grbl-Mega/wiki/Connecting-Grbl-Mega
* 限位开关： https://github.com/gnea/grbl/wiki/Wiring-Limit-Switches

grbl 中需要注意：

* 采用左手坐标系
* 重新打开串口，即可 RESET
* 设置中的软限位 `$20=1`，运动到小于0的位置，会进入“假死”状态，需要 RESET 恢复
* 设置中的硬限位 `$21=1`，碰到限位开关会进入“假死”状态，需要 RESET 恢复
  

X,Y,Z 轴每mm步数( `$100`, `$101`, `$102` )，公式： `360 ÷ 电机步距角 ÷ 丝杆螺距 × 细分数`