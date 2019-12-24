视觉识别摄像头积木块编程指南
===============================

实时调试的时候MU跑完一次要复位

视觉识别
---------

初始化端口程序块
""""""""""""""""""

.. image:: images/initialization_port.png
   :width: 231

MU00代表智能识别摄像头，此外还包括MU01、MU10、MU11等摄像头，初始化端口程序块
即初始化所设置的摄像头和端口。

恢复默认设置程序块
""""""""""""""""""

.. image:: images/restore_the_default.png
   :width: 184

将智能识别摄像头恢复默认设置。

算法检测程序块
""""""""""""""""""

.. image:: images/algorithm_testing.png
   :width: 282

智能识别摄像头可以检测各种算法，算法包括色块检测、颜色识别、球体检测、人体检测、形状卡片、交通卡片、数字卡片。

判断摄像头检测程序块
""""""""""""""""""""""

.. image:: images/camera_detection.png
   :width: 250

判断智能识别摄像头是否检测到某种算法，然后执行下一条指令。

检测到颜色识别程序块
""""""""""""""""""""""

.. image:: images/color_recognition_detected.png
   :width: 309

判断智能识别摄像头是否检测到设置坐标的颜色识别，然后执行下一条指令。

检测到色块颜色程序块
""""""""""""""""""""""

.. image:: images/patch_testing.png
   :width: 291.5

判断智能识别摄像头是否检测到黑、白、红、黄等色块，然后执行下一条指令。

获取算法程序块
"""""""""""""""

.. image:: images/acquisition_algorithm.png
   :width: 342

获取选定智能识别摄像头的纵向坐标、横向坐标、宽度、高度的算法检测。

获取颜色识别程序块
"""""""""""""""""""

.. image:: images/get_color_recognition.png
   :width: 279.5

获取智能识别摄像头在红、绿、蓝等不同通道的颜色识别。

获得算法形状卡片程序块
"""""""""""""""""""""""

.. image:: images/get_shape_card.png
   :width: 286

获得算法形状卡片，钩、叉、圆形、三角形，用来执行下一条特定的指令。

获得算法交通卡片程序块
""""""""""""""""""""""

.. image:: images/transportation_card.png
   :width: 298.5

获得算法交通卡片，向左、向右、掉头、停车，用来执行下一条特定的指令。

获得算法数字卡片程序块
""""""""""""""""""""""

.. image:: images/digital_card.png
   :width: 281.5

获得算法数字卡片,0～9，用来执行下一条特定的指令。

获得算法颜色识别程序块
""""""""""""""""""""""

.. image:: images/color_identification.png
   :width: 312

获得算法颜色识别，不同颜色执行不同的指令。

LED识别颜色程序块
""""""""""""""""""

.. image:: images/recognize_color.png
   :width: 402.5

分别设置led1、led2识别到某种颜色或未识别到某种颜色，执行下一条指令。

设置算法性能程序块
""""""""""""""""""

.. image:: images/algorithm_performance.png
   :width: 327

可以对算法进行优先级排序，设置某种算法的速度优先、性能均衡或准确率优先。

数码变焦程序块
"""""""""""""""

.. image:: images/digital_zoom.png
   :width: 219

设置智能识别摄像头的数码变焦，分为自动及1～5个等级。

摄像头白平衡程序块
""""""""""""""""""

.. image:: images/camera_white_balance.png
   :width: 241.5

设置智能识别摄像头的白平衡，分为自动、锁定白平衡、白光模式和黄光模式。

高帧率模式程序块
""""""""""""""""""

.. image:: images/high_frame_rate.png
   :width: 219

设置智能识别摄像头的高帧率模式。






