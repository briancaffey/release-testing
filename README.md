# Release Testing

## How Release Please works: an introduction

This is an easy introduction to `release-please` and how it can be used on medium-sized teams.

- A project on GitHub has a default branch called `dev`
- Developers make feature branches off of the `dev` branch
- Feature branches follow a pattern of `feature/ACME-123-my-feature`
- `ACME-123` is the ticket pattern used in Jira
- Developer opens a PR for their feature branch targeting the default branch (`dev`)
- Once all CI pipelines pass and 2 PR reviews are given, the developer can merge their feature branch into the `dev` branch. The developer should always be responsible for clicking the "merge button" when they are ready to do so.
- Commits that are added to the `dev` branch should all be squash commits and should follow conventional commit format
- A new release can be created that will generate either a new minor version or patch version (X.X.1 -> X.X.2 or X.1.X -> X.2.X)
- New releases are created with `release-please` using a GitHub Actions workflow triggered with `workflow-dispatch`
- Developers should be encouraged to make new releases as soon as their code is merged in

## Adding a new release

To make a new release, make a new commit to the `main` branch.