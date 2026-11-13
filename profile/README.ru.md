<div align="center">

<img src="https://raw.githubusercontent.com/Mistgate/mistgate/main/web/public/favicon.svg" width="80" height="80" alt="Логотип Mistgate">

<h2>Mistgate</h2>

<p><b>Свой VPN для своих людей — без возни с серверами.</b></p>

<p><sub><b>Бета</b> · до 1.0 API, хранимые настройки и протокол ноды ещё могут меняться</sub></p>

<p><a href="https://github.com/Mistgate/.github/blob/main/profile/README.md">English</a> · <b>Русский</b></p>

</div>

Mistgate — открытая панель для тех, кто держит VPN для других людей: семьи, друзей, сообщества или небольшой команды. Она работает с Hysteria2, VLESS и AmneziaWG. Сервер добавляется из браузера по IP и паролю root, у каждого человека одна ссылка. Панель проверяет каждый сервер так же, как это делает приложение, и пишет в Telegram, если какой-то из них сломался. Это два статических бинарника на Go, SQLite и systemd, без Docker, лицензия AGPL-3.0.

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Mistgate/mistgate/main/docs/images/readme/overview-dark-ru.webp">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/Mistgate/mistgate/main/docs/images/readme/overview-light-ru.webp">
  <img alt="Админка Mistgate: шесть нод с их состоянием и скоростью, одна открытая проблема, последние события" src="https://raw.githubusercontent.com/Mistgate/mistgate/main/docs/images/readme/overview-dark-ru.webp" width="100%">
</picture>

### Панель

- **Код:** [Mistgate/mistgate](https://github.com/Mistgate/mistgate)
- **Документация:** [mistgate.app/ru](https://mistgate.app/ru/)
- **Релизы:** [подписанные сборки для Linux amd64 и arm64](https://github.com/Mistgate/mistgate/releases/latest)
- **Сравнение** с 3x-ui, Remnawave, Hiddify, PasarGuard и s-ui: [таблица с источниками](https://github.com/Mistgate/mistgate/blob/main/docs/ru/reference/comparison.md)

### Приложение для Windows

Mistgate для Windows — собственное приложение панели; оно работает и с любой обычной ссылкой подписки. Hysteria2, AmneziaWG и VLESS в одном окне: приложение само выбирает сервер и протокол, которые работают в вашей сети, пускает через VPN только то, что вы выбрали (по сайтам, спискам и программам), держит трафик kill switch'ем, пока туннель лежит, и показывает, что заблокировано там, где вы находитесь. С панелью Mistgate оно регистрирует ПК своим ключом и показывает тариф, трафик, устройства и прокси для Telegram.

<img alt="Mistgate для Windows: подключено, справа список серверов" src="https://raw.githubusercontent.com/Mistgate/mistgate-client/main/docs/img/home.png" width="100%">

- **Код:** [Mistgate/mistgate-client](https://github.com/Mistgate/mistgate-client)
- **Скачать:** [последний релиз для Windows 10 и 11, x64](https://github.com/Mistgate/mistgate-client/releases/latest)
- **Обновления** приходят из этих релизов; приложение ставит только установщик, подписанный ключом проекта
- На русском, английском, китайском, фарси и турецком. Бета, как и панель

### Как помочь

- Поставьте панель на свободный VPS и [заведите issue](https://github.com/Mistgate/mistgate/issues), если что-то сломалось или непонятно написано.
- Попробуйте приложение для Windows в своей сети и [напишите](https://github.com/Mistgate/mistgate-client/issues), что не подключается.
- Поправьте страницу документации: у каждой страницы на mistgate.app есть ссылка «Править страницу на GitHub».
- Прочитайте [CONTRIBUTING.md](https://github.com/Mistgate/mistgate/blob/main/CONTRIBUTING.md) и пришлите pull request. Агентам для программирования — сначала [AGENTS.md](https://github.com/Mistgate/mistgate/blob/main/AGENTS.md).
- Об уязвимостях сообщайте закрыто: [SECURITY.md](https://github.com/Mistgate/mistgate/blob/main/SECURITY.md).
