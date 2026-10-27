# Home Assistant Add-ons

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
