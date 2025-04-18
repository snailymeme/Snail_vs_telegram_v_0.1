# Snail vs Telegram

Игра гонки улиток для Telegram бота и Web App

## Описание
Snail vs Telegram - это игра, где пользователи делают ставки на гонки улиток в Telegram. Улитки разных типов соревнуются в лабиринте, и игроки могут выбирать своего фаворита.

## Особенности
- Разные типы улиток с уникальным поведением (Racer, Explorer, Snake, Stubborn, Deadender)
- Процедурно генерируемые лабиринты
- Реализация Telegram Web App
- Интеграция с Telegram ботом

## Установка и запуск
1. Клонировать репозиторий
2. Установить зависимости: `npm install`
3. Запустить скрипт: `./restart.sh`

## Требования
- Node.js
- Python 3
- Токен Telegram бота (в файле .env)

## Подготовка проекта

### Шаг 1: Установка зависимостей

```bash
npm install
```

### Шаг 2: Настройка переменных окружения

Скопируйте `.env.example` в `.env` и настройте переменные окружения:

```bash
cp .env.example .env
```

Отредактируйте файл `.env` и укажите:

```bash
TELEGRAM_BOT_TOKEN=ваш_токен_бота
```

## Запуск проекта

### Вариант 1: Быстрый запуск всех компонентов

Для запуска всех компонентов (ngrok, HTTP сервер, Telegram Bot) используйте:

```bash
npm run dev
```

### Вариант 2: Запуск отдельных компонентов

#### Только HTTP сервер:

```bash
npm run app
```

#### Только Telegram бот:

```bash
npm run bot
```

#### Только ngrok туннель:

```bash
npm run ngrok
```

### Другие сценарии запуска

#### Запуск с очисткой портов:

```bash
npm run start:clean
```

## Структура проекта

```
├── js/
│   ├── modules/       # Модульные компоненты приложения
│   │   ├── config.js  # Конфигурация и константы
│   │   ├── ui.js      # Компоненты пользовательского интерфейса
│   │   ├── gameState.js  # Управление состоянием игры
│   │   └── ...
│   ├── patches/       # Патчи для разных типов улиток
│   └── main.js        # Основной скрипт приложения
├── images/            # Изображения для игры
├── css/               # CSS стили
├── bot.js             # Telegram бот
├── start.js           # Единый скрипт запуска
└── .env               # Переменные окружения
```

## Новая архитектура

Проект был реорганизован для улучшения модульности и производительности:

1. **Модульная структура**: Код разделен на логические модули с четкими обязанностями
2. **Оптимизация рендеринга**: Добавлена двойная буферизация для улучшения производительности Canvas
3. **Централизованная конфигурация**: Константы и настройки собраны в модуле config.js
4. **Улучшенная загрузка изображений**: Реализована система кэширования изображений
5. **Упрощенные скрипты запуска**: Все скрипты запуска объединены в один с параметрами

## Использование

1. В Telegram найдите своего бота и отправьте команду `/start`
2. Нажмите на кнопку "🎮 Играть" для открытия Web App
3. Выберите улитку и сделайте ставку
4. Нажмите "Начать гонку" и наблюдайте за соревнованием
5. Получите выигрыш, если ваша улитка победит!

## Текущие ограничения

> ⚠️ **Примечание:** В текущей версии новые кнопки выбора улиток имеют обновленный дизайн, но полная функциональность находится в процессе доработки. Они будут полностью активны в следующем обновлении.

## Разработчики

Проект Snail to Riches разрабатывается командой энтузиастов, любящих улиток и мини-игры для Telegram. 