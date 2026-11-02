# Modified Odoo Community Modules

Scope: `/odoo18/modified_modules` and its contained Odoo 18 addons.
Remote: https://github.com/nafoloh/odoo-modified-modules-.git

- Access only addons relevant to the user's active request. Ask before accessing
  another addon outside the authorized scope. Modules created in the session
  are in scope.
- Never run `git init`. Preserve existing source and Git history.
- Future commits, pushes, pulls, fetches, branch changes, and merges require an
  explicit user request. The initial repository setup request authorizes its
  baseline commit and publication.
- Preserve addon technical names, upstream attribution, licenses, and local
  changes. Record known upstream versions and commits in the root README.
- Update addon documentation in the same iteration as behavior changes. Keep
  user instructions consistent with the UI language and update existing workflows.
  Repository organization changes update the root documentation.
- Remove addon `__pycache__` directories and `.pyc` files before finishing changes.
- Never commit credentials, local server configuration, dumps, or runtime output.
- Run relevant checks; do not claim Odoo runtime validation from syntax checks.
- Run Odoo CLI commands as `odoo18`, using
  `/odoo18/venv/bin/python /odoo18/odoo/odoo-bin` and `/etc/odoo/odoo.conf`.
  Relevant upgrades/tests on `DB-TEST-DEBUG` are authorized. Do not change
  production or server configuration as part of repository-only setup.
