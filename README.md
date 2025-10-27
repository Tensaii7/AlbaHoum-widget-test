# AlbaHoum-widget-test

Минимальная тестовая страница на React для проверки виджета из репозитория `hata-project-front-react-webpack`.

## Быстрый старт (локально)

1) Соберите и раздайте `dist` фронта:

```bash
cd ../hata-project-front-react-webpack
npm run build
npx http-server dist -p 3000
```

2) Откройте файл `index.html` в этом каталоге (двойной клик или через простой http-сервер) и убедитесь, что скрипт загружается с `http://localhost:3000/widget.js`.

3) Виджет появится под заголовком. При необходимости укажите дополнительные атрибуты:

```html
<script src="http://localhost:3000/widget.js"
        data-check-in="2025-10-10"
        data-check-out="2025-10-12"
        data-width="100%"
        data-height="640"></script>
```

По умолчанию в `index.html` используется ширина `100%` и высота `640`.

## Продакшен

Замените `src` на боевой хост:

```html
<script src="https://alba-houm.ru/widget.js" data-width="100%" data-height="640"></script>
```

Дополнительно можно передать JSON-конфиг через `data-config` или тело тега `<script>`. См. `../hata-project-front-react-webpack/WidgetGuide.md`.
