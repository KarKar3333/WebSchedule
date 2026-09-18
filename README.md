````markdown
# SheduleNSMK

Веб-приложение для создания и управления расписанием учебных занятий.

## Возможности

- просмотр расписания по группам и дням недели;
- поддержка двух учебных недель;
- добавление, редактирование и удаление занятий;
- управление группами, преподавателями, предметами и аудиториями;
- привязка нескольких предметов к одному преподавателю;
- Drag & Drop для перемещения занятий;
- обмен занятиями при перемещении в занятую ячейку;
- проверка конфликтов расписания;
- поиск по расписанию;
- добавление заметок к занятиям;
- печать расписания;
- тёмная тема;
- разграничение прав доступа пользователей.

## Роли

В системе предусмотрены три роли:

- **Администратор** — управление пользователями и справочниками;
- **Преподаватель** — работа с доступными ему предметами и занятиями;
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

### 1. Клонирование

```bash
git clone <URL_РЕПОЗИТОРИЯ>
cd SheduleNSMK
````

### 2. Установка PHP-зависимостей

```bash
composer install
```

### 3. Установка JavaScript-зависимостей

```bash
npm install
```

### 4. Настройка окружения

Создать `.env` из `.env.example`.

Windows PowerShell:

```powershell
Copy-Item .env.example .env
```

Linux/macOS:

```bash
cp .env.example .env
```

### 5. Генерация ключа приложения

```bash
php artisan key:generate
```

### 6. Создание базы данных

Проект использует SQLite.

Создать файл базы данных:

Windows PowerShell:

```powershell
New-Item database/database.sqlite -ItemType File
```

Linux/macOS:

```bash
touch database/database.sqlite
```

В `.env` указать:

```env
DB_CONNECTION=sqlite
```

### 7. Создание таблиц

Выполнить миграции:

```bash
php artisan migrate
```

При необходимости заполнить базу данными:

```bash
php artisan db:seed
```

### 8. Запуск

Запустить Laravel:

```bash
php artisan serve
```

Для разработки frontend:

```bash
npm run dev
```

После запуска открыть адрес, указанный командой `php artisan serve`.

## Сборка frontend

Для production-сборки:

```bash
npm run build
```

## Структура проекта

```text
app/
├── Http/
│   ├── Controllers/
│   ├── Middleware/
│   └── Requests/
├── Models/
└── Providers/

database/
├── migrations/
├── seeders/
└── database.sqlite

resources/
├── css/
├── js/
└── views/

routes/
└── web.php

public/
└── assets/

tests/
├── Feature/
└── Unit/

artisan
composer.json
composer.lock
package.json
package-lock.json
vite.config.js
.env.example
.gitignore
README.md
```

## Работа с расписанием

Расписание представлено в виде таблицы.

* столбцы — учебные группы;
* строки — дни недели и пары;
* карточки — занятия.

Карточка занятия содержит информацию о предмете, преподавателе, аудитории, неделе и заметке.

Занятия можно перемещать между ячейками с помощью Drag & Drop.

При перемещении занятия в занятую ячейку система выполняет обмен занятий.

## База данных

Структура базы данных создаётся с помощью Laravel Migration:

```bash
php artisan migrate
```

Основные сущности:

* пользователи;
* группы;
* преподаватели;
* предметы;
* аудитории;
* занятия;
* связи преподавателей и предметов.

Файл SQLite не хранится в репозитории и создаётся локально при установке проекта.
