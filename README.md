# CSS Flexbox Cheat Sheet

### display: `flex` , `inline-flex`

Описывает элемент как flex-контейнер

*Применяется:* к контейнеру

### flex-direction: `row` , `row-reverse` , `column` , `column-reverse`

Указывает направление осей flex-контейнера

*Применяется:* к контейнеру

### flex-wrap: `nowrap` , `wrap` , `wrap-reverse`

Разрешает flex-элементам располагаться в несколько строк, а также может указывать направление строк `flex-direction`

*Применяется:* к контейнеру

### flex-flow: `row-nowrap` , `column-reverse` , `column-wrap` , `row-reverse wrap-reverse`

Сокращённое свойство для `flex-direction` и `flex-wrap`

*Применяется:* к контейнеру

---

## Выравнивания для flex-контейнера

### justify-content: `flex-start` , `flex-end` , `center` , `space-between` , `space-around` , `space-evenly`

Выравнивание flex-элементов вдоль главной оси

### align-items: `flex-start` , `flex-end` , `center` , `baseline` , `strecth`

Выравнивание flex-элементов вдоль поперечной оси

### align-content: `flex-start` , `flex-end` , `center` , `space-between` , `space-around` , `space-evenly` , `strecth`

Выравнивает ряды flex-эементов вдоль поперечной оси, если значение свойства `flex-wrap` указано отличное от `nowrap`, т.е. работает для нескольких рядов

---

## Выравнивания для flex-элементов

### align-self: `flex-start` , `flex-end` , `center` , `baseline` , `stretch`

Выравнивает flex-элемент вдоль поперечной оси

### order: `число-позиция`

Изменяет порядок flex-элемента в потоке. Может иметь и отрицательное значение

---

## Управление размерами flex-элемента

### flex-basis: `auto`, `любое значение в px, %, em`

Базовый размер flex-элемента. Имеет приоритет над свойствами `height` и `width`. Применяет изменения по направлению главной оси, т.е. если главная ось направлена слева-направо, то будет изменяться ширина flex-элемента, иначе высота.

При одновременном использовании свойств `flex-basis` вместе с `flex-grow` элемент может быть больше чем он указан во `flex-basis`, но не менее. Это справедливо если flex-контейнеру указан `flex-wrap` со значением `wrap` или `wrap-reverse`.

### flex-grow: `положительное число-коэффициент`

Растягивание flex-элементов на заданный коэффициент.

### flex-shrink: `положительное число-коэффициент`

Коэффициент степени сжатия flex-элементов. Свойство противоположно `flex-grow`.
