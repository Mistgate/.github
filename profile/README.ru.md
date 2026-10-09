<div align="center">

<img src="https://raw.githubusercontent.com/Mistgate/mistgate/main/web/public/favicon.svg" width="80" height="80" alt="Логотип Mistgate">

<h2>Mistgate</h2>

<p><b>Свой VPN для своих людей — без возни с серверами.</b></p>

<p><a href="https://github.com/Mistgate/.github/blob/main/profile/README.md">English</a> · <b>Русский</b></p>

</div>

Mistgate — открытая панель для тех, кто держит VPN для других людей: семьи, друзей, сообщества или небольшой команды. Сейчас она работает с Hysteria2 и AmneziaWG, VLESS REALITY на подходе. Сервер добавляется из браузера по IP и паролю root, у каждого человека одна ссылка. Панель проверяет каждый сервер так же, как это делает приложение, и пишет в Telegram, если какой-то из них сломался. Это два статических бинарника на Go, SQLite и systemd, без Docker, лицензия AGPL-3.0.

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Mistgate/mistgate/main/docs/images/readme/overview-dark-ru.webp">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/Mistgate/mistgate/main/docs/images/readme/overview-light-ru.webp">
  <img alt="Админка Mistgate: шесть нод с их состоянием и скоростью, одна открытая проблема, последние события" src="https://raw.githubusercontent.com/Mistgate/mistgate/main/docs/images/readme/overview-dark-ru.webp" width="100%">
</picture>

- **Код:** [Mistgate/mistgate](https://github.com/Mistgate/mistgate)
- **Документация:** [mistgate.app/ru](https://mistgate.app/ru/)
- **Релизы:** [подписанные сборки для Linux amd64 и arm64](https://github.com/Mistgate/mistgate/releases/latest)
- **Сравнение** с 3x-ui, Remnawave, Hiddify, PasarGuard и s-ui: [таблица с источниками](https://github.com/Mistgate/mistgate/blob/main/docs/ru/reference/comparison.md)

### Как помочь

- Поставьте панель на свободный VPS и [заведите issue](https://github.com/Mistgate/mistgate/issues), если что-то сломалось или непонятно написано.
- Поправьте страницу документации: у каждой страницы на mistgate.app есть ссылка «Править страницу на GitHub».
- Прочитайте [CONTRIBUTING.md](https://github.com/Mistgate/mistgate/blob/main/CONTRIBUTING.md) и пришлите pull request. Агентам для программирования — сначала [AGENTS.md](https://github.com/Mistgate/mistgate/blob/main/AGENTS.md).
- Об уязвимостях сообщайте закрыто: [SECURITY.md](https://github.com/Mistgate/mistgate/blob/main/SECURITY.md).
