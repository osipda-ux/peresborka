# Пересборка — сайт мероприятия

Вечер для тех, кто работает на себя. 5 ноября 2026, Москва, 19:00–23:00.
Эксперты: Наталья Исакова, Ивелена (Елена Иванова), Вадим Тарасов.

## Как опубликовать на GitHub Pages (5 минут)

1. Создайте на github.com новый публичный репозиторий, например `peresborka`.
2. Нажмите **Add file → Upload files** и перетащите всё содержимое этой папки
   (index.html, папку assets, файлы .nojekyll и README.md). Нажмите **Commit changes**.
3. Откройте **Settings → Pages**. В блоке *Build and deployment* выберите
   **Source: Deploy from a branch**, ветка **main**, папка **/ (root)**. Сохраните.
4. Через 1–2 минуты сайт откроется по адресу `https://<ваш-логин>.github.io/peresborka/`.

Свой домен: в **Settings → Pages → Custom domain** впишите домен и добавьте у регистратора
CNAME-запись на `<ваш-логин>.github.io`.

## Что поменять перед запуском

- **Кнопка записи в Telegram.** В `index.html` найдите строку
  `const CONFIG = { contactUrl: "" };` и впишите ссылку организатора,
  например `"https://t.me/username"`. В окне записи появится кнопка «Написать организатору».
- **Превью для мессенджеров.** Для красивой карточки ссылки в Telegram/WhatsApp замените
  в `index.html` `content="assets/og.jpg"` на полный адрес:
  `https://<ваш-логин>.github.io/peresborka/assets/og.jpg`.

## Что внутри

- `index.html` — вся страница (стили и скрипты внутри).
- `assets/vendor` — библиотеки анимации (GSAP, Three.js, Lenis), лежат локально:
  сайт не зависит от внешних CDN и быстро открывается в России.
- `assets/fonts` — шрифты Playfair Display, Manrope, Caveat (локально).
- `assets/video` — ролики экспертов и отзывы, сжатые для веба.
