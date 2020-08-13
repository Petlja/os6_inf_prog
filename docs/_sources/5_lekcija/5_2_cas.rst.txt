
5.2. Корњача графика - понављање
################################


У програмима које задајемо корњачи често су облици правилни и неке се
наредбе понављају. Стога у програмима можемо користити и
петље. 

Квадрат - петља
'''''''''''''''
.. level:: 1
	   
.. questionnote::

   Исправи наредни програм тако да корњача црта квадрат чија је
   страница дугачка 100 корака.

Програм који исцртава квадрат можемо да скратимо ако уведемо наредбу
којом постижемо да се неки задати низ наредби више пута понови. Као
што смо видели, у језику Python најлакши начин да се то уради је
наредба ``for``.  Као што смо већ видели, наредбу *ponovi n puta*
можемо записати као ``for i in range(n):``. Подсетимо се, не смемо да
заборавимо двотачку, а наредбе које се понављају наводимо увучене
неколико размака у односу на положај наредбе ``for``.
   
.. activecode:: корњача_квадрат_петља
   :nocodelens:

   import turtle
   for i in range(0):        # ponovi 4 puta:
       turtle.forward(0)     #   idi napred 100 koraka
       turtle.left(0)        #   okreni se nalevo za 90 stepeni

Погледај наредни видео:

.. ytpopup:: d1vAfYFq-l8
    :width: 735
    :height: 415
    :align: center


Провери своје разумевање петљи тако што ћеш поређати наредбе програма
у ком корњача исцртава једнакостранични троугао.

.. parsonsprob:: троугао_ређање

   Поређај делове кода тако да представљају исправно решење овог задатка.
   -----
   import turtle
   =====
   turtle.color("red")
   =====
   for i in range(3):
   =====
      turtle.forward(100)
   =====
      turtle.left(120)

       
Испрекидана линија
''''''''''''''''''
.. level:: 1

.. questionnote::

   У једном од претходних задатака нацртали смо испрекидану линију
   тако што смо пуно пута понављали исте наредбе. Скрати претходни
   програм коришћењем петље тако што ћеш нацртати испрекидану линију
   која се састоји од пет делова.

.. activecode:: испрекидана_линија
   :nocodelens:
   :enablecopy:
   :playtask:

   import turtle
   for i in range(5):
                                  # idi napred 20 koraka
                                  # podigni olovku
                                  # idi napred 20 koraka
                                  # spusti olovku
   ====
   import turtle
   for i in range(5):
       turtle.forward(20)           # idi napred 20 koraka
       turtle.penup()               # podigni olovku
       turtle.forward(20)           # idi napred 20 koraka
       turtle.pendown()             # spusti olovku


Погледај наредни видео:

.. ytpopup:: JeoAB84nG7w
    :width: 735
    :height: 415
    :align: center


Отисци корњаче
''''''''''''''
.. level:: 1

.. questionnote::
   
   Напиши програм који коришћењем понављања исцртава 5 отисака корњаче
   размакнутих по 30 пиксела. Напиши програм без коришћења петље, а
   затим га скрати коришћењем петље.


.. activecode:: пет_отисака_корњаче
   :nocodelens:
   :enablecopy:
   :playtask:

   import turtle
   ====
   import turtle
   turtle.penup()
   turtle.shape("turtle")
   for i in range(5):
       turtle.stamp()
       turtle.forward(30)


       

