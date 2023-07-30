7.4. Квиз
#########

Питање 1.
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. mchoice:: izrazi_zbir_dva_broja
    :answer_a: 19 + 26
    :feedback_a: Нетачно    
    :answer_b: 45
    :feedback_b: Тачно
    :answer_c: Python окружење ће исписати поруку о грешци.
    :feedback_c: Нетачно    
    :correct: b

	Шта ће исписати Пајтон окружење када му у командну линију унесеш следећи израз? Изабери тачан одговор.

	.. code-block:: python
	
	 19 + 26


Питање 2.
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. mchoice:: izrazi_zbir_dva_broja_b
    :answer_a: -3,6
    :feedback_a: Нетачно    
    :answer_b: 13.6
    :feedback_b: Тачно
    :answer_c: -3.6
    :feedback_c: Нетачно    
    :answer_d: 13,6
    :feedback_d: Нетачно    
    :correct: b

    Шта је резултат извршавања следеће наредбе?

	.. code-block:: python

	 5.0 + 8.6

Питање 3.
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. mchoice:: izrazi_proizvod_zapis
    :answer_a: 22 * 58
    :feedback_a: Тачно
    :answer_b: 22 x 58
    :feedback_b: Нетачно    
    :answer_c: 22 ^ 58
    :feedback_c: Нетачно    
    :correct: a

    Који од записа представља производ бројева 22 и 58 забележен *Python* изразом? Изабери тачан одговор.

Питање 4.
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. mchoice:: izrazi_zbir_brojeva_b
    :answer_a: print(7,5 + 7,9)
    :feedback_a: Нетачно    
    :answer_b: print(7,5 * 7,9)
    :feedback_b: Нетачно    
    :answer_c: 15.4
    :feedback_c: Нетачно    
    :answer_d: print(7.5 + 7.9)
    :feedback_d: Тачно
    :correct: d

    Написати наредбу којом се израчунава и исписује колики рачун треба да плати Мила у самупослузи 
    ако је купила кесицу бомбона која кошта 7,5 динара и паковање жвака које коштају 7,9 динара.

Питање 5.
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. mchoice:: racun
    :answer_a: 49 - 32 + 2
    :feedback_a: Тачно
    :answer_b: (49-32) * 2
    :feedback_b: Нетачно    
    :answer_c: 49 - 32 * 2
    :feedback_c: Нетачно    
    :answer_d: 49 - 32 - 2
    :feedback_d: Нетачно    
    :correct: a

    Написати у програмском језику *Python* израз којим се израчунава број за 2 већи од разлике бројева 49 и 32. Изабери тачан одговор.



Питање 6.
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. mchoice:: izrazi_zabelezi_izraz_1_1
    :multiple_answers:
    :answer_a: 26 : ( 25 + 70 )
    :feedback_a: Нетачно    
    :answer_b: ( 45 - 26 ) ( 25 - 70 )
    :feedback_b: Нетачно    
    :answer_c: 26 * 25 * ( 45 - 25 )
    :feedback_c: Тачно
    :answer_d: 45 - 26 * - 25 - 70
    :feedback_d: Тачно
    :answer_e: 45 - [(26 + 25) - 70]
    :feedback_e: Нетачно    
    :correct: ['c', 'd']


    Који од понуђених израза представљају исправно записане *Python* изразе? Изабери тачне одговоре.

Питање 7.
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. mchoice:: procenti
    :answer_a: 0.25
    :feedback_a: Нетачно    
    :answer_b: 25
    :feedback_b: Нетачно    
    :answer_c: tata / 100
    :feedback_c: Тачно
    :answer_d: tata
    :feedback_d: Нетачно    
    :correct: c

    Ивана је одлучила да свој џепарац потроши на поклоне. 36% џепарца је потрошила на поклон за маму, а 39% џепарца је потрошила на поклон за сестру. Остатак џепарца је потрошила на поклон за тату. Допуни наредни програм који 
    израчунава колико новца је Ивана потрошила на поклон за тату, ако је њен џепарац 1135 динара?

	.. code-block:: python

	 dzeparac = 1135
	 mama = 36 
	 sestra = 39
	 tata = 100 - (mama + sestra)
	 poklon_za_tatu = 1135 * ___________
	 print(poklon_za_tatu)

