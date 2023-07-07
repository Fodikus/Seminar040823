# GB_Python_10_12_14
Домашняя работа №2 к семинару "Знакомство с языком Python"

Задача 10: На столе лежат n монеток. Некоторые из них лежат вверх решкой, а некоторые – гербом. Определите минимальное число монеток, которые нужно перевернуть, чтобы все монетки были повернуты вверх одной и той же стороной. Выведите минимальное количество монет, которые нужно перевернуть.

```
import random

n = int(input("Количество монет: "))
orel = 0
reshka = 0
for i in range(n):
    x = random.randint(0,1)
    print(f"Орел(1) или решка(0): {x}")
    if x == 1:
        orel += 1
    else:
        reshka += 1

if orel < reshka:
    print(f"Переверните {orel} монет с орла на решку, их меньше всего. ")
elif orel == reshka:
    print(f"Количество орлов и решек одинаково, по {orel} штук. ")
else:
    print((f"Переверните {reshka} монет с решки на орла, их меньше всего. "))
```

Задача 12: Петя и Катя – брат и сестра. Петя – студент, а Катя – школьница. Петя помогает Кате по математике. Он задумывает два натуральных числа X и Y (X,Y≤1000), а Катя должна их отгадать. Для этого Петя делает две подсказки. Он называет сумму этих чисел S и их произведение P. Помогите Кате отгадать задуманные Петей числа.

```
x = int(input('Введите первое натуральное число X от 1 до 1000: '))
while x > 1000 or x <= 0:
    x = int(input("Вы ошиблись!\nВведите первое натуральное число X от 1 до 1000: "))

y = int(input('Введите второе натуральное число Y от 1 до 1000: '))
while y > 1000 or y <= 0:
    y = int(input("Вы ошиблись!\nВведите второе натуральное число Y от 1 до 1000: "))

stop = 0
for i in range(x):
    if stop != 1:
        for j in range(y):
            if stop != 1:
                if x == i + j and y == i * j:
                    print(f"Первое задуманное число: {i}, второе задуманное число: {j}.")
                    stop = 1
```

Задача 14: Требуется вывести все целые степени двойки (т.е. числа вида 2k), не превосходящие числа N.

```
n = int(input("Введите число N: "))
p = 1
while p <= n:
    print(p, end=" ")
    p = p * 2
```
