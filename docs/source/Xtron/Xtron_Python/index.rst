Xtron Python 指南
=====================

 1. Xtron有两个可编程的LED灯，4个RGB灯，7个按键（4个方向按键，2个功能按键，1个菜单按键），1个蜂鸣器，光敏传感器，运动传感器，还有2个扩展接口。运用这些模块以及扩展，可以学习Scratch以及Python编程，还可以做很多有趣的创客制作。

 2. 用Scratch进行编程，你需要下载并安装Ovoblock软件。
 
    Scratch & Python编程模式: Ovoblock软件

    Ovoblock是一款基于Scratch 3.0开发的电脑端编程软件，支持Mac、PC和浏览器平台，兼容Scratch 3.0的所有功能，同时也支持python语言开发。

    Ovoblock下载链接：https://www.ovobot.cn/zh-hans/app/#Ovoblock

 3. 在Xtron开始编程之前，我们要加载对应的固件。

    * Xtron开关键处于OFF位置，把Xtron用USB连接到电脑，这时候屏幕显示F4图案。

    * 把  文件复制到Xtron中。

    * 按下RST按键，这时候屏幕是黑色的。（LED闪烁）现在，固件已经加载完成。

 4. 打开Ovobot软件，移除默认的OvoBot Bit设备，在添加设备里加上Xtron。
    
    （此处有动画）

 5. 现在你可以开始Scratch编程了，我们的Xtron有实时和离线两种模式，可以根据你的需求来选择。
    
    * 实时模式： Xtron要连接在电脑上，用于程序的调试，可以点击绿色的运行按键，实时看到程序效果。

    * 离线模式： Xtron在程序下载的时候，要连接在电脑上。下载完成后，无需连线，可以开机直接运行程序。

 6. 你可以从基础的积木块开始学习，积木块的介绍参考 



.. toctree::
   :maxdepth: 1
   :numbered:

   block_basic
   block_robot
   block_MU
   block_extend_basic
