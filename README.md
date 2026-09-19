# SсheduleNSMK

Веб-приложение для создания и управления расписанием учебных занятий.

## Возможности

- просмотр расписания по группам и дням недели;
- поддержка двух учебных недель;
- добавление, редактирование и удаление занятий;
- управление группами, преподавателями, предметами и аудиториями;
- несколько предметов у одного преподавателя;
- Drag & Drop для перемещения занятий;
- обмен занятиями при перемещении в занятую ячейку;
- проверка конфликтов расписания;
- поиск;
- заметки к занятиям;
- печать расписания;
- тёмная тема;
- разграничение прав доступа.

## Роли

- **Администратор** — управление пользователями и справочниками.
- **Преподаватель** — работа с доступными предметами и занятиями.
- **Студент** — просмотр расписания.

## Технологии

- PHP
- Laravel
- SQLite
- Blade
- JavaScript
- CSS
- Vite

## Установка

### 1. Клонирование репозитория

```bash
git clone https://github.com/KarKar3333/WebShedule.git
cd WebShedule
```

### 2. Установка PHP-зависимостей

```bash
composer install
```

### 3. Установка JavaScript-зависимостей

Windows PowerShell:

```powershell
npm.cmd install
```

Если PowerShell разрешает запуск `npm.ps1`, можно использовать:

```bash
npm install
```

### 4. Создание файла окружения

Windows PowerShell:

```powershell
Copy-Item .env.example .env
```

### 5. Создание необходимых директорий Laravel

Windows PowerShell:

```powershell
New-Item -ItemType Directory -Force storage\framework\cache\data
New-Item -ItemType Directory -Force storage\framework\sessions
New-Item -ItemType Directory -Force storage\framework\views
New-Item -ItemType Directory -Force storage\logs
New-Item -ItemType Directory -Force bootstrap\cache
```

### 6. Генерация ключа приложения

```bash
php artisan key:generate
```

### 7. Создание базы данных

Проект использует SQLite.

Windows PowerShell:

```powershell
New-Item database/database.sqlite -ItemType File
```

### 8. Создание таблиц

```bash
php artisan migrate
```

### 9. Заполнение базы начальными данными

```bash
php artisan db:seed
```

### 10. Сборка frontend

Для первого запуска:

```powershell
npm.cmd run build
```

После выполнения должна появиться:

```text
public/build/manifest.json
```

### 11. Запуск Laravel

```bash
php artisan serve
```

После запуска открыть:

```text
http://127.0.0.1:8000
```

## Запуск frontend в режиме разработки

Для разработки можно использовать Vite:

```powershell
npm.cmd run dev
```

Эту команду нужно оставить запущенной в отдельном терминале.

В другом терминале запустить Laravel:

```bash
php artisan serve
```

## Запуск после первой установки

Терминал 1:

```powershell
npm.cmd run dev
```

Терминал 2:

```bash
php artisan serve
```

Затем открыть:

```text
http://127.0.0.1:8000
```

## Сборка frontend

Production-сборка:

```powershell
npm.cmd run build
```

## База данных

Проект использует SQLite.

Структура базы данных создаётся с помощью Laravel Migration:

```bash
php artisan migrate
```

Начальные данные создаются командой:

```bash
php artisan db:seed
```

Локальная SQLite-база не хранится в репозитории.

## Структура проекта

```text
SheduleNSMK/
├── app/
├── bootstrap/
├── config/
├── database/
│   ├── factories/
│   ├── migrations/
│   └── seeders/
├── public/
├── resources/
│   ├── css/
│   ├── js/
│   └── views/
├── routes/
├── storage/
├── tests/
├── artisan
├── composer.json
├── composer.lock
├── package.json
├── package-lock.json
├── phpunit.xml
├── vite.config.js
├── .env.example
├── .gitignore
└── README.md
```


## Отчет по дневнику 
### день 1 

#### Макет главного меню

<img width="841" height="594" alt="изображение" src="https://github.com/user-attachments/assets/3461ac77-793e-470c-bbfe-7410618e500f" />

### день 2

#### Главное меню

<img width="1919" height="914" alt="изображение" src="https://github.com/user-attachments/assets/d50ce423-d745-45ff-9c47-fdbdc0f152bc" />

#### Раздел руппы

<img width="1907" height="645" alt="изображение" src="https://github.com/user-attachments/assets/927390c9-e03a-4680-b4b2-2d6789deab01" />

##### Создание группы и редактирование

<img width="1919" height="496" alt="изображение" src="https://github.com/user-attachments/assets/63dd49d7-416a-42db-8cb8-9887b093be0f" />
<img width="1919" height="465" alt="изображение" src="https://github.com/user-attachments/assets/434b005a-4eca-415e-b863-940370e9443b" />

### Раздел преподаватели 

<img width="1919" height="534" alt="изображение" src="https://github.com/user-attachments/assets/ce5e0b60-b454-4a95-9f2e-a6dcbc5a33b6" />

##### Создание преподавателей и редактирование 

<img width="1123" height="714" alt="изображение" src="https://github.com/user-attachments/assets/1164440d-0cad-4962-801c-7e4f1ce3a64d" />
<img width="1133" height="740" alt="изображение" src="https://github.com/user-attachments/assets/eec674e5-eb22-4a5f-90c8-43b4b2a5606d" />

### Раздел Дисциплины

<img width="1919" height="620" alt="изображение" src="https://github.com/user-attachments/assets/23f567f5-7998-483a-be61-e07888bfd5d8" />

##### Создание дисциплин и редактирование

<img width="1107" height="765" alt="изображение" src="https://github.com/user-attachments/assets/6af833cd-9960-41a7-b9b6-c5c8f800446f" />
<img width="1175" height="697" alt="изображение" src="https://github.com/user-attachments/assets/8efa345a-ae03-49eb-aaad-f0105157f943" />



### День 4 
#### Система Drag & Drop 
<img width="1913" height="909" alt="изображение" src="https://github.com/user-attachments/assets/dfbae074-0e61-4d75-8ed8-d7279054f1ca" />
<img width="1919" height="911" alt="изображение" src="https://github.com/user-attachments/assets/cd7e9175-9fea-4052-b9ef-e800393bea7f" />
<img width="1914" height="898" alt="изображение" src="https://github.com/user-attachments/assets/6120b586-fc71-49ba-a7e0-8cb2066ecd8c" />


#### конфликт преподавателей, групп, дисциплин
<img width="1915" height="908" alt="изображение" src="https://github.com/user-attachments/assets/e91052ce-0286-4e95-b3e0-d2e5a48e8d5d" />

### День 5
#### Индивидуальное задание
##### учет пользователей
<img width="1919" height="918" alt="изображение" src="https://github.com/user-attachments/assets/555a3462-5d0d-4ad8-88d9-323a91f7ff9c" />

##### Создание пользователей и редактирование
<img width="1128" height="629" alt="изображение" src="https://github.com/user-attachments/assets/8da80427-6257-4b3c-aabe-756d89587f3b" />
<img width="1196" height="610" alt="изображение" src="https://github.com/user-attachments/assets/8b8172b1-edb6-46e7-828b-f69ade626d4a" />

##### Разграничение ролей 

###### Страница авторизации

<img width="1919" height="916" alt="изображение" src="https://github.com/user-attachments/assets/a5a65c9e-df45-4806-b6c9-2bd7b5938b15" />

###### Студент

<img width="1919" height="911" alt="изображение" src="https://github.com/user-attachments/assets/50e659a7-9d34-43ea-aa98-5148db62673f" />

<img width="1919" height="912" alt="изображение" src="https://github.com/user-attachments/assets/7a4a7a2d-657c-43be-b9de-afe5ed1fed18" />

##### Преподаватель 

<img width="1911" height="910" alt="изображение" src="https://github.com/user-attachments/assets/9980865c-37e9-45f6-a972-94180e899cb0" />

Ограничение прав доступа 

<img width="1909" height="896" alt="изображение" src="https://github.com/user-attachments/assets/5294ae02-a748-4802-9385-3b6ef60fc5be" />



