# Home Assistant Add-ons

[![Add repository to Home Assistant](https://img.shields.io/badge/Home%20Assistant-Add--on%20Repository-18BCF2?style=for-the-badge&logo=homeassistant&logoColor=white)](https://my.home-assistant.io/redirect/supervisor_add_addon_repository/?repository_url=https%3A%2F%2Fgithub.com%2Fskornehl%2Fha-addons)
[![DLS Bridge](https://img.shields.io/badge/dynamic/yaml?url=https%3A%2F%2Fraw.githubusercontent.com%2Fskornehl%2Fha-addons%2Fmain%2Fdls_mein_essen_bridge%2Fconfig.yaml&query=%24.version&label=DLS%20Bridge&prefix=v&style=for-the-badge&color=6366F1)](dls_mein_essen_bridge/CHANGELOG.md)
[![Kleinanzeigen Bridge](https://img.shields.io/badge/dynamic/yaml?url=https%3A%2F%2Fraw.githubusercontent.com%2Fskornehl%2Fha-addons%2Fmain%2Fkleinanzeigen_bridge%2Fconfig.yaml&query=%24.version&label=Kleinanzeigen%20Bridge&prefix=v&style=for-the-badge&color=6366F1)](kleinanzeigen_bridge/CHANGELOG.md)
[![Checks](https://img.shields.io/github/actions/workflow/status/skornehl/ha-addons/validate.yml?branch=main&style=for-the-badge&label=checks)](https://github.com/skornehl/ha-addons/actions/workflows/validate.yml)
[![License](https://img.shields.io/github/license/skornehl/ha-addons?style=for-the-badge&color=9333EA)](LICENSE)

Add-on repository for the add-ons that back my own Home Assistant
integrations. Each integration lives in its own HACS repository (HACS
expects one integration per repository); the add-ons they talk to are
collected here.

[![Add repository to Home Assistant](https://my.home-assistant.io/badges/supervisor_add_addon_repository.svg)](https://my.home-assistant.io/redirect/supervisor_add_addon_repository/?repository_url=https%3A%2F%2Fgithub.com%2Fskornehl%2Fha-addons)

| Add-on | Used by |
|---|---|
| [DLS Mein Essen Bridge](dls_mein_essen_bridge) | [ha-dls-mein-essen](https://github.com/skornehl/ha-dls-mein-essen) |
| [Kleinanzeigen Bridge](kleinanzeigen_bridge) | [ha-kleinanzeigen](https://github.com/skornehl/ha-kleinanzeigen) |

## Installation

Settings → Add-ons → Add-on Store → ⋮ → Repositories → add
`https://github.com/skornehl/ha-addons`.

Inside Home Assistant an add-on from this repository is reachable as
`http://6dc2c37d-<slug with dashes>:<port>`, e.g.
`http://6dc2c37d-dls-mein-essen-bridge:8099`. The prefix is derived from
the repository URL, so it is the same on every installation.
