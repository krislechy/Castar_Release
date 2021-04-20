# Castar
## _Требования к системе_

- ОС: Windows
### Дистрибутивы
- [NetFramework 4.8](https://dotnet.microsoft.com/download/dotnet-framework/net48)
- [SQLLocalDB](https://download.microsoft.com/download/9/0/7/907AD35F-9F9C-43A5-9789-52470555DB90/ENU/SqlLocalDB.msi)

## _Настройка_
### Настройка бота Telegram
1. Начинаем диалог с [@BotFather](https://t.me/botfather) командой ```/start``` 
2. Создаем бота командой ```/newbot```, и следуем инструкции.
3. После создания бота необходимо запомнить ```API AccessToken```.
4. Прописываем стандартные команды для него, для этого пишем ```/setcommands``` и вставляем: 
```
n - Пример начисления: /n 21450.99 Газпром
fa - Быстрые команды
```
Готово, бот настроен.

### Настройка программы
1. Открываем меню и выбираем пункт ```Настройки```
2. В первую очередь выбираем путь к уже готовой базе в формате ```mdf```, она уже присутствует в репозитории.
3. В пункте ```Редактирование ключей и сессий``` переключаем флаг на ```Включен```.
4. В пункте ```Telegram Бот``` и в поле ```Ключ``` прописываем ```API AccessToken``` ранее полученный от [@BotFather](https://t.me/botfather) после создания бота.
5. Переключаем флаг ```Telegram Бот``` на ```Включен``` в пункте который находится ниже выбора пути к базе.
6. Добавляем пользователя указав его ```ID Telegram``` для того что бы узнать свой ```ID``` пишем своему новому боту комманду ```/start``` в ответ он напишет ```ID``` пользователя.
7. Для получения информации по чекам используются два сервиса, это ```ФНС России```([Личный кабинет](https://lkfl2.nalog.ru/lkfl/)) и [proverkacheka.com](https://proverkacheka.com/), в первом случае понадобиться логин/пароль от кабинета, во втором необходимо зарегистрироваться и получить API Key, для лучшей работы рекомендуется использовать оба варианта. В настройках имеются соответствующие поля, их необходимо заполнить.
### (Опционально) Быстрые команды меню FA
Для настройки необходимо ввести название и сумму покупки, эта информация будет отображаться в диалоге с ```Telegram Бот``` в соответствующем меню.
### (Опционально) Настройка ```Вотчеров(Watchers)``` 
На данный момент доступны вотчеры только ```Пятерочка``` и ```Магнит```.
Для их настройки необходимо заполнить поля ```Сессия``` ключем сессии вида
- Пятерочка: ```Token...```
- Магнит: ```Bearer ...```

Так же необходимо заполнить поля Карта (```GUID```) и Клиент(```ID```).

### Работа с программой
#### Варианты добавления покупки
1. Для добавления покупки достаточно написать ```Telegram Бот``` ```[Наименование покупки] [Сумма]```, например: ```Печеньки 129```, ```Порошок 320.99```, ```Зубная паста 99,99```
2. Сканируем QR-код на чеке:\
![image](https://user-images.githubusercontent.com/20987251/115427191-e9738700-a209-11eb-9a8a-8a4ea768340c.png)\
получаем текст ```t=20210420T1601&s=194.84&fn=9284440300459265&i=82218&fp=1724914770&n=1``` и отправляем боту.
3. Отправляем QR-код боту.\
![image](https://user-images.githubusercontent.com/20987251/115427591-440ce300-a20a-11eb-971d-13b125309cdd.png)
