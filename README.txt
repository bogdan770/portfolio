Портфолио bogdin.dev — как пользоваться

СТРУКТУРА
- index.html       — весь сайт: разметка, стили и контент в одном файле.
- assets/work/     — фото работ (webp), используются в блоке GROUPS.
- assets/media/    — доп. фото и видео для проектов (webp/mp4).
- icons/, favicon.ico — иконки вкладки и значки для телефона/PWA.
- og-image.png     — превью при шаринге ссылки (OpenGraph/Twitter).
- Bogdan-Sliusarenko-Mechanical-Engineer.pdf — файл, который скачивается по кнопке "Download CV".
- CNAME            — домен для GitHub Pages (bogdin.dev).
- robots.txt, sitemap.xml — для поисковых роботов.
- google*.html     — файл подтверждения владения сайтом в Google Search Console. НЕ УДАЛЯТЬ, иначе слетит верификация.

РЕДАКТИРОВАНИЕ ТЕКСТА
Весь контент — в JS-блоках в конце index.html:
- CONFIG       — имя, email, телефон, LinkedIn, локация.
- T            — все подписи интерфейса (кнопки, заголовки секций).
- INTRO_PARAS / INTRO_CARDS — текст блока "About myself" и три карточки под ним.
- GROUPS       — проекты и фотографии в разделе "Work" (заголовки, описания, подписи к фото).
- EXPERIENCE   — таймлайн опыта.
- TESTIMONIALS — отзывы в разделе "Recommendations".

Сайт на одном языке (английский), переключателя RU/EN сейчас нет.

ЗАМЕНА CV
Положи новый PDF рядом с index.html и either:
- назови файл так же: Bogdan-Sliusarenko-Mechanical-Engineer.pdf, либо
- переименуй, и поправь оба атрибута href/download в блоке contact (строка с "Download CV").

ЛОКАЛЬНЫЙ ПРОСМОТР
Открой index.html прямо в браузере — сайт статический, сервер не нужен.

ДЕПЛОЙ
Сайт автоматически публикуется через GitHub Pages из репозитория
github.com/bogdan770/portfolio, ветка main. Чтобы обновить сайт:
  git add <файлы>
  git commit -m "..."
  git push origin main
Через 1-2 минуты изменения появятся на https://bogdin.dev/.
Домен и DNS управляются через Cloudflare.

АНАЛИТИКА
Cloudflare Web Analytics подключена прямо в index.html (тег в конце
<body>). Статистику смотреть на dash.cloudflare.com → Web Analytics.

SEO
- robots.txt разрешает индексацию всем, sitemap.xml указывает на
  единственную страницу /.
- В <head> есть canonical, meta robots/author и JSON-LD (schema.org
  Person) для карточки в поиске Google.
- Сайт подтверждён в Google Search Console (см. google*.html выше).

ЧТО НЕ ВХОДИТ В САЙТ
Папки VEEV/, ss/, файлы Bogdan-Sliusarenko-Portfolio.html и
portfolio-deploy.zip лежат в репозитории локально, но игнорируются
git'ом (.gitignore) — это черновики/исходники, на сайт не попадают.
