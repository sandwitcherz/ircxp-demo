# ircxp — demo version

**ircxp** is an all-in-one IRC server written in Go by [PcXpress](https://pcxpress.fr): server, services (NickServ, ChanServ, OperServ, BotServ, HostServ, FunServ), web client, built-in bouncer, Android app, AI-assisted moderation and administration panel — in **a single binary**, with no dependency to install.

*Français : [README.md](README.md)*

This repository distributes the **demo version**: all the features, limited to **10 connections** and without server links. Enough to try everything at home before buying.

- Online demo: https://ircxp.live (IRC: `ircxp.live`, TLS 6697 / 6667)
- Shop and licences: https://shop.ircxp.live
- Documentation: https://ircxp.live/wiki (English version: button “EN”)

> Current version: **2.2.0**. See the [Releases](../../releases).

## What ircxp contains

- **IRC server and services**: registered accounts and channels, operator levels (helper, ircop, admin, netadmin, devadmin), remembered channel modes, SASL (PLAIN, EXTERNAL).
- **IRCv3**: capability negotiation 3.2 (`CAP LS 302`) with `multi-prefix`, `away-notify`, `account-notify`, `extended-join`, `chghost`, `server-time`, `sasl`, `cap-notify`, `echo-message`, `batch` and `draft/chathistory`.
- **End-to-end encrypted channels**: channel mode `+E`, messages encrypted in the web client (AES-256-GCM, passphrase never sent to the server); only the channels with this mode are encrypted.
- **Web client** (English and French): light and dark themes, avatars, ranks and XP, nickname effects, no installation for your users.
- **Built-in bouncer** (ZNC-style): always-connected session, missed-message history, external networks (also usable from the web client), user panel.
- **Android app**, ready to install.
- **Moderation and GDPR**: AI moderation (`+M`), abuse reports, ready-to-use legal pages, connection log for operators with limited retention.
- **Games and bots**: Quiz, Motus, automatic translation per channel (`+T`), reminders and notes, monitoring.
- **Administration panel**: per-operator access, automatic backups and restore, customizable look.
- **Bridges**: Discord, Fluxer and **IRC ↔ IRC** (for example a channel of Libera linked to a channel of your network; the bots answer on both sides).

## Demo and full licence

| | Demo (this repository) | Network licence |
|---|---|---|
| Connections | 10 at most | unlimited |
| Server links (hub / leaf) | no | yes |
| Updates and support | no | yes |

The full licence can be ordered on https://shop.ircxp.live.

## Download

Go to the **[Releases](../../releases)** and take the archive for your system:

| System | Archive |
|---|---|
| Linux 64-bit | `ircxp-demo-vX.Y.Z-linux-amd64.tar.gz` |
| Linux ARM64 | `ircxp-demo-vX.Y.Z-linux-arm64.tar.gz` |
| Raspberry Pi (ARMv7) | `ircxp-demo-vX.Y.Z-linux-armv7.tar.gz` |
| Windows 64-bit | `ircxp-demo-vX.Y.Z-windows-amd64.zip` |
| Windows ARM64 | `ircxp-demo-vX.Y.Z-windows-arm64.zip` |
| macOS Apple Silicon | `ircxp-demo-vX.Y.Z-darwin-arm64.tar.gz` |
| macOS Intel | `ircxp-demo-vX.Y.Z-darwin-amd64.tar.gz` |

Each release has a `SHA256SUMS` file to check the download:

```sh
sha256sum -c SHA256SUMS --ignore-missing
```

## Quick install (Linux)

```sh
tar xzf ircxp-demo-v*-linux-amd64.tar.gz
cd ircxp-demo-v*-linux-amd64
cp config.example.json config.json   # then adapt the server name
./ircxp
```

The server listens for IRC on ports 6667 (plain) and 6697 (TLS), and opens the web client and the administration panel. The archive contains the complete documentation in `docs/` (in French: installation, configuration, services, bouncer, moderation…) and an `ircxp.service` file for systemd.

## Licence

The demo version is provided **free of charge for evaluation**. Its redistribution and commercial use are forbidden without a licence. The source code is not provided. See [LICENSE.en.md](LICENSE.en.md) (English) and [LICENSE.md](LICENSE.md) (French, the reference text).

## Contact

Questions, quotes, support: **support@ircxp.live**, or on IRC: https://ircxp.live.

Created and hosted by [PcXpress](https://pcxpress.fr).
