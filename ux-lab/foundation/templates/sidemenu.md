# Шаблон: Sidemenu (раздел с боковым меню и таблицами)

| Поле | Значение |
|------|----------|
| Сверка | ✔ сверено с Figma (node `1:8358`) |
| Уровень | шаблон (экран) |
| Источник | Figma · Life-04_Templates · страница «Sidemenu» |
| fileKey | `g3P4HUG0FGh62FZHQKQW7l` (node `1:8358`) |
| Ссылка | https://www.figma.com/design/g3P4HUG0FGh62FZHQKQW7l/Life-04_Templates?node-id=1-8358 |

## Назначение

Рабочий раздел сервиса с боковым меню и списком/таблицей (десктоп 1920×1080).
На странице несколько экранов-состояний: **Сервисы**, статус **«Черновик»**,
**«Отметить выполненным»**, **«Информация о сервисе»**, табличный вид (spreadsheet).

## Раскладка

Sidebar (rail 64) → Content: Header (56) → Block: **Sidemenu** (навигация раздела)
+ **All** с **Toolbar** сверху (поиск, сортировка, действия) и таблицей/списком.

## Из чего собран

- Sidebar, Header, Toolbar → [`../components/sidebar-3-0.md`](../components/sidebar-3-0.md), [`../components/header.md`](../components/header.md), [`../components/toolbar.md`](../components/toolbar.md)
- Cell (2.0) → [`../components/cell-2-0.md`](../components/cell-2-0.md)
- Tag (статусы строк) → [`../components/tag.md`](../components/tag.md)
- Userpic → [`../components/userpic.md`](../components/userpic.md)
- Dropdown, InputSearch → [`../components/dropdown.md`](../components/dropdown.md), [`../components/input-search.md`](../components/input-search.md)
- Action Button, Pagination → [`../components/action-button.md`](../components/action-button.md), [`../components/pagination.md`](../components/pagination.md)

## Состояния / варианты

- Список «Сервисы», строка со статусом «Черновик», действие «Отметить выполненным»,
  экран «Информация о сервисе», таблица (spreadsheet).

## Когда применять

- Разделы управления списками/таблицами: заявки, задачи, сервисы — с фильтрами,
  сортировкой и статусами (Tag). Пустое состояние — через Empty Content.

## Связанные

- Каталог компонентов: [`../components/INDEX.md`](../components/INDEX.md)
- Токены: [`../tokens.md`](../tokens.md)
- Текст — по [`../../rules/07-voice-and-copy.md`](../../rules/07-voice-and-copy.md).
