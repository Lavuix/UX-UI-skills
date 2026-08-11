# RUNNING — как запустить оркестр из CLI

Design Kit — это **вход и база правил**. Собирает макеты внешняя цепочка агентов
**Design Orchestra**: [github.com/chefspb-arch/design-orchestra](https://github.com/chefspb-arch/design-orchestra).
Ниже — как поднять её из терминала, чтобы кит заработал.

## Что нужно

- **Claude Code** (подписка Pro/Max/Team).
- **Figma MCP** (remote) + место **Dev** или **Full** на платном тарифе Figma.
- Оболочка: **POSIX shell** (macOS/Linux) или **PowerShell 5.1+** (Windows).
  Инсталлятор под Windows — на PowerShell; под Unix агенты ставятся одной ссылкой.

## Установка команды `orchestra`

Скачай и распакуй репозиторий (Code → Download ZIP), затем из его корня:

### macOS / Linux

```bash
chmod +x dist/orchestra.sh
mkdir -p ~/.local/bin
ln -s "$PWD/dist/orchestra.sh" ~/.local/bin/orchestra
```

Проверь, что `~/.local/bin` в `PATH` (иначе `orchestra` не найдётся):

```bash
echo $PATH | tr ':' '\n' | grep -q "$HOME/.local/bin" && echo ok || echo 'add ~/.local/bin to PATH'
```

Если `ok` не вывелось — добавь в `~/.zshrc` строку `export PATH="$HOME/.local/bin:$PATH"`
и открой новый терминал.

> `orchestra -Share` (`--share`) под Unix недоступна — требует Windows-анонимизации.

### Windows (PowerShell)

```powershell
powershell -ExecutionPolicy Bypass -File .\install.ps1
```

Регистрирует команду `orchestra`. Перезапусти PowerShell. Если «скрипты запрещены» —
`Set-ExecutionPolicy -Scope CurrentUser RemoteSigned`.

## Запуск в проекте

```bash
cd path/to/your/project    # твой проект (НЕ папка design-orchestra)
orchestra                  # изолированно ставит агентов в проект
claude                     # проверь в шапке: путь — ТВОЙ проект
```

Внутри Claude Code — по порядку:

```
/start                     # первая команда сессии, без текста рядом
/feature specs/your-spec.md
```

**Почему `/start` первой и без сопроводительного текста:** иначе Figma-плагин
может перехватить запрос. `/feature` запускает полную цепочку: спека → макеты с
гейтами решений.

## Команды внутри Claude Code

| Команда | Что делает |
|---------|-----------|
| `/start` | инициализация сессии оркестра |
| `/feature specs/<файл>.md` | полный цикл: спека → макеты с гейтами |
| `/concept` | визуальные направления для greenfield |
| `/foundation` | дизайн-система из референса |
| `/log <описание>` | записать правку, сделанную вручную вне цикла |

## Команды в терминале

| Команда | Что делает |
|---------|-----------|
| `orchestra` | установить агентов в текущий проект |
| `orchestra -Status` | версия, состояние «мозга», где лежит seed |
| `orchestra -Update` | обновить агентов; мозг/спеки не трогаются, изменённое → `*.bak` |
| `orchestra -Promote` | правила проекта → общий seed (для новых проектов) |
| `orchestra -Share` | предложить правила в публичный seed (только Windows) |

## Что оркестр создаёт в проекте

- `.claude/agents|skills/` — копии агентов (перезаписываются `-Update`).
- `brain/` — обучение под проект (правила, которые ведёт Chronicler).
- `specs/` — спеки-входы (сюда кладёшь файлы из этого кита).
- `PROJECT.md` — паспорт проекта (собирает Scout).
- `CHANGELOG-DESIGN.md` — **история версий дизайна** (ведёт Chronicler).

## Два разных версионирования — не путать

| | Файл | Кто ведёт | Что версионирует |
|---|---|---|---|
| **Кит** | [`VERSION`](VERSION) + [`CHANGELOG.md`](CHANGELOG.md) | ты, вручную (SemVer) | правила, токены, плейбук, best-practices |
| **Дизайн** | `CHANGELOG-DESIGN.md` в проекте | агент Chronicler | сами макеты и решения по ним |

## Куда ложится этот кит

- `specs/` кормит `/feature`.
- `ux-lab/foundation/tokens.md` — источник стиля.
- `ux-lab/rules/` — чеклист для гейтов ревью.
- `ux-lab/best-practices/` — переносится в правила `brain/`, когда Chronicler
  начнёт их предлагать.

## Seed (общая база правил)

- macOS/Linux: `${XDG_DATA_HOME:-~/.local/share}/design-orchestra/seed`
- Windows: `%APPDATA%\design-orchestra\seed`

## Типовые грабли

- **`orchestra: command not found`** → `~/.local/bin` не в `PATH` (см. выше) либо
  не перезапустил терминал.
- **`/feature` «съел» Figma-плагин** → запускай `/start` первой командой, без текста рядом.
- **Scout не видит библиотеку** → опубликуй её (Assets → Publish) и включи в файле.
