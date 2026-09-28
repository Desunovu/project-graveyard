# Архив проектов

Монорепозиторий с завершёнными и замороженными проектами. Каждый проект лежит в
`projects/<имя>/` и содержит **полный состав файлов** на момент архивации.

> **История сжата.** Вместо исходной истории каждого проекта здесь один коммит с
> финальным состоянием кода. Всего 6 коммитов и 566 исходных коммитов. Причина —
> архив предназначен для хранения состояния, а не для работы с `git blame`,
> `git bisect` или историей изменений. Оригиналы с полной историей остались на GitHub.

## Состав архива

| # | Проект | Стек | Файлов | Исходных коммитов | Последний коммит | Был |
|---|--------|------|-------:|------------------:|-----------------|-----|
| 1 | [ariadne-react-store](projects/ariadne-react-store) | Python, JavaScript, React, GraphQL | 178 | 303 | 2024-01-31 | public |
| 2 | [fastapi-vue-blog](projects/fastapi-vue-blog) | Python, Vue, TypeScript, MongoDB | 134 | 193 | 2023-12-27 | public |
| 3 | [RSLogix_signal_processing](projects/RSLogix_signal_processing) | Python, Shell | 26 | 19 | 2022-08-29 | public |
| 4 | [simintech-arduino-training-stand](projects/simintech-arduino-training-stand) | C++ | 5 | 8 | 2023-11-27 | private |
| 5 | [rocket_simulation](projects/rocket_simulation) | Python | 16 | 12 | 2022-09-01 | private |
| 6 | [emoji-search-engine](projects/emoji-search-engine) | Python | 8 | 31 | 2024-06-20 | private |

**Итого: 367 файлов, 6 проектов.** Все 367 файлов сверены по SHA-1 с исходными
репозиториями — расхождений нет.

---

## 1. ariadne-react-store

Учебный проект интернет-магазина: GraphQL-бэкенд на Ariadne и SQLAlchemy,
фронтенд на React.

- **Стек:** Python, JavaScript, HTML, CSS, Dockerfile, Mako, Shell
- **Темы:** `ariadne` `graphql` `minio` `online-store` `pet-project` `postgresql` `react` `sqlalchemy`
- **Период:** 2022-08-21 → 2024-01-31 · 303 коммита · 178 файлов
- **Исходник:** <https://github.com/Desunovu/ariadne-react-store>

## 2. fastapi-vue-blog

Учебный проект блога: FastAPI + MongoDB в бэкенде, Vue 3 + TypeScript во
фронтенде, генерация статей через GPT.

- **Стек:** Vue, TypeScript, Python, Dockerfile, JavaScript, HTML, Sass
- **Темы:** `beanie` `fastapi` `mongodb` `pet-project` `vuejs`
- **Лицензия:** MIT
- **Период:** 2023-07-21 → 2023-12-27 · 193 коммита · 134 файла
- **Исходник:** <https://github.com/Desunovu/fastapi-vue-blog>

## 3. RSLogix_signal_processing

Обработка сигналов ПЛК: генератор конфигураций Allen-Bradley RSLogix из
Excel-шаблонов, выгрузка тегов и программ для Studio 5000.

- **Стек:** Python, Shell
- **Период:** 2022-06-20 → 2022-08-29 · 19 коммитов · 26 файлов
- **Исходник:** <https://github.com/Desunovu/RSLogix_signal_processing>

## 4. simintech-arduino-training-stand

Учебный стенд «Связь Arduino Nano со средой моделирования SimInTech».

- **Стек:** C++
- **Период:** 2023-04-09 → 2023-11-27 · 8 коммитов · 5 файлов
- **Исходник:** <https://github.com/Desunovu/simintech-arduino-training-stand>

## 5. rocket_simulation

Двумерный симулятор ракеты на Python (физика, рендеринг, звук, меню).

- **Стек:** Python
- **Размер:** ~36 МБ — в основном `demo.gif` (27,6 МБ) и аудио
- **Период:** 2020-06-11 → 2022-09-01 · 12 коммитов · 16 файлов
- **Исходник:** <https://github.com/friends-of-steve-rambo/rocket_simulation>

## 6. emoji-search-engine

Telegram-бот для поиска эмодзи по текстовому описанию.

- **Стек:** Python
- **Период:** 2024-06-14 → 2024-06-20 · 31 коммит · 8 файлов
- **Исходник:** <https://github.com/Desunovu/emoji-search-engine>

---

## Что важно знать об этом архиве

### Лицензии

Лицензия указана **только** у `fastapi-vue-blog` (MIT). У остальных пяти
проектов лицензии нет, то есть по умолчанию действует «все права защищены» —
свободного использования, копирования и распространения кода нет. Если нужен
другой статус, лицензию нужно добавить явно.

### Исключённые файлы

`projects/emoji-search-engine/.env` намеренно не включён. Файл был закоммичен в
оригинале в обход `.gitignore` и содержал заглушку `BOT_TOKEN`. Перед
публикацией архива всё содержимое репозиториев было просканировано на
утечку ключей — реальных секретов не обнаружено, ротация не требуется.

### Чего здесь нет

При слиянии репозиториев **не переносятся** (это ограничение GitHub, а не
сборки): issues, pull requests, releases, wiki, звёзды, watchers, topics и
description. Вся эта информация осталась в исходных репозиториях.

### Проекты, которые намеренно не вошли

- `obsidian` — активная личная база заметок
- `wannabuythis` — живой портфолио-проект

Они не архивировались и остаются в исходных репозиториях.

### Как читать этот архив

```bash
cd projects/<имя>
# каждый проект самодостаточен и запускается из своей папки
```
