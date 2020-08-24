1.3. Вежбање 
#############

Пребаци обе лоптице у рупу
''''''''''''''''''''''''''
.. level:: 2

.. questionnote::

   Задатак је исти као мало пре, једино се лавиринт мало
   променио. Потребно је да робот пребаци обе лоптице у рупу.

.. karel:: Карел_пребаци_две_лоптице_2
   :blockly:

   {
        setup:function() {
            var world = new World(5,5);
            world.setRobotStartAvenue(5);
            world.setRobotStartStreet(5);
            world.setRobotStartDirection("W");
            world.putBall(3, 3);
            world.putBall(1, 2);
            world.putHoles(5, 1, 2);
	    
	    world.addEWWall(2, 4, 1);
 	    world.addEWWall(2, 3, 1);
 	    world.addNSWall(1, 4, 1);
 	    world.addNSWall(2, 4, 1);

	    world.addEWWall(2, 2, 1);
 	    world.addEWWall(2, 1, 1);
 	    world.addNSWall(1, 2, 1);
 	    world.addNSWall(2, 2, 1);

	    world.addEWWall(4, 4, 2);
	    world.addNSWall(3, 2, 3);
	    world.addEWWall(4, 1, 2);
	
 	    var robot = new Robot();

	    var code = ["from karel import *",
	                "??? # idi do prve loptice i uzmi je",
			"??? # idi do druge loptice i uzmi je",
			"??? # idi do rupe i ostavi obe loptice"];
            return {robot:robot, world:world, code:code};
        },
	
        isSuccess: function(robot, world) {
           return world.getBalls(5, 1) == 0;
        }
   }

.. reveal:: Карел_пребаци_две_лоптице_2_reveal
   :showtitle: Прикажи решење
   :hidetitle: Сакриј решење

   Једно могуће решење (не и једино) је следеће.	       

   .. activecode:: Карел_пребаци_две_лоптице_2_решење
      :passivecode: true
		    
      from karel import *
      # idi do prve loptice i uzmi je
      napred()
      napred()
      levo()
      napred()
      napred()
      uzmi()
      # idi do druge loptice i uzmi je
      desno()
      napred()
      napred()
      levo()
      napred()
      uzmi()
      # idi do rupe i ostavi loptice
      napred()
      levo()
      napred()
      napred()
      napred()
      napred()
      ostavi()
      ostavi()


Размакнуте лоптице
''''''''''''''''''
.. level:: 2

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
.. level:: 2

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


      
