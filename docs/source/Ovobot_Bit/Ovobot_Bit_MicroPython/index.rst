Ovobot Bit MicroPython指南
===========================

开始编程前，首先需要导入必要的库：

.. code-block:: python

    from microbit import *
    from ovobot import *

以下是使用Scratch给Ovobot Bit机器人编程的快速参考，如果你是第一次给机器人编程请先阅读接下来的部分：

.. toctree::
   :maxdepth: 1

运动
-----

.. py:function:: move(dir, speed)

    通过设定机器人运动方向、运动速度和持续时间来让机器人运动，速度范围为0~255。

    :param int dir: 可以为0或者1，0：机器人向前运动，1：机器人向后运动。
    :param int speed: 设置机器人运动的速度，数值范围为0~255。

例子：

.. code-block:: python

    from ovobot import *
    from microbit import *


    moveAtSpeed(0,100)
    sleep(1* 1000)
    stopMove()

解析：当绿旗被点击时，Bit机器人以100的速度匀速前进（0代表前进，1代表后退），等待1秒后停止运动。

.. py:function:: move(dir, speed, s)

    通过设定机器人运动方向、运动速度和持续时间来让机器人运动，速度范围为0~255。

    :param int dir: 可以为0或者1，0：机器人向前运动，1：机器人向后运动。
    :param int speed: 设置机器人运动的速度，数值范围为0~255。
    :param int s: 控制机器人持续运行指定的时间（秒）。

例子：

.. code-block:: python

    from ovobot import *


    move(0,100,1)

解析：当绿旗被点击时，Bit机器人以100的速度匀速前进（0代表前进，1代表后退），持续时间为1秒。

.. py:function:: rotateAtSpeed(dir, speed)

    设置机器人向左或者向右的旋转速度，速度范围为0~255。

    :param int dir: 可以为0或者1，0：机器人向左旋转，1：机器人向右旋转。
    :param int speed: 设置机器人旋转的速度，数值范围为0~255。

例子：

.. code-block:: python

    from ovobot import *
    from microbit import *


    rotateAtSpeed(0,100)
    sleep(1* 1000)
    stopMove()

解析：当绿旗被点击时，Bit机器人以100的速度向左旋转（0代表向左，1代表向右），等待1秒后停止运动。

.. py:function:: rotate(dir, speed, s)

    设置机器人向左或者向右的旋转速度以及持续时间，速度范围为0~255。

    :param int dir: 可以为0或者1，0：机器人向左旋转，1：机器人向右旋转。
    :param int speed: 设置机器人旋转的速度，数值范围为0~255。
    :param int s: 控制机器人持续运行指定的时间（秒）。

例子：

.. code-block:: python

    from ovobot import *


    rotate(0,100,1)

解析：当绿旗被点击时，Bit机器人以100的速度向左旋转（0代表向左，1代表向右），持续时间为1秒。

.. py:function:: stopMove()

    设置左右两个电机的运动速度为0。

例子：

.. code-block:: python

    from ovobot import *
    from microbit import *


    rotateAtSpeed(0,100)
    sleep(1* 1000)
    stopMove()

解析：当绿旗被点击时，Bit机器人以100的速度向左旋转，等待1秒后停止运动。

.. py:function:: rawMotorWithPwm(speed,speed)

    分别驱动Bit的左右两个轮子的转速。

    :param int speed: 设置驱动Bit的左轮的转速，数值范围为-255~255。
    :param int speed: 设置驱动Bit的右轮的转速，数值范围为-255~255。

例子：

.. code-block:: python

    from ovobot import *
    from microbit import *


    rawMotorWithPwm(-255,100)
    sleep(1* 1000)
    rawMotorWithPwm(100,-255)
    stopMove()

解析：当绿旗被点击时，Bit机器人的驱动电机以左轮-255、右轮100的速度行走，
等待1秒后，再以左轮100右轮-255的速度前进后停止运动。 （即先左拐再右拐）

外观
-----

.. py:function:: setledGroupColor(color,color)


    可以分别设置左右两侧LED灯的颜色。

    :param int color: 设置左侧LED灯的颜色，可以为0-8，0：红色，1：橙色，2：黄色，3：绿色，4：蓝色，5：靛蓝色，6：紫色，7：白色，8：黑色。
    :param int color: 设置右侧LED灯的颜色，可以为0-8，0：红色，1：橙色，2：黄色，3：绿色，4：蓝色，5：靛蓝色，6：紫色，7：白色，8：黑色。

例子：

.. code-block:: python

    from ovobot import *
    from microbit import *


    while True:
      setledGroupColor(1,4)
      sleep(1* 1000)
      setledGroupColor(3,6)
      sleep(1* 1000)

解析：当绿旗被点击时，Bit机器人的彩色灯左侧为橙色，右侧为蓝色，等待1秒后，彩色灯左侧变为绿色，右侧变为紫色，
再等待1秒后变回原来的颜色， 如此重复执行这一指令。

.. py:function:: display.scroll(value，delay = 150，*，wait = True，loop = False，monospace = False)

value在显示屏上水平滚动，如果value为整数或浮点数，则首先使用将其转换为字符串str()。
该delay参数控制文本滚动的速度。
如果wait为True，则此功能将阻塞直到动画结束，否则动画将在后台发生。
如果loop为True，则动画将永远重复。
如果monospace为True，则字符将全部占用5个像素列的宽度，否则在滚动时每个字符之间将恰好有1个空白像素列。
请注意wait，loop和monospace参数必须使用其关键字指定。

.. py:function:: display.show(value，delay = 400，*，wait = True，loop = False，clear = False)

如果value为字符串，浮点数或整数，则按顺序显示字母/数字。
否则，如果value是可重复的图像序列，请依次显示这些图像。每个字母，数字或图像delay之间以毫秒为单位显示。
如果wait为True，则此功能将阻塞直到动画结束，否则动画将在后台发生。
如果loop为True，则动画将永远重复。
如果clear为True，则在迭代完成后将清除显示。
请注意wait，loop和clear参数必须使用其关键字指定。
详情请参考：https://microbit-micropython.readthedocs.io/en/latest/tutorials/images.html

例子：

.. code-block:: python

    from microbit import *


    display.show(Image("09090:90909:90009:09090:00900"))
    sleep(0.5* 1000)
    display.show(Image("99999:00009:99999:90000:99999"))
    sleep(0.5* 1000)

解析：当绿旗被点击时，Bit机器人的LED灯显示“❤”的图案，等待0.5秒后，变为显示“2”的图案，同样显示0.5秒。

.. py:function:: display.clear()

    将所有LED的亮度设置为0（熄灭）。

例子：

.. code-block:: python

    from microbit import *


    display.show(Image("09090:90909:90009:09090:00900"))
    sleep(2* 1000)
    display.clear()

解析：当绿旗被点击时，Bit机器人的LED灯显示“❤”的图案，等待2秒后，熄灭屏幕。

.. py:function:: display.set_pixel(x, y, action)

    点亮Bit机器人LED点阵屏上某个坐标的LED，x、y的数值范围为0~4，零点在点阵屏的左上角，水平向右为x轴，竖直向下为y轴。
    
    :param int x: 对应x轴的坐标，数值范围为0~4。
    :param int y: 对应y轴的坐标，数值范围为0~4。
    :param int action: 0：熄灭，9：点亮。

.. py:function:: display.set_pixel(x, y, value)

    将列x和行的LED亮度设置为value，必须是0到9之间的整数。

    :param int x: 设置对应x轴的坐标，数值范围为0~4。
    :param int y: 设置对应y轴的坐标，数值范围为0~4。
    :param int value: 0：熄灭，9：点亮。

.. py:function:: display.get_pixel(x, y)

    以0（熄灭）和9（点亮）之间的整数返回列x和行的LED亮度y。

    :param int x: 设置对应x轴的坐标，数值范围为0~4。
    :param int y: 设置对应y轴的坐标，数值范围为0~4。

声音
-----

.. py:function:: music.pitch(频率，持续时间= -1，pin = microbit.pin0，wait = True)

以指定的毫秒数以给定的整数频率播放音高。
例如，如果频率设置为440，长度设置为1000，则我们将听到标准音乐会A的声音达一秒钟​​。
请注意，您一次只能在一根针上弹一个音高。
如果wait设置为True，则此功能正在阻止。
如果duration为负，则连续播放音调，直到阻塞呼叫被中断，或者在后台呼叫的情况下，设置或调用了新的频率stop。
详情请参考：https://microbit-micropython.readthedocs.io/en/latest/music.html

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

引脚
-----

.. py:function:: pin1.is_touched()

    如果引脚被用手指触摸，返回True，否则返回False。
    该测试是通过测量引脚与地面之间有多少电阻来完成的。低电阻可提供的读数True。
    为了使用手指获得可靠的读数，您可能需要用身体的另一部分（例如另一只手）触摸接地插针。

.. py:function:: pin1.read_analog()

    读取施加到该引脚的电压，并将其返回为0（表示0V）和1023（表示3.3V）之间的整数。

.. py:function:: pin1.write_analog(n)

    在引脚上输出PWM信号，占空比与所提供的成正比。
    value可以是整数或0（0％占空比）之间的浮点数和1023（100％占空比）。

.. py:function:: pin1.read_digital()

    如果引脚为高电平，则返回1；如果引脚为低电平，则返回0。

.. py:function:: pin1.write_digital(n)

    如果value为1，则将引脚设置为高电平；如果为0，则将其设置为低电平。

无线通讯
--------

.. py:function:: radio.on()

    打开无线通讯，由于无线电会消耗功率并占用您可能需要的内存，因此需要显式调用此方法。

.. py:function:: radio.off()

    关闭无线通讯，从而节省电量和内存。

.. py:function:: radio.reset()

    复位无线通讯，将设置重置为其默认值

.. py:function:: radio.send('str')

    发送无线消息。

    :param int str: 字符串，可以是文字、字母、数字。

.. py:function:: radio.send_bytes(list_tobytes([1, 2]))

    发送无线消息列表。

.. py:function:: list_tobytes([radio.receive()

    接收无线消息。

.. py:function:: list_tobytes(bytes_tolist(radio.receive_bytes()))

    接收无线消息列表。

.. py:function:: radio.config(channel=1)

    设置无线通讯频道。

事件
-----

.. py:function:: from microbit import *

    当机器人处于离线模式时，启动Ovobot Bit，执行此模块下方的程序。

例子：

.. code-block:: python

    from microbit import *
    import music

    music.pitch(262 , 500 , pin=pin0 , wait=True)

解析：当机器人处于离线模式时，启动Ovobot Bit，播放C音符持续一个节拍。

.. py:function:: on_button_action_pressed():

    按钮指的是micro:bit的两个可编程按键，分为A和B，当对应Bit的按钮被按下时，执行此模块下方的程序。

    :param int action: 设置对应按钮，a代表A键，b代表B键。

例子：

.. code-block:: python

    from microbit import *
    from ovobot import *

    def on_button_a_pressed():
      move(0,100,1)

    while True:
      if button_a.is_pressed():
        on_button_a_pressed()

解析：当按下micro:bit的可编程按键A键时，Bit机器人以100的速度前进，持续时间为1秒。

.. py:function:: on_irbutton_button_pressed():

    当红外遥控器对应的按钮被按下时，则会执行程序块下方的程序。

    :param int button: 设置对应按钮，1-21代表不同的按钮。

例子：

.. code-block:: python

    from ovobot import *

    def on_irbutton_m_pressed():
      move(1,255,2)

    while True:
      if irkeyIsPressed(1):
        on_irbutton_m_pressed()

解析：当按下红外遥控器的M键时，Bit机器人以255的速度后退，持续时间为2秒。

.. py:function:: fon_loudness_greater_than_vol():

    当响度大于设置数值时，则会执行程序块下方的程序。

    :param int vol: 可设置响度大小。

控制
-----

.. py:function:: sleep(n)

    将暂停执行指令等待n毫秒，一秒是1000毫秒。n可以是整数或浮点数。

    :param int s: 控制机器人停止运动指定的时间（秒）。

侦测
-----

.. py:function:: button_action.is_pressed():

    选择机器人按键触发事件的回调函数。

    :param int action: 设置对应按钮，a代表A键，b代表B键。

.. py:function:: irkeyIsPressed(button):

    如果M按键按下的话，返回值就是True, 否则返回值是false。

    :param int button: 设置对应按钮，1-21代表不同的按钮。

.. py:function:: accelerometer.is_gesture(name):

    判断机器人的姿态，执行程序块下方的程序。

    :param int action: 设置机器人姿态的对应按钮，包括被摇晃、向上倾斜、正面朝上、自由下落等。

.. py:function:: accelerometer.get_values()

    根据x、y、z方向，以正整数或负整数获取轴上的加速度测量值，测量单位为毫克。
    默认情况下，加速度计的配置范围为+/- 2g，因此此方法将在+/- 2000mg范围内返回。

    :param int axis: 可选择返回x轴、y轴或z轴的加速度值。
   
.. py:function:: loudness()

    我们用响度来表示声音传感器的反馈值，响度的范围大小是0-255。

.. py:function:: readBatteryLevel()

    电池电量模块可以实时显示Bit的百分比电量。

.. py:function:: caliGyro()

    校正Bit的俯仰、横滚和侧偏的角速度。

.. py:function:: (getGyrox()

    反馈Bit的俯仰、横滚和侧偏的角速度。

.. py:function:: getYaw()

    反馈Bit侧偏的角度。

.. py:function:: compass.heading()

    根据上述读数计算得出的罗盘方向为从0到360范围内的整数，代表以度为单位的角度，顺时针方向，北为0。

.. py:function:: compass.get_field_strength()

    反馈当前环境中总磁场强度，单位是纳特斯拉。用磁铁靠近电子罗盘，看看磁场强度有什么变化。

.. py:function:: compass.calibrate()

    开始校准过程：一条指示性消息将滚动给用户，此后他们将需要旋转设备以便在LED显示屏上画一个圆圈。

.. py:function:: temperature()

    反馈温度传感器检测到的温度值。

.. py:function:: display.read_light_level()

    反馈光敏传感器感应环境光线的强度。可以尝试修改亮度级别，看看不同级别对应什么样的亮度。

.. py:function:: running_time()

    反馈Bit机器人的运行时间。

.. py:function:: readDistance(No)

    反馈Bit机器人超声波传感器检测到的距离。

    :param int No: 可选择超声波传感器模块，0代表模块1、1代表模块2、2代表模块3、3代表模块4。

.. py:function:: anyWasNearBySonic(No):

    反馈Bit机器人超声波传感器有没有检测到障碍物。

    :param int No: 可选择超声波传感器模块，0代表模块1、1代表模块2、2代表模块3、3代表模块4。

.. py:function:: readLineSensorData(No,dir)

    可以分别反馈巡线传感器左右两个光电对管检测的灰度值，黑色物体的返回值接近0，白色物体返回值接近255。

    :param int No: 可选择巡线传感器模块，0代表模块1、1代表模块2、2代表模块3、3代表模块4。
    :param int dir: 0代表左侧，1代表右侧。

.. py:function:: readLineState(No,dir,color):

    分别用于判断巡线传感器左侧或者右侧是否检测到黑色或白色，条件成立时返回为真。

    :param int No: 可选择巡线传感器模块，0代表模块1、1代表模块2、2代表模块3、3代表模块4。
    :param int dir: 0代表左侧，1代表右侧，2代表全部。
    :param int color: 0代表黑色，1代表白色。

运算
-----





变量
-----













