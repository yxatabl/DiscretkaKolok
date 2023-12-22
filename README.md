## Теоретический минимум по Дискретной Математике. Модуль 2
1. Определение высказывания - утверждение, о котором можно сказать, что оно истинно или ложно

3. Арность операции (функции) - число аргументов данной операции
4. Булева алгебра - множество B, в которое входят элементы 0 и 1, на котором заданы бинарные операции конъюнкции и дизъюнкции, и унарная операция отрицания
    - Закон коммутативности
    - Закон ассоциативности
    - Закон дистрибутивности
    - Закон тождества
    - Закон дополнения
5. Булево множество - множество B, состоящее только из 0 и 1
6. ~~Закон единственности дополнения~~ (Гитхаб, контора *********(плохих людей), не дает нормально систему уравнений вставить)
8. Закон инволюции: $\neg\neg a = a$
9. ~~Теорема склеивания~~ (см. пункт 5)
10. ~~В чем отличие функции и формулы?~~ (Философия какая-то, а мы здесь не за этим)
11. Число булевых функций n аргументов - $2^{2^n}$
12. ДНФ - дизъюнктивная нормальная форма - дизъюнкция выражений, которые либо:
    - отдельный аргумент (возможно с инверсией) $A, \neg A$
    - простая конъюнкция некоторых аргументов $AB, \neg AC$
13. КНФ - конъюнктивная нормальная форма - конъюнкция выражений, которые либо:
    - отдельный аргумент (возможно с инверсией)
    - простая дизъюнкция некоторых аргументов
14. Минтерм - булева функция, которая принимает единичное значение только на одном наборе значений переменных
15. СДНФ - совершенная дизъюнктивная нормальная форма - представление функции в виде дизъюнкции минтермов
16. Импликанта функции $f$ - функция $\varphi$, все минтермы которой, входят в множество минтермов функции $f$ 
17. Простая импликанта - импликанта, состоящая из одной простой конъюнкции, такой, что никакая её часть не является импликантой функции
18. Число импликант функции - $2^m$, где $m$ - число минтермов
19. Минимизация булевой формулы - нахождение наименьшего числа простых импликант, которые в дизъюнкции описывают исходную функцию \
Методы минимизации:
    - Алгебраический
    - Меиод Квайна
    - Карты Карно
20. Сокращенная ДНФ - запись функции, в которой:
    1. Любые два слагаемых отличажтся минимум в двух местах
    2. Ни один из конъюнктов не содержится в другом
21. Тупиковая ДНФ - сокращенная ДНФ, которая не содержит лишних (не влияющих на таблицу истинности) импликант
22. Минимальная ДНФ - тупиковая ДНФ, которая содержит минимальное число вхождений переменных
23. Макстерм - булева функция, принимающая единичные значения на всех наборах аргументов, кроме одного
24. СКНФ - КНФ, которая не имеет одинаковых дизъюнкций и все они полные (макстермы)
25. Теорема разложения для ДНФ/КНФ: \
    ДНФ: $f(A_1, A_2,..., A_n) = A_1 * f(1, A_2, ..., A_n) + \neg A_1*f(0, A_2, ..., A_n)$ \
    КНФ: $f(A_1, A_2,..., A_n) = [A_1 + f(0, A_2, ..., A_n)] * [\neg A_1 + f(1, A_2, ..., A_n)]$
26. Полином Жегалкина - полином с коэффициентами 0 и 1, где произведение представлено операцией конъюнкции, а сложение - сложением по модулю 2 ($XOR$)\
Методы построения:
    1. Преобразование ДНФ
    1. Метод неопределенных коэффициентов
    1. Метод треугольников
    1. Метод Паскаля
27. Суперпозиция функций - функция, полученная из некоторого множества функций путем подстановок одной функции в другую и/или отождествления переменных 
28. Подстановка функции $g$ в функцию $f$ - замена $i$-го аргумента функции $f$ значением функции $g$
29. Отождествление переменных в функции f - подстановка $i$-го аргумента функции $f$ вместо $j$-го
30. Замкнутое множество функций - такое множество, что любая функция алгебры логики, выражаемая с помощью содержащихся в множестве функций, уже содержится в этом множестве
31. Замыкание множества функций - некоторое подмножество всех булевых функций, являющихся суперпозициями функций из $A$. Обозначается $[A]$
32. Полная система функций - множество функций, для которого замыкание совпадает с множеством всех булевых функций
33. Безызбыточная полная система функций - полная система функций, которая перестает быть таковой после исключения из неё любой функции
34. Самодвойственная функция - функция, которая на противоположных наборах дает противоположные значения (число самодвойственных функций - $2^{2^{n-1}}$ - половина числа наборов)
35. Линейная функция - функция, которая не имеет конъюнкций в своем представлении в виде полинома Жегалкина (число линейных функций - $2^{n+1}$)
36. Монотонная функция - функция, которая на сравнимых наборах не убывает
37. Сравнимые наборы - $a$ и $b$, если $\forall i: a_i \leq b_i$ (возрастающие наборы)
38. Функция, сохраняющая константу - функция, возвращающая 0/1 на нулевом/единичном наборе аргументов (число функций, сохраняющих ноль/единицу - $2^{2^n-1}$)
39. Формулировка критерия Поста - набор булевых функций является полным тогда и только тогда, когда он не содержится полностью ни в одном из предполных классов $S, M, L, T_0, T_1$ 
40. Полные системы из одной функции:
    - стрелка Пирса ($A \downarrow B$)
    - штрих Шеффера ($A | B$)
41. Частично определенная (недоопределенная) функция - булева функция, значение которой определено не на всех наборах
42. Кодирование - это функция $c: A^* \rightarrow B^*$, где $B$ - кодирующий алфавит
43. Однозначно декодируемый код - функция $C$, которая обладает свойством, что $a_1 \not= a_2 \Rightarrow c(a_1) \not = c(a_2)$ (инъекция)
44. Равномерный код - кодирование каждого символа алфавита производится с помощью строк одинаковой длины (блоковый)
45. Энтропия сообщения - частота встречаемости символов в кодируемом сообщении
46. Неравенство Крафта-Макмиллана - пусть заданы кодируемый и кодирующий алфавиты, состоящие из $n$ и $d$ символов, соответсвенно, и заданы желаемые длины кодовых слов: $l_1, l_2, ..., l_n$. Тогда необходимым и достаточным условием существования разделимого и префиксного кодов, обладающих заданным набором длин кодовых слов, является выполнение неравенства: ${\sum}^n_{i=1}d^{-l_i} \leq 1$
48. Префиксная/суффиксная схема - код, в котором, никакое кодовое слово не является началом/концом другого
49. Избыточность схемы алфавитного кодирования - это средняя длина ее кодового слова
50. Формула подсчета избыточности схемы: $l = {\sum}^n_{i=1} p_i*l_i, \\ P = \{p_1, p_2, ..., p_n\},$ $l_i$ - длина кодового слова $c_i$
51. Код Хаффмана
    1. Символы входного алфавита образуют список свободных узлов. Каждый лист имеет вес, который может быть
    равен либо вероятности, либо количеству вхождений символа в сжимаемое сообщение
    2. Выбираются два свободных узла дерева с наименьшими весами
    3. Создается их родитель с весом, равным их суммарному весу
    4. Родитель добавляется в список свободных узлов, а два его потомка удаляются из этого списка
    5. Одной дуге, выходящей из родителя, ставится в соответствие бит 1, другой — бит 0. Битовые значения ветвей, исходящих от корня, не зависят от весов потомков
    6. Шаги, начиная со второго, повторяются до тех пор, пока в списке свободных узлов не останется только один
    свободный узел. Он и будет считаться корнем дерева
52. Код Шеннона - Фано
    1. Символы первичного алфавита выписывают по убыванию вероятностей
    2. Символы полученного алфавита делят на две части, суммарные вероятности символов которых максимально близки друг другу
    3. В префиксном коде для первой части алфавита присваивается двоичная цифра «0», второй части — «1»
    4. Полученные части рекурсивно делятся, и их частям назначаются соответствующие двоичные цифры в префиксном коде.
53. Арифметическое кодирование - алгоритм сжатия информации без потерь, который при кодировании ставит в соответствие тексту вещественное число из отрезка $[0;1)$
54. Расстояние Хэмминга - число позиций, в которых различаются соответсвующие символы двух строк одинаковой длины
55. ~~Код Хэмминга~~ (Лень писать, и так понятно)
56. ~~Принцип поиска и исправление ошибок в коде Хэмминга~~ (Лень писать, и так понятно) 
57. Код Грея - такое упорядочевание двоичных векторов, что соседние векторы находятся на расстоянии Хэмминга равное единице (отличаются только в одном разряде)
58. Циклический код - код, в котором первый и последний вектора отличаются в одном разряде
