xtron机器人积木块编程指南
=============================

小车扩展
---------

设置移动速度程序块
""""""""""""""""""

.. image:: images/x_movement_speed.png
   :width: 194

设置Bit的前进或后退的速度，数值范围为0~255。

设置移动速度及时间程序块
""""""""""""""""""""""""

.. image:: images/x_movement_speed_time.png
   :width: 283

通过设定机器人运动方向、运动速度和持续时间来让机器人运动，速度范围为0~255。

设置旋转速度程序块
"""""""""""""""""""

.. image:: images/x_rotation_speed.png
   :width: 194

设置机器人向左或者向右的旋转速度，速度范围为0~255。

设置旋转速度及时间程序块
""""""""""""""""""""""""

.. image:: images/x_rotation_speed_time.png
   :width: 283

设置机器人向左或者向右的旋转速度以及持续时间，速度范围为0~255。   

停止运动程序块
"""""""""""""""

.. image:: images/x_stop_move.png
   :width: 97

设置左右两个电机的运动速度为0。  

驱动电机程序块
"""""""""""""""

.. image:: images/x_drive_motor.png
   :width: 230

分别驱动Bit的左右两个轮子的转速。  

控制舵机旋转度数程序块
"""""""""""""""""""""""

.. image:: images/steering_gear_rotating.png
   :width: 181

Xtron控制舵机旋转，旋转度数的范围大小是-90~90。

响度程序块
"""""""""""

.. image:: images/x_loudness.png
   :width: 83

我们用响度来表示声音传感器的反馈值，响度的范围大小是0~255。

超声波传感器距离程序块
"""""""""""""""""""""""

.. image:: images/x_ultrasonic_distance.png
   :width: 238

反馈Bit机器人超声波传感器检测到的距离。

超声波传感器检测到障碍物程序块
"""""""""""""""""""""""""""""""

.. image:: images/ultrasonic_detection_of_obstacles.png
   :width: 287

反馈Bit机器人超声波传感器有没有检测到障碍物。

巡线传感器数值程序块
""""""""""""""""""""""

.. image:: images/tracking_sensor_value.png
   :width: 271.5

可以分别反馈巡线传感器左右两个光电对管检测的灰度值，黑色物体的返回值接近0，白色物体返回值接近255。

巡线传感器颜色检测程序块
"""""""""""""""""""""""""

.. image:: images/ultrasonic_color.png
   :width: 363.5

分别用于判断巡线传感器左侧或者右侧是否检测到黑色或白色，条件成立时返回为真。

