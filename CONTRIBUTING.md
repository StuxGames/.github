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

## Branches and going live

- Work and releases happen on `test`, or on a feature branch merged back into it. The commit scripts refuse to run on `staging` or `main`; push a release with `git push origin test --tags`
- `staging` is pre-production. It changes only through a merged pull request from `test` (`gh pr create --base staging --head test`). There's no staging deployment: a release waits there, checked, before going live
- `main` is live. It changes only through a merged pull request from `staging` (`gh pr create --base main --head staging`). Merging into `main` updates the org profile at github.com/StuxGames
- Nothing is pushed straight to `staging` or `main`. Pull requests need CI to pass, and Leo merges them

## Versioning

This project uses [Date Versioning](https://datevers.ing). To release:

1. Add a `## vYY.MM.DD` entry at the top of `CHANGELOG.md`, with its sections in this order: Added, Changed, Fixed, Removed, Security, Deprecated.
2. Set `VERSION.md` to the same bare version (no `v`): today's **UTC** date as `YY.MM.DD`, or `YY.MM.DD-1`, `-2`… for later releases the same UTC day. Never a future date. Use UTC, not local time: just after midnight in the UK it is still the previous day in UTC.
3. Run `bash tests/version.sh`.
4. Run `./commit.sh` (or `commit.bat` on Windows). It checks the version, commits and tags `vYY.MM.DD`, and never pushes.
