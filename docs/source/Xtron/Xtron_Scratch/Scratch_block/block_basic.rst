基础积木块编程指南
===================

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

 1. 显示清空

        .. image:: images/according_to_empty.png
            :width: 57

    用来清空LCD屏幕上之前显示的所有内容。在同一个位置显示不同的内容，如果不清空，会和之后显示的内容重叠。
    
    .. image:: images/null.png

 2. 设置屏幕背景色

        .. image:: images/rest.png
            :width: 124.5

    * 该积木块可以设置屏幕的背景色，通过颜色、饱和度、亮度来调节颜色，数值范围均为0~100。
    * 点击下方的【滴管图标】，可以从已有的角色中一键吸取上面的颜色。

    .. image:: images/null.png

3. 设置文本内容程序块

        .. image:: images/draw_text_content.png
            :width: 222

    * 把文本内容显示在某个坐标（x，y）。
    * 文本内容可以是字母、数字，暂时不支持中文显示。
    * 坐标的范围是X：0~160， Y: 0~120
    
    .. image:: images/null.png

 4. 显示生效

        .. image:: images/according_to_take_effect.png
            :width: 57

    在设置好屏幕背景以及屏幕显示内容后，加上显示生效积木块，屏幕上才会显示我们设置好的背景及内容。

    .. image:: images/null.png

 例子：
    
    * 设置屏幕背景颜色为蓝色；
    * 在屏幕的中间循环显示“ Hello! Welcome to Xtron!", 每次显示一个单词。

        .. image:: images/lizi3.png
            :width: 196

 5. 设置画笔颜色

        .. image:: images/brush_color.png
            :width: 113

    * 设置画笔的颜色，通过颜色、饱和度、亮度来调节颜色，数值范围均为0~100。
    * 点击下方的【滴管图标】，可以从已有的角色中一键吸取上面的颜色。
    * 设置画笔颜色后，绘制的图形以及显示的文字都会使用该颜色。

    .. image:: images/null.png

 6. 绘制线一条水平或者垂直的线段

        .. image:: images/draw_line_length.png
            :width: 254.5

    * 在某个坐标（x，y）绘制一条水平或垂直的线段，线的长度≤显示屏的长度。
    * 坐标的范围是X：0~160， Y: 0~120
    * 如果是水平线，线段长度+ X的坐标<160; 如果是垂直线，线段长度+ Y的坐标<120. 否则线段显示不完整。
    * 所有绘制的图案，都要加上显示生效积木块，才会在屏幕上显示出来。
    
    .. image:: images/null.png

 7. 绘制一条线段

        .. image:: images/draw_the_line.png
            :width: 265

    * 绘制一条从一个坐标（x1，y1）到另一个坐标（x2，y2）的线段
    * 坐标的范围是X：0~160， Y: 0~120
    * 和上一个积木块的区别是，这个积木块绘制的线段是任意的方向，上一个只能是水平或者垂直方向。
    
    .. image:: images/null.png

 8. 绘制一个矩形

        .. image:: images/draw_a_rectangle.png
            :width: 305

    * 在某个坐标（x，y）处绘制一个矩形，通过设置矩形的宽和高来设置矩形的大小。
    * 可以选择实心矩形或者是空心矩形。
    * 坐标的范围是X：0~160， Y: 0~120。
    * 如果坐标值加上矩形大小，超过了显示范围，会显示不完整。
    
    .. image:: images/null.png

 9. 绘制一个圆形

        .. image:: images/draw_a_hollow_circle.png
            :width: 254.5

    * 在某个坐标（x，y）绘制一个圆形，通过设置圆的半径来改变圆的大小。
    * 可以选择实心圆形或者是空心圆形。
    * 坐标的范围是X：0~160， Y: 0~120
    * 如果坐标值加上矩形大小，超过了显示范围，会显示不完整。
    
    .. image:: images/null.png

 10. 绘制一个三角形

        .. image:: images/draw_a_hollow_triangle.png
            :width: 540

    * 通过设置三角形三个点的坐标（x1，y1）、（x2，y2）、（x3，y3）来绘制一个三角形。
    * 可以选择实心三角形或者是空心三角形。
    * 坐标的范围是X：0~160， Y: 0~120

     .. image:: images/null.png

 11. 设置RGB颜色

        .. image:: images/red_green_blue.png
            :width: 208.5

    * 该程序块用来设置RGB的颜色，在设置屏幕颜色或者画笔颜色的时候，可以用指定的RGB的值来设置颜色。
    * 红绿蓝三种颜色的数值范围分别为0~255。
    * 比如红色有很多种：粉红（255,192,203，深红（220,20,60），淡紫红（255,240,245），弱紫罗兰红（219,112,147），深粉红（255,20,147）等，我们通过设置不同的RGB值就可以精确的显示不同的颜色。
    
    .. image:: images/null.png

 例子：

    * 按向上按钮，选择画笔的颜色；
    * 按向下按钮，用选择的画笔颜色画一个实心矩形；
    * 按向左按钮，用选择的画笔颜色画一个水平线段；
    * 按向右按钮，用选择的画笔颜色画一个空心三角形；

         .. image:: images/lizi4.png
            :width: 543.5


声音
-----

 1. 播放音符

        .. image:: images/play_tone.png
            :width: 188

    * 该积木块可以播放音符，音符以及节拍长度可以在下拉框里选择。
    * 点击音符，显示的是中央C的音调，可以用左右两边的箭头来切换高低音，左边是低音，右边是高音。
    * 简谱和音名的对应关系：我们在生活中，一般接触到的都是1234567这样的简谱，但我们积木块是用五线谱的音名来显示的，在C调的乐谱中，它们之间的对应关系如下。

        .. image:: images/music.png

     C调中，C、D、E、F、G、A、B分别对应简谱中的1、2、3、4、5、6、7，一个唱名为四分音符持续1个节拍，下方有一个横杠的是八分音符持续1/2节拍，音符后有一个横杠的为二分音符持续2个节拍，同学们按照音符和节拍数编写整段音乐。

     比如下面的上学歌，不划线是四分音符，在这首曲子中是一个节拍，一道下划线的节拍相当于八分音，在这首曲子中是1/2拍。
    
     一些音符后面会加-，表示音符持续，例如7 - 代表 7 这个音占了两个节拍，7- - 则表示3个节拍。

        .. image:: images/song.png
    
    .. image:: images/null.png

 2. 暂停播放

        .. image:: images/rest.png
            :width: 152

    使用该积木块可以停止声音，停止的节拍数可以在下拉框中选择。
    
    .. image:: images/null.png








