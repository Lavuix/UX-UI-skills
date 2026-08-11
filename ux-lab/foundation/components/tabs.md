# Компонент: Tabs

| Поле | Значение |
|------|----------|
| Статус | ? не финализирован |
| Сверка | ✔ сверено с Figma (node `5:32`) |
| Уровень | молекула |
| Источник | Figma · Life-20_Kit_Light · страница «Tabs» |
| fileKey | `M03BFuFuarl4z15GXCFnxh` (node `5:32`) |
| Ссылка | https://www.figma.com/design/M03BFuFuarl4z15GXCFnxh/Life-20_Kit_Light?node-id=5-32 |

> Статус `?` — компонент ещё не финализирован. Страница содержит Tabs и SegmentControl.

## Назначение

Переключение между разделами одного экрана: вкладки (Tabs) и сегмент-контрол
(SegmentControl).

## Оси вариантов

- **Tabs:** Type = Regular; вкладка (`.Items`) Active = Yes · No × State = Enabled · Hovered · Pressed · Disabled
- **SegmentControl:** Size = S · M · L; сегмент (`.items`) Type = Neutral · Primary ×
  Selected = Yes · No × States = Enabled · Hovered · Pressed · Disabled × Size = S · M · L

## Форма и размеры

Вкладка/сегмент высотой ≈28 (S) … 40 (L). Активная — одна.

## Правила применения

- **Tabs** — для навигации по разделам; **SegmentControl** — для переключения режима/фильтра.
- Один активный элемент; количество вкладок держим небольшим (влезает без скролла).
- Подписи короткие, по бренд-войсу.
- Компонент берём из библиотеки как есть — привязки токенов/стилей живут внутри
  него, руками не трогаем.

## Связанные

- Токены: [`../tokens.md`](../tokens.md)
- Текст в компоненте — по [`../../rules/07-voice-and-copy.md`](../../rules/07-voice-and-copy.md).
