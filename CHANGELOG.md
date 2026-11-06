# Changelog

All notable changes to Stux.Cloud Status are documented here. Each release's sections follow
a fixed order: Added, Changed, Fixed, Removed, Security, Deprecated. This project is pre-stable and uses
[Semantic Versioning](https://semver.org) `0.x.y`; its first stable release will be its first
[Date Version](https://datevers.ing) (`YY.MM.DD`), with no 1.0.0.

## v0.1.0

### Added

- Stux.Cloud Status (`status.stux.cloud`), built with [GitHup](https://githup.stux.group): checks every 5 minutes (catching up when GitHub runs the schedule late), incident Issues, and the status page deployed to GitHub Pages by `.github/workflows/status.yml`
- Monitors for Stux.Cloud's public sites, with full names: the Stux.Cloud website and Media CDN; the six region websites with a server (United Kingdom, Spain, Finland, France, United States, Canada); the Region, Instance, Coming Soon and Maintenance Pages and the GitHub Pages Redirect; and the archived v1 and v2 page snapshots. Links to Stuxedo Status (the servers) and Stux.Group Status
- Its own badge icon as the logo and favicon: the Stux.Cloud mark on a round avatar with a heartbeat badge in the bottom-right corner, in Stux.Cloud's teal. `scripts/badge-icons.py` (copied from RoboStux/Status, which copied StuxGroup/Services', adapted from TheRidgwells/Projects') builds the favicon set into `icons/`, which GitHup publishes at the site root. The README header shows the same icon
- Stux.Cloud branding (teal `#07878e` accent) and GitHup's Boring Legal Stuff hub and six legal pages for Stux.Cloud, plus its 404, sitemap page, `sitemap.xml` and `robots.txt`
- `dev-server.sh` / `dev-server.bat` (example data, DEV_MODE on by default, `--no-dev-mode` for production rendering), `commit.sh` / `commit.bat` for tagged releases, and `tests/version.sh`
