Тест
############


Робот у лавиринту на слици се налази на пољу (4,5). 

.. image:: ../_images/karel1.png      
   :align: center

На ком ће се пољу наћи робот извршавањем следеће наредбе?

 .. code-block:: python
    
  levo()


.. mchoice:: karel_osnovno_1
    :answer_a: Налазиће се на истом пољу.
    :feedback_a: Тачно
    :answer_b: Налазиће се на пољу (3,5).
    :feedback_b: Нетачно    
    :answer_c: Налазиће се на пољу (5,5).
    :feedback_c: Нетачно    
    :correct: a
    
    Изабери тачан одговор:

Робот у лавиринту на слици се налази на пољу (5,3). 

.. image:: ../_images/karel1_1.png      
   :align: center

Након извршавања којег од наредних програма ће се робот наћи на пољу (3,3)?

Програм 1.
 .. code-block:: python
    
    from karel import *
    levo()
    napred()
    levo()
    napred()

Програм 2.
 .. code-block:: python
    
    from karel import *
    levo()
    levo()
    napred()
    napred()


.. mchoice:: karel_osnovno_2
    :answer_a: Извршавањем програма 1.
    :feedback_a: Нетачно    
    :answer_b: Извршавањем програма 2.
    :feedback_b: Тачно
    :answer_c: Извршавањем било ког од дата два програма робот стиже на исто поље (3,3).
    :feedback_c: Нетачно    
    :correct: b
    
    Изабери тачан одговор:



Питање 3.*
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Нека је Карел робот у положају као на слици.

.. image:: ../_images/karel2.png   
   :align: center

Поређај команде тако да робот на најкраћи начин стигне до рупе.

(1) 
  .. code-block:: python
    
    levo()

(2) 
  .. code-block:: python
    
    napred()


(Одговор упиши навођењем редних бројева команди у одговарајућем редоследу, нпр. 1221)


.. fillintheblank:: karel_osnovno_3

   Одговор: |blank|

   - :^\s*121112\s*$: Тачно
     :x: Одговор није тачан.
      
      




Питање 4.
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Нека је Карел робот у положају као на слици.

.. image:: ../_images/karel3.png 
   :align: center

У ком положају ће се наћи робот након извршавања следећег дела кода:

  .. code-block:: python
    
    desno(); desno();


.. mchoice:: karel_nazad
    :answer_a: Робот ће се померити за два поља на лево и бити на пољу (1,1).
    :feedback_a: Нетачно    
    :answer_b: Робот ће се окренути за 180 степени и налазити се на пољу на ком се налазио и пре извршавања датог кода.        
    :feedback_b: Тачно
    :answer_c: Робот ће се померити за два поља на десно и бити на пољу (5,1).
    :feedback_c: Нетачно    
    :answer_d: Ниједан од понуђених одговора није тачан.     
    :feedback_d: Нетачно    
    :correct: b
    
    Изабери тачан одговор:



Питање 5.*
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Нека је Карел робот у положају као на слици.

.. image:: ../_images/karel3.png 
   :align: center

На ком пољу ће се робот наћи након извршавања следећег дела кода:

  .. code-block:: python
    
    napred(); levo(); levo(); napred();


.. mchoice:: karel_nazad_2
    :answer_a: Робот ће се померити за два поља лево и бити на пољу (1,1).
    :feedback_a: Нетачно    
    :answer_b: Робот ће се налазити се на пољу на ком се налазио и пре извршавања датог кода. 
    :feedback_b: Тачно
    :answer_c: Робот ће се померити за два поља десно и бити на пољу (5,1).       
    :feedback_c: Нетачно    
    :answer_d: Ниједан од понуђених одговора није тачан.     
    :feedback_d: Нетачно    
    :correct: b
    
    Изабери тачан одговор:



Питање 6.
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Нека je дат следећи део кода.

.. code-block:: python

  for i in range(2):
    napred()
    desno()
  napred()

Који од наредних кодова ће дати исти резултат при извршавању?         


.. mchoice:: karel_for
    :answer_a: napred(); napred(); desno(); napred(); desno();
    :feedback_a: Нетачно    
    :answer_b: napred(); napred(); napred(); desno();
    :feedback_b: Нетачно    
    :answer_c: napred(); desno(); napred(); desno(); napred(); 
    :feedback_c: Тачно
    :answer_d: napred(); desno(); desno(); napred(); 
    :feedback_d: Нетачно    
    :correct: c
    
    Изабери тачан одговор:



Питање 7.
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Нека je дат следећи део кода.

.. code-block:: python

  napred() 
  for i in range(2):
    desno()
  napred()


Који од наредних кодова ће дати исти резултат при извршавању?         


.. mchoice:: karel_for2
    :answer_a: napred(); napred(); desno(); napred(); desno();
    :feedback_a: Нетачно    
    :answer_b: napred(); napred(); napred(); desno();
    :feedback_b: Нетачно    
    :answer_c: napred(); desno(); napred(); desno(); napred(); 
    :feedback_c: Нетачно    
    :answer_d: napred(); desno(); desno(); napred(); 
    :feedback_d: Тачно
    :correct: d
    
    Изабери тачан одговор:



Питање 8.*
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



Питање 9.
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Нека je дат следећи део кода.

.. code-block:: python

  uzmi()
  napred()

Шта се дешава када робот треба да изврши команду uzmi(), при чему на пољу на ком се налази нема лоптица?         


.. mchoice:: karel_uzmierr
    :answer_a: Робот извршава следећу команду, napred().
    :feedback_a: Нетачно    
    :answer_b: Пајтон окружење јавља грешку, а робот прелази на извршавање следеће команде.
    :feedback_b: Нетачно    
    :answer_c: Пајтон окружење јавља грешку и прекида даље извршавање програма.  
    :feedback_c: Тачно
    :correct: c
    
    Изабери тачан одговор:



Питање 10.
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Извршавањем којег од наредних делова кода ће робот прво извршити проверу да ли има бар једну лоптицу код себе, а затим оставити једну лоптицу на пољу на ком се налази?

(1)
  .. code-block:: python

    ima_loptica_kod_sebe()
    ostavi()

(2)
  .. code-block:: python

    if (ima_loptica_kod_sebe()):
    ostavi()    
    
(3)
  .. code-block:: python

    if (ima_loptica_kod_sebe()):
      ostavi()  

(4)
  .. code-block:: python

    while (ima_loptica_kod_sebe()):
      ostavi()  

(5)
  .. code-block:: python

    if (broj_loptica_kod_sebe()):
      ostavi()   


.. mchoice:: karel_if
    :answer_a: 1 
    :feedback_a: Нетачно    
    :answer_b: 2 
    :feedback_b: Нетачно    
    :answer_c: 3        
    :feedback_c: Тачно
    :answer_d: 4
    :feedback_d: Нетачно    
    :answer_e: 5
    :feedback_e: Нетачно    
    :correct: c
    
    Изабери тачан одговор:



Питање 11.*
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Нека је Карел робот у положају као на слици

.. image:: ../_images/karel6.png 
   :align: center

и нека је дат следећи програм:

.. code-block:: python

  from karel import *
  napred()
  if (ima_loptica_na_polju()):
        uzmi()      
 
Колико ће лоптица робот сакупити извршавањем датог програма?  


.. mchoice:: karel_slaganje2
    :answer_a: Петнаест.
    :feedback_a: Нетачно    
    :answer_b: Пет.
    :feedback_b: Нетачно    
    :answer_c: Једну.
    :feedback_c: Тачно
    :answer_d: Три.
    :feedback_d: Нетачно    
    :answer_e: Ниједну.
    :feedback_e: Нетачно    
    :correct: c
    
    Изабери тачан одговор:



Питање 12.*
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Нека робот има задатак да са поља на ком се налази сакупи све лоптице, при чему се не зна унапред колико ће их на датом пољу бити.  
Извршавањем којих од наведених наредби ће робот успети да обави тај задатак? 

(1)
  .. code-block:: python

    for i in range(ima_loptica_na_polju()):    
      uzmi()
  
(2)
  .. code-block:: python

    for i in range(broj_loptica_na_polju()):    
      uzmi()

(3)
  .. code-block:: python

    while (ima_loptica_na_polju()):    
      uzmi()  

(4)
  .. code-block:: python

    while (broj_loptica_na_polju()):    
      uzmi() 
  


.. mchoice:: karel_brloptica
    :multiple_answers:
    :answer_a: Програм (1)
    :feedback_a: Нетачно    
    :answer_b: Програм (2)
    :feedback_b: Тачно
    :answer_c: Програм (3)
    :feedback_c: Тачно
    :answer_d: Програм (4)
    :feedback_d: Нетачно    
    :correct: ['b', 'c']
    
    Изабери тачан одговор:



Питање 13.**
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Нека је Карел робот у положају као на слици

.. image:: ../_images/karel5.png 
   :align: center

и нека је лавиринт ЗАЧАРАН тако да се при сваком покретању програма може променити дужина лавиринта и распоред лоптица на пољима, при чему на пољу (1,1) никад нема лоптица и број лоптица на једном пољу није  већи од 1. 
Извршавањем којих од наредних програма ће робот проћи кроз цео лавиринт и caкупити све лоптице? 

(1)
  .. code-block:: python

    from karel import *       
    while (moze_napred()):    
      napred()
      uzmi()
  
(2)
  .. code-block:: python

    from karel import *       
    while (moze_napred()): 
      napred()   
      if (ima_loptica_na_polju()):  
        uzmi()

(3)
  .. code-block:: python

    from karel import *       
    while (moze_napred()):   
      if (ima_loptica_na_polju()):  
        uzmi()
      napred() 

(4)

  .. code-block:: python

    from karel import *       
    while (moze_napred()):    
      while (ima_loptica_na_polju()):
        napred()  
        uzmi()

(5)

  .. code-block:: python

    from karel import *       
    while (moze_napred()):    
      napred()
      while (ima_loptica_na_polju()):  
        uzmi()          
   


.. mchoice:: karel_slaganje
    :multiple_answers:
    :answer_a: Програм (1)
    :feedback_a: Нетачно    
    :answer_b: Програм (2)
    :feedback_b: Тачно
    :answer_c: Програм (3)
    :feedback_c: Нетачно    
    :answer_d: Програм (4)
    :feedback_d: Нетачно    
    :answer_e: Програм (5)
    :feedback_e: Тачно
    :correct: ['b', 'e']
    
    Изабери тачан одговор:



Питање 14.*
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Нека је Карел робот у положају као на слици

.. image:: ../_images/karel7.png 
   :align: center

Извршавањем којих од наредних програма ће робот проћи кроз цео лавиринт, caкупити свих пет лоптица и убацити их у рупу? 

(1)
  .. code-block:: python

    from karel import *   
    napred()    
    for i in range(5):    
      uzmi()
      for i in range(5):
      ostavi()
  
(2)
  .. code-block:: python

    from karel import *   
    napred()    
    for i in range(5):    
      uzmi()
      napred()
      for i in range(5):
      ostavi()

(3)
  .. code-block:: python

    from karel import *   
    napred()    
    for i in range(5):    
      uzmi()
      napred()
      ostavi()

(4)
  .. code-block:: python

    from karel import *   
    napred()    
    for i in range(5):    
      uzmi()
    napred()
    for i in range(5):
      ostavi()
  


.. mchoice:: karel_dve_petlje
    :answer_a: Програм (1)
    :feedback_a: Нетачно    
    :answer_b: Програм (2)
    :feedback_b: Нетачно    
    :answer_c: Програм (3)
    :feedback_c: Нетачно    
    :answer_d: Програм (4)
    :feedback_d: Тачно
    :correct: d
    
    Изабери тачан одговор:



Питање 15.*
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
      
      




Питање 16.**
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



Питање 17.**
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Нека је Карел робот у положају као на слици

.. image:: ../_images/karel7.png 
   :align: center

и нека је његов задатак да caкупи свих пет лоптица и убаци их у рупу. 
Дат је недовршен програм који би требало да представља решење роботовог задатка. 

.. code-block:: python

    from karel import *   
    napred()    
    for i in range(5):    
      ____________
       
      ____________

У блоку for петље недостаје неколико команди. Допуни тело петље навођењем неких од наредних команди у одговарајућем редоследу тако да ће робот извршавањем допуњеног програма обaвити свој задатак.

(1)
  .. code-block:: python

    napred() 

(2)
  .. code-block:: python

    levo()

(3)
  .. code-block:: python

    uzmi()  

(4)
  .. code-block:: python

    ostavi()

Од могућих решења, одабрати оно које подразумева најмањи број команди и у коме Карел оставља лоптицу чим дође до поља.
(Одговор упиши навођењем редних бројева команди распоређених у одговарајући редослед, нпр. 12213)


.. fillintheblank:: karel_jedna_petlja

   Одговор: |blank|

   - :^\s*31422122\s*$: Тачно
     :x: Одговор није тачан.
      
      
Питање 18.**
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Нека је Карел робот у положају као на слици.

.. image:: ../_images/karel9.png  
   :align: center

Извршавањем којих од наредних програма ће робот успешно обићи цео лавиринт бар једанпут без обзира да ли су димензије лавиринта промењене или не?

(1)
  .. code-block:: python

    from karel import *
    while (moze_napred()):
      napred()

(2)
  .. code-block:: python

    from karel import *
    while (moze_napred()):
      desno()
      while (moze_napred()):
        napred()

(3)
  .. code-block:: python

    from karel import *
    while (moze_napred()):
      while (moze_napred()):
        napred()
      desno()

(4)
  .. code-block:: python

    from karel import *
    if (moze_napred()):
      while (moze_napred()):
        napred()
    else:
        desno()

(5)
  .. code-block:: python

    from karel import *
    while (moze_napred()):
      if (moze_napred()):
        napred()
      else:
        desno()


.. mchoice:: karel_jedna_petlja3
    :answer_a: Програм (1)
    :feedback_a: Нетачно    
    :answer_b: Програм (2)
    :feedback_b: Нетачно    
    :answer_c: Програм (3)
    :feedback_c: Тачно
    :answer_d: Програм (4)
    :feedback_d: Нетачно    
    :answer_e: Програм (5)
    :feedback_e: Нетачно    
    :correct: c
    
    Изабери тачан одговор:



