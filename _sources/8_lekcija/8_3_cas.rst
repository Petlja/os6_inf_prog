8.3 Позициони запис бројева
###########################

Ако је укупан број центиметара био 123, тада је број метара 1, број
дециметара 2 и број центиметара 3. Решавањем претходног задатка смо
заправо одређивали појединачне цифре коришћене у запису тог
троцифреног броја. Приказана техника може бити уопштена тако да се
одређују све цифре и у запису дужих бројева.


Цифре броја
'''''''''''

.. questionnote::

   Хајде сада да пронађемо и сабцеремо цифре неког броја! Користићемо целобројно дељење (количник
   и остатак) да бисмо пронашли једну по једну цифру нашег броја, а затим ћемо их једноставно сабрати.

.. activecode:: цифре_броја
   :runortest: broj, kontrolni_broj
   :enablecopy:
		
   # -*- acsection: general-init -*-
   # -*- acsection: var-init -*-
   broj = 623145
   # -*- acsection: main -*-
   c0 = (broj // 1) % 10
   c1 = (broj // 10) % 10
   c2 = 0 # ispravi ovaj red
   c3 = (broj // 1000) % 10
   c4 = 0 # ispravi ovaj red
   zbir = c0 + c1 + c2 + c3 + c4
   # -*- acsection: after-main -*-
   print(zbir)
   ====
   from unittest.gui import TestCaseGui
   class myTests(TestCaseGui):
       def testOne(self):
          for broj, kontrolni_broj in [(71425, 19), (33214, 13), (62040, 12)]:
             self.assertEqual(acMainSection(broj = broj)["kontrolni_broj"],kontrolni_broj,"За број %s контролни број је %s." % (broj, kontrolni_broj))
   myTests().main()

У овом примеру радимо следеће:

- Цифру јединицу добијамо тако што број прво целобројно поделимо са 1 (приметимо да се број при томе не мења) а затим нађемо остатак при дељењу броја са 10.
- Цифру десетицу обијамо тако што број прво целобројно поделимо са 10 (чиме цифра десетица долази скроз десно) а затим нађемо остатак при дељењу броја са 10.
- Цифру стотину добијамо тако што број прво целобројно поделимо са 100 (чиме цифра стотина долази скроз десно) а затим нађемо остатак при дељењу броја са 10.

.. infonote::
   Цифре одређујемо здесна налево, тако што делимо број са
   тежином цифре (за цифру јединица број делимо са 1, десетица са 10,
   стотина са 100 итд.) и проналазимо остатак при дељењу са 10.

Целобројно дељење - време и углови
----------------------------------

За разлику од бројева и јединица мере које записујемо у систему чија
је основа 10, при раду са временом и угловима користимо систем чија је
основа број 60. Тако један сат има 60 минута, а један минут 60
секунди. Слично, један степен има 60 угаоних минута, а један угаони
минут има 60 угаоних секунди. Прикажимо сада кроз неколико задатака
како можемо у програмима вршити израчунавања у којима учествују време
и углови.

Конверзија сати и минута у минуте и обратно
'''''''''''''''''''''''''''''''''''''''''''

.. questionnote::

   Ако се зна колико је тренутно сати и минута, израчунај колико је
   минута протекло од претходне поноћи.

Пошто у једном сату има 60 минута, довољно је да помножиш број сати
са 60 и на то додаш број минута.

.. activecode:: сати_и_минути_у_минуте
   :runortest: sati, minuta, minuta_od_ponoci
   :enablecopy:

   # -*- acsection: general-init -*-
   # -*- acsection: var-init -*-
   sati = 2
   minuta = 60
   # -*- acsection: main -*-
   minuta_od_ponoci = 0 # ispravi ovaj red
   # -*- acsection: after-main -*-
   print(minuta_od_ponoci)
   ====
   from unittest.gui import TestCaseGui
   class myTests(TestCaseGui):
       def testOne(self):
          for sati, minuta, minuta_od_ponoci in [(14, 19, 859), (11, 13, 673), (23, 59, 1439)]:
             self.assertEqual(acMainSection(sati = sati, minuta = minuta)["minuta_od_ponoci"],minuta_od_ponoci,"У %s:%s протекло је %s минута од поноћи." % (sati, minuta, minuta_od_ponoci))
   myTests().main()
   
   
.. questionnote::

   Ако се зна колико је минута протекло од претходне поноћи, израчунај
   колико је тренутно сати и минута.

Ако са :math:`s` обележимо тренутни број сати, са :math:`m` тренутни
број минута, а са :math:`M` број минута протеклих од поноћи, тада важи
да је :math:`M = s \cdot 60 + m`, при чему за :math:`m` важи да је
број између :math:`0` и :math:`59`, што јасно указује на то да се
тражене вредности могу израчунати применом целобројног дељења.
   
.. activecode:: минути_у_сате_и_минуте
   :runortest: minuta_od_ponoci, sati, minuta
   :enablecopy:

   # -*- acsection: general-init -*-
   # -*- acsection: var-init -*-
   minuta_od_ponoci = 125
   # -*- acsection: main -*-
   sati = 0     # ispravi ovaj red
   minuta = 0   # ispravi ovaj red
   # -*- acsection: after-main -*-
   print(sati, minuta)
   ====
   from unittest.gui import TestCaseGui
   class myTests(TestCaseGui):
       def testOne(self):
          for sati, minuta, minuta_od_ponoci in [(14, 19, 859), (11, 13, 673), (23, 59, 1439)]:
             self.assertEqual(acMainSection(minuta_od_ponoci = minuta_od_ponoci)["sati"],sati,"У %s:%s протекло је %s минута од поноћи." % (sati, minuta, minuta_od_ponoci))
             self.assertEqual(acMainSection(minuta_od_ponoci = minuta_od_ponoci)["minuta"],minuta,"У %s:%s протекло је %s минута од поноћи." % (sati, minuta, minuta_od_ponoci))
   myTests().main()

