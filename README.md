# ВитаМилк — лендинг концепции

Лендинг по презентации «Концепция развития и монетизации конного хозяйства»: бренд ВитаМилк и пять линеек (Kids, VitaMilk, Cosmetics, Lumière, NOIR), агротуризм, фестивали, магазин на ферме, визуальная система и выводы.

Статический сайт без сборки: откройте `index.html` в браузере или раздайте папку любым статическим сервером, например `python3 -m http.server`.

- `index.html` — разметка, секции идут в порядке слайдов
- `styles.css` — стили, цвета линеек заданы переменными в `:root`
- `script.js` — мобильное меню, появление блоков при прокрутке, подсветка пункта меню
- `assets/img/` — изображения из презентации

## Публикация

Сайт деплоится на GitHub Pages workflow-ом `.github/workflows/pages.yml` при каждом пуше в ветку `claude/hopeful-dirac-ur2n4w`: https://jmsbrn.github.io/konnaya-ferma/ (сайт «БалансПро» — https://jmsbrn.github.io/konnaya-ferma/buhgalteriya/)

## Сайт бухгалтерской компании «БалансПро»

Отдельный одностраничный сайт в папке `buhgalteriya/` (`index.html`, `styles.css`, `script.js`): бухгалтерский аутсорсинг, услуги, преимущества, перечень работ, отзывы, форма заявки, модальное окно «Заказать звонок» и плавающая кнопка связи. Изображения не используются — только CSS-градиенты и встроенные SVG-иконки.

Перед публикацией замените заглушки: название компании, телефон, e-mail, адрес, ссылки на Telegram/Viber, политику конфиденциальности и примеры отзывов. Формы пока проверяют поля только в браузере — для отправки заявок нужно подключить обработчик (почта, Telegram-бот или CRM).

### Деплой «БалансПро» на Netlify

Workflow `.github/workflows/netlify.yml` выкладывает папку `buhgalteriya/` на Netlify при пуше в `claude/awesome-darwin-x03qh7` или вручную (Actions → Deploy to Netlify → Run workflow). Нужны секреты репозитория (Settings → Secrets and variables → Actions):

- `NETLIFY_AUTH_TOKEN` — персональный токен: Netlify → User settings → Applications → Personal access tokens;
- `NETLIFY_SITE_ID` — Project ID сайта: создайте пустой сайт (Add new project → Deploy manually) и скопируйте ID из Project configuration.

Альтернатива без токенов: в Netlify выберите Import from Git и этот репозиторий — `netlify.toml` уже указывает папку публикации `buhgalteriya`.
