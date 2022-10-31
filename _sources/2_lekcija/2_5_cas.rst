2.5. Вежбање 
############

На крају ти остављамо неколико задатака за вежбу. Оне задатке које не
стигнеш да урадиш на часу уради за домаћи задатак.


Покупи лоптице до којих можеш да дођеш
''''''''''''''''''''''''''''''''''''''

.. questionnote::

   Помози роботу да покупи све лоптице. Наравно, лавиринт је опет
   зачаран и распоред препрека и лоптица испред робота се мења
   приликом сваког покретања програма. Лоптице се налазе доњем реду 
   лавиринта.
   
.. karel:: Карел_покупи_лоптице_до_којих_можеш_да_дођеш
    :blockly:
   
    {
      setup: function() {

         function random(n) {
             return Math.floor(n * Math.random());
         }

         var world = new World(4 + random(4), 2);
         world.setRobotStartAvenue(1);
         world.setRobotStartStreet(2);
         world.setRobotStartDirection("E");

         world.addEWWall(1, 1, 1);
         var balls = 0;
         var prevBall = false;
         for (var i = 2; i <= world.getAvenues(); i++) {
             if (random(2) == 0 || (balls == 0 && i == world.getAvenues() - 1)) {
                 balls++;
                 if (!prevBall)
                    world.addNSWall(i-1, 1, 1);
                 world.putBall(i, 1);
                 prevBall = true;
             } else {
                 if (prevBall)
                    world.addNSWall(i-1, 1, 1);
                 world.addEWWall(i, 1, 1);
                 prevBall = false;
             }
         }

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

У сваком кораку робот треба да се помери напред, затим да се окрене за
90 степени (ка југу) и провери да ли је испред њега препрека. Ако нема
препреке, тј. ако може да иде напред, онда треба да оде напред, узме
лоптицу, окрене се за 180 степени (ка северу), поново оде напред и
окрене се за 90 степени (ка истоку). У супротном само треба да се
окрене за 90 степени (ка истоку).

.. reveal:: Карел_покупи_лоптице_до_којих_можеш_да_дођеш_reveal
   :showtitle: Прикажи решење
   :hidetitle: Сакриј решење

   Једно могуће решење (не и једино) је следеће.               

   .. activecode:: Карел_покупи_лоптице_до_којих_можеш_да_дођеш_решење
      :passivecode: true
                    
      from karel import *
      while moze_napred():
          napred()
          # okreni se prema jugu
          desno()
          # proveri da li je prepreka ispred tebe
          if moze_napred():
              # idi po lopticu
              napred()
              uzmi()
              # vrati se nazad
              levo()
              levo()
              napred()
              desno()
          else:
              # okreni se prema istoku
              levo()


Кретање укруг
'''''''''''''

Покушај да решиш и наредни, мало тежи задатак. 

.. questionnote::

   Напиши програм којим се роботу наређује да се креће укруг око лавиринта и да покупи све лоптице на које наиђе.

Једна идеја за решење је да четири пута поновимо наредбе којима робот
иде напред док год може и купи све лоптице на које наиђе.

.. karel:: Карел_покупи_лоптице_у_круг_1
    :blockly:
   
    {
      setup: function() {
           var dim = 5;
	   var world = new World(dim, dim);
           world.setRobotStartAvenue(1);
           world.setRobotStartStreet(1);
           world.setRobotStartDirection("E");

	   for (var i = 1; i <= dim; i++)
	      if (Math.random() > 0.5)
	         world.putBall(i, 1);
	   for (var i = 1; i <= dim; i++)
	      if (Math.random() > 0.5)
	         world.putBall(i, dim);
	   for (var i = 2; i <= dim-1; i++)
	      if (Math.random() > 0.5)
	         world.putBall(1, i);
	   for (var i = 2; i <= dim-1; i++)
	      if (Math.random() > 0.5)
	         world.putBall(dim, i);

	   world.addEWWall(2, 1, dim-2);
	   world.addEWWall(2, dim-1, dim-2);
           world.addNSWall(1, 2, dim-2);
           world.addNSWall(dim-1, 2, dim-2);
	   
           var robot = new Robot();
	   var code = ["from karel import *",
        "for i in range(4):",
        "    while moze_napred():",
        "        ??? # popravi ovu liniju",
        "        if ima_loptica_na_polju():",
        "            ??? # popravi ovu liniju",
        "    ??? # popravi ovu liniju"
        ]
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
