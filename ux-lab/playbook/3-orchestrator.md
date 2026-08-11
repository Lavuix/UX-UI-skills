# 3. Как запустить оркестратор

Design Orchestra — цепочка агентов Claude Code, которая собирает Figma-макеты из
спеки: [github.com/chefspb-arch/design-orchestra](https://github.com/chefspb-arch/design-orchestra).

> Полная инструкция по запуску из CLI (macOS/Linux + Windows, грабли, seed) — в
> [`RUNNING.md`](../../RUNNING.md) в корне кита. Здесь — краткая выжимка.

## Что нужно

- Claude Code (подписка Pro/Max/Team).
- Figma MCP (remote) + место Dev или Full на платном тарифе Figma.
- POSIX shell (macOS/Linux) или PowerShell 5.1+ (Windows). Агенты — markdown и
  работают где угодно.

## Установка команды `orchestra`

Скачать репозиторий (Code → Download ZIP), распаковать, затем из его корня:

**macOS / Linux:**
```bash
chmod +x dist/orchestra.sh
mkdir -p ~/.local/bin
ln -s "$PWD/dist/orchestra.sh" ~/.local/bin/orchestra   # ~/.local/bin должен быть в PATH
```

**Windows (PowerShell):**
```powershell
powershell -ExecutionPolicy Bypass -File .\install.ps1   # затем перезапусти PowerShell
```

## Первый запуск

```
cd path/to/project      # твой проект
orchestra               # изолированная установка агентов в проект
claude                  # проверь в шапке: путь — ТВОЙ проект
/start                  # первой командой сессии, без текста рядом
/feature specs/your-spec.md
```

## Команды

| Команда | Что делает |
|---------|-----------|
| `orchestra` | установить агентов в текущий проект |
| `orchestra -Status` | версия, состояние «мозга», где лежит seed |
| `orchestra -Update` | обновить агентов; мозг/спеки не трогаются, изменённое → `*.bak` |
| `orchestra -Promote` | правила проекта → общий seed (для новых проектов) |
| `orchestra -Share` | предложить правила в публичный seed (единственная команда, что ходит в сеть) |

## Цепочка агентов

Scout (паспорт проекта) → Spec Analyst (план + 4 гейта) → UX Advisor (обоснование
против прецедентов) → Builder (пишет в Figma) → Respondent (панель, слепой A/B) →
Chronicler (журнал → правила → метрика обучения). Плюс `/concept` (визуальные
направления для greenfield) и `/foundation` (дизайн-система из референса). Два
места, где решение принимаешь ты.

## Грабли из FAQ

- Начинай сессию с `/start` **первой** командой, без текста рядом — иначе
  Figma-плагин перехватит запрос. Затем `/feature specs/<файл>.md`.
- «orchestra не найдена» → перезапусти PowerShell.
- «скрипты запрещены» → `Set-ExecutionPolicy -Scope CurrentUser RemoteSigned`.
- Scout «не видит» библиотеку → опубликуй её (Assets → Publish) и включи в файле.

## Как ложится наш ux-lab

Наши файлы — вход и база для оркестра: `specs/` кормит `/feature`,
`foundation/tokens.md` — источник стиля, `rules/` — чеклист для гейтов,
`best-practices/` можно переложить в правила `brain/`, когда Chronicler начнёт их
предлагать.
