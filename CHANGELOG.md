# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Date Versioning](https://datevers.ing) since v26.10.23 (`YY.MM.DD`, the UTC release date, with `-1`, `-2`… for later releases the same day); earlier releases used [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## v26.11.06-3

### Added

- CI (`.github/workflows/ci.yml`), on pushes to `main` and `test` and on pull requests: `tests/version.sh`, a check that `profile/README.md` exists, and markdownlint. Pull requests from
  `test` into `main` now need it to pass, as CONTRIBUTING's Branches section says
- `.markdownlint.json`, the same Markdown rules the Stux.Games template repos use (plus MD026 off, for the profile's "Welcome…!" headings)

### Fixed

- The profile's activity image has alt text ("Stux.Games GitHub activity")

## v26.11.06-2

### Added

- A `test` branch: work happens on `test` (or a branch off it), and reaches `main` only through a pull request from
  `test` that Leo reviews and merges. Release commits and tags are made on `test`. CONTRIBUTING has a Branches section
  and the README's Versioning section says so

### Changed

- `commit.sh` and `commit.bat` suggest `git push origin test --tags`

## v26.11.06-1

### Fixed

- The profile said the GitHub Pages Redirect sends stuxgames.github.io to Stux.Games; it sends it to this GitHub
  organisation (github.com/StuxGames)

## v26.11.06

### Added

- The organisation profile lists the brand's sites (**Stux.Games**, **Stux.Games Games** and **Stux.Games Status**) and
  its templates (**Stux.Games Gamepage**, **Soonpage**, **Maintenancepage** and **GitHub Pages Redirect**), and has a
  Service Status section linking status.stux.games
- `CONTRIBUTING.md` has profile conventions: keep it in step with the org's repos, full names, public repos only, and
  light/dark logos

### Changed

- The logo and footer icons on the profile and README use the light/dark `<picture>` form, so they suit both GitHub
  themes
- The README lists the metrics workflow, and CONTRIBUTING's workflow no longer points at an `[Unreleased]` section

### Removed

- The empty `[Unreleased]` heading, left below v26.10.23 when the project moved to Date Versioning

## v26.10.23

### Added

- `tests/version.sh`, which checks that `VERSION.md` is a valid Date Version, a real calendar date not in the future, and the same as the newest entry in this changelog

### Changed

- Switched from Semantic Versioning to [Date Versioning](https://datevers.ing): releases are numbered by their UTC release date as `YY.MM.DD`, with `-1`, `-2`… for later releases the same day. This release follows v1.0.3
- `commit.sh` and `commit.bat` refuse a `VERSION.md` that isn't a valid Date Version or is dated in the future (UTC), and warn when it's dated before today
- `README.md` and `CONTRIBUTING.md` describe Date Versioning and the release steps

## [1.0.3] - 2026-10-08
### Changed
- Split the profile's "Our Projects" table into "Our Games" (Flappie Race, MultiPong) and "Open-Source Game Tools" (GameServerList, GameServerManager, FlappieRaceBackend), with a no-break space after each emoji so it never wraps onto its own line, matching the Stux.Dev profile.

### Fixed
- Flappie Race and MultiPong's descriptions were guesses ("Flappy-style racing game", "a multiplayer take on Pong"). They now describe what the repos contain: a Godot multiplayer game with a server browser, and multiplayer Pong in JavaScript with its own client and server.

## [1.0.2] - 2026-10-08
### Added
- Bluesky and LinkedIn badges (`bsky.app/profile/stux.games`, `linkedin.com/company/stuxgames`) in the "Connect with Us!" section, alongside the existing GitHub followers badge, matching the other Stux.Group brand profiles.

## [1.0.1] - 2026-10-05
### Changed
- New Stux.Games slogan, "Made to be played.", in `profile/README.md` and `README.md`, replacing "Leaders in Game Development."

## [1.0.0] - 2026-10-05
### Added
- Initial Stux.Games org profile (`profile/README.md`) with the welcome, mission, contact and "Our Activity" sections and the shared Stux.Group footer, matching the other Stux.Group brand `.github` repos.
- `generateMetrics.yml` workflow that renders the "Our Activity" stats onto the `metrics` branch.
- `README.md`, `CONTRIBUTING.md`, `VERSION.md`, `commit.sh`/`commit.bat` and `.gitignore`, following the standard release flow.
