# lab7-puzhuk-notion — Puzhuk's Workspace

Author: Alexander Puzhuk | Студия проката фото- и видеотехники

**Опубликованная версия в Notion:**  
https://statuesque-bass-37b.notion.site/lab7-puzhuk-notion-Puzhuk-s-Workspace-41731880417e801b9bbded43fe8133e3

---

## Кнопка быстрого действия (Button)
* **Название:** `+ Быстрый заказ аренды (Puzhuk)`
* **Действие:** `Add page to Rentals_Puzhuk` (`OrderTitle = "Новый экспресс-заказ"`, `Status = "Активен"`)

---

## База данных 1: Clients_Puzhuk

| Name | Tier | Discount | Rentals_Puzhuk (Relation) |
| :--- | :--- | :--- | :--- |
| Алексей Волков | VIP | 15 | ORD-101 Съемка клипа |
| Студия КадрПро | VIP | 20 | ORD-108 Короткий метр |
| Мария Соколова | Regular | 10 | ORD-105 Документальный фильм |
| Дмитрий Лебедев | Regular | 10 | ORD-106 Свадебный проект |
| Илья Морозов | New | 0 | ORD-107 Подкаст в студии |
| Агентство Визуал | VIP | 15 | ORD-110 Репортаж |
| Анна Козлова | Regular | 5 | ORD-109 Обзор недвижимости |
| Павел Новиков | New | 0 | ORD-102 Реклама авто |
| КиноЛаб продакшн | VIP | 20 | ORD-104 Интервью |
| Елена Смирнова | Regular | 10 | ORD-103 Аэросъемка |

---

## База данных 2: Equipment_Puzhuk

| Model | Category | DailyRate | Rentals_Puzhuk (Relation) |
| :--- | :--- | :--- | :--- |
| Sony FX3 Cinema Line | Камера | 4500 | ORD-101 Съемка клипа |
| RED Komodo 6K | Камера | 8000 | ORD-109 Обзор недвижимости |
| DJI Inspire 3 | Дрон | 9500 | ORD-108 Короткий метр |
| DJI Mavic 3 Pro | Дрон | 3500 | ORD-103 Аэросъемка |
| Aputure LS 600d Pro | Свет | 2500 | ORD-107 Подкаст в студии |
| Nanlite Forza 300B | Свет | 1800 | ORD-105 Документальный фильм |
| Sony FE 24-70mm f/2.8 GM II | Оптика | 1500 | ORD-102 Реклама авто |
| Sigma 35mm f/1.4 Art | Оптика | 1000 | ORD-106 Свадебный проект |
| Rode Wireless PRO | Звук | 1200 | ORD-110 Репортаж |
| Zoom F6 Field Recorder | Звук | 1600 | ORD-104 Интервью |

---

## База данных 3: Rentals_Puzhuk

| OrderTitle | Status | ReturnDate | Days | Client (Relation) | Equipment (Relation) | OrderStatusFormula (Formula) |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| ORD-101 Съемка клипа | Активен | November 20, 2026 | 4 | Алексей Волков | Sony FX3 Cinema Line | ⏳ В аренде (осталось 6 дн.) |
| ORD-102 Реклама авто | Завершён | November 1, 2026 | 3 | Павел Новиков | Sony FE 24-70mm f/2.8 GM II | ✅ Сдан (3 дн.) |
| ORD-103 Аэросъемка | Активен | November 5, 2026 | 2 | Елена Смирнова | DJI Mavic 3 Pro | 🔥 Просрочен на 8 дн.! |
| ORD-104 Интервью | Завершён | October 25, 2026 | 1 | КиноЛаб продакшн | Zoom F6 Field Recorder | ✅ Сдан (1 дн.) |
| ORD-105 Документальный фильм | Активен | November 25, 2026 | 7 | Мария Соколова | Nanlite Forza 300B | ⏳ В аренде (осталось 11 дн.) |
| ORD-106 Свадебный проект | Бронь | December 1, 2026 | 2 | Дмитрий Лебедев | Sigma 35mm f/1.4 Art | ⏳ В аренде (осталось 17 дн.) |
| ORD-107 Подкаст в студии | Активен | November 8, 2026 | 1 | Илья Морозов | Aputure LS 600d Pro | 🔥 Просрочен на 5 дн.! |
| ORD-108 Короткий метр | Завершён | October 15, 2026 | 5 | Студия КадрПро | DJI Inspire 3 | ✅ Сдан (5 дн.) |
| ORD-109 Обзор недвижимости | Бронь | December 10, 2026 | 3 | Анна Козлова | RED Komodo 6K | ⏳ В аренде (осталось 26 дн.) |
| ORD-110 Репортаж | Активен | November 18, 2026 | 2 | Агентство Визуал | Rode Wireless PRO | ⏳ В аренде (осталось 4 дн.) |
