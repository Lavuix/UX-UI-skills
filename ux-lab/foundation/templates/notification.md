# Шаблон: Notification (главный экран + панель уведомлений)

| Поле | Значение |
|------|----------|
| Сверка | ✔ сверено с Figma (node `40:2369`) |
| Уровень | шаблон (экран) |
| Источник | Figma · Life-04_Templates · страница «Notification» |
| fileKey | `g3P4HUG0FGh62FZHQKQW7l` (node `40:2369`) |
| Ссылка | https://www.figma.com/design/g3P4HUG0FGh62FZHQKQW7l/Life-04_Templates?node-id=40-2369 |

## Назначение

Главный экран-каталог (десктоп 1536×864): подразделения, поддержка, избранные
материалы — плюс всплывающая **панель уведомлений** поверх контента.

## Раскладка

Sidebar (rail 64) → Content: Header (56) → Block из двух колонок:
- **Sidemenu** (320): навигация из `Cell` (разделы Main + Catalog) и `Floating button` внизу.
- **All**: блок «Подразделения» (сетка иконок-ссылок), «Поддержка» (Doc/FAQ/Help),
  «Избранное» — вкладки (`Tabs`) + сетка `Cards` 3×N + `Action Button` «показать ещё».
- **Notification Block** — выпадающая панель: список `Cell` + `Action Button` (все уведомления).

## Из чего собран

- Sidebar → [`../components/sidebar-3-0.md`](../components/sidebar-3-0.md)
- Header → [`../components/header.md`](../components/header.md)
- Cell (2.0) → [`../components/cell-2-0.md`](../components/cell-2-0.md)
- Cards → [`../components/cards.md`](../components/cards.md)
- Tabs → [`../components/tabs.md`](../components/tabs.md)
- Floating Button → [`../components/floating-button.md`](../components/floating-button.md)
- Action Button → [`../components/action-button.md`](../components/action-button.md)

## Состояния / варианты

- Панель уведомлений открыта (поверх главного экрана).

## Когда применять

- Стартовый экран-каталог с разделами и лентой материалов; всплывающая панель
  уведомлений — типовой паттерн доступа к событиям из Header.

## Связанные

- Каталог компонентов: [`../components/INDEX.md`](../components/INDEX.md)
- Токены: [`../tokens.md`](../tokens.md)
- Текст — по [`../../rules/07-voice-and-copy.md`](../../rules/07-voice-and-copy.md).
