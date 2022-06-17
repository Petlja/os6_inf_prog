2.2. Вежбање
###############

Лоптице на три стране
'''''''''''''''''''''



.. questionnote::

   Помози роботу да покупи све лоптице. Пошто је лавиринт зачаран,
   мораћеш да употребиш петљу са провером услова.

.. karel:: Карел_лоптице_на_три_стране
  :blockly:

   {
     setup: function() {

         function random(n) {
             return Math.floor(n * Math.random());
         }
     
         var N = 4 + random(3);
         var world = new World(N, N);
         world.setRobotStartAvenue(1);
         world.setRobotStartStreet(N);
         world.setRobotStartDirection("S");
         for (var i = N-1; i >= 1; i--)
            world.putBall(1, i);
         for (var i = 2; i <= N; i++)
            world.putBall(i, 1);
         for (var i = 2; i <= N; i++)
             world.putBall(N, i);
     
         world.addNSWall(1, 2, N-1);
         world.addEWWall(2, 1, N-2);
         world.addNSWall(N-1, 2, N-1); ;
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

.. reveal:: Карел_лоптице_на_три_стране_reveal
   :showtitle: Прикажи решење
   :hidetitle: Сакриј решење

   Једно могуће решење (не и једино) је следеће.               

   .. activecode:: Карел_лоптице_на_три_стране_решење
      :passivecode: true
                    
      from karel import *
      for i in range(3):
          while moze_napred():
              napred()
              uzmi()
          levo() 