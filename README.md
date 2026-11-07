<p align="center">
  <img src="https://status.stux.cloud/icon-512.png" height="100" alt="Stux.Cloud Status icon">
</p>

# Stux.Cloud Status

### *Live status of Stux.Cloud's websites and pages, powered by [GitHup](https://githup.stux.group).*

**Status page:** [status.stux.cloud](https://status.stux.cloud)

<!-- A live badge: reads the overall status straight from data/summary.json (after the first check). -->
[![Stux.Cloud status](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fraw.githubusercontent.com%2FStuxCloud%2FStatus%2Fmain%2Fdata%2Fsummary.json&query=%24.status&label=status&style=for-the-badge)](https://status.stux.cloud)

## Current status

Updated by GitHup whenever the status page is rebuilt (hourly, and when a status changes). The
table fills in after the workflow's first check.

<!-- githup:start -->
<!-- This table is written by GitHup (https://github.com/StuxGroup/GitHup); edits here are overwritten. -->

**All systems operational** · [Live status page](https://status.stux.cloud/)

| Group | Monitor | Status | Uptime (24 h) | Uptime (7 d) | Uptime (30 d) | Response time (24 h) |
| ----- | ------- | ------ | ------------- | ------------ | ------------- | -------------------- |
| Stux.Cloud | [Stux.Cloud](https://stux.cloud/) | Up | 100.00% | 100.00% | 100.00% | 420 ms |
| Stux.Cloud | [Stux.Cloud Media CDN](https://global.media.stux.cloud/icon.png) | Up | 100.00% | 100.00% | 100.00% | 192 ms |
| Regions | [Stux.Cloud United Kingdom Region](https://uk.stux.cloud/) | Up | 100.00% | 100.00% | 100.00% | 224 ms |
| Regions | [Stux.Cloud Spain Region](https://es.stux.cloud/) | Up | 100.00% | 100.00% | 100.00% | 467 ms |
| Regions | [Stux.Cloud Finland Region](https://fi.stux.cloud/) | Up | 100.00% | 100.00% | 100.00% | 556 ms |
| Regions | [Stux.Cloud France Region](https://fr.stux.cloud/) | Up | 100.00% | 100.00% | 100.00% | 491 ms |
| Regions | [Stux.Cloud United States Region](https://us.stux.cloud/) | Up | 100.00% | 100.00% | 100.00% | 207 ms |
| Regions | [Stux.Cloud Canada Region](https://ca.stux.cloud/) | Up | 100.00% | 100.00% | 100.00% | 203 ms |
| Regions | [Stux.Cloud EMEA Region](https://emea.stux.cloud/) | Up | 100.00% | 100.00% | 100.00% | 280 ms |
| Regions | [Stux.Cloud Europe Region](https://eu.stux.cloud/) | Up | 100.00% | 100.00% | 100.00% | 342 ms |
| Regions | [Stux.Cloud AMER Region](https://amer.stux.cloud/) | Up | 100.00% | 100.00% | 100.00% | 402 ms |
| Regions | [Stux.Cloud APAC Region](https://apac.stux.cloud/) | Up | 100.00% | 100.00% | 100.00% | 298 ms |
| Regions | [Stux.Cloud Australia Region](https://au.stux.cloud/) | Up | 100.00% | 100.00% | 100.00% | 333 ms |
| Regions | [Stux.Cloud Japan Region](https://jp.stux.cloud/) | Up | 100.00% | 100.00% | 100.00% | 303 ms |
| Regions | [Stux.Cloud Singapore Region](https://sg.stux.cloud/) | Up | 100.00% | 100.00% | 100.00% | 280 ms |
| Regions | [Stux.Cloud India Region](https://in.stux.cloud/) | Up | 100.00% | 100.00% | 100.00% | 290 ms |
| Pages | [Stux.Cloud Region Page](https://regionpage.stux.cloud/) | Up | 100.00% | 100.00% | 100.00% | 132 ms |
| Pages | [Stux.Cloud Instance Page](https://instancepage.stux.cloud/) | Up | 100.00% | 100.00% | 100.00% | 130 ms |
| Pages | [Stux.Cloud Coming Soon Page](https://soonpage.stux.cloud/) | Up | 100.00% | 100.00% | 100.00% | 125 ms |
| Pages | [Stux.Cloud Maintenance Page](https://maintenancepage.stux.cloud/) | Up | 100.00% | 100.00% | 100.00% | 118 ms |
| Pages | [Stux.Cloud GitHub Pages Redirect](https://stuxcloud.github.io/) | Up | 100.00% | 100.00% | 100.00% | 81 ms |
| Archived pages | [Stux.Cloud Region Page v2](https://regionpage-v2.stux.cloud/) | Up | 100.00% | 100.00% | 100.00% | 130 ms |
| Archived pages | [Stux.Cloud Instance Page v2](https://instancepage-v2.stux.cloud/) | Up | 100.00% | 100.00% | 100.00% | 122 ms |
| Archived pages | [Stux.Cloud Instance Page v1](https://instancepage-v1.stux.cloud/) | Up | 100.00% | 100.00% | 100.00% | 117 ms |
| Archived pages | [Stux.Cloud Coming Soon Page v2](https://soonpage-v2.stux.cloud/) | Up | 100.00% | 100.00% | 100.00% | 121 ms |
| Archived pages | [Stux.Cloud Maintenance Page v2](https://maintenancepage-v2.stux.cloud/) | Up | 100.00% | 100.00% | 100.00% | 142 ms |
<!-- githup:end -->

## What's monitored

Every 5 minutes (when GitHub runs the schedule late, a run checks up to 4 times, 5 minutes apart, to fill the gap), GitHup checks each monitor in [`.githup.yml`](.githup.yml):

- **Stux.Cloud:** [stux.cloud](https://stux.cloud) and the Stux.Cloud media CDN
- **Regions:** every region's website: those on their own server (United Kingdom, Spain, Finland,
  France, United States, Canada), and the placeholder sites for regions with no server yet (EMEA, Europe, AMER,
  APAC, Australia, Japan, Singapore, India)
- **Pages:** the Stux.Cloud Region Page, Instance Page, Coming Soon Page, Maintenance Page and
  GitHub Pages Redirect
- **Archived pages:** the earlier designs kept online as snapshots (the v1 and v2 pages)
- The servers behind each region are on [Stuxedo Status](https://status.stuxedo.com), linked
  under Elsewhere. Only public sites are listed here

To add a monitor, add it to the right group there (or a new group). A group can also hold `links:` instead of monitors, for sites that should be listed but not checked.

When something goes down, GitHup opens an Issue on this repository (labelled `githup`,
`incident`, `status` and the monitor's slug) and closes it with the downtime when it recovers.
To announce planned maintenance, open an Issue yourself with the `githup` and `incident` labels
(plus the monitor's slug to link it); it shows on the status page.

## How it works

- **`.github/workflows/status.yml`** runs a GitHup `check` every 5 minutes (with `fill-gaps`, up to 4 checks when the schedule is late) and commits the
  results to `data/` as `github-actions[bot]`. When a status changes, hourly, and on pushes, it
  builds the GitHup status page into `_site` (with `site-dir`), and deploys it with `actions/deploy-pages`.
- **The page's icon** is its own badge icon: the Stux.Cloud mark on a round avatar with a heartbeat
  badge, in Stux.Cloud's teal. `scripts/badge-icons.py` builds the favicon set into `icons/`, which
  GitHup publishes at the site root (`site.icons`); `site.logo` and `site.favicon` point at its
  `icon-512.png`.
- **`legal:` in `.githup.yml`** makes GitHup generate the **Boring Legal Stuff** hub at `/legal/`
  with its six sub-pages, a themed `404.html`, a `/sitemap/` page, `sitemap.xml` and `robots.txt`
  (the base URL is `site.url`). Nothing is hand-made, and the footer shows only
  **Powered by GitHup**. This repo's own `CHANGELOG.md` and `VERSION.md` are for this repo only.
- **`data/`** is the monitoring history. Don't edit it by hand.
- **The status table above** is written by GitHup's `readme` mode between the
  `<!-- githup:start -->` and `<!-- githup:end -->` markers. Don't edit inside them.

## Local development

```bash
./dev-server.sh                 # or dev-server.bat on Windows; add a port as the last argument
./dev-server.sh --no-dev-mode   # production rendering
```

`dev-server` generates 90 days of example data, builds the status page into `.dev/public` with
`DEV_MODE` on, with its legal pages, 404 and sitemap, and serves it at
`http://127.0.0.1:8000`. It uses GitHup from `$GITHUP_PATH`, a sibling `../GitHup` or
`../../Stux.Group/GitHup` checkout, or a fresh clone in `.dev/GitHup`.

## Hosting

GitHub Pages, deployed by Actions (**Settings → Pages → Source: GitHub Actions**), with the custom
domain `status.stux.cloud` set in the Pages settings. DNS: a `CNAME` record for `status` (in the
`stux.cloud` zone, ahead of its `*` wildcard) pointing at `stuxcloud.github.io`. The repository is
public, so the page's live refresh can read `data/summary.json` straight from GitHub.

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md).

## Versioning

This project uses [Date Versioning](https://datevers.ing): each release is numbered by its UTC release date as `YY.MM.DD` (for example `26.11.06`), with `-1`, `-2`… for later releases the same day. See [CHANGELOG.md](CHANGELOG.md) for what changed in each release.

Work happens on `test` (or a branch off it), never on `main`. Changes reach `main` only through a pull request from `test`; the release commit and tag are made on `test` and go live when the pull request is merged.

## License

&copy; 2026 Stux.Group. All rights reserved. This repository is not licensed for reuse or
redistribution, see [LICENSE](LICENSE).

---

*Built & Maintained by <picture><source media="(prefers-color-scheme: dark)" srcset="https://global.media.stux.cloud/icon-light.png"><source media="(prefers-color-scheme: light)" srcset="https://global.media.stux.cloud/icon-dark.png"><img src="https://global.media.stux.cloud/icon-dark.png" height="14" alt="Stux.Cloud" valign="middle"></picture> [Stux.Cloud](https://github.com/StuxCloud), powered by [GitHup](https://githup.stux.group).
Stux.Cloud is a part of the <picture><source media="(prefers-color-scheme: dark)" srcset="https://global.media.stux.group/icon-light.png"><source media="(prefers-color-scheme: light)" srcset="https://global.media.stux.group/icon-dark.png"><img src="https://global.media.stux.group/icon-dark.png" height="14" alt="Stux.Group" valign="middle"></picture> Stux.Group brand of businesses.*
