Тест
============================

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

.. mchoice:: grananje_4
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

.. mchoice:: grananje_5
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

.. mchoice:: grananje_6
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

.. mchoice:: grananje_8a
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

.. mchoice:: grananje_7
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

.. mchoice:: grananje_8
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

.. mchoice:: grananje_9
    :answer_a: True
    :feedback_a: Нетачно    
    :answer_b: False
    :feedback_b: Тачно
    :correct: b

    Шта ће Пајтон окружење исписати након извршавања следећег кода? Изабери тачан одговор:

    .. code-block:: python
  
     a = 17
     print( (a < 6) and (a > -10) )
