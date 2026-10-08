# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

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
