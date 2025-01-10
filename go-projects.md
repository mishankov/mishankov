# Проекты на Go

Самые новые проекты сверху

### [Logman](https://github.com/mishankov/logman) (work in progress)

> Golang, DI, TDD, Github Actions

Библиотека для логирования, предоставляющая возможность как использование без дополнительной настройки так и глубокую кастомизацию с помощью DI. Написана по методологии TDD, высокий процент покрытия тестами

### [Simple System Monitor](https://github.com/mishankov/simple-system-monitor)

> Golang, Docker, Github Actions, SvelteKit, WebSocket

Веб-приложение для мониторинга ресурсов Linux сервера. Приложение написано в гексагональной архитектуре. Для репозиториев написаны тесты. Конфигурация через переменные окружения

### [Web-tail](https://github.com/mishankov/web-tail)

> Golang, Docker, Github Actions, Svelte, WebSocket

Веб-приложение для просмотра логов. Получение логов из локального файла, локального Docker контейнера, удалённого файла и удалённого Docker контейнера по SSH. Отправка на фронтенд по вебсокету. Фронтенд реализован на `Svelte`. Изначально бэкенд был написан на Node.JS. При переписывании на Golang использовались библиотеки:
- `chi` - роутинг
- `gorilla/websocket` - вебсокеты для отправки логов на фронтенд

С помощью multistage build собирается легковесный Docker образ

Пайплайн на GitHub Action:
- Собирает бинарники для Linux, macOS и Windows
- Собирает Docker образ и выгружает его в GitHub Packages

### [Advent of Code 2024](https://github.com/mishankov/adventofcode2024)

> Golang, Github Actions

Решения первых 11 дней Advent of Code 2024 года. Корректность алгоритмов относительно тестового инпута проверяется с помощью стандартных инструментов тестирования Golang

### [5 letters helper](https://github.com/mishankov/5-letters-helper)

> Golang, Docker

В оригинале написанная на Python CLI тулза, которая подсказывает следующие возможные шаги в игре "5 букв" (аналог Wordle). В процессе переписывания выделил логику игры в отдельные модули и использовал их для написания Telegram бота с такой же функциональностью. Роутинг на стандартном `net/http`. Для хранения данных используется SQLite. Приложение пакуется в `Docker` контейнер для разворачивания на сервере с помощью `Docker compose`

### [jira_label_manager](https://github.com/mishankov/jira_label_manager)

> Golang

Небольшая CLI тулза, которая позволяет навешивать и снимать лейблы с тасок в Jira. Переписал проект с языка Nim. Задачей было использовать горутины для распараллеливания HTTP вызовов. Для синхронизации используется `sync.WaitGroup`

### [regexp](https://github.com/mishankov/regexp)

> Golang

Первый мини проект, написанный по заданиям с CodeCrafters - https://app.codecrafters.io/courses/grep
