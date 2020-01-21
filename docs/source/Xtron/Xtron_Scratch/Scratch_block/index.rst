Xtron Scratch 积木块指南
========================

 1.Xtron有两个可编程的LED灯，4个RGB灯，7个按键（4个方向按键，2个功能按键，1个菜单按键），1个蜂鸣器，光敏传感器，运动传感器，还有2个扩展接口。运用这些模块以及扩展，可以学习Scratch以及Python编程，还可以做很多有趣的创客制作。
              
 2.用Scratch进行编程，你有两种方式可以选择：
 
    （1）下载并安装Ovoblock软件。
 
      * Ovoblock是一款基于Scratch 3.0开发的电脑端编程软件，支持Mac、PC和浏览器平台，兼容Scratch 3.0的所有功能，同时也支持python语言开发。

      * Ovoblock下载链接：https://www.ovobot.cn/zh-hans/app/#Ovoblock
   
    （2）使用Ovoblock网页版本。

      * 与下载并安装软件相比，不同之处在于，在线编程的时候，你需要运行【Ovobot-link】。

      * Ovobot-link下载地址：https://www.ovobot.cn/zh-hans/product/detail/ovobot-bit/info/#downloads

      * ovoblock在线编程链接： https://ovoblock.ovobot.cn/


 3.在Xtron开始编程之前，你需要加载对应的固件。

    * Xtron开关键处于OFF位置，把Xtron用USB连接到电脑，这时候屏幕显示F4图案.

    .. image:: images/F4.png

    * 点击ovoblock网页或者软件上的【帮助】->【下载固件】获取flasher.uf2文件，把flasher.uf2文件复制到Xtron中。

      【Xtron python固件】可以让Xtron成为一个创客主板，自带的传感器和屏幕可以做很多内容，并且还可以扩展机器人，AI摄像头以及丰富的扩展模块。

      【Xtron 遥控器固件】可以让Xtron成为Scratch游戏的手柄，你可以用方向键和A B键来代替键盘上对应的按键。手柄有两个模式，一个是按键模式，另一个是重力加速度模式（体感模式），可以通过MENU按键来切换模式。

    * 按下RST按键，这时候屏幕是黑色的。现在，固件已经加载完成。

 4.打开Ovobot软件，移除默认的OvoBot Bit设备，在添加设备里加上Xtron。
    
    .. image:: images/index.gif

 5.现在你可以开始Scratch编程了，我们的Xtron有实时和离线两种模式，可以根据你的需求来选择。
    
    * 调试模式： Xtron要连接在电脑上，用于程序的调试，点击【调试程序】，可以实时看到程序效果。
    * 离线模式： Xtron在程序下载的过程中（LED1和LED2交替闪烁），需连接在电脑上。点击【下载程序】下载完成后，无需连线，可以开机直接运行程序。
     
    .. image:: images/index2.gif

 6.你可以从基础的积木块开始学习，积木块的介绍参考：

    .. toctree::
        :maxdepth: 1

        block_basic
        block_robot
        block_MU
        block_extend_basic
