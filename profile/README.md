<div align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="./assets/banner-dark.svg">
    <source media="(prefers-color-scheme: light)" srcset="./assets/banner-light.svg">
    <img alt="Mistgate: a lightweight, self-hosted VPN panel" src="./assets/banner-dark.svg" width="100%">
  </picture>

  <p><b>English</b> · <a href="https://github.com/Mistgate/.github/blob/main/profile/README.ru.md">Русский</a></p>
</div>

**Mistgate** is a lightweight, self-hosted panel for your own VPN fleet: one Go binary for the panel, one for the node agent, no Docker. Hysteria2 and AmneziaWG live side by side, in one subscription, in one admin UI.

**[Website & documentation](https://mistgate.app/)** · [Source code](https://github.com/Mistgate/mistgate)

## Why another panel

- **Light.** SQLite, systemd, two static binaries. No Docker, no database server. The panel's memory target at idle is 80 MB (a target for now, not a benchmark).
- **AmneziaWG users are not a blind spot.** Every AmneziaWG device is a peer the panel knows about: who is online, traffic per user and per device.
- **A doctor that knows hosters.** Disk and journals filling up, a resolver that cannot resolve, clock drift, port conflicts, a sick network baseline. Found, explained in plain words, fixed with one confirmed click where that is safe.
- **Looked at from the client's side.** Synthetic probes connect the way a real client does (Hysteria2 and AmneziaWG), so a node is green only if traffic really flows.
- **Made for AI agents too.** API tokens and an MCP server, with plan / apply and owner approvals for anything risky.

## What is inside

| The fleet | Access and tooling |
|:--|:--|
| <img src="./assets/icons/zap.svg" width="32" height="32" align="absmiddle" alt="">&nbsp; **Hysteria2 and AmneziaWG**<br>Hysteria2 with Salamander and AmneziaWG 2.0 / 3.1, userspace or kernel module. Several profiles per node. | <img src="./assets/icons/qr.svg" width="32" height="32" align="absmiddle" alt="">&nbsp; **Subscriptions**<br>Per-user links for Happ, Mihomo / Clash YAML, AmneziaVPN keys and `vpn://`, plus a public page with a QR code. |
| <img src="./assets/icons/globe.svg" width="32" height="32" align="absmiddle" alt="">&nbsp; **WARP egress**<br>Send a profile's traffic out through WARP. If the WARP link drops, the profile fails closed instead of leaking direct. | <img src="./assets/icons/users.svg" width="32" height="32" align="absmiddle" alt="">&nbsp; **Users and devices**<br>Groups, one peer per device, traffic limits, DNS presets per user or group. |
| <img src="./assets/icons/pulse.svg" width="32" height="32" align="absmiddle" alt="">&nbsp; **Fleet doctor**<br>Node self-checks with safe fixes, synthetic client probes, alerts with a full lifecycle. | <img src="./assets/icons/window.svg" width="32" height="32" align="absmiddle" alt="">&nbsp; **Admin UI**<br>Russian and English, dark and light, passkey sign-in. |
| <img src="./assets/icons/shield.svg" width="32" height="32" align="absmiddle" alt="">&nbsp; **Signed updates**<br>Node agents check an ed25519-signed manifest themselves. Canary rollout, health gate, automatic rollback. | <img src="./assets/icons/spark.svg" width="32" height="32" align="absmiddle" alt="">&nbsp; **Agent access**<br>Tokens for read-only, operator and admin. Changes go through plan / apply; the risky ones wait for the owner. |

## Desktop client: kl!ck

<a href="https://github.com/vbu00/klick">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/vbu00/klick/main/docs/logo/wordmark-dark.svg">
    <img alt="kl!ck" src="https://raw.githubusercontent.com/vbu00/klick/main/docs/logo/wordmark-light.svg" width="200">
  </picture>
</a>

For Windows we recommend **[kl!ck](https://github.com/vbu00/klick)**: a small open-source VPN client on the unmodified [mihomo](https://github.com/MetaCubeX/mihomo) core. Paste your Mistgate subscription link and get Hysteria2 and AmneziaWG in one window, with TUN, per-site and per-app routing and a kill switch that keeps working when the window is closed. macOS is on the way.

**[Download for Windows](https://github.com/vbu00/klick/releases/latest)** · [Source](https://github.com/vbu00/klick) · MIT

## Status

Mistgate is pre-release. What exists and what is coming:

| Stage | What |
|:--|:--|
| **Done** | Panel and node agent over mTLS · Hysteria2 · AmneziaWG 2.0 / 3.1 · WARP egress · subscriptions and the public user page · DNS presets · health doctor, synthetic probes, alerts · signed node-agent updates with canary and rollback · GitHub panel self-update with checksum verification and rollback · Go SSH node installer with preflight, pinned host keys and encrypted per-job credentials · API tokens and MCP server · admin UI and documentation in ru / en |
| **Now** | SSH-job cancellation · persistent server-access cards · encrypted panel backup and restore to R2 · node-removal cleanup |
| **Next** | Telegram bot for the whole fleet · more subscription formats (Xray JSON, sing-box) and subscription mirrors · a one-line installer |
| **Later** | VLESS REALITY as the first external protocol plugin |

---

<sub>Open source under [AGPL-3.0](https://github.com/Mistgate/mistgate/blob/main/LICENSE).</sub>
