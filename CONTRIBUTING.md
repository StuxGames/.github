# Contributing

Thanks for your interest in contributing to this project.

## Development Workflow

1. Work on `test`, or a feature branch off it (see Branches below).
2. Make focused, well-described commits.
3. Add your changes to a new release entry at the top of `CHANGELOG.md` (see Versioning below).
4. Open a pull request into `test`; `test` reaches `main` through its own pull request.

## Profile Conventions

- Keep `profile/README.md` in step with the org: list every public game, tool, site and template, and drop retired ones. Check against `gh repo list StuxGames` and [games.stux.games](https://games.stux.games).
- Use full names ("Stux.Games Status", "Stux.Games Gamepage"), not bare words like "Status" or "Gamepage".
- Only link public repositories. Private ones (such as `errorpages`) stay off the profile.
- Logos and icons use the light/dark `<picture>` form, from `global.media.stux.games` and `global.media.stux.group`.

## Branches

- Work on `test`, or on a feature branch off it. Never push to `main`
- Changes reach `main` only through a pull request from `test` into `main`, which is reviewed and merged by Leo
- Merging into `main` updates the org profile at github.com/StuxGames; release commits and tags are made on `test` (`git push origin test --tags`) and go live when the pull request is merged

## Versioning

This project uses [Date Versioning](https://datevers.ing). To release:

1. Add a `## vYY.MM.DD` entry at the top of `CHANGELOG.md`, with its sections in this order: Added, Changed, Fixed, Removed, Security, Deprecated.
2. Set `VERSION.md` to the same bare version (no `v`): today's **UTC** date as `YY.MM.DD`, or `YY.MM.DD-1`, `-2`… for later releases the same UTC day. Never a future date. Use UTC, not local time: just after midnight in the UK it is still the previous day in UTC.
3. Run `bash tests/version.sh`.
4. Run `./commit.sh` (or `commit.bat` on Windows). It checks the version, commits and tags `vYY.MM.DD`, and never pushes.
