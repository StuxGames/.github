<p align="center">
  <picture><source media="(prefers-color-scheme: dark)" srcset="https://global.media.stux.games/logo-light.png"><source media="(prefers-color-scheme: light)" srcset="https://global.media.stux.games/logo-dark.png"><img src="https://global.media.stux.games/logo-dark.png" height="100" alt="Stux.Games Logo"></picture>
</p>

# .github

*Made to be played.*

The central repository for the Stux.Games GitHub organization configuration and profile settings.

## Overview

This repository contains the organization-wide configuration files for the Stux.Games GitHub profile, including community health files and the org's public profile page.

## What's Included

- **Profile** — the public org profile shown at [github.com/StuxGames](https://github.com/StuxGames) (`profile/README.md`)
- **Community Files** — contributing guidelines and other org-wide defaults
- **Metrics** — `.github/workflows/generateMetrics.yml` renders the profile's "Our Activity" stats onto the `metrics` branch daily

## How It Works

GitHub automatically applies files from this `.github` repository to all public repositories in the organization (when a specific repository doesn't have its own version), and renders `profile/README.md` as the org's public profile page.

## Getting Started

```bash
git clone https://github.com/StuxGames/.github.git
cd .github
```

## Development

See [CONTRIBUTING.md](CONTRIBUTING.md) for the development workflow and release process.

## Versioning

This project uses [Date Versioning](https://datevers.ing): each release is numbered by its UTC release date as `YY.MM.DD` (for example `26.10.23`), with `-1`, `-2`… for later releases the same day. See [CHANGELOG.md](CHANGELOG.md) for what changed in each release.

## Copyright

Copyright © 2026 Stux Group Ltd. All rights reserved.

---

*Built & Maintained by <picture><source media="(prefers-color-scheme: dark)" srcset="https://global.media.stux.games/icon-light.png"><source media="(prefers-color-scheme: light)" srcset="https://global.media.stux.games/icon-dark.png"><img src="https://global.media.stux.games/icon-dark.png" height="14" alt="Stux.Games" valign="middle"></picture> [Stux.Games](https://github.com/StuxGames), Hosted by <img src="https://github.com/Stuxedo.png" height="14" alt="Stuxedo" valign="middle"> [Stuxedo](https://stuxedo.com).  
Stux.Games is a part of the <picture><source media="(prefers-color-scheme: dark)" srcset="https://global.media.stux.group/icon-light.png"><source media="(prefers-color-scheme: light)" srcset="https://global.media.stux.group/icon-dark.png"><img src="https://global.media.stux.group/icon-dark.png" height="14" alt="Stux.Group" valign="middle"></picture> Stux.Group brand of businesses.*
