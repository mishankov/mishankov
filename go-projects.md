# Проекты на Go

Самые новые проекты сверху

### [Web-tail](https://github.com/mishankov/web-tail)

Приложение для просмотра логов через браузер. Получение логов из локального файла, локального Docker контейнера, удалённого файла и удалённого Docker контейнера по SSH. Отправка на фронтенд по вевсокету. Фронтенд реализован на `Svelte`. Изначально бэкенд был написан на Node.JS. При переписывании на Golang исползовались библиотеки:
- `chi` - роутинг
- `gorilla/websocket` - вебсокеты для отправки логов на фронтенд

С помощью multistage build собирается легковесный Docker образ

Пайплайн на GitHub Action:
- Собирает бинарники для Lunux, macOS и Windows
- Собирает Docker образ и выгружает его в GitHub Packages

### [Advent of Code 2024](https://github.com/mishankov/adventofcode2024)

Решения первых 11 дней Advent of Code 2024 года

### [5 letters helper](https://github.com/mishankov/5-letters-helper)

В оригинале написанная на Python CLI тулза, которая подсказывает следующие возможные шаги в игре "5 букв" (аналог Wordle). В процессе переписывания выделил логику игры в отдельные модули и использовал их для написания Telegram бота с такой же функциональностью. Для хранения данных используется SQLite. Приложение пакуется в `Docker` контейнер для разворачивания на сервере с помощью `Docker compose`

### [jira_label_manager](https://github.com/mishankov/jira_label_manager)

Небольшая CLI тулза, которая позовляет навешивать и снимать лейблы с тасок в Jira. Переписал проект с языка Nim. Задачей было использовать горутины для распараеллеливания HTTP вызовов. Для синхронизации используется `sync.WaitGroup`

### [regexp](https://github.com/mishankov/regexp)

Первый мини проект, написанный по заданиям с CodeCrafters - https://app.codecrafters.io/courses/grep
