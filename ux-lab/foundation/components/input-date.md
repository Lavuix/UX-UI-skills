# Компонент: InputDate

| Поле | Значение |
|------|----------|
| Статус | ? не финализирован |
| Сверка | ✔ сверено с Figma (node `5:12`) |
| Уровень | молекула |
| Источник | Figma · Life-20_Kit_Light · страница «InputDate» |
| fileKey | `M03BFuFuarl4z15GXCFnxh` (node `5:12`) |
| Ссылка | https://www.figma.com/design/M03BFuFuarl4z15GXCFnxh/Life-20_Kit_Light?node-id=5-12 |

> Статус `?` — компонент ещё не финализирован, оси могут измениться.

## Назначение

Поле ввода даты с календарём: выбор одной даты или диапазона.

## Оси вариантов

- **Поле (как Input):** State = Empty · EmptyHovered · EmptyPressed · Typed · Filled · FilledHovered · Disabled × Error = No · Yes
- **Calendar Type:** Single (одна дата) · Multy (диапазон)
- **Ячейка дня (`.Numbers`) Type:** Default · Disabled · NextMonth · Hovered · Selected ·
  Start · StartSelected · EndSelected · EndHovered · и их комбинации (Disabled/Hovered)

## Форма и размеры

Поле ≈ 414×141; календарь Single ≈ 320×445, Multy (диапазон) ≈ 640×445; ячейка дня 20×20.

## Правила применения

- **Single** — для одной даты, **Multy** — для диапазона (с подсветкой Start/End).
- Формат даты — по редполитике (9.10.2022; в датапикере день всегда с ведущим нулём).
- Ошибка — с пояснением; недоступные дни — `Disabled`.
- Компонент берём из библиотеки как есть — привязки токенов/стилей живут внутри
  него, руками не трогаем.

## Связанные

- Токены: [`../tokens.md`](../tokens.md)
- Текст в компоненте — по [`../../rules/07-voice-and-copy.md`](../../rules/07-voice-and-copy.md).
