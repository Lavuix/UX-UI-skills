# Шаблон: Filters (таблица + панель фильтров)

| Поле | Значение |
|------|----------|
| Сверка | ✔ сверено с Figma (node `0:1`) |
| Уровень | шаблон (экран) |
| Источник | Figma · Life-04_Templates · страница «Filters» |
| fileKey | `g3P4HUG0FGh62FZHQKQW7l` (node `0:1`) |
| Ссылка | https://www.figma.com/design/g3P4HUG0FGh62FZHQKQW7l/Life-04_Templates?node-id=0-1 |

## Назначение

Таблица заявок (`requests_table`, spreadsheet) с выезжающей справа **панелью
фильтров**: наборы значений (`MultiSelect`) и диапазоны дат (`Calendar`) + применение.

## Раскладка

Sidebar + Header + content (Sidemenu + spreadsheet). Поверх справа — панель
**filters** (379): шапка (`Popup` с заголовком и закрытием), `Divider`, список
фильтров (MultiSelect × N, Calendar × N) со скроллом, внизу кнопка «Применить».

## Из чего собран

- Sidebar, Header → [`../components/sidebar-3-0.md`](../components/sidebar-3-0.md), [`../components/header.md`](../components/header.md)
- MultiSelect → [`../components/multi-select.md`](../components/multi-select.md)
- Calendar/InputDate → [`../components/input-date.md`](../components/input-date.md)
- Action Button, Divider → [`../components/action-button.md`](../components/action-button.md), [`../components/system.md`](../components/system.md)

## Состояния / варианты

- Панель фильтров открыта поверх таблицы; кнопка применения внизу.

## Когда применять

- Фильтрация таблиц/списков: значения через MultiSelect, периоды через Calendar.
  Панель — выезжающая справа, применение — Primary внизу.

## Связанные

- Каталог компонентов: [`../components/INDEX.md`](../components/INDEX.md)
- Шаблон таблицы с деталью: [`sidepage.md`](sidepage.md)
- Токены: [`../tokens.md`](../tokens.md)
- Текст — по [`../../rules/07-voice-and-copy.md`](../../rules/07-voice-and-copy.md).
