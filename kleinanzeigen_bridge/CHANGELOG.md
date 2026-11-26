# Changelog

## 0.1.4

- Fixes the installation: the pinned kleinanzeigen-bot base image was deleted
  upstream, so every new install (amd64 and aarch64) failed with
  "failed to resolve source metadata: not found" (#5). Now pinned to the
  multi-arch image of the kleinanzeigen-bot release of 2026-11-15, which also
  processes all ad overview pages instead of stopping after 10.

## 0.1.3

- Republish results are matched by the downloaded ad file instead of by
  title, so ads with the same or slightly different titles are reported and
  counted correctly (minimum days between republishes, 30-day counter).
- The job status and message are HTML-escaped on the panel page.
- The kleinanzeigen-bot base image is pinned by digest instead of `latest`.
- Username and password are optional in the schema, so the add-on starts
  before it is configured.
- The reported version comes from `config.yaml` via the build.

## 0.1.2

- Moved to the add-on repository `skornehl/ha-addons`, otherwise unchanged.
  Installed from there, the bridge is reachable as
  `http://6dc2c37d-kleinanzeigen-bridge:8099`.

Earlier versions were released from `skornehl/ha-kleinanzeigen`.
