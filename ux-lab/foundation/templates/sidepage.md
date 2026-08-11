# Шаблон: SidePage (таблица + боковая панель детали)

| Поле | Значение |
|------|----------|
| Сверка | ✔ сверено с Figma (node `1:15486`) |
| Уровень | шаблон (экран) |
| Источник | Figma · Life-04_Templates · страница «SidePage» |
| fileKey | `g3P4HUG0FGh62FZHQKQW7l` (node `1:15486`) |
| Ссылка | https://www.figma.com/design/g3P4HUG0FGh62FZHQKQW7l/Life-04_Templates?node-id=1-15486 |

## Назначение

Список/таблица заявок (`requests_table`, spreadsheet) с **боковой панелью детали**
(SidePage), выезжающей поверх: карточка заявки с аккордеонами, блоком «О заявке»,
статусами и действием «Отметить выполненным». Десктоп 1920.

## Раскладка

Sidebar + Header + **content** с таблицей (title/toolbar сверху, строки со статусами).
Поверх справа — **SidePage** (боковая панель): вкладки, аккордеоны (`.about`,
`.accordion`), теги, кнопки действий.

## Из чего собран

- Sidebar, Header → [`../components/sidebar-3-0.md`](../components/sidebar-3-0.md), [`../components/header.md`](../components/header.md)
- Tag (статусы), Userpic → [`../components/tag.md`](../components/tag.md), [`../components/userpic.md`](../components/userpic.md)
- Tabs, Action Button → [`../components/tabs.md`](../components/tabs.md), [`../components/action-button.md`](../components/action-button.md)
- InputSearch, Dropdown → [`../components/input-search.md`](../components/input-search.md), [`../components/dropdown.md`](../components/dropdown.md)

## Состояния / варианты

- Таблица заявок; открытая боковая панель детали (SidePage) с раскрытыми аккордеонами;
  действие «Отметить выполненным».

## Когда применять

- Просмотр записи из таблицы без ухода с экрана — деталь в боковой панели (master-detail).
- Для полноэкранной формы редактирования — шаблон [`create.md`](create.md).

## Связанные

- Каталог компонентов: [`../components/INDEX.md`](../components/INDEX.md)
- Токены: [`../tokens.md`](../tokens.md)
- Текст — по [`../../rules/07-voice-and-copy.md`](../../rules/07-voice-and-copy.md).
