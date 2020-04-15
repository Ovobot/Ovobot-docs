Xtron Python 指南
=====================

开始编程前，首先需要导入必要的库：

.. code-block:: python

    from microbit import *
    from ovobot import *

以下是使用Scratch给Xtron三合一掌机编程的快速参考，如果你是第一次给Xtron掌机编程请先阅读接下来的部分：

.. toctree::
   :maxdepth: 1

灯光
-----

.. py:function:: pyb(led，action)

    Xtron板载上有2个LED灯，分别为led1、led2，可以分别控制两个灯的点亮和熄灭
    这两个LED灯还用来作为状态的指示灯，比如充电时led1亮红灯，下载代码时led1闪红灯，开机时led2亮蓝灯后熄灭。

    :param int led: 选择控制led1或者led2点亮和熄灭。
    :param int action: off：熄灭，on：点亮。

.. py:function:: pyb.toggle(led)

    电平反转就是数字电路的某个端口（输入或者输出）的状态从一个状态转换到另一个状态，如从“1”变化到“0”,
    数字电路的状态转换时间非常短，理想认为转换时间为0，这个变化过程就叫电平转换。
    即Xtron的led灯从点亮变为熄灭，或者从熄灭变为点亮。
    板载上有两个led灯，分别为led1、led2，可以分别控制两个led灯进行电平反转。

    :param int led: 选择控制led1或者led2电平反转。

.. py:function:: pyb.intensity(led，value)

    设置Xtron板载的led灯的亮度，数值范围为0~255。
    在点亮LED之后再设置亮度才生效，而且只调节前面程序里已经点亮的LED灯的亮度值。

    :param int led: 选择控制led1或者led2的亮度。
    :param int value: 设置板载上对应led的亮度，数值范围为0~255。

.. py:function:: setrgbhexcolor(value,color)

    Xtron上有4个RGB灯，可以分别设置不同的颜色，通过颜色、饱和度、亮度来调节颜色，数值范围均为0~100。
    点击颜色下方的【滴管图标】还可以从已有的角色中一键获取角色上的任意颜色。

    :param int value: 选择控制板载上任意一个led灯。
    :param int color: 选择控制板载上任意一个led灯的颜色。

.. py:function:: setAllcolor(color)

    Xtron上有4个RGB灯，可以分别设置不同的颜色，通过颜色、饱和度、亮度来调节颜色，数值范围均为0~100。
    同样的，还可以从选择的角色中一键吸取已有的颜色。
    和上面的程序块的区别是，上面的是单独设置某一个RGB灯，这个程序块则是同时设置所有的RGB灯。

    :param int color: 选择控制板载上所有led灯的颜色。

.. py:function:: setbrightness(value)

    用来设置Xtron板载的RGB灯的亮度。
    设置亮度值之后，再设置RGB灯的颜色，亮度值才生效。
    如果你想改变亮度值的话，你需要设置亮度值之后，再次设置一下对应的RGB灯颜色。

    :param int value: 设置Xtron板载的RGB灯的亮度。

.. py:function:: colour_rgb(value, value, value)

    分别设置red红色、green绿色、blue蓝色的数值，数值范围为0~255。

    :param int value: 设置板载上对应led的数值，数值范围为0~255。

显示
-----

.. py:function:: lcd.clearScreen()

    用来清空LCD屏幕上之前显示的所有内容。在同一个位置显示不同的内容，如果不清空，会和之后显示的内容重叠。

.. py:function:: lcd.setBgColor(value)

    该积木块可以设置屏幕的背景色，一共有16个颜色可以选择，其中第一个颜色是透明色。

    :param int value: 设置屏幕的背景色。

.. py:function:: lcd.show()

    在设置好屏幕背景以及屏幕显示内容后，加上显示生效积木块，屏幕上才会显示我们设置好的背景及内容。

.. py:function:: lcd.drawText(x,y,string,color)

    把文本内容显示在某个坐标（x，y）处。
    文本内容可以是字母、数字，暂时不支持中文显示。
    坐标的范围是X：0~160， Y: 0~120
    文本内容有16个颜色可选，其中第一个颜色是透明色。

    :param int x y: 通过x轴和y轴的距离，将文本显示在特定的坐标（x，y）上，坐标的范围是X：0~160， Y: 0~120。
    :param int string: 文本内容可以是字母、数字，暂时不支持中文显示。
    :param int color: 文本内容有16个颜色可选，其中第一个颜色是透明色。

.. py:function:: lcd.drawHline(x,y,string,color)

    绘制线一条水平或者垂直的线段，在某个坐标（x，y）绘制一条水平或垂直的线段，线的长度≤显示屏的长度。
    坐标的范围是X：0~160， Y: 0~120
    如果是水平线，线段长度+ X的坐标<160; 如果是垂直线，线段长度+ Y的坐标<120. 否则线段显示不完整。
    所有绘制的图案，都要加上显示生效积木块，才会在屏幕上显示出来。
    文本内容有16个颜色可选，其中第一个颜色是透明色。

    :param int x y: 在某个坐标（x，y）绘制一条水平或垂直的线段，线的长度≤显示屏的长度，坐标的范围是X：0~160， Y: 0~120。
    :param int string: 文本内容可以是字母、数字，暂时不支持中文显示。
    :param int color: 文本内容有16个颜色可选，其中第一个颜色是透明色。

.. py:function:: lcd.drawLine(x1,y1,x2,y2,color)

    绘制一条线段，绘制一条从一个坐标（x1，y1）到另一个坐标（x2，y2）的线段。
    坐标的范围是X：0~160， Y: 0~120
    和上一个积木块的区别是，这个积木块绘制的线段是任意的方向，上一个只能是水平或者垂直方向。
    文本内容有16个颜色可选，其中第一个颜色是透明色。

    :param int x1 y1 x2 y2: 确定坐标1（x1，y1）和坐标2（x2，y2）的位置，坐标的范围是X：0~160， Y: 0~120。
    :param int color: 文本内容有16个颜色可选，其中第一个颜色是透明色。

.. py:function:: lcd.drawRect(x,y,value,value,color)

    绘制一个矩形，在某个坐标（x，y）处绘制一个矩形，通过设置矩形的宽和高来设置矩形的大小。
    可以选择实心矩形或者是空心矩形。
    坐标的范围是X：0~160， Y: 0~120。
    如果坐标值加上矩形大小，超过了显示范围，会显示不完整。
    文本内容有16个颜色可选，其中第一个颜色是透明色。

    :param int x y: 在某个坐标（x，y）处绘制一个矩形，通过设置矩形的宽和高来设置矩形的大小，坐标的范围是X：0~160， Y: 0~120。
    :param int value: 设置矩形的宽和高，如果坐标值加上矩形大小，超过了显示范围，会显示不完整。
    :param int color: 文本内容有16个颜色可选，其中第一个颜色是透明色。

.. py:function:: lcd.circle(x,y,value,color)

    绘制一个圆形，在某个坐标（x，y）绘制一个圆形，通过设置圆的半径来改变圆的大小。
    可以选择实心圆形或者是空心圆形。
    坐标的范围是X：0~160， Y: 0~120
    如果坐标值加上圆形大小，超过了显示范围，会显示不完整。
    文本内容有16个颜色可选，其中第一个颜色是透明色。

    :param int x y: 在某个坐标（x，y）绘制一个圆形，通过设置圆的半径来改变圆的大小。坐标的范围是X：0~160， Y: 0~120。
    :param int value: 设置矩形的宽和高，如果坐标值加上圆形大小，超过了显示范围，会显示不完整。
    :param int color: 文本内容有16个颜色可选，其中第一个颜色是透明色。

.. py:function:: lcd.triangle(x1,y1,x2,y2,x,3,y3，color)

    绘制一个三角形，通过设置三角形三个点的坐标（x1，y1）、（x2，y2）、（x3，y3）来绘制一个三角形。
    可以选择实心三角形或者是空心三角形。
    坐标的范围是X：0~160， Y: 0~120
    文本内容有16个颜色可选，其中第一个颜色是透明色。

    :param int x y: 通过设置三角形三个点的坐标（x1，y1）、（x2，y2）、（x3，y3）来绘制一个三角形。坐标的范围是X：0~160， Y: 0~120。
    :param int value: 设置三角形三个点的坐标，如果坐标值加上三角形大小，超过了显示范围，会显示不完整。
    :param int color: 文本内容有16个颜色可选，其中第一个颜色是透明色。

声音
-----

.. py:function:: music.pitch(频率，持续时间= -1，pin = microbit.pin0，wait = True)

    该积木块可以播放音符，音符以及节拍长度可以在下拉框里选择。
    点击音符，显示的是中央C的音调，可以用左右两边的箭头来切换高低音，左边是低音，右边是高音。
    详情请参考：https://microbit-micropython.readthedocs.io/en/latest/music.html
   
    C调中，C、D、E、F、G、A、B分别对应简谱中的1、2、3、4、5、6、7，一个唱名为四分音符持续1个节拍，下方有一个横杠的是八分音符持续1/2节拍，
    音符后有一个横杠的为二分音符持续2个节拍，同学们按照音符和节拍数编写整段音乐。

    :param int note: 默认选择播放的音符为0，即代表暂停播放。
    :param int beat: 音符播放的节拍数，节拍数为500的倍数，倍数范围为1/16~4。

例子：

.. code-block:: python

    from microbit import *
    import music


    music.pitch(262 , 500 , pin=pin0 , wait=True)
    music.pitch(330 , 1000 , pin=pin0 , wait=True)

解析：当绿旗被点击时，播放C音符持续一个节拍，然后播放E音符持续一个节拍。

.. py:function:: music.stop(pin = microbit.pin0)

    在给定的引脚上停止所有音乐播放，例如：music.stop(pin1)。
    如果没有给出引脚，例如：music.stop()假设为pin0。

    :param int note: 默认选择播放的音符为0，即代表暂停播放。
    :param int beat: 音符播放的节拍数，节拍数为500的倍数，倍数范围为1/16~4。

.. py:function:: music.stopPlay()

    停止播放所有声音。
























事件
-----

.. py:function:: import pyb

    当启动Xtron三合一掌机时，执行此模块下方的程序。

例子：

.. code-block:: python

    import pyb
    import music

    music.pitch(262 , 500 , pin=pin0 , wait=True)

解析：当启动Xtron三合一掌机时，播放C音符持续一个节拍。

.. py:function:: on_button_action_pressed():

    按钮指的是micro:bit的两个可编程按键，分为A和B，当对应Xtron的按钮被按下时，执行此模块下方的程序。

    :param int action: 设置对应按钮，a代表A键，b代表B键。























控制
-----

.. py:function:: move(dir, speed)

    通过设定机器人运动方向、运动速度和持续时间来让机器人运动，速度范围为0~255。

    :param int dir: 可以为0或者1，0：机器人向前运动，1：机器人向后运动。
    :param int speed: 设置机器人运动的速度，数值范围为0~255。






















侦测
-----

.. py:function:: from pyb import read_light_level

    测量光照射的强度

.. py:function:: (getGyrox()

    反馈Xtron的俯仰、横滚和侧偏的角速度。

.. py:function:: acc.get_values()

    根据x、y、z方向，以正整数或负整数获取轴上的加速度测量值，测量单位为毫克。
    默认情况下，加速度计的配置范围为+/- 2g，因此此方法将在+/- 2000mg范围内返回。

    :param int axis: 可选择返回x轴、y轴或z轴的加速度值。


