1.2. Бројачка петља `for`
#######################################

Често робот исту наредбу треба да понови више пута. Да би се такви
програми могли једноставније писати је коришћење **петљи**. Хајде прво да погледамо следећи видео:

.. ytpopup:: TnXzzmUIC70
    :width: 735
    :height: 415
    :align: center

У наставку ћеш се детаљније упознати са **бројачком петљом**.


Иди 8 поља напред
'''''''''''''''''
.. level:: 1
           

.. questionnote::

   У наредном лавиринту постоји 8 поља испред робота. Коришћењем
   петље учини да робот дође до лоптице и да је затим покупи.

Један начин да решимо задатак је да роботу 8 пута задамо наредбу да
иде напред и затим наредбу да покупи лоптицу.
   
.. karel:: Карел_8_поља_напред
   :blockly:

   {
      setup: function() {
	   var world = new World(9, 1);
           world.setRobotStartAvenue(1);
           world.setRobotStartStreet(1);
           world.setRobotStartDirection("E");
	   world.putBall(9, 1);
           var robot = new Robot();
	   var code = ["from karel import *",
	       "napred()", "napred()", "napred()", "napred()", "napred()", "napred()", "napred()", "napred()", "uzmi()"]
	   return {world: world, robot: robot, code: code};
      },

      isSuccess: function(robot, world) {
           return robot.getStreet() === 1 &&
           robot.getAvenue() === 9 &&
	   world.getBalls(9, 1) == 0;
      }
   }


Замислимо колико би досадно било куцати десет или сто пута наредбу да
робот иде напред, када би лавиринт био већи. Пошто се у програмима
често јавља потреба да се неке наредбе понављају, сви програмски
језици обезбеђују начин да се то постигне. У програмском језику
Python, који наш робот Карел разуме, понављање се постиже коришћење
наредбе ``for``. Понављања у програмима се називају **циклуси** или
**петље** (по чему је наша фондација "Петља" добила име). Погледајмо
како се претходни програм може скратити употребом петље ``for``.

.. karel:: Карел_8_поља_напред_for
   :blockly:

   {
      setup: function() {
	   var world = new World(9, 1);
           world.setRobotStartAvenue(1);
           world.setRobotStartStreet(1);
           world.setRobotStartDirection("E");
	   world.putBall(9, 1);
           var robot = new Robot();
	   var code = ["from karel import *",
	       "for i in range(8):", "    napred()", "uzmi()"]
	   return {world: world, robot: robot, code: code};
      },

      isSuccess: function(robot, world) {
           return robot.getStreet() === 1 &&
           robot.getAvenue() === 9 &&
	   world.getBalls(9, 1) == 0;
      }
   }

Овде смо употребили петљу ``for i in range(n):`` која је уобичајени
начин да се изрази да се наредбе наведене у телу петље извршавају
``n`` пута (ми смо уместо ``n`` навели ``8``, чиме смо постигли то да
се наредба ``napred()`` изврши 8 пута). Овим смо дакле рекли "Понови
пет пута корак напред". Уместо ``i`` смо могли употребити и неко друго
слово или реч (или знак ``_``).

Наредбе које се понављају (за њих се каже да чине **тело** петље) се
обавезно морају увући у односу на наредбу ``for`` (обично помоћу
неколико размака, најчешће 4, или једног табулатора тј. карактера
*Tab* који се на тастатурама налази лево од тастера *Q*). Када се
петља заврши, извршава се наредба која је наведена иза петље и то
поравната са речју ``for`` (у претходном програму то је наредба
``uzmi()``).  Наредба ``uzmi()`` након петље ``for`` није увучена, што
значи да се она извршава само једном и то када се заврши извршавање
петље ``for`` тј. када се њено тело изврши одговарајући број
пута. Када би она била увучена и она би се понављала.

Неке честе грешке
'''''''''''''''''

Нагласимо да се на крају линије у којој се употребљава наредба ``for``
обавезно ставља двотачка (симбол ``:``). Ако се она не наведе добићеш
поруку о грешци

::

   SyntaxError: bad input on line ???

Ово значи ``Синтаксичка грешка: лош унос на линији ???`` - број линије
ти може указати на то где је грешка направљена (немој да заборавиш да
провериш и линију изнад те). Јако честа грешка програмера-почетника је
да забораве двотачку на крају наредбе ``for`` - обрати пажњу на тај
важан детаљ.

Ако заборавиш да увучеш тело петље, поново ћеш добити поруку

::

   SyntaxError: bad input on line ???

Још једна грешка која може наступити услед неодговарајућег увлачења
наредби је и

::
   
   IndentationError: unindent does not match any outer indentation level on line ???

На енглеском језику ``IndentationError`` значи *Грешка у
увлачењу*.


У складу са претходном дискусијом, исправи наредни програм.

.. karel:: Карел_8_поља_напред_for_грешке

   {
      setup: function() {
	   var world = new World(9, 1);
           world.setRobotStartAvenue(1);
           world.setRobotStartStreet(1);
           world.setRobotStartDirection("E");
	   world.putBall(9, 1);
           var robot = new Robot();
	   var code = ["from karel import *",
	       "for i in range(8)", "napred()", " uzmi()"]
	   return {world: world, robot: robot, code: code};
      },

      isSuccess: function(robot, world) {
           return robot.getStreet() === 1 &&
           robot.getAvenue() === 9 &&
	   world.getBalls(9, 1) == 0;
      }
   }


Петљама ћемо се много детаљније бавити у поглављу `Понављање
<Ponavljanje.html>`_.

Иди 7 поља напред
'''''''''''''''''
.. level:: 1

Пробај сада самостално да допуниш наредни програм тако да робот покупи
лоптицу. Не заборави да се пре петље окрене у правом смеру.

.. karel:: Карел_7_поља_напред
   :blockly:

   {
      setup: function() {
	   var world = new World(1, 8);
           world.setRobotStartAvenue(1);
           world.setRobotStartStreet(1);
           world.setRobotStartDirection("E");
	   world.putBall(1, 8);
           var robot = new Robot();
	   var code = ["from karel import *"]
	   return {world: world, robot: robot, code: code};
      },

      isSuccess: function(robot, world) {
           return robot.getStreet() === 8 &&
           robot.getAvenue() === 1 &&
	   world.getBalls(1, 8) == 0;
      }
   }

.. reveal:: Карел_7_поља_напред_reveal
   :showtitle: Прикажи решење
   :hidetitle: Сакриј решење

   Карел треба прво да се окрене налево, затим да иде 7 пута напред и
   на крају да узме лоптицу. Прекопирај наредни код у претходни
   програм и испробај га.
   
   .. activecode:: Карел_7_поља_напред_решење
      :passivecode: true
   
      levo()
      for i in range(7):
         napred()
      uzmi()
      
Покупи 10 лоптица
'''''''''''''''''
.. level:: 1
   
.. questionnote::
   Испред робота се налази 10 лоптица. Напиши програм којим робот купи
   све те лоптице.
   
.. karel:: Карел_покупи_10_лоптица
   :blockly:

   {
      setup: function() {
	   var world = new World(2, 1);
           world.setRobotStartAvenue(1);
           world.setRobotStartStreet(1);
           world.setRobotStartDirection("E");
	   world.putBalls(2, 1, 10);
           var robot = new Robot();
	   var code = ["from karel import *"]
	   return {world: world, robot: robot, code: code};
      },

      isSuccess: function(robot, world) {
           return robot.getStreet() === 1 &&
           robot.getAvenue() === 2 &&
	   world.getBalls(2, 1) == 0;
      }
   }

*Савет*: употреби поново петљу ``for`` да се иста наредба не би
понављала пуно пута.

Покупи пет лоптица на пет поља испред
'''''''''''''''''''''''''''''''''''''
.. level:: 1
   
.. questionnote::

   Напиши програм у којем робот купи лоптице на пет поља испред себе.

.. karel:: Карел_покупи_5_лоптица_на_5_поља_испред
   :blockly:

   {
      setup: function() {
	   var world = new World(6, 1);
           world.setRobotStartAvenue(1);
           world.setRobotStartStreet(1);
           world.setRobotStartDirection("E");
	   for (var i = 2; i <= 6; i++)
	      world.putBalls(i, 1, 1);
           var robot = new Robot();
	   var code = ["from karel import *",
	               "for i in range(5):",
		       "    napred()",
		       "    uzmi()"]
	   return {world: world, robot: robot, code: code};
      },

      isSuccess: function(robot, world) {
           return robot.getStreet() === 1 &&
           robot.getAvenue() === 6 &&
	   robot.getBalls() === 5;
      }
   }
   
Приметимо да су у овом програму две наредбе робота понављале пет пута
(наредба ``napred()`` и наредба ``uzmi()``) и да су обе биле увучене
по 4 карактера. Пробај сада да наредиш роботу да се врати на почетно
поље када покупи лоптице.

.. karel:: Карел_покупи_5_лоптица_на_5_поља_испред_и_врати_се
   :blockly:

   {
      setup: function() {
	   var world = new World(6, 1);
           world.setRobotStartAvenue(1);
           world.setRobotStartStreet(1);
           world.setRobotStartDirection("E");
	   for (var i = 2; i <= 6; i++)
	      world.putBalls(i, 1, 1);
           var robot = new Robot();
	   var code = ["from karel import *",
	               "for i in range(5):",
		       "    napred()",
		       "    uzmi()",
		       "???  # dopuni ovde kod"]
	   return {world: world, robot: robot, code: code};
      },

      isSuccess: function(robot, world) {
           return robot.getStreet() === 1 &&
           robot.getAvenue() === 1 &&
	   robot.getBalls() === 5;
      }
   }


На крају, модификуј програм тако да робот док се враћа оставља по
једну лопту на сваком пољу, тако да распоред лоптица буде исти као и
на почетку.

.. karel:: Карел_покупи_5_лоптица_на_5_поља_испред_и_врати_се_остављајући_лоптице
   :blockly:

   {
      setup: function() {
	   var world = new World(6, 1);
           world.setRobotStartAvenue(1);
           world.setRobotStartStreet(1);
           world.setRobotStartDirection("E");
	   for (var i = 2; i <= 6; i++)
	      world.putBalls(i, 1, 1);
           var robot = new Robot();
	   var code = ["from karel import *",
	               "for i in range(5):",
		       "    napred()",
		       "    uzmi()",
		       "???  # dopuni ovde kod"]
	   return {world: world, robot: robot, code: code};
      },

      isSuccess: function(robot, world) {
           for (var i = 2; i <= 6; i++)
               if (world.getBalls(i, 1) != 1)
                 return false;
           return robot.getStreet() === 1 &&
                  robot.getAvenue() === 1 &&
   	          robot.getBalls() === 0;
      }
   }

   

