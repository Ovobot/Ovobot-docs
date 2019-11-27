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

.. py:function:: moveAtSpeed(dir, speed)

    设置Bit的前进或后退的速度，数值范围为0~255。

    :param int dir: 可以为0或者1，0：机器人向前运动，1：机器人向后运动。
    :param int speed: 设置机器人运动的速度，数值范围为0~255。

.. py:function:: move(dir, speed, s)

    通过设定机器人运动方向、运动速度和持续时间来让机器人运动，速度范围为0~255。

    :param int dir: 可以为0或者1，0：机器人向前运动，1：机器人向后运动。
    :param int speed: 设置机器人运动的速度，数值范围为0~255。
    :param int s: 控制机器人持续运行指定的时间（秒）。

.. py:function:: rotateAtSpeed(dir, speed)

    设置机器人向左或者向右的旋转速度，速度范围为0~255。

    :param int dir: 可以为0或者1，0：机器人向左旋转，1：机器人向右旋转。
    :param int speed: 设置机器人旋转的速度，数值范围为0~255。

.. py:function:: rotate(dir, speed, s)

    设置机器人向左或者向右的旋转速度以及持续时间，速度范围为0~255。

    :param int dir: 可以为0或者1，0：机器人向左旋转，1：机器人向右旋转。
    :param int speed: 设置机器人旋转的速度，数值范围为0~255。
    :param int s: 控制机器人持续运行指定的时间（秒）。

.. py:function:: stopMove()

    设置左右两个电机的运动速度为0。

.. py:function:: rawMotorWithPwm(speed,speed)

    分别驱动Bit的左右两个轮子的转速。

    :param int speed: 设置驱动Bit的左轮的转速，数值范围为-255~255。
    :param int speed: 设置驱动Bit的右轮的转速，数值范围为-255~255。

外观
-----

.. py:function:: setledGroupColor(clr,clr)

    可以分别设置左右两侧LED灯的颜色。

    :param int clr: 设置左侧LED灯的颜色，可以为0-8，0：红色，1：橙色，2：黄色，3：绿色，4：蓝色，5：靛蓝色，6：紫色，7：白色，8：黑色。
    :param int clr: 设置右侧LED灯的颜色，可以为0-8，0：红色，1：橙色，2：黄色，3：绿色，4：蓝色，5：靛蓝色，6：紫色，7：白色，8：黑色。

.. py:function:: display.scroll('str', wait=False, loop=False)

    可以控制Bit机器人点阵屏显示相应的字符。

    :param int str: 字符串，可以是文字、字母、数字。

.. py:function:: display.show(Image("str:str:str:str:str"))

    可以控制Bit机器人点阵屏显示相应的图案。

    :param int str: 字符串，按行对应点阵屏，0：熄灭对应LED灯，9：点亮对应LED灯，比如90909代表第一行第1、3、5个LED灯亮。

.. py:function:: display.clear()

    熄灭Bit机器人LED点阵屏。

.. py:function:: display.set_pixel(x, y, action)

    点亮Bit机器人LED点阵屏上某个坐标的LED，x、y的数值范围为0~4，零点在点阵屏的左上角，水平向右为x轴，竖直向下为y轴。
    
    :param int x: 对应x轴的坐标，数值范围为0~4。
    :param int y: 对应y轴的坐标，数值范围为0~4。
    :param int action: 0：熄灭，9：点亮。

.. py:function:: display.set_pixel(x, y, action)

    分别设置x或y轴的高度。

    :param int x: 设置对应x轴的坐标，数值范围为0~4。
    :param int y: 设置对应y轴的坐标，数值范围为0~4。
    :param int action: 0：熄灭，9：点亮。

.. py:function:: display.get_pixel(x, y)

    分别获得x或y轴的亮度。

    :param int x: 设置对应x轴的坐标，数值范围为0~4。
    :param int y: 设置对应y轴的坐标，数值范围为0~4。

声音
-----

.. py:function:: music.pitch(note , ct , pin=pin0 , wait=True)

    可以选择播放的音符和音符播放的节拍数。

    :param int note: 选择播放的音符，音符范围为low~high。
    :param int ct: 音符播放的节拍数，节拍数为500的倍数，倍数范围为1/16~4。

.. py:function:: music.pitch(note , ct , pin=pin0 , wait=True)

    设置暂停播放的节拍数。

    :param int note: 默认选择播放的音符为0，即代表暂停播放。
    :param int ct: 音符播放的节拍数，节拍数为500的倍数，倍数范围为1/16~4。

引脚
-----

.. py:function:: pin1.is_touched()

    判断引脚是否被接触。

.. py:function:: pin1.read_analog()

    读取选定引脚的模拟值。

.. py:function:: pin1.write_analog(1)

    设置选定引脚的模拟值。

.. py:function:: pin1.read_digital()

    读取选定引脚的数字值。

.. py:function:: pin1.write_digital(0)

    设置选定引脚的数字值。

无线通讯
--------

.. py:function:: radio.on()

    打开无线通讯。

.. py:function:: radio.off()

    关闭无线通讯。

.. py:function:: radio.reset()

    复位无线通讯。

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

    Bit机器人离线程序的入口，离线程序的主程序需连接在此程序块的下方。

.. py:function:: on_button_action_pressed():

    当Bit对应的按钮被按下时，则会执行程序块下方的程序。

    :param int action: 设置对应按钮，a代表A键，b代表B键。

.. py:function:: on_irbutton_button_pressed():

    当红外遥控器对应的按钮被按下时，则会执行程序块下方的程序。

    :param int button: 设置对应按钮，1-21代表不同的按钮。

.. py:function:: fon_loudness_greater_than_vol():

    当响度大于设置数值时，则会执行程序块下方的程序。

    :param int vol: 可设置响度大小。

控制
-----

.. py:function:: sleep(s* 1000)

    等待N秒后执行其下方的程序，N为圆角矩形框内的数值。

    :param int s: 控制机器人停止运动指定的时间（秒）。

.. py:function:: for count in range(No):
  pass

    重复执行其内部程序N次，N为圆角矩形框中的数值。

    :param int No: 控制机器人重复执行其内部程序,输入的数字即执行次数。

.. py:function:: while True:
  pass

    重复执行程序块内部包含的程序。

.. py:function:: if False:
  pass

    当六边形框内的条件满足时执行程序块内部的程序。

.. py:function:: if False:
  pass
  else:
  pass

    当六边形框内的条件满足时执行那么内部的程序，不满足时执行否则内部的程序。

.. py:function:: while not False:
  pass

    等待直到条件为真时才继续执行接下来的程序块。

.. py:function:: while not False:
  pass

    重复执行其内部的程序，直到六边形框内的条件满足，才执行程序块下方的程序。

侦测
-----

.. py:function:: button_action.is_pressed():

    选择机器人按键触发事件的回调函数。

    :param int action: 设置对应按钮，a代表A键，b代表B键。

.. py:function:: irkeyIsPressed(button):

    如果M按键按下的话，返回值就是True, 否则返回值是false。

    :param int button: 设置对应按钮，1-21代表不同的按钮。

.. py:function:: accelerometer.is_gesture("action"):

    判断机器人的姿态，执行程序块下方的程序。

    :param int action: 设置机器人姿态的对应按钮，包括被摇晃、向上倾斜、正面朝上、自由下落等。

.. py:function:: accelerometer.get_axis()

    返回Bit的x、y和z三个轴的加速度值。

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

    返回Bit机器人头部朝向与地球北极方向的夹角，数值范围为顺时针0~359度。

.. py:function:: compass.get_field_strength()

    反馈当前环境中总磁场强度，单位是纳特斯拉。用磁铁靠近电子罗盘，看看磁场强度有什么变化。

.. py:function:: compass.calibrate()

    校正指南针。

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

.. py:function:: readLineState(No,dir,clr):

    分别用于判断巡线传感器左侧或者右侧是否检测到黑色或白色，条件成立时返回为真。

    :param int No: 可选择巡线传感器模块，0代表模块1、1代表模块2、2代表模块3、3代表模块4。
    :param int dir: 0代表左侧，1代表右侧，2代表全部。
    :param int clr: 0代表黑色，1代表白色。

运算
-----

.. py:function:: No + No
.. py:function:: No - No
.. py:function:: No * No
.. py:function:: No / No

    对输入1和输入2的数字分别进行加减乘除的运算。

    :param int No: 在1和2的输入需要运算的数字，对其进行加减乘除。

.. py:function:: random.randint(No, No)

    在输入1和输入2之间取一个随机的数值。

    :param int No: 在1和2的输入需要运算的数字，在它们之间取一个随机的数值。

.. py:function:: No > No
.. py:function:: No < No
.. py:function:: No = No

    分别为判断左面圆角矩形框内的数值是否大于、小于或等于右面的数值。

    :param int No: 在左面圆角矩形框内和左面圆角矩形框内分别输入需要比较大小的数字，对其进行比较，判断出结果。

.. py:function:: str and str

    当两个六边形框内的条件都满足时，都返回真。

    :param int str: 字符串，可以是文字、字母、数字。

.. py:function:: str or str

    当两个六边形框内的任一条件满足时，都返回真。

    :param int str: 字符串，可以是文字、字母、数字。

.. py:function:: not True:

    当六边形框内的条件不满足时反馈为真。

.. py:function:: []

    数组程序块。

.. py:function:: [No, No2, No]

    数组数字程序块。

    :param int No: 数组数字程序块，可添加不同的数组，1、2、3……

.. py:function:: 'str ' + 'str'

    连接程序块。

    :param int str: 字符串，可以是文字、字母、数字。

.. py:function:: 'str'[No]

    设置连接物的字符程序块。

    :param int str: 字符串，可以是文字、字母、数字。
    :param int No: 代表输入数字的第N-1个字符。

.. py:function:: len('str')

    设置链接物字符。

    :param int str: 字符串，可以是文字、字母、数字。

.. py:function:: 'str'.find('str') > -1

    判断包含程序块。

    :param int str: 字符串，可以是文字、字母、数字。

.. py:function:: No % No

    第一个圆角矩形框内的数值除以第二个圆角矩形框内的数值的余数。

    :param int No: 用输入的第一个数字除以输入的第二个数字，对数值取余。

.. py:function:: round(No)

    取圆角矩形框内数据的整数，小数满0.5，整数位加1。

    :param int No: 取输入数字的整数，小数满0.5，整数位加1。

.. py:function:: math.fabs(No)

    把一个数变成非负数，正数的绝对值是它本身，负数的绝对值是它的相反数，0的绝对值是0。

    :param int No: 取输入数字的绝对值，把一个数变成非负数，正数的绝对值是它本身，负数的绝对值是它的相反数，0的绝对值是0。  

变量
-----













