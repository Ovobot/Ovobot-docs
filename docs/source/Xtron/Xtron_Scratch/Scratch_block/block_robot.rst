xtron机器人积木块编程指南
=============================

    如果你想做一个机器人，你可以把Xtron当作机器人的大脑。当然，机器人不能只有大脑，我们需要给它配上一些传感器以及一些硬件模块。

    Ovobot Xtron是Xtron的机器人扩展，它有一个4PIN接口，通过I2C总线连接Ovobot所有的传感器和硬件模块，还有一个包含了IO口、SPI、PWM和I2C功能的20PIN接口。

        .. image:: images/extend1.png

    下面是Xtron的机器人扩展积木块，你可以用这些积木块来让机器人运动，声音传感器让机器人有了听力，超声波和巡线传感器则可以帮助机器人更好的完成一些任务。

    1.设置机器人移动速度

        .. image:: images/x_movement_speed.png
            :width: 194

    该积木块用来设置机器人的前进或后退的速度，数值范围为0~255。

    2.设置机器人移动速度及时间

        .. image:: images/x_movement_speed_time.png
            :width: 283
    
    和上面的积木块的区别是，上一个积木块需要加停止程序才可以让机器人停止运动。而这个积木块有持续时间，持续时间结束后，机器人就停止运动了。


    3.设置旋转速度

        .. image:: images/x_rotation_speed.png
            :width: 194

    设置机器人向左或者向右的旋转速度，速度范围为0~255。

    4.设置旋转速度及时间

        .. image:: images/x_rotation_speed_time.png
            :width: 283

    设置机器人向左或者向右的旋转速度以及持续时间，速度范围为0~255。区别同上。   

    5.停止运动

        .. image:: images/x_stop_move.png
            :width: 97

    可以用该积木块让机器人停止运动。  

    6.驱动电机

        .. image:: images/x_drive_motor.png
            :width: 230

    * 该程序块可以分别设置机器人的左右两个轮子的速度，来实现前进，后退，转弯。 
    * 当左右转速相同，并且数值>0的时候，机器人按照设置速度前进。
    * 当左右转速相同，并且数值<0的时候，机器人按照设置速度后退。
    * 当左轮>0,右轮<0，机器人是左转。   
    * 当右轮>0,左轮<0，机器人是右转。


    7.控制舵机转动

        .. image:: images/steering_gear_rotating.png
            :width: 181

    该积木块可以控制舵机旋转到一定的角度，旋转度数的范围大小是-90~90。可用来制作丰富的带舵机的小制作。

    8.响度

        .. image:: images/x_loudness.png
            :width: 83

    我们用响度来表示声音传感器的反馈值，响度的范围大小是0~255。

    9.超声波传感器距离

        .. image:: images/x_ultrasonic_distance.png
            :width: 238

    该积木块返回值是机器人的超声波传感器检测到离障碍物的距离。

    10.超声波传感器检测到障碍物程序块

        .. image:: images/ultrasonic_detection_of_obstacles.png
            :width: 287

    反馈机器人的超声波传感器是否检测到障碍物。是的话返回值是True, 否则返回值是False.

    11.巡线传感器数值程序块

        .. image:: images/tracking_sensor_value.png
            :width: 271.5

    该积木块可以分别反馈巡线传感器左右两个光电对管检测的灰度值，黑色物体的返回值接近0，白色物体返回值接近255。

    12.巡线传感器颜色检测程序块

        .. image:: images/ultrasonic_color.png
            :width: 363.5

    分别用于判断巡线传感器左侧或者右侧是否检测到黑色或白色，条件成立时返回为真。

