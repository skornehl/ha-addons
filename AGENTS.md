# AGENTS.md

Add-on repository for Home Assistant. Each add-on is the backend of one of
Sebastian's own HACS integrations, which live in their own repositories.

## Conventions

- Conventional Commits, branches `<type>/<slug>`, never push to `main`;
  always a pull request.
- Author: `Sebastian Kornehl <sebastian@kornehl.org>`; add a
  `Co-Authored-By` trailer when an agent did the work.
- English in code, comments and docs.

## Rules for add-ons in this repository

- **Every change to an add-on bumps its `version` in `config.yaml`** and adds
  an entry to its `CHANGELOG.md`. The Supervisor only offers an update when
  the version changes.
- **The hostname prefix is `6dc2c37d`** (`sha1(repository URL)[:8]`), so an
  add-on with slug `foo_bar` is reachable at `http://6dc2c37d-foo-bar:<port>`.
  Integrations use that as their default bridge URL. Renaming or moving this
  repository changes the prefix and breaks every installation.
- Do not publish host ports unless something outside Home Assistant needs
  them: integrations use the internal add-on network.
- A new add-on: new folder with `config.yaml`, `Dockerfile`, `README.md` or
  `DOCS.md`, `CHANGELOG.md`; add it to the README table and the CI matrix.
