<div align="center">

<img src="https://raw.githubusercontent.com/Mistgate/mistgate/main/web/public/favicon.svg" width="80" height="80" alt="Mistgate logo">

<h2>Mistgate</h2>

<p><b>Your own VPN for your people, without babysitting servers.</b></p>

<p><sub><b>Beta</b> · until 1.0 the API, the stored settings and the node protocol may still change</sub></p>

<p><b>English</b> · <a href="https://github.com/Mistgate/.github/blob/main/profile/README.ru.md">Русский</a></p>

</div>

Mistgate is an open-source panel for people who run a VPN for others: family, friends, a community or a small team. It runs Hysteria2, VLESS and AmneziaWG. You add a server from the browser with its IP and root password, and each person gets one link. The panel checks every server the way an app does and tells you in Telegram when one breaks. It is two static Go binaries with SQLite and systemd, no Docker, under the AGPL-3.0.

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Mistgate/mistgate/main/docs/images/readme/overview-dark-en.webp">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/Mistgate/mistgate/main/docs/images/readme/overview-light-en.webp">
  <img alt="The Mistgate admin: six nodes with their health and throughput, one open problem, recent events" src="https://raw.githubusercontent.com/Mistgate/mistgate/main/docs/images/readme/overview-dark-en.webp" width="100%">
</picture>

### The panel

- **Code:** [Mistgate/mistgate](https://github.com/Mistgate/mistgate)
- **Documentation:** [mistgate.app](https://mistgate.app/)
- **Releases:** [signed Linux binaries for amd64 and arm64](https://github.com/Mistgate/mistgate/releases/latest)
- **Compared with** 3x-ui, Remnawave, Hiddify, PasarGuard and s-ui: [the table and its sources](https://github.com/Mistgate/mistgate/blob/main/docs/en/reference/comparison.md)

### The app for Windows

Mistgate for Windows is the panel's own app, and it also works with any plain subscription link. Hysteria2, AmneziaWG and VLESS in one window; it picks the server and the protocol that work on the network you are on, sends through the VPN only what you choose (by site, by list, by program), holds the traffic with a kill switch while the tunnel is down, and shows what is blocked from where you are. With a Mistgate panel it enrols the PC with its own key and shows the plan, the data used, the devices and the Telegram proxies.

<img alt="Mistgate for Windows: connected, the server list on the right" src="https://raw.githubusercontent.com/Mistgate/mistgate-client/main/docs/img/home.png" width="100%">

- **Code:** [Mistgate/mistgate-client](https://github.com/Mistgate/mistgate-client)
- **Download:** [the latest release for Windows 10 and 11, x64](https://github.com/Mistgate/mistgate-client/releases/latest)
- **Updates** come from those releases; the app installs only an installer signed with the project's key
- In English, Russian, Chinese, Persian and Turkish. Beta, like the panel

### How to help

- Run the panel on a spare VPS and [open an issue](https://github.com/Mistgate/mistgate/issues) for anything that breaks or reads unclear.
- Try the Windows app on your network and [tell us](https://github.com/Mistgate/mistgate-client/issues) what does not connect.
- Fix a documentation page: every page on mistgate.app has an edit link.
- Read [CONTRIBUTING.md](https://github.com/Mistgate/mistgate/blob/main/CONTRIBUTING.md) and send a pull request. Coding agents start with [AGENTS.md](https://github.com/Mistgate/mistgate/blob/main/AGENTS.md).
- Report vulnerabilities privately: [SECURITY.md](https://github.com/Mistgate/mistgate/blob/main/SECURITY.md).
