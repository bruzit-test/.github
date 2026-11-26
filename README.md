# BruzIT Test Organization

[![License](https://img.shields.io/github/license/bruzit-test/.github)](LICENSE)
[![Last commit](https://img.shields.io/github/last-commit/bruzit-test/.github)](https://github.com/bruzit-test/.github/commits)
[![MegaLinter](https://github.com/bruzit-test/.github/actions/workflows/megalinter.yaml/badge.svg)](https://github.com/bruzit-test/.github/actions/workflows/megalinter.yaml)
[![Semantic Release](https://github.com/bruzit-test/.github/actions/workflows/semantic-release.yaml/badge.svg)](https://github.com/bruzit-test/.github/actions/workflows/semantic-release.yaml)

BruzIT Test organization profile. The organization itself is defined in [`test.yaml`](https://github.com/bruzit/github-organization-as-code/blob/main/test.yaml) of [BruzIT GitHub Organization as Code](https://github.com/bruzit/github-organization-as-code), which tests against it.

## Features

- **Organization profile** - Public profile shown on the [BruzIT Test GitHub Organization](https://github.com/bruzit-test) page, in [`profile/README.md`](profile/README.md).
- **Renovate preset** - Shared [Renovate](https://docs.renovatebot.com/) configuration for the organization's repositories, in [`renovate-config.json`](renovate-config.json); repositories extend it with `local>bruzit-test/.github:renovate-config`.

## Support

[Open a GitHub issue](../../issues). I answer best effort, as a community project.

## Integration and Deployment

| Workflow                                                                   | Trigger                           | Purpose                                                                            |
|----------------------------------------------------------------------------|-----------------------------------|------------------------------------------------------------------------------------|
| [`megalinter.yaml`](.github/workflows/megalinter.yaml)                     | Pull request                      | Lint changed files with MegaLinter, autofix via app; required check.               |
| [`semantic-release.yaml`](.github/workflows/semantic-release.yaml)         | Push to `main`                    | Version, changelog and GitHub release by semantic-release (`release` environment). |
| [`megalinter-scheduled.yaml`](.github/workflows/megalinter-scheduled.yaml) | Weekly (Monday 06:00 UTC), manual | Lint the whole codebase with MegaLinter.                                           |
| [`renovate.yaml`](.github/workflows/renovate.yaml)                         | Hourly, manual                    | Update dependencies in every organization repository with Renovate via app.        |

## Contributing

Open a pull request to `main`. Write commits per the [Conventional Commits 1.0.0 specification](https://www.conventionalcommits.org/en/v1.0.0/); semantic-release sets the version and changelog from them.

## License and Copyright

MIT License: [`LICENSE`](LICENSE)  
Copyright © 2026 Martin Bružina

## Stats

| Metric           | Badges                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Commits          | [![Commits total](https://img.shields.io/github/commit-activity/t/bruzit-test/.github?label=commits%20total)](https://github.com/bruzit-test/.github/commits/main)                                                                                                                                                                                                                                                                                     |
| Issues           | [![Issues open](https://img.shields.io/github/issues/bruzit-test/.github?label=issues)](https://github.com/bruzit-test/.github/issues) [![Issues total](https://img.shields.io/github/issues-search?query=repo%3Abruzit-test%2F.github%20is%3Aissue&label=issues%20total)](https://github.com/bruzit-test/.github/issues?q=is%3Aissue)                                                                                                                 |
| Pull requests    | [![Pull requests open, not draft](https://img.shields.io/github/issues-search?query=repo%3Abruzit-test%2F.github%20is%3Apr%20is%3Aopen%20draft%3Afalse&label=PRs%20open)](https://github.com/bruzit-test/.github/pulls?q=is%3Apr+is%3Aopen+draft%3Afalse) [![Pull requests total](https://img.shields.io/github/issues-search?query=repo%3Abruzit-test%2F.github%20is%3Apr&label=PRs%20total)](https://github.com/bruzit-test/.github/pulls?q=is%3Apr) |
| Checks on `main` | [![Checks on main](https://img.shields.io/github/check-runs/bruzit-test/.github/main?label=checks%20%28main%29)](https://github.com/bruzit-test/.github/actions?query=branch%3Amain)                                                                                                                                                                                                                                                                   |
| Releases         | [![Latest release](https://img.shields.io/github/v/release/bruzit-test/.github)](https://github.com/bruzit-test/.github/releases/latest) [![Commits since latest release](https://img.shields.io/github/commits-since/bruzit-test/.github/latest)](https://github.com/bruzit-test/.github/releases)                                                                                                                                                    |
| Community        | [![Stargazers](https://img.shields.io/github/stars/bruzit-test/.github)](https://github.com/bruzit-test/.github/stargazers) [![Forks](https://img.shields.io/github/forks/bruzit-test/.github)](https://github.com/bruzit-test/.github/forks) [![Contributors](https://img.shields.io/github/contributors/bruzit-test/.github)](https://github.com/bruzit-test/.github/graphs/contributors)                                                            |
