# Компонент: System

| Поле | Значение |
|------|----------|
| Статус | ? не финализирован |
| Сверка | ✔ сверено с Figma (node `5:30`) |
| Уровень | атом (набор служебных) |
| Источник | Figma · Life-20_Kit_Light · страница «System» |
| fileKey | `M03BFuFuarl4z15GXCFnxh` (node `5:30`) |
| Ссылка | https://www.figma.com/design/M03BFuFuarl4z15GXCFnxh/Life-20_Kit_Light?node-id=5-30 |

> Статус `?` — компонент ещё не финализирован. Страница объединяет служебные элементы.

## Назначение

Служебные системные элементы: индикатор загрузки, разделитель, кнопка мини-аппа,
подложка экрана.

## Оси вариантов

- **Spinner:** Style = Primary · Secondary · Accent × Size = Small · Large
- **MiniappButton:** Property 1 = Enabled · Hovered · Pressed · Disabled × Theme = Light · Dark
- **Divider** — тонкая линия-разделитель.
- **Screen Background** — фон экрана.

## Форма и размеры

Spinner 24 (Small) / 30 (Large); MiniappButton ≈77×32; Divider высотой 1.

## Правила применения

- **Spinner** — короткая неопределённая загрузка (когда структура неизвестна; иначе Skeletons).
- **Divider** — разделять смысловые группы, не каждую строку.
- **MiniappButton** — вход в мини-приложение; тема по фону.
- Компонент берём из библиотеки как есть — привязки токенов/стилей живут внутри
  него, руками не трогаем.

## Связанные

- Токены: [`../tokens.md`](../tokens.md)
- Текст в компоненте — по [`../../rules/07-voice-and-copy.md`](../../rules/07-voice-and-copy.md).
