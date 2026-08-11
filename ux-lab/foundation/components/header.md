# Компонент: Header

| Поле | Значение |
|------|----------|
| Статус | ? не финализирован |
| Сверка | ✔ сверено с Figma (node `5:22`) |
| Уровень | организм |
| Источник | Figma · Life-20_Kit_Light · страница «Header» |
| fileKey | `M03BFuFuarl4z15GXCFnxh` (node `5:22`) |
| Ссылка | https://www.figma.com/design/M03BFuFuarl4z15GXCFnxh/Life-20_Kit_Light?node-id=5-22 |

> Статус `?` — компонент ещё не финализирован.

## Назначение

Верхняя панель раздела (десктоп/веб): заголовок, навигация, поиск, действия.

## Оси вариантов

- **Navigation:** With · Without · Only App Button
- **Kind Search:** Min. Size · Max. Size · Icon
- **Пункт навигации (`.Items`):** Активно = No · Yes × States = Enabled · Hovered · Pressed · Disabled
- **Навкнопка (`.Navbutton`):** States = Enabled · Hover · Pressed · Disabled

## Форма и размеры

Высота панели ≈56; тянется по ширине контента.

## Правила применения

- **Navigation = With** — когда в шапке нужны разделы; **Only App Button** — минимальная.
- **Search = Icon** — компактно (раскрытие по клику); **Max. Size** — когда поиск основной.
- Активный пункт навигации — один.
- Компонент берём из библиотеки как есть — привязки токенов/стилей живут внутри
  него, руками не трогаем.

## Связанные

- Токены: [`../tokens.md`](../tokens.md)
- Текст в компоненте — по [`../../rules/07-voice-and-copy.md`](../../rules/07-voice-and-copy.md).
