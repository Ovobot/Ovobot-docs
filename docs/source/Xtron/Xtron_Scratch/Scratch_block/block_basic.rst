基础积木块编程指南
===================

    以下是使用Scratch给Xtron编程的快速参考，如果你有一些积木块不确定使用方法的话，可以参考下面的说明和例子。


灯光
-----

 1. 设置板载LED

        .. image:: images/set_the_onboard.png
            :width: 176

    * Xtron上有2个LED灯，可以分别设置熄灭和点亮。
    * 这两个LED灯还用来作为状态的指示灯，比如充电时led1亮红灯，下载代码时led1闪红灯，开机时led2亮蓝灯后熄灭。

    .. image:: images/null.png

 2. 板载LED电平反转

        .. image:: images/onboard_level_inversion.png
            :width: 141

    每次执行该程序块会把对应LED电平反转，即Xtron的led灯从点亮变为熄灭，或者从熄灭变为点亮。

    .. image:: images/null.png

 3. 设置板载LED亮度

        .. image:: images/the_onboard_brightness.png
            :width: 195

    * 该程序块可以设置Xtron板载的led灯的亮度，数值范围为0~255。
    * 在点亮LED之后再设置亮度才生效，而且只调节前面程序里已经点亮的LED灯的亮度值。

    .. image:: images/null.png

 例子：

    * 先点亮LED1,等待1S后熄灭LED1. 1s之后，再次点亮LED1，并且设置亮度为40，最后1s后熄灭LED1.
    * 我们看到的现象是：LED1以1S的时间间隔闪烁一次后，亮度变小，又闪烁一次。

        .. image:: images/lizi1.png
            :width: 234

 4. 设置板载RGB灯颜色

        .. image:: images/onboard_RGB_lights.png
            :width: 202

    * Xtron上有4个RGB灯，可以分别设置不同的颜色，通过颜色、饱和度、亮度来调节颜色，数值范围均为0~100。

    * 点击颜色下方的【滴管图标】还可以从已有的角色中一键获取角色上的任意颜色。
    
    .. image:: images/null.png

 5. 设置板载RGB所有灯颜色

        .. image:: images/onboard_RGB_all_lights.png
            :width: 188.5

    * 可以将板载上的4个RGB灯，同时设置为相同的颜色，通过颜色、饱和度、亮度来调节颜色，数值范围均为0~100。
    * 同样的，还可以从选择的角色中一键吸取已有的颜色。
    * 和上面的程序块的区别是，上面的是单独设置某一个RGB灯，这个程序块则是同时设置所有的RGB灯。
    
    .. image:: images/null.png

 6. 设置板载RGB灯亮度

        .. image:: images/brightness_of_onboard_RGB_lamp.png
            :width: 157.5

    * 该程序块用来设置Xtron板载的RGB灯的亮度。
    * 设置亮度值之后，再设置RGB灯的颜色，亮度值才生效。如果你想改变亮度值的话，你需要设置亮度值之后，再次设置一下对应的RGB灯颜色。

    .. image:: images/null.png

 例子：

    * 设置RGB1亮度值为0.5，并且显示紫色，1S之后，RGB1变亮并且换成红色。
    * 看到的现象是， RGB1在紫色和红色之间不停的变化显示，并且两个颜色高度不同。

        .. image:: images/lizi2.png
            :width: 234

显示
-------

 1. 显示清空程序块

        .. image:: images/according_to_empty.png
            :width: 57

    显示清空。
    
    .. image:: images/null.png

 2. 设置屏幕背景色程序块

        .. image:: images/rest.png
            :width: 124.5

    设置屏幕的背景色，通过颜色、饱和度、亮度来调节颜色，数值范围均为0~100。还可以从选择的角色中一键吸取已有的颜色。

    .. image:: images/null.png

 3. 显示生效程序块

        .. image:: images/according_to_take_effect.png
            :width: 57

    显示生效。

    .. image:: images/null.png

 4. 设置画笔颜色程序块

        .. image:: images/brush_color.png
            :width: 113

    设置画笔的颜色，通过颜色、饱和度、亮度来调节颜色，数值范围均为0~100。
    还可以从选择的角色中一键吸取已有的颜色。

    .. image:: images/null.png

 5. 设置文本内容程序块

        .. image:: images/draw_text_content.png
            :width: 222

    绘制某个坐标（x，y）的文本内容，文本内容可以是字母、数字、文字。
    
    .. image:: images/null.png

 6. 绘制线长度程序块

        .. image:: images/draw_line_length.png
            :width: 254.5

    绘制某个坐标（x，y）的水平线或垂直线，线的长度≤显示屏的长度。
    
    .. image:: images/null.png

 7. 绘制线坐标程序块

        .. image:: images/draw_the_line.png
            :width: 265

    绘制从一个坐标（x1，y1）到另一个坐标（x2，y2），两个特定的坐标之间连成一条线。
    
    .. image:: images/null.png

 8. 设置空心矩形程序块

        .. image:: images/draw_a_rectangle.png
            :width: 305

    在某个坐标（x，y）绘制空心矩形或实心矩形，通过设置矩形的宽和高来改变矩形的大小。
    
    .. image:: images/null.png

 9. 设置空心圆程序块

        .. image:: images/draw_a_hollow_circle.png
            :width: 254.5

    在某个坐标（x，y）绘制空心圆或实心圆，通过设置圆的半径来改变圆的大小。
    
    .. image:: images/null.png

 10. 设置空心三角形程序块

        .. image:: images/draw_a_hollow_triangle.png
            :width: 540

    绘制空心三角形或实心三角形，通过设置三角形三个点的坐标（x1，y1）、（x2，y2）、（x3，y3）来改变三角形的大小。

    .. image:: images/null.png

 11. 设置RGB颜色程序块

        .. image:: images/red_green_blue.png
            :width: 208.5

    红绿蓝三种颜色的数值范围分别为0~255。
    
    .. image:: images/null.png

声音
-----

 1. 播放音符程序块

        .. image:: images/play_tone.png
            :width: 188

    可以选择播放的音符和音符播放的节拍数。
    
    .. image:: images/null.png

 2. 暂停播放节拍程序块

        .. image:: images/rest.png
            :width: 152

    可以选择播放的音符和音符播放的节拍数。
    
    .. image:: images/null.png








