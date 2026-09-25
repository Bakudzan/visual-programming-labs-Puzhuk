```mermaid
flowchart TD
    Start([Старт: Пациент пришел]) --> Check{Есть в базе?}
    Check -- Нет --> Create[Создать карту] --> ChooseDoc
    Check -- Да --> ChooseDoc[Выбор врача]
    ChooseDoc --> CheckSlots{Есть талоны?}
    CheckSlots -- Нет --> OtherDay[Запись на другой день] --> Print
    CheckSlots -- Да --> Print[Печать талона]
    Print --> Finish([Конец: Талон выдан])
```