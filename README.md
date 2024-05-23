_В разработке!_

# Темная тема для сайта shikimori.me

## Для начала

Добавьте стиль и создайте в `:root` (по желанию):

```css
/* Импорт стиля */
@import url(https://raw.githubusercontent.com/Dedonych/Shikimori-Dark-Theme/master/shikimori_dark.css);

:root {
  --my-clr:/* Ваш основной цвет (стандартный - #5292d2 - светло синий)*/ ;
}
```

Цвета плохо работают с черным и белым

### Добавляйте в `:root` строчки, чтобы:<br>

- `--news:none` - отключить подсказку в настройках <br>
- `--dropdown:var(--my-clr)` - верхнее меню изменить на основной цвет<br>
- `--link-primary:var(--my-clr)` - сделать основной текст основным цветом (или каким хотите)<br>

#### Темы

Если отключаете темы и хотите оставить стандартный цвет верхнего меню, установите `--dropdown:var(--bckg-dark)`

- `--themes:var(--my-clr)` - отключить все темы (xmas, halloween и т.д.)<br>
- `--icon:var(--def-icon)` - установить дефолт лого
  <br>
- `--xmas:var(--my-clr)` - отключить тему рождества <br>
- `--halloween:var(--my-clr)` - отключить тему хэллоуин

## ColorPicker JS

Для удобного поиска цветов, можете использовать данный скрипт [colorpicker.js](colorpicker.js).
<br>
Можно использовать [TamperMonkey](https://www.tampermonkey.net/) или другое расширение. Или просто вставить в консоль код (F12 для Chrome).
<br>
Описание функций:
 - Изменение цвета `--my-clr`
 - Изменение цвета `--dropdown`
 - Поменять местами цвета
 - Рандомные цвета
 - Скопировать в буфер готовые строчки, для удобного вставление на сайт
 - Сбросить кастомные цвета, к тем , что у вас стояли

## Как выглядит
![image](./posters/main.png)
![image](./posters/profile.png)
![image](./posters/title.png)
## С применением `--dropdown`
![image](./posters/colored.png)
##   С применением `colorpicker.js`
![image](./posters/colorpicker.png)