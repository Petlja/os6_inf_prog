1.2. Вежбање
##################

Помози Карелу да обави задатке!

Пребаци обе лоптице у рупу
''''''''''''''''''''''''''
   
.. questionnote::

   У овом задатку робот Карел има задатак да покупи обе лоптице и
   пребаци их у рупу (на њој пише колико лоптица треба да оставиш у
   рупу).

Помози сада роботу тако што ћеш попунити недостајућа места у коду.
   
.. karel:: Карел_пребаци_две_лоптице_1
   :blockly:

   {
      setup: function() {
	   var world = new World(3, 3);
           world.setRobotStartAvenue(3);
           world.setRobotStartStreet(3);
           world.setRobotStartDirection("E");
           world.putBall(1, 1);
           world.putBall(3, 1);
           world.putHoles(2, 2, 2);
           world.addNSWall(1, 1, 1);
           world.addNSWall(2, 1, 1);
           world.addEWWall(2, 1, 1);
           world.addEWWall(2, 2, 1);
           world.addNSWall(2, 3, 1);
           var robot = new Robot();
	   var code = ["from karel import *",

	   "desno(); napred(); napred();                    # idi do prve loptice",
	   "uzmi();                                         # uzmi je",
	   "???                                             # idi do rupe",
	   "ostavi();                                       # ostavi lopticu",
	   "???                                             # idi do druge loptice",
	   "???                                             # uzmi je",
	   "desno(); desno(); napred(); desno(); napred();  # idi do žutog polja",
	   "ostavi()                                        # ostavi lopticu"]
	   return {world: world, robot: robot, code: code};
      },

      isSuccess: function(robot, world) {
           return world.getBalls(2, 2) == 0;
      }
   }



Пребаци обе лоптице у рупу
''''''''''''''''''''''''''

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
