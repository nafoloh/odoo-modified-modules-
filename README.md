# Modified Odoo Community Modules

## Summary

Maintained copies and local modifications of community addons for Odoo 18.
Repository: https://github.com/nafoloh/odoo-modified-modules-

The source of truth for local edits on this VM is `/odoo18/modified_modules`.
This is a collection of addon copies, not a GitHub fork of one upstream repository.
The initial import contains the supplied working source; no upstream Git history
or exact upstream commit was present in the folder.

## Features

| Addon | Version | Dependency | Upstream | License |
| --- | --- | --- | --- | --- |
| `purchase_request` | 18.0.2.5.0 | `purchase_stock` | [OCA/purchase-workflow, branch 18.0](https://github.com/OCA/purchase-workflow/tree/18.0/purchase_request) | LGPL-3 |

Purchase Request lets users request materials or services, approve requests,
and create or extend requests for quotation from approved request lines.
The supplied local copy includes searches by product description, product,
and source document, plus automatic selection of custom descriptions when
creating purchase order lines. See the addon [overview](purchase_request/README.rst),
[configuration](purchase_request/readme/CONFIGURE.md), and
[user guide](purchase_request/readme/USAGE.md).

### Installation and operation

1. Use Odoo 18 with the addon dependencies available.
2. Include `/odoo18/modified_modules` in the server's `addons_path`, preserving
   all existing paths, if this checkout is not already configured.
3. Update the Apps list and install **Purchase Request** on the intended database.
4. Open **Purchase Requests**, enter the required items, quantities, and dates,
   submit for approval, then select approved request lines and use **Create RFQ**.
5. For procurement-generated requests, follow the product and route setup in
   the linked configuration guide.

Repository setup leaves the existing addon in place. It does not alter server
configuration, install or upgrade addons, or restart Odoo. Runtime activation
was not checked as part of this setup.

### Maintenance and attribution

Preserve each addon's technical directory name, license notices, original authors,
and contributor credits. Addons retain their own licenses; this collection does
not replace those licenses. Record upstream URLs and versions when adding addons,
and record the upstream commit when it is known. Review upstream updates before
merging them with local changes.

Local `AGENTS.md` instructions, agent tool state, editor recovery files, and
temporary files are excluded from Git. Keep addon source, tests, translations,
licenses, and user documentation tracked so clones remain usable and maintainable.

## To-dos

- Record the exact upstream baseline commit when established.
- Run relevant Odoo installation and business workflow tests before deploying
  future behavior changes. Repository setup validates source syntax and integrity,
  but does not establish runtime correctness.

## Changelog

### 2026-11-02

- Added the supplied `purchase_request` source as the initial repository baseline.
- Added repository usage, provenance, maintenance guidance, and ignore rules.
- Checked Python/XML syntax and source integrity; no Odoo runtime tests were run.

### Import validation notes

All 21 Python and 12 XML files passed syntax checks. The 117 imported addon
files match the pre-import SHA-256 snapshot. The existing generated
`purchase_request/README.rst` has trailing whitespace on line 9 and an RST
heading underline on line 143 that Git flags as a conflict marker. These
baseline formatting warnings were retained to preserve the supplied source.
