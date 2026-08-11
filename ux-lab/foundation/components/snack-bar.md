# Компонент: SnackBar

| Поле | Значение |
|------|----------|
| Статус | ? не финализирован |
| Сверка | ✔ сверено с Figma (node `5:24`) |
| Уровень | молекула |
| Источник | Figma · Life-20_Kit_Light · страница «SnackBar» |
| fileKey | `M03BFuFuarl4z15GXCFnxh` (node `5:24`) |
| Ссылка | https://www.figma.com/design/M03BFuFuarl4z15GXCFnxh/Life-20_Kit_Light?node-id=5-24 |

> Страница без явной отметки готовности — статус уточняется.

## Назначение

Всплывающее системное уведомление (тост): результат действия, предупреждение,
ошибка, инфо. Рядом — счётчик и иконка уведомлений.

## Оси вариантов

- **SnackBar:** Kind = Success/Done · Warning · Error · Info × Button/Icon = Yes · No ×
  Size = Default · Large
- **Notification Counter:** Type = Digital · Dot × State = Default · Disabled × Style = Accent · Secondary
- **Notification Icon:** Type = Digital · Dot × State × Notification = Yes · No

## Форма и размеры

Тост ≈360 по ширине; Default ≈40–47 высотой, Large ≈98 (с описанием и действием).

## Правила применения

- **Kind** по смыслу: Success — успех, Warning — предупреждение, Error — ошибка, Info — нейтрально.
- **Size = Large** — когда нужен текст-пояснение и действие; Default — короткий статус.
- Текст — по бренд-войсу: что произошло (+ что делать, если нужно). Без восклицаний.
- Тост исчезает сам; для важного — с действием (кнопкой).
- Компонент берём из библиотеки как есть — привязки токенов/стилей живут внутри
  него, руками не трогаем.

## Связанные

- Токены: [`../tokens.md`](../tokens.md)
- Текст в компоненте — по [`../../rules/07-voice-and-copy.md`](../../rules/07-voice-and-copy.md).
