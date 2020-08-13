Тест - гранање
==============

Питање 1.
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. mchoice:: grananje_1
    :answer_a: Биће исписан текст 'ne mozes da predjes ulicu'.
    :feedback_a: Нетачно    
    :answer_b: Биће исписан текст 'predji ulicu'.
    :feedback_b: Тачно
    :answer_c: Биће исписан текст 'zeleno'.
    :feedback_c: Нетачно    
    :answer_d: Ниједан од понуђених одговора није тачан.
    :feedback_d: Нетачно    
    :correct: b

    Шта ће бити резултат извршавања следећег Пајтон кода? Изабери тачан одговор:

    .. code-block:: python

     semafor = 'zeleno'
     if (semafor == 'zeleno'):
     	print('predji ulicu')
     else:
     	print('ne mozes da predjes ulicu')

Питање 2.
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. mchoice:: grananje_2
    :answer_a: Биће исписан текст 'ne mozes da predjes ulicu'.
    :feedback_a: Тачно
    :answer_b: Биће исписан текст 'predji ulicu'.
    :feedback_b: Нетачно    
    :answer_c: Биће исписан текст 'plavo'.
    :feedback_c: Нетачно    
    :answer_d: Ниједан од понуђених одговора није тачан.
    :feedback_d: Нетачно    
    :correct: a

    Шта ће бити резултат извршавања следећег Пајтон кода? Изабери тачан одговор:

    .. code-block:: python

     semafor = 'plavo'
     if (semafor == 'zeleno'):
     	print('predji ulicu')
     else:
     	print('ne mozes da predjes ulicu')


Питање 3.
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. fillintheblank:: grananje_poredjenje

   Шта ће бити резултат извршавања следећег Пајтон кода?

   .. code-block:: python

    a = -1
    b = -1
    if (a > b):
    	print(a)
    else:
    	print(b)

   Одговор: |blank|

   - :^\s*\-1\s*$: Тачно
     :x: Одговор није тачан.

Питање 4.
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. mchoice:: grananje_5
    :answer_a: sarenko
    :feedback_a: Тачно
    :answer_b: rumenko
    :feedback_b: Нетачно    
    :answer_c: Биће исписани називи оба сладоледа.
    :feedback_c: Нетачно    
    :answer_d: Програм неће исписати никакву поруку.
    :feedback_d: Нетачно    
    :correct: a

    Нека је задатак да се напише програм којим се учитавају цене сладоледа Руменко и Шаренко, а затим испише назив скупљег и нека је код који следи његово 
	решење. Шта ће бити резултат извршавања тог кода уколико се при покретању дају исте цене за сладоледе? Изабери тачан одговор:

    .. code-block:: python

     rumenko=int(input('Unesi cenu za rumenka'))
     sarenko=int(input('Unesi cenu za sarenka'))
     if (rumenko>sarenko):
     	print("rumenko")
     else:
     	print("sarenko")

Питање 5.
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. mchoice:: grananje_6
    :answer_a: a % 5 == 0
    :feedback_a: Тачно
    :answer_b: a / 5 == 0
    :feedback_b: Нетачно    
    :answer_c: a // 5 == 0
    :feedback_c: Нетачно    
    :answer_d: Ниједан од наведених одговора није тачан.
    :feedback_d: Нетачно    
    :correct: a

    Који услов треба да буде уписан у следећи код да би код исписивао исправан коментар о дељивости унетог броја а бројем 5? Изабери тачан одговор:

    .. code-block:: python

     a = int(input('Unesi jedan broj'))
     if (   ):
     	print('Broj je deljiv sa 5')
     else:
     	print('Broj nije deljiv sa 5')

Питање 6.
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. mchoice:: grananje_7
    :answer_a: Istinito = true
    :feedback_a: Нетачно    
    :answer_b: Istinito = False
    :feedback_b: Нетачно    
    :answer_c: Istinito = True
    :feedback_c: Тачно
    :answer_d: Istinito = false
    :feedback_d: Нетачно    
    :answer_e: Istinito = T 
    :feedback_e: Нетачно    
    :correct: c

    Која од наведених линија имену Istinito додељује истинитосну вредност ТАЧНО? Изабери тачан одговор:

Питање 7.
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. mchoice:: grananje_8
    :answer_a: True
    :feedback_a: Тачно
    :answer_b: -3 > -24
    :feedback_b: Нетачно    
    :answer_c: False
    :feedback_c: Нетачно    
    :answer_d: Прва команда није разумљива Пајтон окружењу, па ће бити исписана порука о грешци.
    :feedback_d: Нетачно    
    :correct: a

    Шта ће бити резултат извршавања следећег програма? Изабери тачан одговор:

    .. code-block:: python

     a = -3 > -24
     print(a)

Питање 8.
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. mchoice:: grananje_9
    :answer_a: True
    :feedback_a: Нетачно    
    :answer_b: 0 > -20
    :feedback_b: Нетачно    
    :answer_c: False
    :feedback_c: Тачно
    :answer_d: Прва команда није разумљива Пајтон окружењу, па ће бити исписана порука о грешци.
    :feedback_d: Нетачно    
    :correct: c

    Шта ће бити резултат извршавања следећег програма? Изабери тачан одговор:

    .. code-block:: python

     a = not(0 > -20)
     print(a)

Питање 9.
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. mchoice:: grananje_10
    :answer_a: а not> 5
    :feedback_a: Нетачно    
    :answer_b: not (a > 5)
    :feedback_b: Тачно
    :answer_c: (a >= 5)
    :feedback_c: Нетачно    
    :answer_d: !(a > 5)
    :feedback_d: Нетачно    
    :correct: b

    Који од наредних логичких израза одговара исказу  `a није веће од 5`, где а има бројевну вредност? Изабери тачан одговор:

Питање 10.
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. mchoice:: grananje_11
    :answer_a: True
    :feedback_a: Нетачно    
    :answer_b: False
    :feedback_b: Тачно
    :correct: b

    Шта ће Пајтон окружење исписати након извршавања следећег кода? Изабери тачан одговор:

    .. code-block:: python
  
     a = 17
     print( (a < 6) and (a > -10) )

Питање 11.
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. mchoice:: grananje_12
    :answer_a: True
    :feedback_a: Тачно
    :answer_b: False
    :feedback_b: Нетачно    
    :correct: a

    Шта ће Пајтон окружење исписати након извршавања следећег кода? Изабери тачан одговор:

    .. code-block:: python
  
     a = 8
     print( (a < 6) or (a > -10) )

Питање 12.
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. fillintheblank:: grananje_13

   Шта ће бити резултат извршавања следећег кода? 

   .. code-block:: python

    a = 2
    b = 62
    if (( a >= 10) or (b <= 70)) and (a + b > 50):
    	print(a - b)
    else:
    	print(2 * a - b)

   Одговор: |blank|

   - :^\s*\-60\s*$: Тачно
     :x: Одговор није тачан.
      
Питање 13.
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. fillintheblank:: grananje_14

   Који од наредних логичких израза одговара исказу  `Бар један од бројева a и b је ненегативан`?

   (1)

   .. code-block:: python
   
    (a > 0) or (b > 0)

   (2)
   
   .. code-block:: python

    (a > 0) and (b > 0)
   
   (3)

   .. code-block:: python
   
    (a >= 0) or (b >= 0)

   (4)

   .. code-block:: python

    (a >= 0) and (b >= 0)

   Одговор: |blank|

   - :^\s*3\s*$: Тачно
     :x: Одговор није тачан.
      
	  
Питање 14.
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. mchoice:: grananje_15
    :answer_a: (godine > 7 and godine <= 20) or (godine >= 65)
    :feedback_a: Тачно
    :answer_b: (godine > 7 and godine < 20) or (godine > 65)
    :feedback_b: Нетачно    
    :answer_c: godine > 7 and godine <= 20 or godine >= 65
    :feedback_c: Нетачно    
    :answer_d: godine > 7 and godine < 20 or godine > 65
    :feedback_d: Нетачно    
    :correct: a

    Нека је постављен следећи проблем

    `Цена аутобуске карте је` 660 `динара. За децу (деца старија од` 7  `и не старија од` 20 `година) и пензионере (не млађи од` 65 `) одобрава се попуст од` 100 `динара. Напиши програм којим се на основу унетог броја година исписује цена карте.`

    и следећи недовршени код

    .. code-block:: python

     godine = int(input("Unesi koliko imas godina"))
     cena = 660
     if (_______________________):
     	cena = 660 - 100
     print(cena)

    Којим од датих услова треба допунити програм (на означеном месту) да би програм исправно одређивао цену карте? Изабери тачан одговор:

Питање 15.
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. fillintheblank:: grananje_16

   Шта ће исписати Пајтон окружење при извршавању следећег кода

   .. code-block:: python

    poeni = int(input('Unesi broj poena sa testa'))
    if poeni > 85:
    	o = 5
    elif poeni > 70:
    	o = 4       
    elif poeni>55:
    	o = 3     
    elif poeni>39:
    	o = 2
    else:
    	o = 1    
    print(o)

   ако му се као вредност поена да 89?

   Одговор: |blank|

   - :^\s*5\s*$: Тачно
     :x: Одговор није тачан.
      

Питање 16.
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. fillintheblank:: grananje_17

   Шта ће исписати Пајтон окружење при извршавању следећег кода?

   .. code-block:: python

    a = 2
    b = 10
    if (a + b > 10):
    	print(a * a)           
    elif (a + b == 10):
    	print(a-b)
    else:       
    	print(b)

   Одговор: |blank|

   - :^\s*4\s*$: Тачно
     :x: Одговор није тачан.
      
Питање 17.
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. fillintheblank:: grananje_18

   Шта ће исписати Пајтон окружење при извршавању следећег кода?

   .. code-block:: python
      
    a = -10
    b = -8
    c = -1
    if (c > 10):
    	print(a * a)
    elif (a + b > 10) or (b % 2 == 0):
    	print(a - b)   
    else:
    	print(b)

   Одговор: |blank|

   - :^\s*\-2\s*$: Тачно
     :x: Одговор није тачан.
