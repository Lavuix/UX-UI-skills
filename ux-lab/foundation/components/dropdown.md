# Компонент: Dropdown

| Поле | Значение |
|------|----------|
| Статус | ? не финализирован |
| Сверка | ✔ сверено с Figma (node `5:21`) |
| Уровень | молекула |
| Источник | Figma · Life-20_Kit_Light · страница «Dropdown» |
| fileKey | `M03BFuFuarl4z15GXCFnxh` (node `5:21`) |
| Ссылка | https://www.figma.com/design/M03BFuFuarl4z15GXCFnxh/Life-20_Kit_Light?node-id=5-21 |

> Статус `?` — компонент ещё не финализирован. В файле есть версии Legacy и V2 —
> для нового используем **V2**.

## Назначение

Выпадающее меню: список действий или выбор, в т.ч. вложенное многоуровневое дерево
и список с поиском.

## Оси вариантов

- **Меню (Dropdown V2):** Quantity = 1…8 (число пунктов)
- **Пункт (`.Item`):** Type = Icon+Text · Photo+Text × State = Enabled · Hovered · Pressed · Disabled
- **Многоуровневое (`Levels`):** Level = 1…10 (+ Group Name) × Select = No · Yes ×
  State = Active · Hovered · Pressed · Disabled × Kind = Multi · Alone
- **Список с поиском (`DropdownListSearch`):** Type = List · SearchResultIn · Start · Unsearch

## Форма и размеры

Меню ≈280 по ширине; высота по числу пунктов. Пункт с иконкой/фото.

## Правила применения

- Открывается по действию (кнопка, поле), закрывается по выбору/клику вне.
- **Levels** — для вложенных категорий; **Kind = Multi** для множественного выбора.
- Поиск (`DropdownListSearch`) — когда пунктов много.
- Для нового используем **V2**, Legacy не берём в новые макеты.
- Компонент берём из библиотеки как есть — привязки токенов/стилей живут внутри
  него, руками не трогаем.

## Связанные

- Токены: [`../tokens.md`](../tokens.md)
- Текст в компоненте — по [`../../rules/07-voice-and-copy.md`](../../rules/07-voice-and-copy.md).
