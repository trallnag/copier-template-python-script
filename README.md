[![status](https://img.shields.io/badge/status-active-brightgreen)](#project-status)

# Copier Template Python Script

A [Copier](https://copier.readthedocs.io/en/stable/) template for rendering a
repository for a Python script.

Repositories based on this template:

- [trallnag/exec-cmds-defer-errors](https://github.com/trallnag/exec-cmds-defer-errors)
- [trallnag/filter-pre-commit-hooks](https://github.com/trallnag/filter-pre-commit-hooks)

## Repository requirements

All GitHub repositories based on this template must meet the following
requirements.

Feature "Wikis" disabled.

Feature "Discussions" enabled.

Feature "Projects" disabled.

For pull requests the following must be enabled:

- Always suggest updating pull request branches.
- Automatically delete head branches.
- Allow auto-merge.

Ruleset "Master":

- Target default branch.
- Restrict deletions.
- Block force pushes.

Environment "PyPI" with tag pattern `v*.*.*`.

## PyPI setup

Add a new pending publisher [here](https://pypi.org/manage/account/publishing/).

The workflow name is "release.yaml".

The environment name is "PyPI".

## Project status

The project is maintained by me, [trallnag](https://github.com/trallnag), and I
am interested in keeping it alive as I am actively using it.

## Contributing

No point in contributing. Made for my (trallnag) personal use only.

## Licensing

This work is licensed under the
[ISC license](https://en.wikipedia.org/wiki/ISC_license). See
[`LICENSE`](LICENSE) for the license text.
