1.5. Вежбање 
#############

Искористи петљу и помози Карелу у следећим задацима!
   
Покупи 10 лоптица
'''''''''''''''''
   
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

   

Размакнуте лоптице
''''''''''''''''''

.. questionnote::

   Помози роботу да покупи три лоптице испред себе. Напиши програм без
   петље и програм са петљом.


.. karel:: Карел_размакнуте_лоптице
  :blockly:

   {
     setup: function() {
        var world = new World(7, 1);
        world.setRobotStartAvenue(1);
        world.setRobotStartStreet(1);
        world.setRobotStartDirection("E");

        world.putBall(3, 1);
        world.putBall(5, 1);
        world.putBall(7, 1);

        var robot = new Robot();
        var code = ["from karel import *"]
        return {world: world, robot: robot, code: code};
     },

     isSuccess: function(robot, world) {
          for (var i = 1; i <= world.getAvenues(); i++)
             for (var j = 1; j <= world.getStreets(); j++)
                if (world.getBalls(i, j) != 0)
                   return false;
         return true;
     }
   }
          
.. reveal:: Карел_размакнуте_лоптице_reveal
   :showtitle: Прикажи решење
   :hidetitle: Сакриј решење
 
   Једно могуће решење са петљом (не и једино) је следеће.               
 
   .. activecode:: Карел_размакнуте_лоптице_решење
      :passivecode: true
                    
      from karel import *
      for i in range(3):
          napred()
          napred()
          uzmi()

Покупи по три лоптице на пет поља испред
''''''''''''''''''''''''''''''''''''''''

.. questionnote::

   На сваком од пет поља испред робота налазе се по три
   лоптице. Напиши програм на основу којег робот купи све те лоптице.

   
.. karel:: Карел_покупи_по_3_лоптице_на_5_поља_испред
   :blockly:

   {
      setup: function() {
	   var world = new World(6, 1);
           world.setRobotStartAvenue(1);
           world.setRobotStartStreet(1);
           world.setRobotStartDirection("E");
	   for (var i = 2; i <= 6; i++)
	      world.putBalls(i, 1, 3);
           var robot = new Robot();
	   var code = ["from karel import *",
	               "for i in range(5):",
		       "    napred()",
		       "    for j in range(3):",
		       "        uzmi()"]
	   return {world: world, robot: robot, code: code};
      },

      isSuccess: function(robot, world) {
          for (var i = 1; i <= world.getAvenues(); i++)
             for (var j = 1; j <= world.getStreets(); j++)
                if (world.getBalls(i, j) != 0)
                   return false;
         return true;
      }
   }

Приметимо да се у претходном програму петља ``for`` налази у телу
петље ``for``. Такве се петље називају **угнежђене петље**. Приметимо
да смо у њима морали употребити различита слова (у спољној смо
употребили ``i``, а у унутрашњој ``j``). Више детаља о овоме биће у
наредним поглављима.
