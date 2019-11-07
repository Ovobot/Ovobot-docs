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

    控制机器人向指定的方向以一定的速度运动。

    :param int dir: 可以为0或者1，0：机器人向前运动，1：机器人向后运动。
    :param int speed: 设置机器人运动的速度，数值范围为0~255。

.. py:function:: move(dir, speed, ms)

    控制机器人向指定的方向以一定的速度运动。

    :param int dir: 可以为0或者1，0：机器人向前运动，1：机器人向后运动。
    :param int speed: 设置机器人运动的速度，数值范围为0~255。
    :param int ms: 控制机器人持续运行指定的时间（毫秒）。

外观
-----

声音
-----

引脚
-----

无线通信
--------

事件
-----

控制
-----

侦测
-----

运算
-----

变量
-----

