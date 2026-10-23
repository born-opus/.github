# Born Opus defaults

Templates every Born Opus repository uses unless it has its own. GitHub reads them from this repository, which is
why it's public, so keep anything private out of it.

- `pull_request_template.md`: the summary, what changed, screenshots in light and dark, and the checks that apply.
- `ISSUE_TEMPLATE/release.md`: every step for one version of an app, from the release pull request to the App Store.

A repository with its own `.github/pull_request_template.md` or `.github/ISSUE_TEMPLATE/` uses those instead.
Tempus does, with checks named for its own iCloud records and Tempus AI. A change here that every app should follow
goes into Tempus's copies too. The reasons behind these templates are in Tempus's `docs/decisions/`.
