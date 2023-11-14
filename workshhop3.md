# АНАЛИЗ ДАННЫХ И ИСКУССТВЕННЫЙ ИНТЕЛЛЕКТ
Отчет по лабораторной работе #3 выполнил(а):
- Малышев Тимофей Евгеньевич
- РИ220930
Отметка о выполнении заданий (заполняется студентом):

| Задание | Выполнение | Баллы |
| ------ | ------ | ------ |
| Задание 1 | * | 60 |
| Задание 2 | * | 20 |
| Задание 3 | * | 20 |

знак "*" - задание выполнено; знак "#" - задание не выполнено;

Работу проверили:
- к.т.н., доцент Денисов Д.В.
- к.э.н., доцент Панов М.А.
- ст. преп., Фадеев В.О.

[![N|Solid](https://cldup.com/dTxpPi9lDf.thumb.png)](https://nodesource.com/products/nsolid)

[![Build Status](https://travis-ci.org/joemccann/dillinger.svg?branch=master)](https://travis-ci.org/joemccann/dillinger)

Структура отчета

- Данные о работе: название работы, фио, группа, выполненные задания.
- Цель работы.
- Задание 1.
- Код реализации выполнения задания. Визуализация результатов выполнения (если применимо).
- Задание 2.
- Код реализации выполнения задания. Визуализация результатов выполнения (если применимо).
- Задание 3.
- Код реализации выполнения задания. Визуализация результатов выполнения (если применимо).
- Выводы.
- ✨Magic ✨

## Цель работы
Разработать оптимальный баланс для десяти уровней игры Dragon Picker

## Задание 1
### Предложите вариант изменения найденных переменных для 10 уровней в игре. Визуализируйте изменение уровня сложности в таблице. 
Ход работы:
У дракона есть переменная speed, отвечающая за скорость его полёта.
Количество энергетических щитов.
Время спавна яиц.
А также я добавил свою переменную. Некий гоал, чтобы пройти на следующий уровень, количество яиц нужных для прохождения на следующую по сложности сцену

![image](https://github.com/Slry1/AD/assets/129071869/91aa5068-a182-48e1-b15f-7a53a3d34733)


https://docs.google.com/spreadsheets/d/1J4yuhRYRWakPQwz5t9bnkk7gWQXyqX089jOoQ9Drd1A/edit?usp=sharing

## Задание 2
### Создайте 10 сцен на Unity с изменяющимся уровнем сложности.
Ход работы:
Было создано 10 сцен. У каждой сцены есть buildIndex, в зависимости от него былы изменены переменные.
Также в счетчике очков добавил условие перехода на следующую сцену (score > 10*buildIndex) NextLevel()

## Задание 3
### Решение в 80+ баллов должно заполнять google-таблицу данными из Python. В Python данные также должны быть визуализированы.
Ход работы:
```py
from matplotlib import pyplot as plt 
import gspread
import numpy as np
gc = gspread.service_account(filename='timohamalyshevdatascience-4cabc74eb811.json')
sh = gc.open("UnityWorkshop3").sheet1
levels = range(1,11)
speed = [1 + (i-1)*2 for i in levels]
eggtimer = [2 - (i-1)*0.2 if i <7 else 1.5 - (i-1)*0.1  for i in levels]
shields = [3,3,3,3,2,2,2,1,1,1]
goal = [i*10 for i in levels]

for i in levels:
    sh.update_cell(3, i, speed[i-1])
    sh.update_cell(6, i, eggtimer[i-1])
    sh.update_cell(9, i, shields[i-1])
    sh.update_cell(12, i, i*10)

plt.plot(levels, speed)  
plt.title("Скорость дракона")
plt.xticks(ticks=levels, labels=levels) 
plt.ylabel('Speed')
plt.xlabel('Уровень')
plt.show()

plt.plot(levels, eggtimer)  
plt.title("Таймер появления яиц") 
plt.ylabel('Time in sec')
plt.xlabel('Уровень')
plt.show()

plt.plot(levels, shields)  
plt.title("Количество энергетических щитов") 
plt.ylabel('Щиты')
plt.xlabel('Уровень')
plt.show() 

plt.plot(levels, goal)  
plt.title("Количество очков для прохождения уровня") 
plt.ylabel('Очки')
plt.xlabel('Уровень')
plt.show() 
```
![image](https://github.com/Slry1/AD/assets/129071869/14a6d146-3058-437d-8273-c3e2eb23d940)
![image](https://github.com/Slry1/AD/assets/129071869/87b6dae5-a98e-41e9-9418-1619efb45720)


## Выводы
В ходе работы был рассмотрен прототип игры Dragon Picker, в нем были выявлены переменные, которые можно было отредактировать для балансировки сложности. Была созданна и заполена через Python gspread Google-таблица, визуализированы переменные, через matplotlib в коде, в таблице при помощи встроенных методов. Также в прототип игры было добавленно 10 сцен, в которых постепенно увелчивается сложность.

| Plugin | README |
| ------ | ------ |
| Dropbox | [plugins/dropbox/README.md][PlDb] |
| GitHub | [plugins/github/README.md][PlGh] |
| Google Drive | [plugins/googledrive/README.md][PlGd] |
| OneDrive | [plugins/onedrive/README.md][PlOd] |
| Medium | [plugins/medium/README.md][PlMe] |
| Google Analytics | [plugins/googleanalytics/README.md][PlGa] |

## Powered by

**BigDigital Team: Denisov | Fadeev | Panov**
