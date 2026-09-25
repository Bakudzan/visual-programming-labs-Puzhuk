```mermaid

flowchart TD

&#x20;   Start(\[Старт: Открытие приложения]) --> CheckCars{Авто рядом есть?}

&#x20;   CheckCars -- Нет --> SearchMore\[Расширить радиус поиска] --> Start

&#x20;   CheckCars -- Да --> Book\[Забронировать авто]

&#x20;   Book --> Inspect\[Осмотр кузова]

&#x20;   Inspect --> CheckDamage{Есть царапины?}

&#x20;   CheckDamage -- Да --> SendPhoto\[Отправить фото в поддержку] --> Unlock

&#x20;   CheckDamage -- Нет --> Unlock\[Нажать 'Начать аренду']

&#x20;   Unlock --> OpenDoors\[Разблокировка дверей]

&#x20;   OpenDoors --> Finish(\[Конец: Поездка началась])

```



