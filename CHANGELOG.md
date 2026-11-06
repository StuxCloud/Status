# Changelog

All notable changes to Stux.Cloud Status are documented here. Each release's sections follow
a fixed order: Added, Changed, Fixed, Removed, Security, Deprecated. This project uses
[Date Versioning](https://datevers.ing) since v26.11.06, its first stable release (`YY.MM.DD`, the UTC release date, with
`-1`, `-2`… for later releases the same day); v0.1.0 used [Semantic Versioning](https://semver.org).

## v26.11.06

The first stable release. Like every GitHup status page, Stux.Cloud Status is stable from the start, so it moves straight
to Date Versioning; there is no 1.0.0.

### Changed

- Switched from Semantic Versioning to [Date Versioning](https://datevers.ing): releases are numbered by their UTC release date as `YY.MM.DD`, with `-1`, `-2`… for later releases the same day. This release follows v0.1.0
- `commit.sh` and `commit.bat` (now the same as the other GitHup status pages') accept only a valid Date Version that isn't in the future (UTC), and warn when it's dated before today; `tests/version.sh` checks Date Versions only
- `README.md` and `CONTRIBUTING.md` describe Date Versioning and the release steps

## v0.1.0

### Added

- Stux.Cloud Status (`status.stux.cloud`), built with [GitHup](https://githup.stux.group): checks every 5 minutes (catching up when GitHub runs the schedule late), incident Issues, and the status page deployed to GitHub Pages by `.github/workflows/status.yml`
- Monitors for Stux.Cloud's public sites, with full names: the Stux.Cloud website and Media CDN; the six region websites with a server (United Kingdom, Spain, Finland, France, United States, Canada); the Region, Instance, Coming Soon and Maintenance Pages and the GitHub Pages Redirect; and the archived v1 and v2 page snapshots. Links to Stuxedo Status (the servers) and Stux.Group Status
- Its own badge icon as the logo and favicon: the Stux.Cloud mark on a round avatar with a heartbeat badge in the bottom-right corner, in Stux.Cloud's teal. `scripts/badge-icons.py` (copied from RoboStux/Status, which copied StuxGroup/Services', adapted from TheRidgwells/Projects') builds the favicon set into `icons/`, which GitHup publishes at the site root. The README header shows the same icon
- Stux.Cloud branding (teal `#07878e` accent) and GitHup's Boring Legal Stuff hub and six legal pages for Stux.Cloud, plus its 404, sitemap page, `sitemap.xml` and `robots.txt`
- `dev-server.sh` / `dev-server.bat` (example data, DEV_MODE on by default, `--no-dev-mode` for production rendering), `commit.sh` / `commit.bat` for tagged releases, and `tests/version.sh`
