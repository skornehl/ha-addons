# Changelog

## 0.2.5

- Recover from a crashed browser: when the page stops responding, the
  bridge now starts a fresh browser and logs in again instead of reporting
  `ready` while every call fails.
- The coordinate login fallback no longer runs after the form was already
  filled, and it replaces field contents instead of appending to them, so
  it cannot send a garbled login to the DLS account.
- The API only answers HA Core and the Supervisor; other add-ons get 403.
- The `log_level` option now works.
- Runs with the default Docker init again (`init: false` removed), so
  Chromium's exited child processes are reaped.

## 0.2.4

- Moved to the add-on repository `skornehl/ha-addons`. Installed from there,
  the bridge is reachable as `http://6dc2c37d-dls-mein-essen-bridge:8099`.
- The host port 8099 is no longer published by default. The integration
  uses the internal add-on network; the port can still be enabled in the
  add-on's network settings.

Earlier versions were released from `skornehl/ha-dls-mein-essen`.
