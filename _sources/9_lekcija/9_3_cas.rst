9.3. Вежбање - цели и реални бројеви
####################################

Ако на часу нисте стигли да урадите све задатке, уради их сада, у
склопу домаћег задатка. Након тога покушај да урадиш и наредних
неколико задатака.


Прочитане стране књиге
''''''''''''''''''''''
.. level:: 1

.. questionnote::

   Књига има 282 стране. Марко је првог дана прочитао трећину, другог
   дана половину остатка, а трећег књигу прочитао до краја. Колико
   страна је прочитао ког дана? Напиши програм тако да исправно ради
   и ако је број страна првог дана другачији.

.. activecode:: Читање
   :runortest: broj_strana, prvi_dan, drugi_dan, treci_dan
   :enablecopy:

   # -*- acsection: general-init -*-
   # -*- acsection: var-init -*-
   broj_strana = 282
   # -*- acsection: main -*-
   prvi_dan = 0      # ispravi ovaj red
   drugi_dan = 0     # ispravi ovaj red
   treci_dan = 0     # ispravi ovaj red
   # -*- acsection: after-main -*-
   print(prvi_dan, drugi_dan, treci_dan)
   ====
   from unittest.gui import TestCaseGui
   class myTests(TestCaseGui):
       def testOne(self):
          for broj_strana, dan in [(369, 123), (333, 111)]:
             self.assertEqual(acMainSection(broj_strana = broj_strana)["prvi_dan"],dan,"Ако књига има %s страна, први дан је прочитано %s страна." % (broj_strana,dan))
             self.assertEqual(acMainSection(broj_strana = broj_strana)["drugi_dan"],dan,"Ако књига има %s страна, други дан је прочитано %s страна." % (broj_strana,dan))
             self.assertEqual(acMainSection(broj_strana = broj_strana)["treci_dan"],dan,"Ако књига има %s страна, трећи дан је прочитано %s страна." % (broj_strana,dan))
   myTests().main()
   

.. reveal:: пресек_решење11
   :showtitle: Прикажи решење
   :hidetitle: Сакриј решење

   Марко је прочитао 94 стране сваког дана. Првог дана је прочитао
   трећину и остале су му две трећине. Другог дана је прочитао пола од
   тога тј. опет трећину и за трећи дан му је остала последња трећина.
	       
   .. activecode:: Читање_решење

      broj_strana = 282		
      prvi_dan = broj_strana / 3
      drugi_dan = (broj_strana - prvi_dan) / 2
      treci_dan = broj_strana - prvi_dan - drugi_dan
      print(treci_dan)

      


