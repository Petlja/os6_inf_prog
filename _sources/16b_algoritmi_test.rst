Тест
============================

Питање 1.
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. mchoice:: к1
    :answer_a: Исписују се бројеви до n чија је цифра јединица већа од 2.
    :feedback_a: Тачно
    :answer_b: Исписују се парни бројеви до n.
    :feedback_b: Нетачно    
    :answer_c: Исписују се бројеви већи од 2.
    :feedback_c: Нетачно    
    :correct: a

    Шта је резултат извршавања селдећег програма? Изабери тачан одговор:

    (1)

    .. code-block:: python

     n = int(input())
     while n > 0:
     	if n % 10 > 2:
        	print(n)
     	n = n - 1

Питање 2.
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. mchoice:: к2
    :answer_a: За сваку дату страницу израчунава се површина квадрата са том странице.
    :feedback_a: Тачно
    :answer_b: израчунава се површина квадрата.
    :feedback_b: Нетачно    
    :answer_c: Ништа од наведеног.
    :feedback_c: Нетачно    
    :correct: a

    Шта је резултат извршавања селдећег програма? Изабери тачан одговор:

    .. code-block:: python

     def povrsina(a):
     	return a * a

     stranice = [13, 18, 43, 11, 8]
     for a in stranice:
     	print("Stranica:", a, "Povrsina:", povrsina(a))



Питање 3.
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. mchoice:: к3
    :answer_a: Oд унета три броја исписује се број који је мањи од 12.
    :feedback_a: Нетачно
    :answer_b: Oд унета три броја исписује се број који је већи од 12.
    :feedback_b: Тачно    
    :answer_c: Ништа од наведеног.
    :feedback_c: Нетачно    
    :correct: b

    Шта је резултат извршавања следећег кода? Изабери тачан одговор:

    .. code-block:: python

     for i in range(3):
     visina = int(input("Unesi broj:"))
     if visina > 12:  
        print (visina)

Питање 4.
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. mchoice:: к4
    :answer_a: :
    :feedback_a: Нетачно
    :answer_b: for
    :feedback_b: Тачно    
    :answer_c: >
    :feedback_c: Нетачно    
    :correct: b

    Шта би требало написати на место ___ како би се из листе издвојиле и исписале само температуре веће од 0?

    .. code-block:: python

     temperature = [2, -1, 0, -8, -10, -1, 4, 5, 8, 6]
     negativne_temperature = [t __ t in temperature if t > 0]
     print(negativne_temperature)


Питање 5.
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. mchoice:: m5
    :answer_a: i
    :feedback_a: Нетачно
    :answer_b: or
    :feedback_b: Нетачно    
    :answer_c: and
    :feedback_c: Тачно    
    :correct: c

    Шта би требало написати на место ___ како би код био исправан?

    .. code-block:: python

     prosek_ognjen = 4.75
     prosek_mira = 5.00
     prosek_jelica = 5.00
     if prosek_pera >= 4.50 ___ prosek_mira >= 4.50 ___ prosek_jelica >= 4.50:
     	print("Svi učenici su odlični")
     else:
     	print("Nisu svi učenici odlični")
