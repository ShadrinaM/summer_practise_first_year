# Проект "Решение интеграла методом левых прямоугольников на C++"

## Описание
Этот проект представляет собой программу на языке программирования C++, предназначенную для вычисления численного значения интеграла функции Function(x, t) в заданном интервале [a, b] с заданным шагом h и количеством разбиений n.

## Функции

Function(x, t)
Функция, для вычисления точного значения функции при данных значений x и t.

IntegralSum(x, n, h)
Функция, для вычисления  значения интеграла в заданной точке х, для количества разбиений n и с шагом h.

## Переменные
x, y, h, a, b, c, d - переменные типа double, используемые для хранения значений x, значения функции, шага, нижней границы интегрирования, верхней границы интегрирования, нижней границы для x и верхней границы для x соответственно.
N[4] - массив типа double, хранящий информацию о необходимых количествах разбиений.
discrepancy[4] - массив типа double, хранящий значения максимальной невязки.
s - строка, используемая для промежуточного хранения данных, выдаваемых программой.

## Алгоритм
Пользователь вводит значения нижней границы интегрирования a, верхней границы интегрирования b, нижней границы для x c, верхней границы для x d и четыре числа разбиений N.
Перебирая x от c до d с шагом (d - c) / 20, программа вычисляет значение функции в заданной точке и записывает его в строку s, разделяя знаками табуляции.
Для каждого значения x, программа также вычисляет значение интеграла с четырьмя различными количествами разбиений N и записывает их в строку s, разделяя знаками табуляции.
Программа сравнивает значения, полученные разными способами, и записывает в массив discrepancy[4] их разницу, если значение невязки получается больше чем то, которое до этого находилось в массиве.
Программа заменяет все символы «.» в строке s на «,».
Программа записывает все данные из строки s в текстовый файл table.txt.
Программа записывает в файл table.txt значения максимальных невязок для каждого из значений разбиения и закрывает файл.
Для создания графиков функций используйте Microsoft Excel. Откройте файл table.txt через Excel, задайте параметры импорта с табуляцией в качестве разделителя и постройте графики, основываясь на полученных приближенных и точных значениях в одной системе координат.
