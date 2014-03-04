imagelightbox.js
================

Lightbox jQuery плагинам всегда не хватало простоты. И в виду имеется не только дизайн, но и общая реализация. Большинсто lightbox плагинов содержит много нежелательных особенностей по умолчанию и отвратительную поддержку сенсорных экранов.

Так ImageLightbox.js является аскетичным плагином, не содержащим в себе ничего лишнего, и работающим только с изображениями.

Полноэкранное DEMO: http://cdpn.io/ohzLq

Особенности:

    Аскетичность. По умолчанию отсутствуют заголовки, фон и элементы навигации.
    Минимализм. Чистота html-разметки. Вес плагина всего 4кб.
    Кастомизация.
    Адаптивность.
    Поддержка iOS, Android, Windows Phone.
    Совместимость с jQuery 1.x и 2.x.
    Предварительная загрузка изображений.
    Использование свойст CSS transform и transition для анимации.
    Поддержка клавиатуры.

HTML
Необходим только один элемент по умолчанию:
<img src="picture.jpg" id="imagelightbox" />

CSS
По умолчанию нет таблицы стилей. Минимальные рекомендации:
#imagelightbox {
  position: fixed;
  z-index: 9999;
}

Javascript
Пример базового подключения:

<script src="jquery.js"></script>
<script src="imagelightbox.js"></script>
<script>
    $( function()
    {
        $( 'a' ).imageLightbox();
    });
</script>

ImageLightbox() поддерживает ряд опций.
По умолчанию:
$( selector ).imageLightbox(
{
    selector:       'id="imagelightbox"',   // string; селектор 
    allowedTypes:   'png|jpg|jpeg|gif',     // string; поддерживаемые форматы
    animationSpeed: 250,                    // integer; скорость анимации
    preloadNext:    true,                   // bool;            предзагрузка следующего изображения
    enableKeyboard: true,                   // bool;            управление с клавиатуры (стрелки Влево/Вправо и Esc)
    quitOnEnd:      false,                  // bool;            выход после просмотра последнего изоьражения
    quitOnImgClick: false,                  // bool;            выход при клике по изображению
    quitOnDocClick: true,                   // bool;            выход при клике по странице вне изображения
    onStart:        false,                  // function/bool;   вызов функции когда lightbox стартует
    onEnd:          false,                  // function/bool;   вызов функции при выходе из lightbox
    onLoadStart:    false,                  // function/bool;   вызов функции при загрузке изображения
    onLoadEnd:      false                   // function/bool;   вызов функции при завершении загрузки изображения
});

 
