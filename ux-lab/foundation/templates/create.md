# Шаблон: Create (создание сущности)

| Поле | Значение |
|------|----------|
| Сверка | ✔ сверено с Figma (node `1:2`) |
| Уровень | шаблон (экран) |
| Источник | Figma · Life-04_Templates · страница «Create» |
| fileKey | `g3P4HUG0FGh62FZHQKQW7l` (node `1:2`) |
| Ссылка | https://www.figma.com/design/g3P4HUG0FGh62FZHQKQW7l/Life-04_Templates?node-id=1-2 |

## Назначение

Экраны создания/заполнения сущности в десктопе. На странице два экрана:
- **Создание заявки** — форма подачи заявки (состояние «незаполнена», вид
  предоставления «Электронно»).
- **Рац. предложение** — калькулятор расчёта экономического эффекта (аккордеоны с
  формулами и полями ввода).

## Раскладка

Десктоп 1920×1080. Слева **Sidebar** (rail 64) → **Content**: **Header** (56) сверху,
ниже блок из трёх колонок — **Sidemenu** (320, навигация из `Cell`), центральная
**форма** (≈818), правая **панель действий** (360, кнопки и статус-блок).

## Из чего собран

- Sidebar → [`../components/sidebar-3-0.md`](../components/sidebar-3-0.md)
- Header → [`../components/header.md`](../components/header.md)
- Cell (2.0) (сайдменю) → [`../components/cell-2-0.md`](../components/cell-2-0.md)
- Input, TextArea → [`../components/input.md`](../components/input.md), [`../components/text-area.md`](../components/text-area.md)
- InputDate/Calendar → [`../components/input-date.md`](../components/input-date.md)
- Controls (radio) → [`../components/controls.md`](../components/controls.md)
- Action Button → [`../components/action-button.md`](../components/action-button.md)
- Hint 2.0 → [`../components/hint-2-0.md`](../components/hint-2-0.md)
- Divider (System) → [`../components/system.md`](../components/system.md)

## Состояния / варианты

- Форма «незаполнена» (пустые поля, обязательные помечены звёздочкой).
- Калькулятор с аккордеонами (свёрнутые/раскрытые секции расчётов).

## Когда применять

- Экраны создания/подачи (заявка, предложение, расчёт) с формой в центре и
  действиями справа. Главное действие — Primary в правой панели.

## Связанные

- Каталог компонентов: [`../components/INDEX.md`](../components/INDEX.md)
- Токены: [`../tokens.md`](../tokens.md)
- Текст — по [`../../rules/07-voice-and-copy.md`](../../rules/07-voice-and-copy.md).
