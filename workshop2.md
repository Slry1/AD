# АНАЛИЗ ДАННЫХ И ИСКУССТВЕННЫЙ ИНТЕЛЛЕКТ
Отчет по лабораторной работе #2 выполнил(а):
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
Научиться передавать в Unity данные из Google Sheets с помощью Python.

## Задание 1
### Пошагово выполнить каждый пункт раздела "ход работы" с описанием и примерами реализации задач
Ход работы:
- Выберите одну из компьютерных игр, приведите скриншот её геймплея и краткое описание концепта игры. Выберите одну из игровых переменных в игре (ресурсы, внутри игровая валюта, здоровье персонажей и т.д.), опишите её роль в игре, условия изменения / появления и диапазон допустимых значений. Постройте схему экономической модели в игре и укажите место выбранного ресурса в ней.

### World of Warcraft

![image](https://github.com/Slry1/AD/assets/129071869/af69dd63-5fff-4ca9-8336-7391a831639d)
World of Warcraft представляет собой ММО РПГ, в которой игрок управляет одним игровым персонажем — обитателем фэнтезийной вселенной Warcraft. В роли этого персонажа игрок может исследовать виртуальный мир игры, сражаться с различными противниками, включая персонажей других игроков; выполнять задания неигровых персонажей, участвовать в совместном с другими игроками прохождении подземелий и других подобных занятиях. Успешное выполнение заданий позволяет игроку улучшить характеристики персонажа и его снаряжение, что открывает доступ к новым, более сложным заданиям и подземельям. Большинство заданий на начальном этапе выполняются в одиночку, но сложность заданий возрастает по мере увеличения уровня игрока, и многие задания предполагают, что игрок будет действовать в группе. Для каждой группы игроков, желающих посетить подземелье, создается его отдельная копия, так что разные группы игроков не могут помешать друг другу исследовать подземелье и собирать сокровища. Разные подземелья рассчитаны на игроков разного уровня и на разное количество участников — обычно речь о группе численностью до пяти персонажей, но игра может предлагать игрокам и «рейды», в которых может быть занято до 40 игроков одновременно. В составе группы игроки принимают на себя разные роли — обычно группа состоит из танка, лекаря и трёх бойцов: танк должен первым вступать в бой и отвлекать на себя врагов, лекарь — восстанавливать потерянные танком и бойцами очки здоровья, а бойцы — наносить как можно больше урона врагам и победить их как можно скорее. Как в подземельях, так и в общем мире игры существуют сильные враги и боссы, для победы над которыми необходимы слаженные действия группы игроков.

#### Золото.
Золото в игре является ключевой игровой валютой(аналог реальным деньгам), за которую можно купить почти все, даже реальные деньги. Нужно больше золота!
Эту валюту игрок может получить в качестве дропа с игрового моба, награды за выполненный квест, продажи игровых предметов вендорам(NPC продавцам) и другим игрокам через аукцион или обмен. Т.к. это является главной валютой WoW, за нее также можно предоставлять различного рода услуги, например прохождение рейда или получение достижений.
Тратить эту валюту можно на покупку расходников, материалов для крафта, различных маунтов(езодовых животных), экипировки, оружия, игровых услуг, оплату комиссии за выставление предметов на аукцион, оплату игровой подписки WoW, а также на починку снаряжения. Это основные убытки золота, из этого только малая часть выводится из игры, а большая курсирует между игроками. Из-за этого и того, что в игре очень большой приток золота, существует явная инфляция.
Диапозон допустимых значений. 1 бронза = 1/100 серебра. 1 серебро = 1/100 золота. При получении больше 99 бронзы или серебра оно автоматически переводится в более дорогую валюту. У золота таких ограничений нет, хотя лимит золота на одного персонажа 9,999,999.

![image](https://github.com/Slry1/AD/assets/129071869/7e521f08-231f-40e0-b5fa-f00ef0b68287)


## Задание 2
### С помощью скрипта на языке Python заполните google-таблицу данными, описывающими выбранную игровую переменную в выбранной игре (в качестве таких переменных может выступать игровая валюта, ресурсы, здоровье и т.д.). Средствами google-sheets визуализируйте данные в google-таблице (постройте график, диаграмму и пр.) для наглядного представления выбранной игровой величины.

```py

import gspread
import numpy as np
gc = gspread.service_account(filename='timohamalyshevdatascience-4cabc74eb811.json')
sh = gc.open("UnityWorkshop2")
rng = np.random.default_rng()
price_start = 100000 #gold
priceinf = 0
mon = list(range(1,11))
i = 0
while i <= len(mon):
    i += 1
    if i == 0:
        continue
    else:
        priceinf = rng.random()
        price_start = price_start*(0.65+priceinf)
        tempInf = str(price_start)
        tempInf = tempInf.replace('.',',')
        sh.sheet1.update(('A' + str(i)), str(i))
        sh.sheet1.update(('B' + str(i)), str(priceinf))
        sh.sheet1.update(('C' + str(i)), str(tempInf))
        print(tempInf)

```
![image](https://github.com/Slry1/AD/assets/129071869/faece205-af2b-42cc-8995-efcca88cd1ea)
Стоимость WoW токена

## Задание 3
### Настройте на сцене Unity воспроизведение звуковых файлов, описывающих динамику изменения выбранной переменной. Например, если выбрано здоровье главного персонажа вы можете выводить сообщения, связанные с его состоянием.

```cs

using System.Collections;
using System.Collections.Generic;
using UnityEngine;
using UnityEngine.Networking;
using SimpleJSON;

public class NewBehaviourScript : MonoBehaviour
{
    public AudioClip goodSpeak;
    public AudioClip normalSpeak;
    public AudioClip badSpeak;
    private AudioSource selectAudio;
    private Dictionary<string, float> dataSet = new Dictionary<string, float>();
    private bool statusStart = false;
    private int i = 1;

    // Start is called before the first frame update
    void Start()
    {
        StartCoroutine(GoogleSheets());
    }

    // Update is called once per frame
    void Update()
    {
        if (dataSet["Mon_" + i.ToString()] <= 150000 & statusStart == false & i != dataSet.Count)
        {
            StartCoroutine(PlaySelectAudioGood());
            Debug.Log(dataSet["Mon_" + i.ToString()]);
        }

        if (dataSet["Mon_" + i.ToString()] > 150000 & dataSet["Mon_" + i.ToString()] < 200000 & statusStart == false & i != dataSet.Count)
        {
            StartCoroutine(PlaySelectAudioNormal());
            Debug.Log(dataSet["Mon_" + i.ToString()]);
        }

        if (dataSet["Mon_" + i.ToString()] >= 200000 & statusStart == false & i != dataSet.Count)
        {
            StartCoroutine(PlaySelectAudioBad());
            Debug.Log(dataSet["Mon_" + i.ToString()]);
        }
    }

    IEnumerator GoogleSheets()
    {
        UnityWebRequest curentResp = UnityWebRequest.Get("https://sheets.googleapis.com/v4/spreadsheets/1AoMozYmNCb0HNveh7bV23EfZNLaBTVb9ACcz13CiIzQ/values/Лист1?key=AIzaSyBwlEL9nlbODC9PP1XaOFF81PvCASbA_To");
        yield return curentResp.SendWebRequest();
        string rawResp = curentResp.downloadHandler.text;
        var rawJson = JSON.Parse(rawResp);
        foreach (var itemRawJson in rawJson["values"])
        {
            var parseJson = JSON.Parse(itemRawJson.ToString());
            var selectRow = parseJson[0].AsStringList;
            dataSet.Add(("Mon_" + selectRow[0]), float.Parse(selectRow[2]));
        }
    }

    IEnumerator PlaySelectAudioGood()
    {
        statusStart = true;
        selectAudio = GetComponent<AudioSource>();
        selectAudio.clip = goodSpeak;
        selectAudio.Play();
        yield return new WaitForSeconds(3);
        statusStart = false;
        i++;
    }
    IEnumerator PlaySelectAudioNormal()
    {
        statusStart = true;
        selectAudio = GetComponent<AudioSource>();
        selectAudio.clip = normalSpeak;
        selectAudio.Play();
        yield return new WaitForSeconds(3);
        statusStart = false;
        i++;
    }
    IEnumerator PlaySelectAudioBad()
    {
        statusStart = true;
        selectAudio = GetComponent<AudioSource>();
        selectAudio.clip = badSpeak;
        selectAudio.Play();
        yield return new WaitForSeconds(4);
        statusStart = false;
        i++;
    }
}

```
Если стоимость WoW токена меньше 150к золота = хороший звук, от 150к до 200к = нормально, более 200к = "Вы самый жестокий тиран в королевстве, ваша светлость"


## Выводы

В ходе работы был изучен метод передачи данных из Google Sheets в Unity и их визуализации, а также заполенение данных в Google Sheets при помощи Python. Мною был приведен пример экономической модели игры World of Warcraft.
 
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
