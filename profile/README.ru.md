<div align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="./assets/banner-dark.svg">
    <source media="(prefers-color-scheme: light)" srcset="./assets/banner-light.svg">
    <img alt="Mistgate — лёгкая панель для собственного VPN" src="./assets/banner-dark.svg" width="100%">
  </picture>

  <p><a href="https://github.com/Mistgate">English</a> · <b>Русский</b></p>
</div>

**Mistgate** — лёгкая панель для собственного VPN-флота: один бинарь на Go для панели, один для агента ноды, без Docker. Hysteria2 и AmneziaWG живут рядом — в одной подписке и в одной админке.

**[Исходный код](https://github.com/Mistgate/mistgate)** · [Документация](https://github.com/Mistgate/mistgate/tree/main/docs/ru)

## Зачем ещё одна панель

- **Лёгкая.** SQLite, systemd, два статических бинаря. Без Docker и без отдельного сервера БД. Цель по памяти для панели в простое — 80 МБ (пока цель, а не замер).
- **Пользователи AmneziaWG на виду.** Каждое устройство AmneziaWG — пир, о котором панель знает: кто онлайн, трафик по пользователям и по устройствам.
- **Доктор, который знает хостеров.** Заполненный диск и журналы, резолвер, который не резолвит, уход часов, занятые порты, больная сетевая база. Находит, объясняет простыми словами и, где это безопасно, исправляет одним подтверждённым нажатием.
- **Взгляд со стороны клиента.** Синтетические проверки подключаются как настоящий клиент (Hysteria2 и AmneziaWG), поэтому нода «зелёная», только если трафик действительно идёт.
- **Удобна и для AI-агентов.** API-токены и MCP-сервер: изменения по схеме «план → применить», всё рискованное ждёт подтверждения владельца.

## Что внутри

| Флот | Доступ и инструменты |
|:--|:--|
| <img src="./assets/icons/zap.svg" width="32" height="32" align="absmiddle" alt="">&nbsp; **Hysteria2 и AmneziaWG**<br>Hysteria2 с Salamander и AmneziaWG 2.0 / 3.1 — в userspace или модулем ядра. Несколько профилей на ноду. | <img src="./assets/icons/qr.svg" width="32" height="32" align="absmiddle" alt="">&nbsp; **Подписки**<br>Личные ссылки для Happ, Mihomo / Clash YAML, ключи AmneziaVPN и `vpn://`, плюс страница пользователя с QR-кодом. |
| <img src="./assets/icons/globe.svg" width="32" height="32" align="absmiddle" alt="">&nbsp; **Выход через WARP**<br>Трафик профиля можно пустить через WARP. Если связь с WARP пропала, профиль закрывается, а не утекает напрямую. | <img src="./assets/icons/users.svg" width="32" height="32" align="absmiddle" alt="">&nbsp; **Пользователи и устройства**<br>Группы, свой пир на каждое устройство, лимиты трафика, DNS-пресеты для пользователя или группы. |
| <img src="./assets/icons/pulse.svg" width="32" height="32" align="absmiddle" alt="">&nbsp; **Доктор флота**<br>Самопроверки нод с безопасными исправлениями, синтетические проверки, тревоги с полным жизненным циклом. | <img src="./assets/icons/window.svg" width="32" height="32" align="absmiddle" alt="">&nbsp; **Админка**<br>Русский и английский, тёмная и светлая темы, вход по passkey. |
| <img src="./assets/icons/shield.svg" width="32" height="32" align="absmiddle" alt="">&nbsp; **Подписанные обновления**<br>Агенты нод сами проверяют манифест, подписанный ed25519. Канареечная раскатка, проверка здоровья, автоматический откат. | <img src="./assets/icons/spark.svg" width="32" height="32" align="absmiddle" alt="">&nbsp; **Доступ для агентов**<br>Токены «только чтение», «оператор» и «админ». Изменения идут через «план → применить», рискованные ждут владельца. |

## Клиент для компьютера: kl!ck

<a href="https://github.com/vbu00/klick">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/vbu00/klick/main/docs/logo/wordmark-dark.svg">
    <img alt="kl!ck" src="https://raw.githubusercontent.com/vbu00/klick/main/docs/logo/wordmark-light.svg" width="200">
  </picture>
</a>

Для Windows советуем **[kl!ck](https://github.com/vbu00/klick)** — небольшой открытый VPN-клиент на неизменённом ядре [mihomo](https://github.com/MetaCubeX/mihomo). Вставляете ссылку подписки Mistgate и получаете Hysteria2 и AmneziaWG в одном окне: TUN, маршрутизация по сайтам и программам и Kill Switch, который работает, даже когда окно закрыто. Версия для macOS скоро.

**[Скачать для Windows](https://github.com/vbu00/klick/releases/latest)** · [Исходники](https://github.com/vbu00/klick) · MIT

## Статус

Mistgate ещё не вышел. Что уже есть и что впереди:

| Этап | Что |
|:--|:--|
| **Готово** | Панель и агент ноды по mTLS · Hysteria2 · AmneziaWG 2.0 / 3.1 · выход через WARP · подписки и страница пользователя · DNS-пресеты · доктор, синтетические проверки, тревоги · подписанные обновления агента с канарейкой и откатом · API-токены и MCP-сервер · админка и документация на русском и английском |
| **Сейчас** | Раскатка нод по SSH из интерфейса с предпроверками · зашифрованное хранилище паролей серверов · зашифрованные бэкапы панели в R2 |
| **Дальше** | Telegram-бот на весь флот · новые форматы подписок (Xray JSON, sing-box) и зеркала подписок · самообновление панели · установка одной командой |
| **Потом** | VLESS REALITY как первый внешний плагин протокола |

---

<sub>Открытый исходный код под лицензией [AGPL-3.0](https://github.com/Mistgate/mistgate/blob/main/LICENSE).</sub>
