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
Обучить перцептрон в Unity

## Задание 1
### в проекте Unity реализовать перцептрон, который умеет производить вычисления:
OR | дать комментарии о корректности работы
AND | дать комментарии о корректности работы
NAND | дать комментарии о корректности работы
XOR | дать комментарии о корректности работы

Ход работы:
Прикрепил к пустому GameObject скрипт perceptron.cs, изучил его. 

### Добавил входные данные для функции OR
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

### Добавил входные данные для функции AND

![image](https://github.com/Slry1/AD/assets/129071869/3b808f61-1b5c-4455-b297-df4972df3cfd)
![image](https://github.com/Slry1/AD/assets/129071869/0ae700d8-7518-496a-a4dc-38bf9b70002c)

Повторяем тот же процесс для этой функции

![image](https://github.com/Slry1/AD/assets/129071869/c6167a10-b38f-4cd3-b728-94fa25903ac1)
![image](https://github.com/Slry1/AD/assets/129071869/7b36d038-1518-4990-940c-4ce7360a16f7)
![image](https://github.com/Slry1/AD/assets/129071869/7b877f10-f107-4c5f-b85b-ab9912fda557)
![image](https://github.com/Slry1/AD/assets/129071869/811781dc-32c7-4d37-abb0-5e2ea68ab09a)
![image](https://github.com/Slry1/AD/assets/129071869/470a39f9-e24a-46bb-bdb3-d1683167e16b)
![image](https://github.com/Slry1/AD/assets/129071869/ef1e1a27-fb64-4204-b091-0759125364b1)
![image](https://github.com/Slry1/AD/assets/129071869/b8dec21c-a38a-4443-a576-55f74b442ecb)
![image](https://github.com/Slry1/AD/assets/129071869/4f72ffb1-9fd6-4c35-808b-ce2a3ca787cf)

При обучении моделей мы можем наблюдать, что на 1-5 эпохах модель не может правильно обучится и выдает неправильные предикты, количество ошибок с возрастанием эпох не всегда уменьшается. На 6 эпохах и более модель обучается и дает правильные предикты

### Функция NAND
Таблица истинности для NAND:

![image](https://github.com/Slry1/AD/assets/129071869/af7b10f9-2da5-4cfa-bde6-353ae6f36a30)

Добавляем входные данные для NAND и тестируем обучаемость модели при разных эпохах...

![image](https://github.com/Slry1/AD/assets/129071869/eb4ebeb5-7eab-4015-ae02-700da1dc68ee)
![image](https://github.com/Slry1/AD/assets/129071869/edfa3d50-46ed-423c-8a84-9ea4f93ea48a)

![image](https://github.com/Slry1/AD/assets/129071869/476e69a9-2d33-42a7-8247-a67dfdf8ae1a)
![image](https://github.com/Slry1/AD/assets/129071869/f0c5f7f8-bba3-470f-95f2-95962f16704d)
![image](https://github.com/Slry1/AD/assets/129071869/b762965d-5d0c-449f-8122-92d419ba8006)
![image](https://github.com/Slry1/AD/assets/129071869/701eca47-7482-4e9d-824c-dc2e42e369d0)
![image](https://github.com/Slry1/AD/assets/129071869/abac2d86-d656-41e9-9421-d7c3a4ef6243)
![image](https://github.com/Slry1/AD/assets/129071869/c61a1de4-bc6b-4f60-b3d4-dee88fef53b6)
![image](https://github.com/Slry1/AD/assets/129071869/741d92e1-b667-4c55-aa68-d6e65aa03de4)
![image](https://github.com/Slry1/AD/assets/129071869/73e8f63f-71dc-4d95-a0d0-49aa3255265e)

Можем наблюдать разное количество ошибок на всех эпохах, это указывает на то, что при малом количестве эпох, успешность модели зависит от удачи. На эпохах 7 и более уже больше моделей успешно обучаются 

### XOR

Таблица истинности функции:

![image](https://github.com/Slry1/AD/assets/129071869/31c4b3f8-359d-472e-bce5-16739c2cc4c0)

Добавляем входные данные для XOR и тестируем модели на разных эпохах.

![image](https://github.com/Slry1/AD/assets/129071869/07d5828a-cfdf-49f5-9981-d3cc04591eed)
![image](https://github.com/Slry1/AD/assets/129071869/a7b393e1-dbd5-45ff-881e-356930e333cc)

![image](https://github.com/Slry1/AD/assets/129071869/8f97ed5a-2dca-4db5-b3f1-18c5ef20cfad)
![image](https://github.com/Slry1/AD/assets/129071869/0beb2172-b550-435d-b206-ef1c7247fc10)
![image](https://github.com/Slry1/AD/assets/129071869/217147d2-b93a-4124-a5f4-28e50af3a913)
![image](https://github.com/Slry1/AD/assets/129071869/10764266-db6f-4ed6-bb08-e4a6d3e45df0)
![image](https://github.com/Slry1/AD/assets/129071869/40ca9624-79fa-4f62-9218-d4e1a8a249d8)
![image](https://github.com/Slry1/AD/assets/129071869/f981bd4e-2c0f-4331-9c49-9f0a5cfbdf89)
![image](https://github.com/Slry1/AD/assets/129071869/0b01a598-a810-432f-b874-8ea9236cb1f9)
![image](https://github.com/Slry1/AD/assets/129071869/a425d292-8b6e-469c-8a96-c5795037a902)

Тут мы можем увидеть, что при обучении модели на малом количестве эпох, модель еще может случайно угадать ответ, но при дальнейшем обучении модель выдает всегда 4 ошибки. Это указывает на недостатки в самом методе обучения модели. Даже при 100 эпохах, когда модель должна быть переобученна в хлам, она выдает 4 ошибки.

![image](https://github.com/Slry1/AD/assets/129071869/99cfde80-df0c-444f-b499-67543f2e7389)




## Задание 2
### Построить графики зависимости количества эпох от ошибки  обучения. Указать от чего зависит необходимое количество эпох обучения.
Ход работы:

https://docs.google.com/spreadsheets/d/156yOswVvQjznHSDJu2H_wAbB_TYeE5IfkK5uF-whxCg/edit?usp=sharing

![image](https://github.com/Slry1/AD/assets/129071869/5f15bef5-d699-42ef-84fa-09917eba995d)

Данный метод обучения хорошо подходит для обучения простых функций по типу AND OR или NAND, а XOR напрочь отказывается обучаться.

Количество эпох для корректного обучения зависит от простоты датасета, чем сложнее датасет, тем больше эпох нужно чтобы модель могла вычленить корректную зависимость, но если работать с произвольными данными при увеличении эпох модель может переобучиться на одном датасете, и выдать меньше правильных ответов. В нашем датасете всего 2^2 возможных вариаций. Поэтому при излишних эпохах наша модель не пострадает.

На маленьком количестве эпох модель зачастую гадает, и может выдавать вообще любые ответы (1 или 0), допустим только нули или только единицы, с увеличением эпох растет и количество корректно обученных моделей, начиная примерно с 7 эпох модель может почти 100% корректно обучится

## Задание 3
### Построить визуальную модель работы перцептрона на сцене Unity.

Ход работы:
Создал 8 кубов, нули и единицы. Черные - нули, а белые это единицы. Логика состоит в том, что если результат соприкосновения двух кубов(единицы и нулей) равняется нулю, то оба объекта уничтожаются. Скрипт перцептрона прикреплен к верхним кубам

Ссылка на проект Unity с перцептроном: https://github.com/Slry1/Perceptron

```c#

using System.Collections;
using System.Collections.Generic;
using UnityEngine;

[System.Serializable]
public class TrainingSet
{
    public double[] input;
    public double output;
}

public class Perceptron : MonoBehaviour
{
    public GameObject attached;
    public TrainingSet[] ts;
    double[] weights = { 0, 0 };
    double bias = 0;
    double totalError = 0;

    double DotProductBias(double[] v1, double[] v2)
    {
        if (v1 == null || v2 == null)
            return -1;

        if (v1.Length != v2.Length)
            return -1;

        double d = 0;
        for (int x = 0; x < v1.Length; x++)
        {
            d += v1[x] * v2[x];
        }

        d += bias;

        return d;
    }

    double CalcOutput(int i)
    {
        double dp = DotProductBias(weights, ts[i].input);
        if (dp > 0) return (1);
        return (0);
    }

    void InitialiseWeights()
    {
        for (int i = 0; i < weights.Length; i++)
        {
            weights[i] = Random.Range(-1.0f, 1.0f);
        }
        bias = Random.Range(-1.0f, 1.0f);
    }

    void UpdateWeights(int j)
    {
        double error = ts[j].output - CalcOutput(j);
        totalError += Mathf.Abs((float)error);
        for (int i = 0; i < weights.Length; i++)
        {
            weights[i] = weights[i] + error * ts[j].input[i];
        }
        bias += error;
    }

    double CalcOutput(double i1, double i2)
    {
        double[] inp = new double[] { i1, i2 };
        double dp = DotProductBias(weights, inp);
        if (dp > 0) return (1);
        return (0);
    }

    void Train(int epochs)
    {
        InitialiseWeights();

        for (int e = 0; e < epochs; e++)
        {
            totalError = 0;
            for (int t = 0; t < ts.Length; t++)
            {
                UpdateWeights(t);
                Debug.Log("W1: " + (weights[0]) + " W2: " + (weights[1]) + " B: " + bias);
            }
            Debug.Log("Количество эпох: "+ (e+1) + " TOTAL ERROR: " + totalError);
        }
    }

    void Start()
    {
        attached = gameObject;
        Train(10);
        Debug.Log("Test 0 0: " + CalcOutput(0, 0));
        Debug.Log("Test 0 1: " + CalcOutput(0, 1));
        Debug.Log("Test 1 0: " + CalcOutput(1, 0));
        Debug.Log("Test 1 1: " + CalcOutput(1, 1));
    }

    void OnCollisionEnter(Collision collision)
    {
        int objNum = attached.name == "Cube 1" ? 1 : 0;
        int collidedNum = collision.gameObject.name == "Cube 1" ? 1 : 0;
        if (CalcOutput(objNum,collidedNum) == 0)
        {
            Destroy(collision.gameObject);
            Destroy(gameObject);
        }
    }

    void Update()
    {

    }
}

```

![image](https://github.com/Slry1/AD/assets/129071869/8c6e8a4d-ff35-4f8f-9645-18d4f089cdd2)


### OR

![image](https://github.com/Slry1/AD/assets/129071869/efc66fc4-f963-4c3c-968e-858f200305f9)

### AND

![image](https://github.com/Slry1/AD/assets/129071869/66fc76f9-8a24-4ba4-ab50-c3012dc9a393)

### NAND

![image](https://github.com/Slry1/AD/assets/129071869/8f5d0ad1-53d4-4b82-b52c-94fe2d1805d4)

### XOR

![image](https://github.com/Slry1/AD/assets/129071869/e6521796-9a70-4839-bcea-1f0bbd74859b)
![image](https://github.com/Slry1/AD/assets/129071869/eac545fe-14a1-4c5e-910e-d032616fdb15)

Т.к. перцептрон не обучается корректно на функции XOR, он выдает неправильные ответы. При 10 эпохах, 0 XOR 0 = 1 или 0 XOR 0, 0 XOR 1 = 1

## Выводы

В ходе работы был изучен, обучен и описан перцептрон на логических функциях OR, AND, NAND, XOR. Также была выявляена зависимость ошибок от количества эпох обучения. Построена визуальная модель работы перцептрона на сцене Unity. https://github.com/Slry1/Perceptron

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
