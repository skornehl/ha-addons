# Changelog

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
