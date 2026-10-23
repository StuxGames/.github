# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Date Versioning](https://datevers.ing) since v26.10.23 (`YY.MM.DD`, the UTC release date, with `-1`, `-2`… for later releases the same day); earlier releases used [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## v26.10.23

### Added

- `tests/version.sh`, which checks that `VERSION.md` is a valid Date Version, a real calendar date not in the future, and the same as the newest entry in this changelog

### Changed

- Switched from Semantic Versioning to [Date Versioning](https://datevers.ing): releases are numbered by their UTC release date as `YY.MM.DD`, with `-1`, `-2`… for later releases the same day. This release follows v1.0.3
- `commit.sh` and `commit.bat` refuse a `VERSION.md` that isn't a valid Date Version or is dated in the future (UTC), and warn when it's dated before today
- `README.md` and `CONTRIBUTING.md` describe Date Versioning and the release steps

## [Unreleased]

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
