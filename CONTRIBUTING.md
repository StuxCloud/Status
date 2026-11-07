<p align="center">
  <img src="https://status.stux.cloud/icon-512.png" height="80" alt="Stux.Cloud Status icon">
</p>

# Contributing to Stux.Cloud Status

Stux.Cloud Status is Stux.Cloud's status page, [status.stux.cloud](https://status.stux.cloud), built with
[GitHup](https://githup.stux.group). To report an outage, open an Issue. Bugs or ideas for the
status page software belong in [StuxGroup/GitHup](https://github.com/StuxGroup/GitHup/issues).

## Local setup

You need Python 3.11+ and nothing else.

```bash
./dev-server.sh [--no-dev-mode] [port]   # or dev-server.bat on Windows
```

## Project conventions

- **Monitors live in `.githup.yml`.** Its syntax is documented in the
  [GitHup docs](https://githup.stux.group/docs/). Only add public sites Stux.Cloud runs, with
  their full names ("Stux.Cloud Region Page", not "regionpage"). The servers belong on Stuxedo's status (status.stuxedo.com).
- **The status page itself is GitHup's**, including the legal pages and 404. Change how it
  looks or works in GitHup, not here.
- **Brand.** Stux.Cloud is teal (`#07878e`), and `site.accent` is the same.
- **Icon.** The page's logo and favicons are its own badge icon: the Stux.Cloud mark with a heartbeat badge in the
  bottom-right corner, in Stux.Cloud's colours. They live in [`icons/`](icons), which GitHup publishes at the site
  root. To rebuild them (needs Pillow):

  ```bash
  curl -so /tmp/stux-cloud-icon.png https://global.media.stux.cloud/icon-light.png
  python -I scripts/badge-icons.py stux-cloud /tmp/stux-cloud-icon.png icons --size=512 --favicons
  rm icons/stux-cloud-status.png   # the same image as icons/icon-512.png
  ```

- **Legal pages.** The `legal:` block in `.githup.yml` drives **Boring Legal Stuff** at `/legal/`.
  Keep it accurate.
- **Don't edit `data/` by hand.** It belongs to GitHup and the workflow.

## Branches

- Work on `test`, or on a feature branch off it. Never push to `main`
- Changes reach `main` only through a pull request from `test` into `main`, which needs CI to pass and is reviewed and merged by Leo
- The Status workflow commits monitoring data (and the README's status table) straight to `main` as `github-actions[bot]`. Start new work from an up-to-date `test` (`git merge origin/main` into it) so the pull request stays clean
- Merging into `main` rebuilds the status page; release commits and tags are made on `test` (`git push origin test --tags`) and go live when the pull request is merged

## Versioning

This project uses [Date Versioning](https://datevers.ing). To release:

1. Add a `## vYY.MM.DD` entry at the top of `CHANGELOG.md`, with its sections in this order: Added, Changed, Fixed, Removed, Security, Deprecated.
2. Set `VERSION.md` to the same bare version (no `v`): today's **UTC** date as `YY.MM.DD`, or `YY.MM.DD-1`, `-2`… for later releases the same UTC day. Never a future date. Use UTC, not local time: just after midnight in the UK it is still the previous day in UTC.
3. Run `bash tests/version.sh`.
4. Run `./commit.sh` (or `commit.bat` on Windows). It checks the version, commits and tags `vYY.MM.DD`, and never pushes.
5. Push `test` with its tag (`git push origin test --tags`) and open a pull request from `test` into `main`.
