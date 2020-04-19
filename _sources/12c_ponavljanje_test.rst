Тест
====

Питање 1.
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. mchoice:: pit1
    :answer_a: 0, 1, 3, 6, 10
    :feedback_a: Тачно
    :answer_b: 0, 1, 2, 3, 4
    :feedback_b: Нетачно    
    :answer_c: 10
    :feedback_c: Нетачно    
    :answer_d: 15
    :feedback_d: Нетачно    
    :correct: a

    Шта је резултат извршавања следећег кода? Изабери тачан одговор:

    .. code-block:: python

     s = 0
     for i in range(5):
     	s = s + i
     	print(s)

Питање 2.
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. mchoice:: pit2
    :answer_a: 1
    :feedback_a: Тачно
    :answer_b: 2
    :feedback_b: Нетачно    
    :answer_c: 3
    :feedback_c: Нетачно    
    :correct: a

    Која од следећих наредби исисује три пута `Здраво, свете!` ? Изабери тачан одговор:

    (1)
	
    .. code-block:: python
	
     for i in range(3):
     	print("Здраво, свете!")

    (2)
	
    .. code-block:: python
	
     for i in range(3):
     print("Здраво, свете!")

    (3)
	
    .. code-block:: python
	
     for i in range(3)
     	print("Здраво, свете!")

Питање 3.
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. fillintheblank:: pit3

   Шта ће бити резултат извршавања наредног кода? Изабери тачан одговор:

   .. code-block:: python

    for i in range(9,12,8):
    	print(i)

   Одговор: |blank|

   - :^\s*9\s*$: Тачно
     :x: Одговор није тачан.

Питање 4.
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. mchoice:: pit4
    :answer_a: 15
    :feedback_a: Нетачно 
    :answer_b: 21
    :feedback_b: Тачно   
    :answer_c: 10
    :feedback_c: Нетачно    
    :answer_d: 14
    :feedback_d: Нетачно    
    :correct: b

    Шта је резултат извршавања следећег кода? Изабери тачан одговор:

    .. code-block:: python

     s = 0
     for i in range(7):
     	s = s + i
     print(s)

Питање 5.
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. mchoice:: pit5
    :answer_a: 12
    :feedback_a: Нетачно 
    :answer_b: 6
    :feedback_b: Нетачно       
    :answer_c: 24
    :feedback_c: Нетачно    
    :answer_d: 0
    :feedback_d: Тачно
    :correct: d

    Шта је резултат извршавања следећег кода? Изабери тачан одговор:

    .. code-block:: python

     p = 0
     for i in range(4):
     	p = p * i
     print(p)
