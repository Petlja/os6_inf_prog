6.5. Вежбање - корњача графика
##############################

Пре него пређеш на задатке за вежбање погледај следећи урађени пример и утврди своје знање:

.. ytpopup:: _Y7YNX1eWAE
    :width: 735
    :height: 415
    :align: center

Шарени облик
''''''''''''
.. level:: 2

.. questionnote::

   Наредни интересантан облик се добија тако што корњача црта црвену
   линију дужине 50 и затим се налево окреће за 31 степен, затим црта
   зелену линију дужине 70 и окреће се налево за 71 степен, затим црта
   плаву линију дужине 90 и окреће се налево за 101 степен након чега
   се цртеж наставља по истом принципу. Напиши програм који анализом
   остатка при дељењу са 3 бројача у петљи одређује шта треба да
   уради.

.. activecode:: периода3
   :nocodelens:
   :enablecopy:
   :playtask:

   import turtle

   turtle.speed(0)
   turtle.width(5)
   for i in range(120):
       if i % 3 == 0:
           turtle.color("red")
           turtle.forward(50)
           turtle.left(31)
       ???
   ====
   import turtle
    
   turtle.speed(0)
   turtle.width(5)
   for i in range(120):
       if i % 3 == 0:
           turtle.color("red")
           turtle.forward(50)
           turtle.left(31)
       if i % 3 == 1:
           turtle.color("green")
           turtle.forward(70)
           turtle.left(71)
       if i % 3 == 2:
           turtle.color("blue")
           turtle.forward(90)
           turtle.left(101)
           
Квадрат шарених ивица
'''''''''''''''''''''
.. level:: 2

.. questionnote::

   Дефиниши процедуру за цртање линије у којој се насумично смењују
   дужи две боје. Параметри процедуре треба да буду број дужи, дужина
   сваке дужи и две боје. Употреби процедуру да нацрташ квадрат коме
   ће ивице бити састављене од таквих линија.

.. activecode:: квадрат_шарених_ивица
   :nocodelens:
   :enablecopy:
   :playtask:

   import turtle
    
   def sarena_duz(n, a, boja1, boja2):
       for ???:
           if i % 2 == 0:
               turtle.color(boja1)
           else:
               turtle.color(boja2)
           ???
    
   turtle.width(10)
   sarena_duz(11, 10, "red", "blue")
   turtle.left(90)
   sarena_duz(11, 10, "green", "yellow")
   ???
   ???
   turtle.left(90)
   ???
   turtle.left(90)
   ====      
   import turtle
    
   def sarena_duz(n, a, boja1, boja2):
       for i in range(n):
           if i % 2 == 0:
               turtle.color(boja1)
           else:
               turtle.color(boja2)
           turtle.forward(a)
    
    
   turtle.width(10)
   sarena_duz(11, 10, "red", "blue")
   turtle.left(90)
   sarena_duz(11, 10, "green", "yellow")
   turtle.left(90)
   sarena_duz(11, 10, "orange", "black")
   turtle.left(90)
   sarena_duz(11, 10, "purple", "cyan")
   turtle.left(90)
   
   
