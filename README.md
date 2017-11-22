## Работа со шрифтами и пакетом *font-awesome*

Ставим плагин отсюда:
https://www.npmjs.com/package/font-awesome

```
npm install font-awesome --save
```
Плагин нужен для работы с иконками Гугла. Если такие иконки не нужны, плагин можно не ставить.

В главном SCSS файле вставляем строчку @import "../../node_modules/font-awesome/scss/font-awesome";

Выбирать иконки и код для встраивания здесь: http://fontawesome.io/

Выбранный код встраиваем на страницу html(pug), что-то типа *i.fa.fa-book(aria-hidden="true")*

Иконка будет отображаться во всех браузерах кроме Firefox, для устранения этого бага вставляем в head сайта строчку:
```
link(rel="stylesheet" type="text/css" href="http://maxcdn.bootstrapcdn.com/font-awesome/4.2.0/css/font-awesome.min.css")
```

### Шрифты
Закидываем в папку *source* папку *font* со шрифтами

Бесплатные шрифты можно брать здесь: https://fonts.google.com/

Подсоединение локальных шрифтов в файле main.scss:

```
@import "global/fonts";
```
Для удобства можно создать файл vars.scss подключить его к файлу стилей, и создавать удобные алисы названий шрифтов