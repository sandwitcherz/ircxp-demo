# ircxp — version de démonstration

**ircxp** est un serveur IRC tout-en-un écrit en Go par [PcXpress](https://pcxpress.fr) : serveur, services (NickServ, ChanServ, OperServ, BotServ, HostServ, FunServ), client web, bouncer intégré, application Android, modération assistée par IA, panel d'administration — dans **un seul binaire**, sans dépendance à installer.

*English: [README.en.md](README.en.md)*

Ce dépôt distribue la **version de démonstration** : toutes les fonctions, limitée à **10 connexions** et sans liaison entre serveurs. De quoi tout essayer chez vous avant d'acheter.

- Démo en ligne : https://ircxp.live (IRC : `ircxp.live`, TLS 6697 / 6667)
- **Toutes les fonctions : [FEATURES.md](FEATURES.md)**
- Boutique et licences : https://shop.ircxp.live
- Documentation : https://ircxp.live/wiki (version anglaise : bouton « EN »)

> Version actuelle : **2.3.0**. Voir les [Releases](../../releases).

## Ce que contient ircxp

- **Serveur IRC et services** : comptes et salons enregistrés, niveaux d'opérateurs (helper, ircop, admin, netadmin, devadmin), modes de salon mémorisés, SASL.
- **IRCv3** : négociation des capacités 3.2 (`CAP LS 302`) avec `multi-prefix`, `away-notify`, `account-notify`, `extended-join`, `chghost`, `server-time`, `sasl`, `cap-notify`, `echo-message`, `batch` et `draft/chathistory`.
- **Salons chiffrés de bout en bout** : mode `+E`, messages chiffrés dans le client web (AES-256-GCM, phrase secrète jamais envoyée au serveur) ; seuls les salons avec ce mode sont chiffrés.
- **Client web** (français et anglais) : thèmes clair et sombre, avatars, rangs et XP, effets de pseudo, ouvert dans un navigateur sans rien installer.
- **Bouncer intégré** (façon ZNC) : session toujours connectée, historique des messages manqués, réseaux externes, panneau utilisateur.
- **Application Android** prête à installer.
- **Modération et RGPD** : modération IA (+M), signalements, pages légales prêtes à l'emploi.
- **Jeux et bots** : Quiz, Motus, traduction automatique par salon (+T), rappels et notes, monitoring.
- **Panel d'administration** : accès par opérateur, sauvegardes automatiques et restauration, apparence personnalisable.
- **Passerelles** Discord, Fluxer et **IRC ↔ IRC** (par exemple un salon de Libera relié à un salon de ton réseau ; les bots répondent des deux côtés).

## Démo et licence complète

| | Démo (ce dépôt) | Licence réseau |
|---|---|---|
| Connexions | 10 au plus | illimitées |
| Liaison entre serveurs (hub / leaf) | non | oui |
| Mises à jour et assistance | non | oui |

La licence complète se commande sur https://shop.ircxp.live.

## Téléchargement

Rendez-vous dans les **[Releases](../../releases)** et prenez l'archive de votre système :

| Système | Archive |
|---|---|
| Linux 64 bits | `ircxp-demo-vX.Y.Z-linux-amd64.tar.gz` |
| Linux ARM64 | `ircxp-demo-vX.Y.Z-linux-arm64.tar.gz` |
| Raspberry Pi (ARMv7) | `ircxp-demo-vX.Y.Z-linux-armv7.tar.gz` |
| Windows 64 bits | `ircxp-demo-vX.Y.Z-windows-amd64.zip` |
| Windows ARM64 | `ircxp-demo-vX.Y.Z-windows-arm64.zip` |
| macOS Apple Silicon | `ircxp-demo-vX.Y.Z-darwin-arm64.tar.gz` |
| macOS Intel | `ircxp-demo-vX.Y.Z-darwin-amd64.tar.gz` |

Chaque release contient un fichier `SHA256SUMS` pour vérifier le téléchargement :

```sh
sha256sum -c SHA256SUMS --ignore-missing
```

## Installation rapide (Linux)

```sh
tar xzf ircxp-demo-v*-linux-amd64.tar.gz
cd ircxp-demo-v*-linux-amd64
cp config.example.json config.json   # puis adaptez le nom du serveur
./ircxp
```

Le serveur écoute en IRC sur les ports 6667 (clair) et 6697 (TLS), et ouvre le client web et le panel d'administration. L'archive contient la documentation complète dans `docs/` (installation, configuration, services, bouncer, modération…) et un fichier `ircxp.service` pour systemd.

## Licence

La version de démonstration est fournie **gratuitement pour évaluation**. Sa redistribution et son usage commercial sont interdits sans licence. Le code source n'est pas fourni. Voir [LICENSE.md](LICENSE.md) (texte de référence, en français) et [LICENSE.en.md](LICENSE.en.md) (traduction anglaise).

## Contact

Questions, devis, assistance : **support@ircxp.live**, ou sur IRC : https://ircxp.live.

Créé et hébergé par [PcXpress](https://pcxpress.fr).
