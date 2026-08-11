# Design Kit

**Версия:** см. [`VERSION`](VERSION) · история — [`CHANGELOG.md`](CHANGELOG.md)

Hypothesis-driven design как повторяемый процесс: каждый макет рождается из
проверяемой гипотезы, проходит проверку по UI/UX-правилам, а подтверждённые
выводы копятся в базу и переиспользуются.

## Что где

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
