# Design Kit

> 🟢 **Впервые здесь? → [START-HERE.md](START-HERE.md)** — инструкция для новичка:
> что открыть, как рисовать макеты через Claude (CLI / настольный / VS Code),
> два режима и как отправить находку в библиотеку практик.

**Версия:** см. [`VERSION`](VERSION) · история — [`CHANGELOG.md`](CHANGELOG.md)

Hypothesis-driven design как повторяемый процесс: каждый макет рождается из
проверяемой гипотезы, проходит проверку по UI/UX-правилам, а подтверждённые
выводы копятся в базу и переиспользуются.

## Что где

- **[`CLAUDE.md`](CLAUDE.md)** — инструкция для CLI-агента: как работать с китом и
  когда подсказывать, что зафиксировать (Claude Code читает её автоматически).
- **[`RUNNING.md`](RUNNING.md)** — как запустить оркестр из CLI (macOS/Linux + Windows).
- **[`VERSION`](VERSION)** + **[`CHANGELOG.md`](CHANGELOG.md)** — версионирование кита (SemVer).
- **`ux-lab/`** — ядро процесса:
  - `README.md` — схема цикла и карта папок (начни отсюда).
  - `playbook/` — как делать по каждой фазе: гипотезы, проверка, оркестратор,
    тесты, сборка, извлечение стиля.
  - `rules/` — свод самых важных UI/UX-правил (+ Definition of Done).
  - `foundation/tokens.md` — реальные токены, извлечённые из Figma.
  - `templates/`, `hypotheses/`, `best-practices/` — шаблоны и база знаний.
- **`specs/`** — спеки-входы для оркестра Design Orchestra (`/feature specs/<файл>.md`).

## С чего начать

1. Прочитать `ux-lab/README.md` — как устроен цикл.
2. Свериться с `ux-lab/rules/README.md` — чеклист Definition of Done.
3. Завести гипотезу из `ux-lab/templates/hypothesis.md`, оформить спеку в `specs/`.
4. Запустить оркестр по `RUNNING.md`: `orchestra` → `claude` → `/start` → `/feature`.

## Как пополнять и версионировать

Кит живёт за счёт того, что тяжело давшиеся уроки в него **возвращаются**. Порядок
(подробно — в [`CLAUDE.md`](CLAUDE.md)):

1. **Долго с чем-то возились / нашли неочевидное решение** → запиши паттерн:
   скопируй `ux-lab/best-practices/patterns/_TEMPLATE.md`, заполни, добавь строку в
   `ux-lab/best-practices/INDEX.md`. Уровень уверенности не завышай: пока это вывод
   из работы, а не A/B — ставь ⚪ допущение или 🟡 тесты.
2. **Любое изменение `ux-lab/` или `specs/`** → пункт в `CHANGELOG.md` + поднятая
   версия в `VERSION` по SemVer (MAJOR ломает, MINOR добавляет, PATCH правит).
3. Зафиксируй:
   ```bash
   git add -A && git commit -m "..." && git tag vX.Y.Z && git push && git push --tags
   ```

Claude Code при работе в этом репо читает `CLAUDE.md` и сам подсказывает шаги 1–2.

## Лицензия

[MIT](LICENSE) © Lavuix.
