# Корпоративный стиль CSS

---

### Синтаксис
  * После значения свойства обязательно ставится точка с запятой.
  * Для отступов внутри правил используются `Tab`. 
  * Шестнадцатеричное значение цвета сокращается, где невозможно пишется полностью из всех шести символов. 
  * Для записи используются строчные буквы. Например, `#f5f5f5`, `#000`.
  * Названия тегов и свойств в правилах пишутся строчными буквами.
  * Начальный ноль для значений сокращается (например, .5 вместо 0.5).
  * Во всех случаях в стилях используются двойные кавычки. 
  * В необязательных случаях кавычки не опускаются.
  * После двоеточия в правилах ставится один пробел `top: 10px;`. 
  * А перед двоеточием пробел не нужен.
  * После запятых внутри значений `rgb()`, `rgba()`, `hsl()`, `hsla()` или `rect()` пробелы ставятся !!! Это повышает удобочитаемость.
  > ```css
  >	rgba(0, 0, 0, 0.8)
  >```
  * До и после комбинатора между селекторами (например, `p > a`, `ul > li`) ставится один пробел.
  * Каждое объявление в правиле пишется на новой строке.
  * Перед открывающейся фигурной скобкой пробел не ставится. 
  * После скобки запись идёт с новой строки:
  > ```css
  > .selector{
  > 	color: #f5f5f5;
  > }
  > ```
  * Закрывающая фигурная скобка пишется на новой строке и без отступа.
  * Единицы измерения не пишутся, там где в них нет необходимости. Например, `border: 0`.
  >```css
  >/* Хорошо */
  >.selector,
  >.selector-secondary,
  >.selector[type="text"] {
  >	padding: 15px;
  >	margin-bottom: 15px;
  >	background-color: rgba(0, 0, 0, 0.5);
  >	box-shadow: 0 1px 2px #ccc, inset 0 1px 0 #ff0000;
  >}
  >
  >/* Плохо */
  >	.selector, .selector-secondary, .selector[type=text]{
  >		padding:15px;
  >		margin:0px 0px 15px;
  >		background-color:rgba(0,0,0,.5);
  >		box-shadow:0px 1px 2px #CCC,inset 0 1px 0 #FFFFFF}
  >```

### Валидность
 * CSS должен проходить проверку на валидность. Для проверки используется  современный [валидатор css](https://jigsaw.w3.org/css-validator/#validate_by_uri+with_options) или [Unicorn](https://validator.w3.org/unicorn/?ucn_lang=ru).
 > Невалидность которую дают сторонние плагины и скрипты можно не исправлять
 
### Имена классов *(Желательно использовать БЭМ методологию)*
  * Пишутся строчными буквами, дефис используется (но не camelCase). 
  * Дефисы служат разделителями во взаимосвязанных классах (например, `.button` и `.button-danger`).
  * Имена классов должны быть такими, чтобы по ним можно было быстро понять какому элементу страницы задан класс.
  * Избегайте сокращений (единственное исключение — `.btn` для кнопок), но не делайте их слишком длинными (более трёх слов).
  * Для написания классов используются английские слова и термины.
  * Транслитом названия классов и атрибутов не пишутся.
  >```css
  >/* Хорошо */
  >.alert-danger { … }
  >.tweet .user-picture { … }
  >.button { … }
  >.layout-center { … }
  >
  >
  >/* Плохо */
  >.testElement { … }
  >.t { … }
  >.big_red_button { … }
  >.knopka { … }
  >```

### Правило @import
  * Правило `@import` работает медленнее, чем тег `<link>`. 
  > В стилях @import не должен использоваться.

### Варианты шрифта
  * Альтернативные варианты шрифта и тип семейства указываются в конце перечисления font-family. 
  * В случае использования нестандартных шрифтов альтернативный веб-безопасный шрифт и тип семейства указываются, чтобы в случае отсутствия нестандартного шрифта в системе, изменения внешнего вида страницы были минимальны. Альтернативный шрифт должен быть такого же типа, что и нестандартный. 
  * Порядок шрифтов следующий: нестандартный шрифт, веб-безопасный, тип шрифта
  > ```css
  > 	font-family: 'Open Sans', Arial, Helvetica, sans-serif;
  > ```
  * Название шрифта написанного слитно(без пробелов) писать без кавычек, название разделенное пробелами брать в кавычки

Пример 
  > ```css
  > 	font-family:  myriadpro-regular, sans-serif;
  > 	font-family: 'myriadpro regular', sans-serif;
  > ```