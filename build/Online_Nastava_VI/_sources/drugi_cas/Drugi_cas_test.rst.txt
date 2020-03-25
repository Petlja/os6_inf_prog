====
Тест
====

Питање 1
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Нека је Карел робот у положају као на слици.

.. image:: ../_images/karel4.png 
   :align: center

Извршавањем којих од наредних програма ће робот стићи до поља (4,1) и узети лоптицу?

(1)
  .. code-block:: python
    
    from karel import *
    while mozeNapred():
        napred()
    uzmi()

(2)        
  .. code-block:: python
    
    from karel import *
    while mozeNapred():
        napred()
        uzmi()

(3)
  .. code-block:: python
    
    from karel import *
    for i in range(3):
        napred()
    uzmi()

(4)
  .. code-block:: python
    
    from karel import *
    for i in range(3):
        napred()
        uzmi()


.. mchoice:: karel_uzmi
    :multiple_answers:
    :answer_a: 1 
    :feedback_a: Тачно
    :answer_b: 2 
    :feedback_b: Нетачно    
    :answer_c: 3        
    :feedback_c: Тачно
    :answer_d: 4
    :feedback_d: Нетачно    
    :correct: ['a', 'c']
    
    Изабери тачан одговор:

Питање 2.
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Нека је Карел робот у положају као на слици

.. image:: ../_images/karel8.png 
   :align: center

и нека је његов задатак да сиђе низ степенице и caкупи све лоптице које му се нађу на путу. 
Дат је недовршен програм који би требало да представља решење роботовог задатка. 

.. code-block:: python

    from karel import *      
    while (moze_napred()):    
      ____________
       
      ____________

У блоку петље недостаје неколико наредби. Допуни тело петље навођењем што мање понуђених наредби у одговарајућем редоследу, тако да Карел узме сваку лоптицу чим може, а да се извршавањем програма исправно решава задатак.

(1)
  .. code-block:: python

    napred() 

(2)
  .. code-block:: python

    desno()

(3)
  .. code-block:: python

    uzmi()

(Одговор упиши навођењем редних бројева наредби распоређених у одговарајући редослед, нпр. 12213)


.. fillintheblank:: karel_jedna_petlja2

   Одговор: |blank|

   - :^\s*1213222\s*$: Тачно
     :x: Одговор није тачан.
      
      




Питање 3.
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Нека се Карел робот налази у лавиринту као на слици

.. image:: ../_images/karel10.png 
   :align: center

и нека је лавиринт ЗАЧАРАН тако да се при сваком покретању програма може променити дужина лавиринта и број лоптица на пољима. У свакој верзији лавиринт се састоји из једнаког броја поља са лоптицама и поља са рупама наизменично распоређених (као на слици).  

Извршавањем којих од наредних програма ће робот проћи кроз цео лавиринт, на сваком месту где има лоптица сакупити све лоптице и убацити их у прву наредну рупу?  

Напомена: Сматра се да је код исправан уколико при извршавању Пајтон окружење не пријави грешку, као што је грешка која би се јавила при извршавању команде napred() када се робот налази испред зида лавиринта.

(1)
  .. code-block:: python

    from karel import *   
    while (moze_napred()):
      while (ima_loptica_na_polju()):
        uzmi()
      while (ima_loptica_kod_sebe()):
        ostavi()
      napred()   
  
(2)
  .. code-block:: python

    from karel import *   
    napred()
    while (moze_napred()):
      while (ima_loptica_kod_sebe()):
        ostavi()
      napred()
      while (ima_loptica_na_polju()):
        uzmi()
      napred()  

(3)
  .. code-block:: python

    from karel import *   
    while (moze_napred()):
      while (ima_loptica_na_polju()):
        uzmi()
      napred()
      while (ima_loptica_kod_sebe()):
        ostavi()
      napred()  

(4)
  .. code-block:: python

    from karel import *   
    while (moze_napred()):
      napred()
      while (ima_loptica_na_polju()):
        uzmi()
      napred()
      while (ima_loptica_kod_sebe()):
        ostavi()

(5)
  .. code-block:: python

    from karel import *   
    while (moze_napred()):
      while (ima_loptica_na_polju()):
        uzmi()
      napred()
      while (ima_loptica_kod_sebe()):
        ostavi()
  


.. mchoice:: karel_brloptica_for
    :multiple_answers:
    :answer_a: Програм (1)
    :feedback_a: Нетачно    
    :answer_b: Програм (2)
    :feedback_b: Нетачно    
    :answer_c: Програм (3)
    :feedback_c: Нетачно    
    :answer_d: Програм (4)
    :feedback_d: Тачно
    :answer_e: Програм (5)
    :feedback_e: Тачно
    :correct: ['d', 'e']
    
    Изабери тачан одговор:
