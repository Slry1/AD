# АНАЛИЗ ДАННЫХ И ИСКУССТВЕННЫЙ ИНТЕЛЛЕКТ [in GameDev]
Отчет по лабораторной работе #1 выполнил(а):
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
Ознакомиться с основными операторами зыка Python на примере реализации линейной регрессии.

## Задание 1
### в проекте Unity реализовать перцептрон, который умеет производить вычисления:
OR | дать комментарии о корректности работы
AND | дать комментарии о корректности работы
NAND | дать комментарии о корректности работы
XOR | дать комментарии о корректности работы

Ход работы:
Прикрепил к пустому GameObject скрипт perceptron.cs, изучил его. 

## Добавил входные данные для функции OR
![image](https://github.com/Slry1/AD/assets/129071869/ddd09606-a659-4eca-b9a5-95e31dcd4497)
![image](https://github.com/Slry1/AD/assets/129071869/d87f7300-799b-4227-b1da-c8d13d99eb2d)

После этого начал пробовать менять количество эпох для обучения

Для одной эпохи:

![image](https://github.com/Slry1/AD/assets/129071869/d3831170-bc55-43fb-93ec-e01cd6d16cd6)

Для двух:

![image](https://github.com/Slry1/AD/assets/129071869/50447eb6-dc51-4981-8867-9bf6ff34f965)

Для трех:

![image](https://github.com/Slry1/AD/assets/129071869/384b40c1-6396-41c0-ade5-0231bbfe1c14)
![image](https://github.com/Slry1/AD/assets/129071869/f45c862a-c3ce-4d2c-813b-8b0276117d63)

При трех эпохах некоторые модели уже могут научиться безошибочно выполнять функцию OR, но кажется, что нужно добавить еще эпох, чтобы все модели были обучены правильно

Четыре эпохи:

![image](https://github.com/Slry1/AD/assets/129071869/c37a3add-5842-4d80-aeba-9e9b21b7f007)
![image](https://github.com/Slry1/AD/assets/129071869/18b319a1-0102-46aa-9a08-dc6dfadf0031)

При четырех большинство моделей уже может правильно обучиться, однако некоторые модели все-равно могут допускать ошибки

Пять:

![image](https://github.com/Slry1/AD/assets/129071869/b1fac503-4d48-478b-9527-f2ff266e2c77)

Шесть:

![image](https://github.com/Slry1/AD/assets/129071869/1ff06acb-f06f-409d-8b23-2dca7d0035b4)

При пяти эпохах и более уже все модели могуть обучиться без ошибок.

## Добавил входные данные для функции AND

Повторяем тот же процесс для этой функции

![image](https://github.com/Slry1/AD/assets/129071869/c6167a10-b38f-4cd3-b728-94fa25903ac1)
![image](https://github.com/Slry1/AD/assets/129071869/7b36d038-1518-4990-940c-4ce7360a16f7)
![image](https://github.com/Slry1/AD/assets/129071869/7b877f10-f107-4c5f-b85b-ab9912fda557)
![image](https://github.com/Slry1/AD/assets/129071869/811781dc-32c7-4d37-abb0-5e2ea68ab09a)
![image](https://github.com/Slry1/AD/assets/129071869/470a39f9-e24a-46bb-bdb3-d1683167e16b)
![image](https://github.com/Slry1/AD/assets/129071869/ef1e1a27-fb64-4204-b091-0759125364b1)
![image](https://github.com/Slry1/AD/assets/129071869/b8dec21c-a38a-4443-a576-55f74b442ecb)
![image](https://github.com/Slry1/AD/assets/129071869/4f72ffb1-9fd6-4c35-808b-ce2a3ca787cf)

При обучении моделей мы можем наблюдать, что на 1-4





## Задание 2
### Построить графики зависимости количества эпох от ошибки  обучения. Указать от чего зависит необходимое количество эпох обучения.
- Перечисленные в этом туториале действия могут быть выполнены запуском на исполнение скрипт-файла, доступного [в репозитории](https://github.com/Den1sovDm1triy/hfss-scripting/blob/main/ScreatingSphereInAEDT.py).
- Для запуска скрипт-файла откройте Ansys Electronics Desktop. Перейдите во вкладку [Automation] - [Run Script] - [Выберите файл с именем ScreatingSphereInAEDT.py из репозитория].

Ход работы:


## Задание 3
### Построить визуальную модель работы перцептрона на сцене Unity.

Ход работы:


## Выводы

Абзац умных слов о том, что было сделано и что было узнано.

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
