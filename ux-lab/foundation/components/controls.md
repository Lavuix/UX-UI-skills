# Компонент: Controls

| Поле | Значение |
|------|----------|
| Статус | ✅ готов |
| Сверка | ✔ сверено с Figma (node `5:7`) |
| Уровень | атом |
| Источник | Figma · Life-20_Kit_Light · страница «Controls» |
| fileKey | `M03BFuFuarl4z15GXCFnxh` (node `5:7`) |
| Ссылка | https://www.figma.com/design/M03BFuFuarl4z15GXCFnxh/Life-20_Kit_Light?node-id=5-7 |

## Назначение

Управляющие элементы выбора в формах: переключатель, чекбокс, радиокнопка —
как строка с подписью и как самостоятельный контрол.

## Оси вариантов

**Controls (строка с подписью):**
- **Type:** Switch · Checkbox · Radio
- **Position:** Left · Right (сторона подписи относительно контрола)
- **State:** Enabled · Warning · Error · Disabled

**Отдельные контролы (на этой же странице):**
- **CheckboxSquare:** Type = Unselected · Selected · Indeterminate × State (Enabled/Hovered/Pressed/Disabled)
- **CheckboxRound:** Type = Unselected · StrokeSelected · Selected · Indeterminate × State
- **Radiobutton:** Type = Unselected · Selected × State
- **Switch:** State = Enabled On/Off · Disabled On/Off

## Форма и размеры

Контрол 24×24, строка ≈ 52 по высоте. Состояния Warning/Error добавляют текст
подсказки под строкой.

## Правила применения

- **Checkbox** — множественный выбор; **Radio** — единичный из группы; **Switch** —
  мгновенное вкл/выкл без подтверждения.
- **Indeterminate** — только для «выбрано частично» в группе чекбоксов.
- **Warning / Error** — с текстом-пояснением; ошибка по бренд-войсу: что не так + как исправить.
- **Position = Right** — по умолчанию для настроек-строк; Left — в компактных формах.
- Компонент берём из библиотеки как есть — привязки токенов/стилей живут внутри
  него, руками не трогаем.

## Связанные

- Токены: [`../tokens.md`](../tokens.md)
- Текст в компоненте — по [`../../rules/07-voice-and-copy.md`](../../rules/07-voice-and-copy.md).
