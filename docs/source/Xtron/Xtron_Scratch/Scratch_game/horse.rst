第七课 赛马
==============

今日任务:  
""""""""""""

    今天我要和同学们一起来设计一个赛马的小程序，你可以控制程序中的一匹马，然后按Xtron上的向右方向键（或其他按键），让这匹马跑起来，按下Xtron上的A键（或B键），马儿跳起来越过跑道上的蓝色线条。
    当然，如果想成为第一匹冲线的小马，那就要看你的运气和按键的使用了！

任务拆解:
""""""""""""

    .. image:: images/SM1.png
       :width: 500

动手操作：
""""""""""""

    第一步：设计游戏主场景、失败场景、胜利场景。

    .. image:: images/SM2.png
       :width: 500

    .. image:: images/SM3.png
       :width: 500

    .. image:: images/SM4.png
       :width: 500

    .. image:: images/SM5.png
       :width: 200

    第二步：确定主持人角色、小马角色（自己控制的小马，
    通过颜色编辑的方式修改一下颜色，进行区分），将以上各个角色摆放至舞台之上，如下图：

    .. image:: images/SM6.png
       :width: 500

    .. image:: images/SM7.png
       :width: 500

    第三步：角色全部就位，下面我们要考虑如何脚本的问题了，我们先从主持人开始，
    主持人的功能是讲解游戏规则和被点击之后游戏开始，我给大家些提示：

    .. image:: images/SM8.png
       :width: 140

    如何实现支持人被点击后，游戏开始呢？

    .. image:: images/SM9.png
       :width: 80

    想想！谁要接收这个广播呢？

    不要以为上面的想清楚了就结束了，
    这个主持人被点击之后还能一直待在舞台上么？如果想让这个主持人被点击之后消失掉，怎么实现？

    .. image:: images/SM10.png
       :width: 100

    第四步：编程时，头脑一定要清晰，刚才我问了一个问题，谁应该接收start game广播呢？答案肯定是小马们了，
    接下来就是比较关键的为小马编写脚本，我们这步先为陪跑的小马编写脚本，最后在为我们控制的小马编写脚本。

    .. image:: images/SM11.png
       :width: 200

    给小马们设定一个初始位置x和y，统一在起跑线位置出发。

    .. image:: images/SM12.png
       :width: 300

    这步有什么用？为什么是随机数？

    .. image:: images/SM13.png
       :width: 250

    这个颜色就是终点线的颜色！

    .. image:: images/SM14.png
       :width: 400

    陪跑的小马碰到终点线，应该有什么操作？想一想！

    提示：

    .. image:: images/SM15.png
       :width: 100

    这个hit可以理解为撞（终点）线的意思！那么，问题又来了，谁接收这个hit广播呢？

    第五步：我们为自己控制的小马（本例中蓝色小马）编写脚本。

    .. image:: images/SM11.png
       :width: 200

    给小马设定一个初始位置x和y，统一在起跑线位置出发。

    .. image:: images/SM12.png
       :width: 300

    重复执行什么？我们这匹自己控制的小马身上肩负的使命可不少啊！首先，按下右键，他可以移动；其次，按下A或B键，
    他可以跳跃；然后，如果他第一个冲到终点，游戏胜利！不是第一个冲到终点，游戏失败！
    还有，碰到蓝色线条游戏失败！肩负着这么多使命（判断），头脑中的脚本就成型了。

    右键移动：

    .. image:: images/SM17.png
       :width: 250

    这步想明白了么？

    .. image:: images/SM18.png
       :width: 300

    终点胜利：这步你好好想想！为啥自己控制的小马到了终点就胜利呢？

    .. image:: images/SM19.png
       :width: 230

    A或B键跳跃：

    .. image:: images/SM20.png
       :width: 220

    .. image:: images/SM21.png
       :width: 220

    A或B键跳跃的脚本我实现的比较笨，你自己想想有没有更好的跳跃方式，可以越过蓝色线条！

    碰到蓝色线条失败：

    .. image:: images/SM22.png
       :width: 200

    或自己控制的小马脚本到这还么有结束，为啥？刚才我问了一个问题，为什么其他陪跑的小马碰到终点线要判断一下自己是不
    是第一个过线的，那么自己控制的小马为什么不需要判断直接就认定游戏胜利呢？
    原因是，那个hit的广播其实就是广播给自己控制的小马的！

    .. image:: images/SM23.png
       :width: 140

    这下明白了吧！

    第六步：把陪跑小马的脚本依次复制给角色2、4、5、6，别忘了改一下x和y的值！这是是否细心的问题，当然，如果没改出了错，你肯定也知道哪儿错了！

    第七步：别忘了我们的场景哟！

    .. image:: images/SM24.png
       :width: 400

    第八步：运行一下你的程序，看看有没有什么bug。

课后反思：
""""""""""""

    （1）如果一开始我不指定哪匹小马是我控制的，我在游戏中随机选择一个小马进行比赛，这个怎么实现？

    （2）无论游戏胜利和失败，我想让主持人出来说胜利或失败，这个怎么实现？












