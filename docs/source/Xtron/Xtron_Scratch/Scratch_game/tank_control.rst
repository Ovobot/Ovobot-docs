第三课 坦克控制
==================

今日任务:  
""""""""""""

    今天我们要制作一个可以利用Xtron的按键控制（上下左右）方向、发射子弹的坦克，
    并且，当“子弹”击中敌方坦克时，敌方坦克会发生“爆炸”。

任务拆解:  
""""""""""""

    .. image:: images/TKKZ1.png
        :width: 500

动手操作：
""""""""""""

    第一步：绘制角色1（坦克）。小提示：用左侧的矩形工具绘制更方便！

    .. image:: images/TKKZ2.png
        :width: 500

    第二步：绘制角色2（炮弹），可以使用毛笔工具绘制，数值可以设置为20。

    .. image:: images/TKKZ3.png
        :width: 500

    两个角色（角色1、角色2绘制完如下）：

    .. image:: images/TKKZ4.png
        :width: 400

    第三步：为角色1添加脚本。

    .. image:: images/TKKZ5.png
        :width: 280

    新建消息，输入新消息的名称fire。

    .. image:: images/TKKZ6.png
        :width: 300

    第四步：为角色2添加脚本。

    .. image:: images/TKKZ7.png
        :width: 400

    第五步：看运行结果。

    .. image:: images/TKKZ8.png
        :width: 300

    第六步：接下来我们来创作子弹碰到敌方坦克后，敌方坦克“爆炸”的效果。

    绘制角色3（敌方坦克）：

    .. image:: images/TKKZ9.png
        :width: 400

    为角色3 设计第二个爆炸造型：

    .. image:: images/TKKZ10.png
        :width: 300

    为角色3 设计脚本：

    .. image:: images/TKKZ11.png
        :width: 300

课后思考：
""""""""""""

    （1）会用变量的同学可以思考一下怎么计分？（击中一辆敌方坦克+1分？）

    （2）我们利用上面的程序制作出的我方坦克虽然可以上下移动，但是只能向上发射子弹，
    怎么才能让我方坦克可以根据坦克面向的方向，向上下左右四个方向发射子弹呢？











