# Foundation — токены дизайн-системы «Life»

Реальные значения, выгруженные из Figma (формат W3C Design Tokens).
Машиночитаемый источник — рядом в [`tokens/`](tokens/) (те же файлы, что экспортит Figma).

**Режимы:** тема — Light / Dark; типографика — Web / Mobile / Legacy (Proxima).
Значения цветов приведены как разрешённый HEX (семантика уже раскрыта из Brand).

## Правила применения (коротко)

- **Цвета — только токены темы** (`content/*`, `background/*`, `border/*`), напрямую,
  без слоя стилей. Палитра бренда — примитивы, **напрямую не используем** (см. ниже).
- **Отступы / радиусы** — токены `--space-*` / `--radius-*` напрямую.
- **Типографика** — через **текстовые стили** + режим коллекции (единственный слой,
  где есть стили; см. раздел «Как это применяется в Figma»).
- **Числа руками не вписывать** — иначе ломается переключение темы и режима.

## Отступы (Spaces)

| Токен | px |
|-------|----|
| `--space-none` | 0 |
| `--space-4` | 4 |
| `--space-8` | 8 |
| `--space-10` | 10 |
| `--space-12` | 12 |
| `--space-16` | 16 |
| `--space-24` | 24 |
| `--space-32` | 32 |
| `--space-40` | 40 |
| `--space-48` | 48 |
| `--space-64` | 64 |

## Радиусы (Radiuses)

| Токен | px |
|-------|----|
| `--radius-none` | 0 |
| `--radius-2` | 2 |
| `--radius-4` | 4 |
| `--radius-8` | 8 |
| `--radius-10` | 10 |
| `--radius-12` | 12 |
| `--radius-16` | 16 |
| `--radius-24` | 24 |
| `--radius-round` | 100 |

## Палитра бренда (Brand — примитивы)

> ⛔ **Напрямую не использовать.** Это примитивные и дополнительные цвета, из которых
> **собраны темы**. В макетах и компонентах берём **токены темы** (раздел
> «Семантические цвета»), а не значения отсюда. Бренд-палитра — справочная база и
> исходник для тем.

### Neutral

| Шаг | HEX |  | Шаг | HEX |
|-----|-----|--|-----|-----|
| 5 | `#FCFCFD` |  | 60 | `#667387` |
| 10 | `#F9F9FA` |  | 65 | `#4E5867` |
| 15 | `#F3F5F7` |  | 70 | `#444C59` |
| 20 | `#E6E8ED` |  | 75 | `#3B434F` |
| 25 | `#D7DAE1` |  | 80 | `#2D333C` |
| 30 | `#C8CCD6` |  | 85 | `#292F37` |
| 35 | `#BCC1CE` |  | 90 | `#262A32` |
| 40 | `#ABB0C1` |  | 95 | `#22262D` |
| 45 | `#9CA3B6` |  | 100 | `#1E2228` |
| 50 | `#8890A7` |  | White | `#FFFFFF` |
| 55 | `#7A879D` |  | Black | `#000000` |

### Purple

| Шаг | HEX |  | Шаг | HEX |
|-----|-----|--|-----|-----|
| 5 | `#FAF8FE` |  | 55 | `#9474DC` |
| 10 | `#F3EFFD` |  | 60 | `#7E62BA` |
| 15 | `#E7DEFA` |  | 65 | `#604B8F` |
| 20 | `#DED1F9` |  | 70 | `#53417B` |
| 25 | `#D6C7F7` |  | 75 | `#49396C` |
| 30 | `#CBB7F5` |  | 80 | `#382C53` |
| 35 | `#C1AAF3` |  | 85 | `#33284C` |
| 40 | `#B59AF1` |  | 90 | `#2E2445` |
| 45 | `#AC8DEF` |  | 95 | `#2A213E` |
| 50 | `#A07DEC` |  | 100 | `#251D37` |

### Blue

| Шаг | HEX |  | Шаг | HEX |
|-----|-----|--|-----|-----|
| 5 | `#F5FAFF` |  | 55 | `#1284FF` |
| 10 | `#E6F2FF` |  | 60 | `#006EE4` |
| 15 | `#CDE5FF` |  | 65 | `#0055AF` |
| 20 | `#B9DBFF` |  | 70 | `#004998` |
| 25 | `#A9D3FF` |  | 75 | `#004186` |
| 30 | `#90C5FF` |  | 80 | `#003267` |
| 35 | `#7BBAFF` |  | 85 | `#002E5F` |
| 40 | `#60ACFF` |  | 90 | `#002A56` |
| 45 | `#49A1FF` |  | 95 | `#00264E` |
| 50 | `#2B91FF` |  | 100 | `#FFFFFF` |

### Green

| Шаг | HEX |  | Шаг | HEX |
|-----|-----|--|-----|-----|
| 5 | `#F2FCF6` |  | 55 | `#009C37` |
| 10 | `#DFF6E8` |  | 60 | `#00842F` |
| 15 | `#BFEDCF` |  | 65 | `#006624` |
| 20 | `#A4E6BB` |  | 70 | `#00581F` |
| 25 | `#90E0AC` |  | 75 | `#004D1B` |
| 30 | `#6BD691` |  | 80 | `#003C15` |
| 35 | `#4CCD7A` |  | 85 | `#003713` |
| 40 | `#21C15A` |  | 90 | `#003212` |
| 45 | `#00B740` |  | 95 | `#002D10` |
| 50 | `#00A73B` |  | 100 | `#00280E` |

### Yellow

| Шаг | HEX |  | Шаг | HEX |
|-----|-----|--|-----|-----|
| 5 | `#FDFADF` |  | 55 | `#918927` |
| 10 | `#FDF3AC` |  | 60 | `#7B7421` |
| 15 | `#FCE34C` |  | 65 | `#5F5819` |
| 20 | `#F4D73E` |  | 70 | `#524C16` |
| 25 | `#EDCD3B` |  | 75 | `#494313` |
| 30 | `#E0BE37` |  | 80 | `#38330F` |
| 35 | `#D7B334` |  | 85 | `#332F0D` |
| 40 | `#C9A431` |  | 90 | `#2F2A0C` |
| 45 | `#BF992E` |  | 95 | `#2A260B` |
| 50 | `#B18B2B` |  | 100 | `#262209` |

### Orange

| Шаг | HEX |  | Шаг | HEX |
|-----|-----|--|-----|-----|
| 5 | `#FFF8F1` |  | 55 | `#C27332` |
| 10 | `#FFEEDC` |  | 60 | `#A5622B` |
| 15 | `#FFDDB8` |  | 65 | `#7E4B21` |
| 20 | `#FFCF9A` |  | 70 | `#6D411C` |
| 25 | `#FFC384` |  | 75 | `#603919` |
| 30 | `#FFB05C` |  | 80 | `#492B13` |
| 35 | `#FFA03A` |  | 85 | `#432811` |
| 40 | `#FF8A0C` |  | 90 | `#3D2410` |
| 45 | `#F37E00` |  | 95 | `#37210E` |
| 50 | `#DF7400` |  | 100 | `#311D0D` |

### Red

| Шаг | HEX |  | Шаг | HEX |
|-----|-----|--|-----|-----|
| 5 | `#FEF8F8` |  | 60 | `#E11B11` |
| 10 | `#FDEDEE` |  | 65 | `#AE1603` |
| 15 | `#FBDBDD` |  | 70 | `#961500` |
| 20 | `#F9CCCF` |  | 75 | `#841500` |
| 25 | `#F8C1C5` |  | 80 | `#670F00` |
| 30 | `#F6AEB3` |  | 85 | `#5F0F00` |
| 35 | `#F49FA5` |  | 90 | `#570E00` |
| 40 | `#F28B92` |  | 95 | `#4F0D00` |
| 45 | `#F07A82` |  | 100 | `#470B00` |
| 50 | `#ED636C` |  | 5 2 | `#FEF8F8` |
| 55 | `#EB4F56` |  |  |  |

## Семантические цвета — Light

| Роль | enabled | hovered | pressed | disabled |
|------|---------|---------|---------|----------|
| `content/primary-a` | `#1E2228` | `#444C59` | `#000000` | `#BCC1CE` |
| `content/primary-b` | `#FFFFFF` | `#FFFFFF` | `#FFFFFF` | `#BCC1CE` |
| `content/secondary` | `#667387` | `#7A879D` | `#4E5867` | `#BCC1CE` |
| `content/tertiary` | `#9CA3B6` | `#ABB0C1` | `#7A879D` | `#BCC1CE` |
| `content/accent` | `#E11B11` | `#AE1603` | `#961500` | `#BCC1CE` |
| `content/system/positive` | `#009C37` |  |  |  |
| `content/system/negative` | `#E11B11` |  |  |  |
| `content/system/warning` | `#FF8A0C` |  |  |  |
| `content/system/neutral` | `#4E5867` |  |  |  |
| `content/action` | `#1284FF` | `#006EE4` | `#004998` | `#BCC1CE` |
| `background/primary-a` | `#FFFFFF` | `#FCFCFD` | `#F9F9FA` | `#F9F9FA` |
| `background/primary-b` | `#1E2228` | `#444C59` | `#000000` | `#BCC1CE` |
| `background/secondary-a` | `#F3F5F7` | `#E6E8ED` | `#D7DAE1` | `#F9F9FA` |
| `background/secondary-b` | `#4E5867` | `#7A879D` | `#3B434F` | `#F9F9FA` |
| `background/tertiary` | `#E6E8ED` | `#D7DAE1` | `#C8CCD6` | `#F9F9FA` |
| `background/accent` | `#E11B11` | `#AE1603` | `#961500` | `#F9F9FA` |
| `border/primary-a` | `#1E2228` | `#444C59` | `#000000` | `#E6E8ED` |
| `border/primary-b` | `#FFFFFF` | `#E6E8ED` | `#D7DAE1` | `#E6E8ED` |
| `border/secondary` | `#D7DAE1` | `#C8CCD6` | `#BCC1CE` | `#E6E8ED` |
| `border/accent` | `#E11B11` | `#AE1603` | `#961500` | `#E6E8ED` |

## Семантические цвета — Dark

| Роль | enabled | hovered | pressed | disabled |
|------|---------|---------|---------|----------|
| `content/primary-a` | `#F3F5F7` | `#C8CCD6` | `#D7DAE1` | `#3B434F` |
| `content/primary-b` | `#F3F5F7` | `#C8CCD6` | `#D7DAE1` | `#3B434F` |
| `content/secondary` | `#667387` | `#4E5867` | `#3B434F` | `#3B434F` |
| `content/tertiary` | `#667387` | `#4E5867` | `#3B434F` | `#3B434F` |
| `content/accent` | `#AE1603` | `#841500` | `#670F00` | `#3B434F` |
| `content/system/positive` | `#009C37` |  |  |  |
| `content/system/negative` | `#E11B11` |  |  |  |
| `content/system/warning` | `#FF8A0C` |  |  |  |
| `content/system/neutral` | `#4E5867` |  |  |  |
| `content/action` | `#2B91FF` | `#006EE4` | `#004998` | `#3B434F` |
| `background/primary-a` | `#1E2228` | `#22262D` | `#262A32` | `#262A32` |
| `background/primary-b` | `#ABB0C1` | `#8890A7` | `#7A879D` | `#262A32` |
| `background/secondary-a` | `#262A32` | `#292F37` | `#22262D` | `#262A32` |
| `background/secondary-b` | `#262A32` | `#292F37` | `#22262D` | `#262A32` |
| `background/tertiary` | `#2D333C` | `#3B434F` | `#2D333C` | `#262A32` |
| `background/accent` | `#AE1603` | `#841500` | `#670F00` | `#262A32` |
| `border/primary-a` | `#FFFFFF` | `#E6E8ED` | `#D7DAE1` | `#262A32` |
| `border/primary-b` | `#3B434F` | `#444C59` | `#2D333C` | `#262A32` |
| `border/secondary` | `#2D333C` | `#3B434F` | `#3B434F` | `#2D333C` |
| `border/accent` | `#E11B11` | `#AE1603` | `#961500` | `#262A32` |

## Типографика

| Токен | Web | Mobile | Legacy (Proxima) |
|-------|-----|--------|------------------|
| `font/family/heading` | Inter | Inter | Proxima Nova |
| `font/family/body` | Inter | Inter | Proxima Nova |
| `font/size/headline-large` | 26 | 27.73 | 28 |
| `font/size/headline-medium` | 22 | 23.47 | 24 |
| `font/size/headline-small` | 18 | 19.2 | 20 |
| `font/size/title-medium` | 15 | 16 | 16 |
| `font/size/title-small` | 13 | 13.87 | 14 |
| `font/size/body-medium` | 15 | 16 | 16 |
| `font/size/body-small` | 13 | 13.87 | 14 |
| `font/size/label-medium` | 11 | 11.73 | 12 |
| `font/size/label-small` | 10 | 10.67 | 10 |
| `font/weight/text` | 400 | 400 | 400 |
| `font/weight/accent` | 500 | 500 | 600 |
| `font/weight/heading` | 600 | 600 | 700 |
| `font/lineHeight/headline-large` | 35 | 37.33 | 38 |
| `font/lineHeight/headline-medium` | 30 | 32 | 32 |
| `font/lineHeight/headline-small` | 24 | 25.6 | 28 |
| `font/lineHeight/title-medium` | 21 | 22.4 | 22 |
| `font/lineHeight/title-small` | 18 | 19.2 | 20 |
| `font/lineHeight/body-medium` | 23 | 24.53 | 22 |
| `font/lineHeight/body-small` | 20 | 21.33 | 20 |
| `font/lineHeight/label-medium` | 17 | 18.13 | 16 |
| `font/lineHeight/label-small` | 14 | 14.93 | 10 |

> Web/Mobile используют **Inter**, Legacy — **Proxima Nova**. Размеры/интервалы в px.

### Как это применяется в Figma (⚠️ не хардкодить px)

Значения выше — **источник**, а не способ применения. В Figma три уровня:

1. **Переменные** (эти токены) — коллекция типографики с **3 режимами: Web / Mobile /
   Legacy (Proxima)**.
2. **Текстовые стили** (Figma Text Styles) — именованный набор, к которому привязаны
   переменные. Семейство шрифта задано **на стиле**; размер / вес / интервал тянутся
   из переменных. Набор стилей (из файла Font):

   | Стиль | Назначение | Вес |
   |-------|-----------|-----|
   | `headline-large` / `-medium` / `-small` | заголовки | heading |
   | `title-medium` / `-small` | подзаголовки | accent |
   | `body-medium` / `body-small` | основной текст | `-light` = text, `-hard` = accent |
   | `label-medium` / `label-small` | подписи, метки | `-light` = text, `-hard` = accent |

3. **Применение:** вешаешь **текстовый стиль**, а платформенный размер выбирается
   **режимом коллекции** (Web / Mobile / Legacy) на фрейме. Сменил режим → стиль сам
   подтянул другие значения.

**Правило для макетов и для Builder оркестра:** применять именно **стили и переменные**,
а не вписывать числа руками — иначе смена режима и темы перестанет работать.